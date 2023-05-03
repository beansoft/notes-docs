# 安装

如何安装和管理代码笔记插件。

## 支持的操作系统
从代码笔记2023.1.2版本开始，代码笔记在下列操作系统中支持原生编译的SQLite引擎：


|              | x86 | x86_64 | aarch64 |
|--------------|-----|--------|---------|
| Windows      | ✔   | ✔      | ✔       |
| macOS        |     | ✔      | ✔       |
| Linux (libc) | ✔   | ✔      | ✔       |
| Linux (musl) | ✔   | ✔      |         |


在未列出的操作系统中，会使用纯Java的SQLite。

## 先决条件


1. JetBrains 开发工具 2020.3+

首先您需要安装一款集成开发工具，可以从 [Jetbrains](https://www.jetbrains.com.cn)
或者 [Android Studio](https://developer.android.google.cn/studio/) 下载安装。 Notes 支持所有主要的 Jetbrains
系开发工具包括 IDEA 社区版, IDEA Ultimate, WebStorm, Android Studio, PhpStorm, RubyMine, GoLand 等。

> 不同开发工具的区别主要是付费版的开发工具才会为某些语言例如C++, JavaScript提供高级编程语言开发功能如重构，调试等。
>
{style="note"}

2. JBR(JetBrains 运行时Java虚拟机) `可选`

   **旧版 Android Studio 需要使用 JBR 才能预览Markdown内容或查看 Evernote 富文本内容**
> 你可以使用下面的方法来安装带有JCEF浏览器的JBR：
>
> 请参考文章 [Selecting-the-JDK-version-the-IDE-will-run-under](https://intellij-support.jetbrains.com/hc/en-us/articles/206544879-Selecting-the-JDK-version-the-IDE-will-run-under), 选中列表项 **JetBrains Runtime with JCEF** 完成安装.
>
{style="note"}

[//]: # (下面的内容必须添加 id 才能区分不同的大纲 参考 https://plugins.jetbrains.com/plugin/20158-writerside/docs/structural-elements.html#chapter-block )
## 在开发工具中安装 `%product%` 插件 {id="install-in-ide"}

1. 启动开发工具并按下 <shortcut key="ShowSettings" /> 打开 IDE 设置页面并选择 <ui-path>Plugins</ui-path>。
2. 在 <ui-path>Plugins</ui-path> 对话框中切换到 <ui-path>Marketplace</ui-path> 标签页。
3. 在 <control>Marketplace</control> 标签页，搜索 `%product%`。
4. 选中 `%product%` 插件并点击 <control>Install</control>。
5. 点击 <control>OK</control> 来应用更改，如出现提示请重启IDE。 

![](notes-install.png){thumbnail="true" thumbnail-same-file="true" }

## 下载并从磁盘安装 `%product%` 插件 {id="install-from-disk"}

1. 打开插件版本页面 [%plugin_versions_page%](%plugin_versions_page%).
2. 点击 <control>Download</control> 得到一个 ZIP 压缩文件。
3. 启动开发工具并按下 <shortcut key="ShowSettings" /> 打开 IDE 设置页面并选择 <ui-path>Plugins</ui-path>。
4. 点击 ![Settings](settings.svg) 然后选择  ![](plugin.svg) <control> Install Plugin from Disk…</control>。
5. 选中 ZIP 压缩文件然后点击 <control>OK</control>。
6. 点击 <control>OK</control> 来应用更改，如出现提示请重启IDE。


## 更新已安装的 `%product%` 插件 {id="update"}

1. 启动开发工具并按下 <shortcut key="ShowSettings" /> 打开 IDE 设置页面并选择 <ui-path>Plugins</ui-path>。
2. 在 <ui-path>Plugins</ui-path> 对话框中切换到 <ui-path>Installed</ui-path> 标签页。
3. 检查 `%product%` 插件是否需要更新。 
4. 点击 <control>Update</control>.
5. 点击 <control>OK</control> 来应用更改，如出现提示请重启IDE。

## 卸载 `%product%` 插件 {id="uninstall"}

> 取消选择插件名字右侧的复选框可以禁用 `%product%` 插件。
>
{style="note"}

1. 启动开发工具并按下 <shortcut key="ShowSettings" /> 打开 IDE 设置页面并选择 <ui-path>Plugins</ui-path>。
2. 在 <ui-path>Plugins</ui-path> 对话框中切换到 <ui-path>Installed</ui-path> 标签页。
3. 在 <control>Installed</control> 标签页，搜索 `%product%`。
4. 右键点击 `%product%` 插件并选择 <control>Uninstall</control>。
5. 点击 <control>OK</control> 来应用更改，如出现提示请重启IDE。

