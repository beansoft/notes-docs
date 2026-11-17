# Full Text Boolean Search

The notes search bar has a **Full Text Boolean (AND/OR/NOT)** toggle. When it is on, the text you type is parsed as an
[SQLite FTS5](https://www.sqlite.org/fts5.html#full_text_query_syntax) query expression instead of plain keywords, so
you can combine terms with boolean operators, group them, and search exact phrases.

## Turning it on

1. Open the **Notes** tool window and click the search (magnifier) button above the notes list, or press `Ctrl+F` / `⌘F`, to show the search bar.
2. Click the filter icon (**Full Text Boolean (AND/OR/NOT)**) on the right side of the search field.
3. Type a query. Results refresh immediately whenever the toggle is switched.

The setting is application-wide and remembered across IDE restarts.

> The toggle is **disabled** in two cases:
> - the project uses the **Git/Markdown storage engine** — that engine has no FTS5 index; it is only available with
>   the default SQLite storage;
> - the **"Search in title only"** option is on — that mode searches the title with a plain substring (SQL `LIKE`)
>   match, so boolean syntax does not apply.

## Default mode vs. boolean mode

| | Default mode (toggle off) | Boolean mode (toggle on) |
|---|---|---|
| `react hook` | both words must appear | both words must appear (implicit AND) |
| `AND` / `OR` / `NOT` | searched as literal words | treated as operators |
| `( )` | literal characters | groups sub-expressions |
| `"..."` | literal characters | exact phrase |
| Prefix matching | last word only | every bare word |

## Syntax

Every search covers both the note **title** and **content**. Matching is substring-based (trigram index), so `act`
also finds `React`. Matching is case-insensitive.

| Syntax | Example | Meaning |
|---|---|---|
| space (implicit AND) | `react hook` | notes containing both `react` and `hook` |
| `AND` | `react AND hook` | same as above, explicit |
| `OR` | `react OR vue` | notes containing either word |
| `NOT` | `pool NOT mysql` | contains `pool` but not `mysql` |
| `( )` | `(react OR vue) AND component` | grouping; controls precedence |
| `"phrase"` | `"connection pool"` | the exact phrase, words adjacent and in order |
| `NEAR( )` | `NEAR(react hook)` | both words close to each other (default distance 10) |
| `NEAR( , N)` | `NEAR(react hook, 5)` | both words with at most N units between them (see below) |
| `column:` | `name:redis` / `code:redis` | restrict a word to the title (`name`) or content (`code`) |
| `*` | `hik*` | explicit prefix; bare words already get one automatically |

Operator precedence (FTS5): `NOT` binds tightest, then `AND`, then `OR`. Use parentheses when in doubt:
`react OR vue AND hook` means `react OR (vue AND hook)`.

### Examples

```text
spring AND transaction              # notes about Spring transactions
docker OR kubernetes                # either container topic
redis NOT cluster                   # Redis notes that don't mention cluster
(mysql OR postgres) AND index       # database index notes for either DB
"connection pool" NOT hikari        # exact phrase, excluding HikariCP notes
name:todo AND code:release          # "todo" in the title, "release" in the content
NEAR(kafka consumer)                # kafka and consumer close to each other
NEAR(kafka consumer, 20)            # same, with an explicit distance
```

## Rules and limitations

- **Operators must be UPPERCASE.** `and`, `or`, `not` in lowercase are searched as ordinary words.
- **Short words (under 3 characters) are supported, with one difference.** The trigram index cannot match words
  shorter than 3 characters (`js`, `db`, two-character CJK words). When the query contains such a word, the plugin
  translates the whole expression into an equivalent substring (`LIKE`) search instead. `AND` / `OR` / `NOT`,
  parentheses, phrases and `name:` / `code:` keep their meaning, so `js OR typescript` and `kafka NOT db` work as
  expected. The only loss: `NEAR(...)` can't measure distance there and acts like `AND`.
- **`NEAR` distance is measured in characters, not words.** The index splits text into overlapping 3-character
  pieces (trigrams), so `N` is roughly the number of characters allowed between the end of the first word and the
  start of the second. `NEAR(react hook, 2)` does **not** match "React Hook" (the space between the words spans 3 trigrams);
  `NEAR(react hook, 5)` does. Pick a generous `N`.
- **Invalid expressions fall back silently.** An unbalanced quote or parenthesis, or a dangling operator
  (`react AND`), makes FTS5 reject the query; the plugin then runs a plain `LIKE` search on the raw text, which usually
  returns nothing. If results look wrong, check the syntax.
- Deleted notes (trash) are never included.

## Troubleshooting

| Symptom | Likely cause |
|---|---|
| Toggle is greyed out | Project uses Git/Markdown storage, or "Search in title only" is on |
| Query returns nothing | Lowercase operators, unbalanced `"` / `( )`, or a dangling operator |
| `NEAR(a b, N)` misses an obvious match | `N` counts characters, not words — increase it |
