# Markdown


mdBook 的[解析器](https://github.com/raphlinus/pulldown-cmark)遵循[CommonMark](https://commonmark.org/)规范。 您可以学习快速[教程](https://commonmark.org/help/tutorial/)，或实时[试用](https://spec.commonmark.org/dingus/) CommonMark。 
完整的 Markdown 概述超出了本文档的范围，但以下是一些基础知识的高级概述。 
如需更深入的体验，请查看 [Markdown 指南](https://www.markdownguide.org)。


## 文本和段落

文本渲染相对可预测：

```markdown
Here is a line of text.

This is a new line.
```

看起来像您期望的那样：

Here is a line of text.

This is a new line.

## 标题

标题使用`#`标记并且应该单独在一行上。 更多`#`意味着更小的标题：

```markdown
### A heading 

Some text.

#### A smaller heading 

More text.
```

### 一个标题

Some text.

#### 一个更小的标题

More text.

## 列表

列表可以是无序或有序的。 有序列表将自动排序：

```markdown
* milk
* eggs
* butter

1. carrots
1. celery
1. radishes
```

* milk
* eggs
* butter

1. carrots
1. celery
1. radishes

## 链接

链接到 URL 或本地文件很容易：

```markdown
Use [mdBook](https://github.com/rust-lang/mdBook). 

Read about [mdBook](mdBook.md).

A bare url: <https://www.rust-lang.org>.
```

Use [mdBook](https://github.com/rust-lang/mdBook). 

Read about [mdBook](mdBook.md).

A bare url: <https://www.rust-lang.org>.

## 图片

包含图像只是包含指向它们的链接的问题，就像上面的 链接 部分一样。 以下 markdown 包含在与此文件相同级别的 `images` 目录中找到的 Rust 徽标的 SVG 图像：

```markdown
![The Rust Logo](images/rust-logo-blk.svg)
```

使用 mdBook 构建时生成以下 HTML：

```html
<p><img src="images/rust-logo-blk.svg" alt="The Rust Logo" /></p>
```

其中，当然显示图像如下：

![The Rust Logo](images/rust-logo-blk.svg)

有关更多信息，请参阅 [Markdown 指南基本语法文档](https://www.markdownguide.org/basic-syntax/)。
