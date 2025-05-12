# Pin notes to symbol
![Beta](beta.svg) Pin to symbol is the most powerful feature introduced in 2025.2, which allows link notes to a programming language's symbol
such as **class**, **field** or **methods** instead link the lines of source code.
Notes
: This feature is still under development, currently only supports **Java** language. 
Other JVM languages such as **Kotlin** will be supported in the next release.

## Benefits
- Always display notes in the right place when move symbols away or pull source code from VCS
- Unique path for both project files or library files
- Easily used symbol picker let you quickly update symbol

## Limitations

- Symbol must be unique via all project files includes libraries
- Java: Represents implicitly declared class is not supported from <a href="https://openjdk.org/jeps/463">JEP 463</a>.
