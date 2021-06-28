---
layout: "lesson"
lang: "zh-Hans"
title: "LaTeX 文档基本结构"
description: "本课展示了 LaTeX 文档的基本结构，以及如何将其构建为一个PDF文件，还有用于控制 LaTeX 的主要特殊字符。"
toc-anchor-text: "Document structure"
toc-description: "The basic structure of a document."
---

# LaTeX 文档基础结构

<span
  class="summary">本课展示了LaTeX文档的基本结构，以及如何将其构建成一个PDF文件，还有用于控制LaTeX的主要特殊字符。</span>

你的第一个 LaTeX 文档将非常简单：目的是向你展示一个文档的外观和如何成功排版。这也是你第一次看到 [如何使用](help) `learnlatex.org` 上的例子的机会。

如果你使用的是本地 LaTeX 安装，在你的编辑器中创建一个名为 `first.tex` 的新文件，然后复制-粘贴下面的文本或将其输入。

如果你使用的是在线系统，你可以直接点击例子中的 `在 TeXLive.net 运行` 或 `在 Overleaf 中打开` 按钮进行尝试。

<p
  class="hint">我们建议，即使你已经在本地配置了 LaTeX，也要尝试一下在线选项；这是一个很好的机会，可以看到不同系统是如何工作的。
  We suggest you try out the online options even if you have set up LaTeX locally; this is a good chance to see how the different options work.</p>

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

保存文件并将其排版为 PDF 文件。如果你使用的是本地的LaTeX安装，具体要按什么按钮取决于你选择的编辑器。你应该得到一个包含上述文本 **和** 页码的 PDF 文件；LaTeX会自动添加页码。

用你喜欢的任何查看 PDF 的程序查看输出的 `first.pdf`。看起来很不错，祝贺你！

如果你想得到 HTML 文件而不是 PDF，请看一下[帮助]((./help))，看看如何做到这一点。

## 处理错误

错误发生。检查你是否完全按照上面的写法输入了文本文件中的每一行。有时，看似很小的输入变化会给结果带来很大的变化，包括导致文件不能工作。如果你陷入困境，试着清空文件，然后重新复制上面的例子。

如果你的 LaTeX 排版运行以一个问号结束，那么你可以通过输入 `x` 和 `<Enter>` 来退出。

LaTeX的错误信息在尽可能变得有帮助的，但它们与其他文字处理软件的信息不一样。有些编辑器也很难以看到 "完整" 的错误信息，这可能会隐藏关键细节。LaTeX 总是创建一个关于它正在做什么的日志；这是一个以 `.log` 结尾的文本文件。你可以在那里看到完整的错误信息，如果你有问题，LaTeX 的专业用户通常会要求你提供一份日志文件的副本。

<p
  class="hint">我们在 <a href="./lesson-15">第 15 课</a> 中介绍了更多关于处理错误的内容。</p>

## 你得到了什么

第一个文件展示了基础知识。LaTeX文档是文本和命令的混合体。命令以反斜线("\")开始，有时在大括号里有参数（或有时在方括号中有可选参数）。然后你通过使用 LaTeX 对你的文件进行排版，得到一个输出的 PDF。

每个LaTeX文档都有一个 `\begin{document}` 和一个匹配的 `\end{document}`。在这两者之间是文档的 *主体*，即你的内容所在。这里的正文有两个段落（在LaTeX中，你用一个或多个空行来分隔段落）。在 `\begin{document}` 之前是 *文档序言(preamble)*，其中有设置文档布局的代码。`\usepackage` 命令将在后面的课程中介绍，在本网站的大多数例子中，它被用来设置字体编码。

LaTeX还有其他 `\begin{...}` 和`\end{...}` 的搭配；我们称这些为 *环境(environments)*。你必须正确匹配它们，以便每一个 `begin{x}` 都有一个 `end{x}`。如果你对它们进行嵌套，那么你必须有`\end{y} ... \end{x}` 来匹配 `\begin{x} ... \begin{y}`，即按 `\begin` 和 `\end` 语句的顺序匹配。

我们可以在 LaTeX 文件中添加以 `%` 开头的注释；让我们用它来显示结构：

```latex
\documentclass[a4paper,12pt]{article} % 使用选项的的 document class
\usepackage[T1]{fontenc}
% 在序言里的注释
\begin{document}
% 这是一个注释
This is   a simple
document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```

你可以看到上面我们有两个段落：注意，我们使用了一个空行来做到这一点。与此同时还注意到，多个空格被当作一个空格处理。

有时你可能还需要一个不跨行的"硬"空格（译者注：hard space，又叫non-breaking space，不换行空格）：在LaTeX中，我们可以用 `~` 来创建，把两段文字"绑"在一起。当我们在课程的后期开始创建交叉引用时，这一点特别有用。

## 特殊字符

你可能已经发现，对LaTeX来说 `\`、`{` 和 `}` 有特殊的含义。以 `\` 起始是 LaTeX 指令：一个 "命令"。大括号字符 `{` 和 `}`用于显示 _强制性参数（mandatory arguments）_ ：命令需要的信息。

还有其他一些具有特殊意义的字符，例如，我们刚刚看到 `~` 是一个"硬"空格。几乎所有这些字符在正常文本中都是 _非常_ 不常见的，这就是为什么它们被选为特殊含义的原因。如果你确实需要显示这些特殊字符中的一个，我们已经在 [进一步的细节页面](more-03) 中提供了一些信息。

## 练习

实验一下在线编辑和排版系统；点击按钮来排版内容，然后在网页中编辑，再重新排版。

试着在你的第一个文件中添加文本，排版并在你的 PDF 中看看发生了什么变化。增加一些不同的段落和可变的空格区域。探索你的编辑器是如何工作的；点击你的源码，找到如何在你的 PDF 中转到同一行。尝试添加一些硬空格，看看它们如何影响断行。
