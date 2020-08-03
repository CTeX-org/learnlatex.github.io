---
title: "查看说明文档并获取帮助"
---
<!-- Translation to be added _after_ English text completed. -->

有数种途经以查看一个宏包或者文档类的说明文档。

## `texdoc`

如果你安装了一个 TeX 发行版（例如，TeXLive、MikTeX），并在安装的时候包含了文档系统，那么可以通过命令行工具 `texdoc` 访问本地存储的文档。使用：


`texdoc` < _pkg_ >


将打开包 `<pkg>` 对应的文档。程序将会搜索可用文档，并打开其中它认为最为匹配你给出的搜索项的结果。使用：


`texdoc -l` < _pkg_ >


以列出所有可能的结果，并从中选择你想要的。


## texdoc.net

这是一个类似于 `texdoc` 工具的[网站](https://texdoc.net/)。通过它你可以像 `texdoc -l` 那样，搜索各种可及文档，然后从中选择你所期望的结果。


## CTAN

[CTAN](https://www.ctan.org) 全称 Comprehensive TeX Archive Network（即 “TeX 综合资料网”）。绝大部分的 LaTeX 包在这发布。你可以通过在站点上搜索这些包以访问其文档。一般而言，这些包被保存在 `ctan.org/pkg/<pkg-name>`，于此你便可以阅读这些保存在 CTAN 上的包的 README 和文档。


## 关于 LaTeX 的书籍

这里有若干本用以进一步提升你 LaTeX 水平的图书。刚起步的时候，你总能从那些精密组织的入门指南上获益良多，毕竟他们能给出比我们这儿讨论的要上多许多的细节。同样，你也许还希望获得一本包含更多细节和推荐的参考书。

LaTeX 小组有一个主要有其成员完成的书的[书籍清单](https://www.latex-project.org/help/books)。最值得一提的是 [Lamport 纂写的官方指南](https://www.informit.com/store/latex-a-document-preparation-system-9780201529838)以及所涉甚广的 [LaTeX Companion](https://www.informit.com/store/latex-companion-9780201362992)。

其他旨在学习 LaTeX 的书籍有如：


- [_Guide to LaTeX_](https://www.informit.com/store/guide-to-latex-9780132651714)，由  Helmut
  Kopka 及 Patrick Daly 所著——可作为电子版获得。
- [_LaTeX for Complete Novices_](https://www.dickimaw-books.com/latex/novices/) 由
  Nicola Talbot 所著——可获得免费的电子版，还可选择低价印刷版。
- [_Using LaTeX to write a PhD thesis_](https://www.dickimaw-books.com/latex/thesis/) 自
  Nicola Talbot——可获得免费的电子版，亦可选择低价印刷版。
- [_LaTeX Beginner's Guide_](https://www.packtpub.com/gb/hardware-and-creative/latex-beginners-guide)
  自 Stefan Kottwitz——电子版和印刷版均可获得。
- [_LaTeX and Friends_](https://www.springer.com/gp/book/9783642238154) 由
  Marc van Dongen 所著——电子版和印刷版均可获得。


## 寻求帮助

你可以在许多在线论坛询问 LaTeX 的相关问题；其中当下风靡的也许是 [TeX - LaTeX StackExchange](https://tex.stackexchange.com)。当你遇到任何问题，首先最好给出一个清楚的例子 —— 也就是为人所熟知的“最小工作案例”（MWE）。这并不意味着这段代码真的起作用（不然你当然就不需要提问了！），而表示你已然尽力使问题代码清晰、独立并且最简。后者意味着它仅有能充分展示问题的文本。

该如何构建一个 MWE？通常，最简单的方法是从：

```latex
\documentclass{article}
\begin{document}
Text
\end{document}
```

开始并逐行增加直到问题复现。或者，你也可以尝试“削减”你的原始文本，但是这可能耗费较长的时间。

如果你需要更多的文本来展示分页或者别的什么效果，则不妨尝试用 `lipsum` 这样的宏包以生成假文段落，以免测试文件过大。


日志文件（即 log 文件）可能是另一个你想要获得的东西；它由 LaTeX 于每次运行时创建，和你的输入有着相同名字不过以拓展名 `.log` 结尾。你可能需要选择“显示拓展”以找出它，这依赖于你的桌面界面。