# 创建书籍

<!--Once you have the `mdbook` CLI tool installed, you can use it to create and render a book.-->
一旦安装了 `mdbook` 命令行工具，您就可以使用它来创建和渲染一本HTML书籍。

## 初始化书籍

`mdbook init` 命令将创建一个包含一本空书的新目录。
为它指定要创建的目录的名称：

```sh
mdbook init my-first-book
```

在生成书之前，它会在命令行交互几个问题。
输入问题后，就可以把当前目录改成新书目录了：

```sh
cd my-first-book
```

渲染书籍的方法有多种，但最简单的方法之一是使用`serve`命令，它将构建您的书籍并启动本地网络服务器：

```sh
mdbook serve --open
```

`--open` 选项将打开您的默认网络浏览器以查看您的新书。
即使在编辑本书内容时，您也可以让服务器保持运行状态，`mdbook` 将自动重建输出并自动刷新您的网络浏览器。

查看 [命令行](../cli/index.html) 以获取有关其他 `mdbook` 命令和 CLI 选项的更多信息.

## 一本书的组成

一本书是由几个文件构建的，这些文件定义了书的设置和布局。

### `book.toml`

在你的书的根目录中，有一个`book.toml`文件描述如何构建你的书的配置。
他是用 [TOML 标记语言](https://toml.io/) 编写的.
通常默认设置足以让你使用。
如果您有兴趣探索 mdBook 提供的更多功能和选项，请查看 [配置](../format/configuration/index.html) 了解更多详细信息。

一个非常基本的 book.toml 可以这么简单:

```toml
[book]
title = "My First Book"
```

### `SUMMARY.md`

本书的下一个主要部分是位于 src/SUMMARY.md 的摘要文件。
该文件包含本书所有章节的列表。
在查看章节之前，必须将其添加到此列表中。

这是一个包含几章的基本摘要文件：

```md
# Summary

[Introduction](README.md)

- [My First Chapter](my-first-chapter.md)
- [Nested example](nested/README.md)
    - [Sub-chapter](nested/sub-chapter.md)
```

尝试在编辑器中打开 src/SUMMARY.md 并添加几章。
如果任何章节文件不存在，`mdbook` 会自动为您创建它们。

有关摘要文件的其他格式化选项的更多详细信息，请查看[SUMMARY.md](../format/summary.md)。

### Source files

你的书的内容都包含在 `src` 目录中。
每一章节都是一个单独的`Markdown`文件。
通常，每一都以带有章节标题的1级标题开始。

```md
# 第一章

内容输入在这里
```

文件的精确布局由您决定。
文件的组织将与生成的 HTML 文件相对应，因此请记住，文件布局是每章URL的一部分。

当 `mdbook serve` 命令运行时，您可以打开任何章节文件并编辑它们。
每次保存文件时，`mdbook` 都会重建这本书并刷新您的网络浏览器。

查看 [Markdown](../format/markdown.md) 以获取有关格式化章节内容的更多信息。

`src` 目录中的所有其他文件都将包含在输出中。
因此，如果您有图像或其他静态文件，只需将它们包含在 `src` 目录中的某个位置。

## 发布书籍

写完书后，您可能希望将它放在某个地方供其他人查看。
第一步是构建本书的输出。
这可以在`book.toml`文件所在的同一目录中使用 `mdbook build` 命令来完成：

```sh
mdbook build
```
这将生成一个名为`book`的目录，其中包含您的书的`HTML`内容。
然后，您可以将此目录放在任何`Web`服务器上以托管它。

有关发布和部署的更多信息，请查看 [持续集成](../continuous-integration.md) 了解更多。