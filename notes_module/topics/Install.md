# Installation

How to install and management the Notes plugin.

## Supported Operating Systems
Since Notes 2023.1.2, the natively compiled SQLite engines will be used for
the following operating systems:

|              | x86 | x86_64 | aarch64 |
|--------------|-----|--------|---------|
| Windows      | ✔   | ✔      | ✔       |
| macOS        |     | ✔      | ✔       |
| Linux (libc) | ✔   | ✔      | ✔       |
| Linux (musl) | ✔   | ✔      |         |


In the other OSs not listed above, the pure-java SQLite is used. (Applies to versions before 3.7.15)

## Prerequisites


1. A JetBrains IDE 2020.3+

Install an IDE if you don't have one from [Jetbrains](https://www.jetbrains.com)
or [Android Studio](https://developer.android.com/sdk/installing/studio.html). Notes support all major Jetbrains
IDEs include IDEA CE, IDEA Ultimate, WebStorm, Android Studio, PhpStorm, RubyMine and GoLand and so on.


> The difference in these IDEs is that only paid IDE supports advanced programming language features such as refactor, debugger and so on for certain languages such as C++, JavaScript and so on.
>
{style="note"}

2. JBR(JetBrains Runtime) `Optional`

   **Old version of Android Studio needs JBR to View Rich-text Evernote content and Markdown Preview**
> You can install jbr with jcef in the following way:
>
> Refer to [Selecting-the-JDK-version-the-IDE-will-run-under](https://intellij-support.jetbrains.com/hc/en-us/articles/206544879-Selecting-the-JDK-version-the-IDE-will-run-under), choose an item says **JetBrains Runtime with JCEF** to install.
> 
{style="note"}

## Install the %product% plugin in IDE


1. Open your IDE and press <shortcut key="ShowSettings" /> to open the IDE settings and select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <control>Marketplace</control> tab.
3. On the <control>Marketplace</control> tab, search for `%product%`.
4. Select the `%product%` plugin and click <control>Install</control>.
5. Click <control>OK</control> to apply the changes and restart your IDE if prompted.

![](notes-install.png){thumbnail="true" thumbnail-same-file="true" }

## Download and install %product% plugin from disk

1. Go to the plugin versions page at [%plugin_versions_page%](%plugin_versions_page%).
2. Click <control>Download</control> and get a ZIP archive.
3. Open your IDE and press <shortcut key="ShowSettings" /> to open the IDE settings.
4. Select <ui-path>Plugins</ui-path>, click ![Settings](settings.svg) and then select  ![](plugin.svg) <control> Install Plugin from Disk…</control>.
5. Select the plugin archive file and click <control>OK</control>.
6. Click <control>OK</control> to apply the changes and restart your IDE if prompted.


## Update an installed %product% plugin

1. Open your IDE and press <shortcut key="ShowSettings" /> to open the IDE settings and select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <ui-path>Installed</ui-path> tab.
3. Check if the `%product%` plugin requires an update.
4. Click <control>Update</control>.
5. Click <control>OK</control> in the <control>Settings</control>  dialog to apply the changes, and restart <control>IDE</control>  if prompted.

## Uninstall the %product% plugin

> You can always disable the `%product%` plugin by clearing the checkbox to the right of its name.
>
{style="note"}

1. Open your IDE and press <shortcut key="ShowSettings" /> to open the IDE settings and select <ui-path>Plugins</ui-path>.
2. In the <ui-path>Plugins</ui-path> dialog, switch to the <ui-path>Installed</ui-path> tab.
3. On the <ui-path>Installed</ui-path> tab, search for `%product%`.
4. Right-click the `%product%` plugin and select <control>Uninstall</control>.
5. Click <control>OK</control> to apply the changes and restart your IDE if prompted.


