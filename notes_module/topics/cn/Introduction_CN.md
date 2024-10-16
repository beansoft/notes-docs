# 代码笔记介绍

为程序员笔记而生

代码笔记是一款超好用的适合程序员在JetBrains产品线使用的代码笔记和书签管理软件, 手不离IDE即可完成创建修改搜索代码笔记功能, 支持附件管理，支持 SQLite
本地数据库存储或者Evernote存储, 支持阅读Evernote笔记和图片. 详细中文说明请滚动到本页面底部. 

B站视频:
<a href="https://www.bilibili.com/video/BV1YW4y1y7DP">IDEA超好用的代码笔记插件 - Notes,
国产插件就是牛</a>


[![Notes](https://img.shields.io/badge/plugin-Notes-x.svg?logo=IntelliJ%20IDEA)
![Version](https://img.shields.io/jetbrains/plugin/v/17501?logo=IntelliJ%20IDEA) 
![Downloads](https://img.shields.io/jetbrains/plugin/d/17501?color=FE2857) 
![Rating](https://img.shields.io/jetbrains/plugin/r/rating/17501)](https://plugins.jetbrains.com/plugin/17501)

为庆祝简体中文版的发布, 国内用户加QQ群 643815976 或者Q 9991483, 立享5折优惠并不定期送一年免费优惠码.

> 中文用户如遇到字体显示问题, 可点击<shortcut>⭐代码笔记</shortcut>工具窗口中的 小齿轮 ![](settings.svg) 打开设置界面的默认列表或者树字体为中文字体例如微软雅黑即可.

{style="note"}

代码笔记正在持续完善中, 欢迎反馈问题和建议.

## 主要功能 💯

* ![beta.svg](beta.svg)可视化 Markdown 编辑器
* ✅ 类似于 Mac 备忘录的操作界面
* ✅ 自动保存代码和笔记
* ✅ 一键粘贴代码或附件为代码笔记
* ✅ 支持附件(需要 %product% 2023.1.0及更高版本)
* ✅ SearchEveryWhere 支持
* ✅ Evernote/印象笔记 同步支持
* ✅ 多达 300 种代码格式高亮
* ✅ 自动保存! 在编辑器中或者修改标题时会实时保存内容
* ✅ 支持对只读的库文件或者Java类文件上直接添加笔记
* ✅ 附件管理及图片缩略图浏览功能
* ✅ 虚拟代码树结构以及全屏窗口模式及代码片段修改
* ✅ 支持相同的代码笔记在同一台电脑上的运行中的多个开发工具中(例如 WebStorm, Android Studio 和IDEA)同时展示
* ✅ 极速搜索: 快速找到你所需要的正确代码
* ✅ 语法高亮编辑器支持多达300种编程语言类型
* ✅ 支持多种编程语言的代码高亮和智能编辑模式, 除IDE内置语言外还支持第三方扩展编程语言例如: [PlantUML integration](https://plugins.jetbrains.com/plugin/7017-plantuml-integration), Scala 和 Rust
* ✅ Markdown 编辑和预览(需要安装Intellij Markdown 插件并运行于[JetBrains Runtime](https://github.com/JetBrains/JetBrainsRuntime) )
* ✅ 易于备份同步, 整个代码笔记仅需一个SQLite 数据库文件进行存储
* ✅ 从编辑器中收藏代码笔记
* ✅ Markdown 流程图支持，安装插件 [Mermaid](https://plugins.jetbrains.com/plugin/20146-mermaid) ；脑图支持，安装插件 [IDEA Mind Map](https://plugins.jetbrains.com/plugin/8045-idea-mind-map)


> 请确保你的 IDEA, Android Studio 版本 >= 2020.3+
> 
> 当然如果插件有更新，请确保更新到最新版本

{style="note"}

欲了解更多Evernote 集成的相关信息, 请点击 [Evernote同步](https://beansoft.github.io/notes-docs/sync-with-evernote.html).

在文件编辑器内一键创建(快捷键<shortcut key="$AddNotes" />或者选择代码后按下 Alt+Enter 组合键), 或通过编辑器行号区域右键点击快速创建笔记, 修改和删除代码笔记, 记录下的笔记将会在编辑器内实时显示.

更好用的书签功能: 智能显示笔记链接的源文件, 支持键盘导航 - 使用上下箭头切换条目, 按下回车键或者双击条目打开链接的文件, 按下ESC键返回主编辑器(从代码笔记小窗口离开).

在代码笔记/Evernote 工具窗口中快速创建笔记。 支持Jetbrains开发工具所能支持的所有编程语言文件, 完全支持 [Markdown](https://plugins.jetbrains.com/plugin/7793-markdown) | [AsciiDoc](https://plugins.jetbrains.com/plugin/7391-asciidoc) | [IDEA Mind Map](https://plugins.jetbrains.com/plugin/8045-idea-mind-map) | [PlantUML 插件集成](https://plugins.jetbrains.com/plugin/7017-plantuml-integration) 能力, 强大的组织和搜索功能, 修改代码笔记并链接到源文件而无需对源文件做任何修改.

祝你创造个人代码知识库, 在敲代码时无需离开IDE打断心流随时随手可用.  
只需要单一插件, 即可保存你的每日工作笔记, 代码片段, 成为你在复杂项目中工作时大展身手的小助手.

## 手不离开发工具 保存,修改, 复用代码笔记
在编辑器中选中要收藏的代码, 右键点击 `将所选代码添加到笔记 ...` 或者使用 <shortcut key="ShowIntentionActions" />的编辑器意图选择添加笔记, 输入标题后按下<shortcut key="Console.Execute" />键就可以在编辑器行首间距图标显示一个⭐图标, 同时行尾也会显示对应的注释信息. 点击此⭐图标或者按下<shortcut key="ShowIntentionActions" />后即可选择编辑笔记标题, 移动文件夹, 删除笔记等操作.

在开发工具底部会多出一个`⭐代码笔记` 工具窗口, 在这个工具窗口可以进行创建删除虚拟文件夹, 修改编程语言, 修改笔记标题和内容, 新建搜索删除笔记等操作.


## 编辑器

程序员开发, 为了程序员. 支持所有主流编程语言, 外加 300 种编程语言的语法高亮(通过使用JetBrains IDE中内置的[TextMates 包](https://macromates.com/textmate/manual/bundles))并支持所有IDE编辑器功能:

*   一键隐藏代码标红
*   阅读器模式
*   显示行号
*   跳转到引用的源代码文件
*   直接运行代码片段(\* 仅支持 Java 语言并且需要禁用阅读器模式)

## 本地存储
代码笔记是离线优先的应用, 它从设计之初就考虑到数据安全, 当你使用SQLite模式时, 不会有任何数据被发送到网上, 你可备份并复制同步单个 notes.db 文件, 可使用任何第三方同步网盘或者使用U盘备份.

## 同步到印象笔记/Evernote

在此模式下所有代码笔记会存储并同步到Evernote或者印象笔记(需要联网在线).  
当在Evernote或者印象笔记中修改了笔记内容时, 请不要忘了在开发工具的Evernote工具窗口中点击 **刷新**按钮.  
无需离开IDE即可浏览Evernote或者印象笔记中通过浏览器剪藏功能收藏的网页, 正确显示富文本内容和图片.  
Evernote/印象笔记集成功能仍在持续迭代中, 欢迎反馈问题或者建议!

[plugin]: https://plugins.jetbrains.com/plugin/17501
[plugin-img]: https://img.shields.io/badge/plugin-Notes-x.svg?logo=IntelliJ%20IDEA