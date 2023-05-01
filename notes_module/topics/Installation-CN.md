# 安装

如何安装和管理代码笔记插件。

## 支持的操作系统
从代码笔记2023.1.2版本开始，代码笔记在下列操作系统中支持原生编译的SQLite引擎：

|              | x86 | x86_64 | armv5 | armv6 | armv7 | arm64 | ppc64 |
|--------------|-----|--------|-------|-------|-------|-------|-------|
| Windows      | ✔   | ✔      |       |       | ✔     | ✔     |       |
| macOS        |     | ✔      |       |       |       | ✔     |       |
| Linux (libc) | ✔   | ✔      | ✔     | ✔     | ✔     | ✔     | ✔     |
| Linux (musl) | ✔   | ✔      |       |       |       | ✔     |       |
| FreeBSD      | ✔   | ✔      |       |       |       | ✔     |       |


在未列出的操作系统中，会使用纯Java的SQLite。

## 先决条件


1. JetBrains 开发工具 2020.3+

Install an IDE if you don't have one from [Jetbrains](https://www.jetbrains.com)
or [Android Studio](https://developer.android.com/sdk/installing/studio.html). Notes support all major Jetbrains
IDEs include IDEA CE, IDEA Ultimate, WebStorm, Android Studio, PhpStorm, RubyMine and GoLand and so on.


> The difference in these IDEs is that only paid IDE supports advanced JavaScript editor and in-IDE debugger.
>
{style="note"}

2. JBR(JetBrains Runtime)

   **Android Studio needs JBR to View Rich-text Evernote content and Markdown Preview**
> You can install jbr with jcef in the following way:
>
> 1. Install the plugin “Choose Runtime”
> 2. Select the corresponding jbr version to download through the link, which must have JCEF. https://confluence.jetbrains.com/display/JBR/Release+notes+and+builds
> 3. Refer to [Selecting-the-JDK-version-the-IDE-will-run-under](https://intellij-support.jetbrains.com/hc/en-us/articles/206544879-Selecting-the-JDK-version-the-IDE-will-run-under), select the downloaded jbr.


## Install the Notes plugin in IDE

1. In the <ui-path>Settings/Preferences</ui-path> dialog <shortcut key="ShowSettings" /> , select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <ui-path>Marketplace</ui-path> tab.
3. In the dialog that opens, search for `Notes`.
4. Click <control>Install</control>.
5. Click <control>OK</control>  in the <control>Settings</control>  dialog to apply the changes, and restart <control>IDE</control>  if prompted.

![](notes-install.png){thumbnail="true" thumbnail-same-file="true" }

## Download and install plugin from disk

1. Go to the plugin page at [https://plugins.jetbrains.com/plugin/17501-notes/versions](https://plugins.jetbrains.com/plugin/17501-notes/versions).
2. Click <control>Get</control> and download a ZIP archive.
3. Open <path> Settings/Preferences | Plugins </path> <shortcut key="ShowSettings" />.
4. Click ![Settings](settings.svg)button in the top-right corner and then select <control>Install Plugin from Disk…</control>.
5. Select the archive and click <control>OK</control>.

## Update an installed Notes plugin

1. In the <ui-path>Settings/Preferences</ui-path> dialog <shortcut key="ShowSettings" /> , select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <ui-path>Updates</ui-path> tab.
3. Check if the **Notes** plugin requires an update.
4. Click <control>Update</control>.
5. Click <control>OK</control> in the <control>Settings</control>  dialog to apply the changes, and restart <control>IDE</control>  if prompted.

## Uninstall the Notes plugin

> You can always disable the Notes plugin by clearing the checkbox to the right of its name.
>
{style="note"}

1. In the <ui-path>Settings/Preferences</ui-path> dialog <shortcut key="ShowSettings" /> , select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <ui-path>Installed</ui-path> tab.
3. On the <ui-path>Installed</ui-path> tab, search for **Notes**.
4. Right-click the **Notes** plugin and select <control>Uninstall</control>.
5. Click <control>OK</control> in the <control>Settings</control>  dialog to apply the changes, and restart <control>IDE</control>  if prompted.


