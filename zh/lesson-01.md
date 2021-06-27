---
layout: "lesson"
lang: "zh"
title: "什么是 LaTeX 以及其是如何工作的"
toc-anchor-text: "Anchor"
toc-description: "Description"
---

# LaTeX 基础

<span
  class="summary">本课程解释了什么是 LaTeX 的基本知识，以及相比于常见的文字处理软件（如 Microsoft Word 或 LibreOffice Writer）其的工作方式。</span>

与常见的文字处理软件（如 Microsoft Word 或 LibreOffice Writer）不同，LaTeX 通常不提供  WYSIWYG（'What You See Is What You Get', "所见即所得"）的特性。使用 LaTeX 需要使用纯文本，并用标记（mark）来充实它。与 HTML 类似，这种标记告诉 LaTeX 文本中某些元素的逻辑意义。

以元素 `<h2>` 为例，其表示HTML文档中的一个新章节。
LaTeX 也有一个类似的命令，在这里我们可以使用 `\section` 命令。

## LaTeX 工作流

因为 LaTeX 文件不是文档本身，而是关于文档每个部分应该是什么的指示，所以你通常不会把你的 LaTeX 文件本身交给其他人。相反，在写完你的LaTeX _源码_ 之后，你在文件上运行 LaTeX（通常使用一个称为 `pdflatex` 的程序）来创建一个 PDF 文件。这个 PDF 文件就是你发送给别人的东西。

不同的人使用不同的语言来描述这个过程。由于使用 LaTeX 有点像编程，所以其经常被称为 "编译" 你的文件，尽管使用 "排版" 更加贴切。

## 多次运行 LaTeX

对于简单的文件，你只需要对文件进行一次排版，就可以得到完整的 PDF。但是一旦你开始添加更复杂的东西，如交叉引用、引用、数字和目录，你可能需要运行 LaTeX 不止一次。我们会告诉你这种情况是什么时候。

## LaTeX 或 pdfLaTeX 或是 ...

在 [下一课](lesson-02) 中，我们将了解到 LaTeX 并不是一个单一的程序。为了不让一切过于复杂，我们将把重点放在一个特定的 LaTeX 程序上，即 pdfLaTeX，用于创建你的 PDF。我们将在课程的后半部分查看其他一些程序，以及为什么你可能想使用它们。
