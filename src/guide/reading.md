# 阅读说明

本章介绍如何阅读mdBook制作的书籍，HTML在线书籍和其他输出格式（如PDF）的书籍格式有所不同。

书籍以*章节* 形式组成,每一节都是单独的一页。很多节按照顺序构成一章。通常每一节以*标题*列表的方式镶嵌在数据的一章中。 

## 导航

浏览书籍章节有好几种方法。

左侧的**侧边栏**提供了所有章节的列表，单击任何章节标题将加载该页面。

如果窗口太窄，特别是在移动显示器上，侧边栏可能不会自动显示。在这种情况下，可以按下页面左上方的菜单图标（三个水平条）来打开和关闭侧边栏。

页面底部的**箭头按钮**可用于导航到上一章或下一章。

键盘上的**左右箭头键**可用于导航到上一章或下一章。

## 顶部菜单栏

页面顶部的菜单栏提供了一些与书籍交互的图标。显示的图标将取决于配置。

| Icon | 描述 |
|------|-------------|
| <i class="fa fa-bars"></i> | 打开或打开侧边栏 |
| <i class="fa fa-paint-brush"></i> | 打开选择器以选择不同的颜色主题。 |
| <i class="fa fa-search"></i> | 打开搜索栏以在书本中搜索。 |
| <i class="fa fa-print"></i> | 使用web浏览器打印整本书。 |
| <i class="fa fa-github"></i> | 打开指向该书源代码的Github地址的链接。 |
| <i class="fa fa-edit"></i> | 打开页面以直接编辑当前正在阅读的页面的源代码。|

点击菜单栏将页面滚动到顶部.

## 搜索

每本书都有一个内置的搜索系统。
单机顶部菜单栏搜索图标(<i class="fa fa-search"></i>) ,或者按键盘上的“S”键将打开搜索框。
输入一些关键词将实时显示匹配的章节和部分.
单击任何结果都将跳转到该部分。向上和向下箭头键可用于导航结果，按键盘确认键将打开突出显示的部分。
加载搜索结果后，匹配的关键字将在文本中突出显示。单击突出显示的单词或按“Esc”键将删除突出显示。

## 代码块

mdBook books are often used for programming projects, and thus support highlighting code blocks and samples.
Code blocks may contain several different icons for interacting with them:
mdBook书籍通常用于编程项目，因此支持高亮显示代码块和代码示例。

代码块可能包含几个不同的图标用于与它们交互：

| Icon | Description |
|------|-------------|
| <i class="fa fa-copy"></i> | 将代码块复制到本地剪贴板，以允许粘贴到另一个应用程序。 |
| <i class="fa fa-play"></i> | 对于 Rust 代码示例，这将执行示例代码并在示例下方显示编译器输出（请参阅 [playground](../format/mdbook.md#rust-playground)）。 |
| <i class="fa fa-eye"></i> | 对于 Rust 代码示例，这将切换“隐藏”行的可见性。 有时，较大的示例会隐藏与所说明内容不特别相关的行（请参阅 [隐藏代码行](../format/mdbook.md#hiding-code-lines)). |
| <i class="fa fa-history"></i> | 对于可编辑代码示例[编辑器](../format/theme/editor.md)，这将撤消您所做的任何更改。 |

这里是一个例子:

```rust
println!("Hello, World!");
```
