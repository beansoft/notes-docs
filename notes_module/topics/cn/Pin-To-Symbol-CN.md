# 固定笔记到符号
![Beta](beta.svg) 固定笔记到符号是2025.2版本首次支持的最强大的功能, 支持链接笔记到编程语言的符号, 如 **类**, **变量** or **方法(函数)**,
而不是链接到源代码的行号.

注意
: 此功能仍在开发中, 目前只支持 **Java** 语言.
**Kotlin**, will be supported in the next release.
Future releases will support more programming languages.

## Benefits
- Always display notes in the right place when moving symbols away or pulling source code from VCS
- Unique path for both project files and library files
- Easily used symbol picker lets you quickly update symbol

## Limitations

- Symbol must be unique via all project files including libraries
- **Java**: Implicitly declared class is not supported. Ref: <a href="https://openjdk.org/jeps/463">JEP 463</a>.
