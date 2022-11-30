# 安装

mdBook有很多种安装方式,选择以下任何一种最适合你的方法。

如果你需要自动化部署mdBook，请查看[持续集成](../continuous-integration.md)一章，了解有关如何安装的更多示例。

## 下载二进制包安装

在[官方的Github](https://github.com/rust-lang/mdBook/releases),选择匹配你操作系统(Windows, macOS, 或者 Linux)的安装包。

下载后，解压安装包，解压后包含`mdbook`这个可执行文件。

为了以后方便使用，可以吧`mdbook`所在的文件加入你操作系统的环境变量`PATH`中。


## 源码安装

想要源码安装`mdbook`你首先需要安装Rust和Cargo

按照[Rust安装说明](https://www.rust-lang.org/tools/install)上的说明进行操作。mdBook当前至少需要Rust版本1.56。

安装Rust后，可以使用以下命令构建和安装mdBook：

```sh
cargo install mdbook
```
这将自动从[crates.io](https://crates.io/)下载依赖构建mdBook，并将其安装在Cargo的全局二进制目录中（默认为`~/.cargo/bin/`）。

如果要卸载程序, 执行命令`cargo uninstall mdbook`.

### 安装最新版本

发布到`crates.io`的版本将略微落后于GitHub上托管的版本。

如果您需要最新版本，您可以自己构建mdBook的git版本。

Cargo让这件事变得 ***超级简单！***!

```sh
cargo install --git https://github.com/rust-lang/mdBook.git mdbook
```

同样的确保将Cargo bin目录添加到`PATH`中。

如果您对修改mdBook本身感兴趣，请查看[投稿指南](https://github.com/rust-lang/mdBook/blob/master/CONTRIBUTING.md)了解更多信息。
