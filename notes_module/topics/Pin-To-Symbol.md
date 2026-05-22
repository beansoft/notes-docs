# Pin notes to symbol
![Beta](beta.svg) Pin to symbol is the most powerful feature introduced in 2025.2, which allows link notes to a programming language's symbol
such as **class**, **field** or **methods** instead link the absolute line number of source code.

Notes
: This feature is still under development and only supports **Java, Kotlin, C#** language.
Future releases will support more programming languages.

ℹ️: C# support [Code Notes for C#](https://plugins.jetbrains.com/plugin/31914-code-notes-for-c-beta) plugin installed, also only works under the Rider IDE.

## Benefits
- Always display notes in the right place when moving symbols away or pulling source code from VCS
- Unique path for both project files and library files
- Easily used symbol picker lets you quickly update symbol

## Limitations

- Symbol must be unique via all project files including libraries
- **Java**: Implicitly declared class is not supported. Ref: <a href="https://openjdk.org/jeps/463">JEP 463</a>.
