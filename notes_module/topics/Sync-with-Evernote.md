# Sync with Evernote

From version 2022.1.1, the Notes plugin supports sync with Evernote. An Evernote tool window is added to your IDE, and all the data there is stored in Evernote by using Evernote Developer token. And the old Notes tool window function is unchanged, it's still stored locally using a single SQLite notes.db file.

Only notes content created by Notes plugin is displayed in your IDE tool window and connected to the source editor, your original Evernote content is safe and untouched, and can be viewed in your IDE. This content is treated as plain text, which is also displayed in your Evernote Desktop/Mobile/Web app, with a tag marked "iNotes", you can view and edit them. No formatting is supported in code notes created, if you edit the notes in Evernote, the content in Notes will omit all style info.

**Android Studio needs JBR to View Richtext Evernote content**
> You can install jbr with jcef in the following way:
>
> 1. Install the plugin “Choose Runtime”
> 2. Select the corresponding jbr version to download through the link, which must have JCEF. https://confluence.jetbrains.com/display/JBR/Release+notes+and+builds
> 3. Refer to [Selecting-the-JDK-version-the-IDE-will-run-under](https://intellij-support.jetbrains.com/hc/en-us/articles/206544879-Selecting-the-JDK-version-the-IDE-will-run-under), select the downloaded jbr.

**Evernote Developer Tokens**

Developer tokens allow you to use the Evernote API to access your personal Evernote account. To learn more about using developer tokens, visit [https://dev.evernote.com](https://dev.evernote.com).

Protect this token as carefully as you protect your Evernote password! Anybody with access to this token has full access to your Evernote account. You can revoke this token at any time by returning to this page.

Your can visit the page directly - [China 印象笔记](https://app.yinxiang.com/api/DeveloperToken.action) | [Evernote International](https://www.evernote.com/api/DeveloperToken.action), you should see sth like (Of course, you have to login):

![screenshot](https://github.com/rhapsodyn/vscode-evernote/raw/master/images/screenshot.jpg)