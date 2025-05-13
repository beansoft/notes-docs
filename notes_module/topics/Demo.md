# Demo

[//]: # (title: Demo)
[//]: # (<excerpt>标签页等功能演示.</excerpt>)

<tldr>

**Code**: [`AllIcons`](https://plugins.jetbrains.com/plugin/9564-react-native-console/analytics)

**Platform UI Guidelines:** [Icons list](https://jetbrains.design/intellij/resources/icons_list/), [Icons](https://jetbrains.design/intellij/principles/icons/)

</tldr>

## TL;DR
Use the <code>&lt;tldr&gt;</code> tag to introduce important facts or prerequisites about the feature you describe. Place it as
the first element of a topic and wrap each fact with the <code>&lt;p&gt;</code> tag.
<p>There can be only one <code>&lt;tldr&gt;</code> element per page.</p>
Use <code>&lt;tldr&gt;</code> only for introducing small amounts of information. We don' recommend using more than three elements
inside of it.

## Glossary

A definition list or a glossary:

Notes
: ![limited support](icon-limited.svg)limited support


![via a plugin](icon-via-plugin.svg)depends on JavaScript plugin in IDEA Ultimate / WebStorm / GoLand / PhpStorm / Pycharm / RubyMine / AppCode / Clion / Rider etc

![limited support](icon-limited.svg)limited support

![available](icon-available.svg)available

{collapsible="true"}
Expanded by default
{collapsible="true" default-state="expanded"}
: This is the definition of the first term.

Collapsed by default
{collapsible="true" default-state="collapsed"}
: This is the definition of the second term.

## 缩进块代码
前面加上缩进后（选中后按下`Tab`键），纯文本内容会自动放进一个无边框区域内，相当于代码块。

    Use the <code>&lt;tldr&gt;</code> tag to introduce important facts or prerequisites about the feature you describe. Place it as
    the first element of a topic and wrap each fact with the <code>&lt;p&gt;</code> tag.
    <p>There can be only one <code>&lt;tldr&gt;</code> element per page.</p>
    Use <code>&lt;tldr&gt;</code> only for introducing small amounts of information. We don' recommend using more than three elements
    inside of it.

## 段落折叠 {collapsible="true" id="unique-id"}

The content.

### {title="Nested chapter's title" id="yet-another-unique-id"}
<title>The title that overrides Nested chapter's title</title>

The content.

## 代码折叠
```java
class Main {
    public static void main(String[] args) {
        System.out.println("Enter two numbers");
        int first = 10;
        int second = 20;
        System.out.println(first + " " + second);
// add two numbers
        int sum = first + second;
        System.out.println("The sum is: " + sum);
    }
}
```
{collapsible="true" default-state="collapsed"
collapsed-title="默认折叠的代码"}


```java
class Main {
}
```
{collapsible="true" default-state="expanded"
collapsed-title="Title to display when a block is collapsed"}


```shell
sudo tar -xzf the-package-*.tar.gz -C /opt
```
{prompt="$"}


## Include a block from another folder {id="include-from-another-folder"}

To include the code example from another file in the repository:

Specify the name of the directory where you will place the code files
in the `snippets` attribute of the `project.ihp` file.

`<snippets src="directoryName"/>`

To include content from other files, use `src` attribute and specify the filename.

[//]: # (The source file must be located under the `codeSnippets` directory.)

To specify a specific line range or comma-separated list to include, use `include-lines` attribute.

To specify a specific code construct, like, method or class, use `include-symbol` attribute.

<table>
<tr>
    <td>Markup</td>
    <td>Result</td>
</tr>
<tr>
<td>

```
&#96;&#96;&#96;kotlin
&#96;&#96;&#96;
{src="newTest.kt" include-lines="2-4"}
```

</td>
<td>

```kotlin
```
{src="newTest.kt" include-lines="2-4"}

</td>
</tr>
<tr>
<td>

```
&#96;&#96;&#96;kotlin
&#96;&#96;&#96;
{src="newTest.kt" include-symbol="hello"}
```
</td>
<td>

```kotlin
```
{src="newTest.kt" include-symbol="hello"}

</td>
</tr>
</table>

## control

Use the `control` tag to refer to UI elements such as buttons, dialogs, checkboxes, and so on.


<control>
Check out from Version Control
</control>

## ui-path

Use the `ui-path` tag to specify a path to a menu option.

In the <ui-path>Settings/Preferences</ui-path> dialog <shortcut>Ctrl+Alt+S</shortcut>

## path

Use the `path` tag for paths to directories and files on your computer or file extensions.

The TOC is stored in the product's
<path>.tree</path> file.

## 样式和小段落
<format style="bold" color="Red">Hello, world!</format>

{style="narrow"}
Default value
: `true`

Example
: 小段落

## 提示信息

> These pages have moved to [JetBrains Marketplace Documentation](https://plugins.jetbrains.com/docs/marketplace). Please update your bookmarks.

{style="warning"}

<tip>Alternatively, you can change the settings directly in the configuration file.</tip>

<note>
    hello
</note>
<warning>warning</warning>

<tip>Tip</tip>

&lt;tooltip&gt; 标记需要在 <path>cfg/glossary.xml</path> 中添加解释.
<tooltip term="RN">RN Console</tooltip>

> This is a warning
>
{style="warning"}

> This is a note in markdown
>
{style="note"}

> This is a tip
>
{style="tip"}

> This is a todo
>
>

## 步骤
<procedure title="步骤" collapsible="true">
    <step>
        <p>
            Call the following command in the terminal:
        </p>
        <code-block lang="bash">
            run this --that
        </code-block>
    </step>
</procedure>

## 图片
![Getting Service](free_discount.png){thumbnail="true" thumbnail-same-file="true"}

<img src="zoom_ide.gif" alt="" />

[//]: # (![Screenshot]&#40;screenshot_.gif&#41;&#41;{width="32" animated="true"  alt="Alt" border-effect="rounded" thumbnail="true" thumbnail-same-file="true"})

## 左右表格
<table>
            <tr>
                <td width="50%">Markup</td>
                <td width="50%">Result</td>
            </tr>
            <tr>
                <td>
                    <code-block>
                        ![](sample-image-white.png) alt="Sample image"  {width="250px"}
                    </code-block>
                </td>
                <td>
                    <img src="zoom_ide.gif" alt="Sample image" width="250"/>
                </td>
            </tr>
</table>

## 标签页 + Markdown
<tabs>
    <code-block lang="java">Java code</code-block>
    <code-block lang="groovy">Groovy code</code-block>
</tabs>


<tabs group="languages">
<tab title="Kotlin" group-key="kotlin">

```kotlin
plugins {
    id("org.jetbrains.intellij") version "..."
}
```

</tab>
<tab title="Groovy" group-key="groovy">

```groovy
plugins {
    id "org.jetbrains.intellij" version "..."
}
```

</tab>
</tabs>

## 标签页联动

<tabs group="languages">
    <tab title="Kotlin" group-key="kotlin">
        <p>This is Kotlin.</p>
    </tab>
    <tab title="Java" group-key="java">
        <p>This is Java.</p>
    </tab>
</tabs>

<tabs  group="languages">
    <tab title="Kotlin Theory" group-key="kotlin">
        <p>This is Kotlin theory.</p>
    </tab>
    <tab title="Java Theory" group-key="java">
        <p>This is Java theory.</p>
    </tab>
</tabs>


## Video
Use `<video>` tag to add local videos or links to videos from YouTube, or Vimeo.

<video src="https://www.youtube.com/watch?v=1uhrSAMzo3I" />