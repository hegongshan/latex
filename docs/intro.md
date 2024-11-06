LaTex文档的基本格式:

```tex
\documentclass[option]{article}
% 导入各种工具包
\usepackage{xxx}
\begin{document}
	% 所有的其他内容均放在这里
	content...
\end{document}
```

<!--more-->

### 注释

* 单行注释使用`%`，例如

```tex
% 单行注释
```

* 多行注释使用`\iffalse...\fi`，例如

```tex
\iffalse
Hello \LaTex
Why I like it.
\fi
```

### 使用中文

LaTex默认不支持中文，如果要在文档中显示中文，需要引入`ctex`包

```tex
\usepackage{ctex}
```

### 文章标题

在导言区使用`\title`命令，指定文章的标题。

示例：

```tex
\title{your title}
...
\begin{document}
	...
    % 必须加\maketitle，否则，不能显示标题
    \maketitle 
	content...
\end{document}

```

### 作者

```tex
\author{author name}
% 比如\author{Gongshan He}

\begin{document}
	content...
\end{document}
```

### 摘要

```tex
\begin{abstract}
	content...
\end{abstract}
```

### 目录

在文档合适的地方，加入如下命令即可。

```tex
\tableofcontents
```

### 章节

```latex
% 章
\chapter{}

% 节
\section{}
\subsection{}
\subsubsection{}
```

注意：章会从新页开始，而节则不会。

### 分页

```tex
\clearpage

\newpage
```

### 设置页码格式

设置页码格式，使用`\pagenumbering{}`，例如：

```latex
% 使用小写罗马字体，如i
\pagenumbering{roman}

% 使用大写罗马字体，如I
\pagenumbering{Roman}

% 使用阿拉伯数字
\pagenumbering{arabic}
```

### 插入脚注

```tex
\footnote{xxx}
```

### 文件包含

设想一下，你正在写一篇论文，论文有Introduction、Related Work、Methodology以及Conclusion and Future Work等章节。为了便于修改，你想让每个章节都有各自的tex文件，并在源文件article.tex中导入这些文件。

在LaTex中，有两种方式可以实现文件包含：`\include{}`和`\input{}`，以`\input{}`为例：

```latex
\documentclass[a4paper]{article}

\begin{document}
  \input{introduction}
  \input{Related Work}
  \input{Methodology}
  \input{Conclusion and Future Work}
\end{document}
```

注意：`\include{}`会执行`\clearpage`；而`\input{}`则不会。

### 文字样式

* 斜体：`\textit{}`。例如，`\textit{HR}` => *HR*
* 加粗：`\textbf{}`。例如，`\textbf{NCF}` => **NCF**
* 上标：`\textsuperscript{}`。例如`\textsuperscript{1}` => <sup>1</sup>

### 插入图片

```tex
...
% 引入包
\usepackage{graphicx}
....
\begin{document}
	....
	\begin{figure}
	  \centering
		\includegraphics[scale=0.2]{图片地址}
		\caption{图片标题}
		\label{图片标签}
	\end{figure}
	....
\end{document}
```

* `\includegraphics`：插入一张图片，在方括号[]中控制图片的大小，{}中是图片的地址；
* `\caption`：图片标题；
* `\label`：为图片添加一个标签，便于在其他地方引用该图片。

#### 插入子图

如果需要一次性插入多张图片，则需要导入subfigure包。

```tex
\usepackage{subfigure}
```

然后，通过如下方式插入子图

```tex
\subfigure[子图标题]{
	\includegraphics{子图地址}
}
```

### 插入表格

```tex
\begin{table}
    \caption{表格的标题}
    \begin{tabular}{|ccc|}
        \hline
        直角a & 直角b & 直角c \\
        \hline
        3 & 4 & 5 \\
        5 & 12 & 13 \\
        \hline
    \end{tabular}
\end{table}
```

tabular中有一个参数，里面声明了表格中列的模式。|ccc|表示表格有三列，都是居中对齐，在第一列前面和第三列后面各有一条垂直的表格线。类似的还有l（左对齐）和r（右对齐）。

行与行之间用命令`\\`隔开，每行内部的表项则用符号&隔开。表格中的横线用`\hline`命令。

* 如果一个表格项占多列，需要使用`\multicolumn`命令

```tex
\multicolumn{占几列}{对齐方式}{表格项}
```

示例：占2列，居中对齐，内容为LaTex

```tex
\multicolumn{2}{c}{LaTex}
```

* 如果一个表格项占多行，需要导入包`\usepackage{multirow}`，然后使用`\multirow`命令

```tex
\multirow{占几行}{对齐方式}{表格项}
```

示例：占2行，居中对齐，内容为LaTex

```tex
\multirow{2}{c}{LaTex}
```

* 在使用多列或者多行命令时，可能需要在表格的局部划线，使用`\cline`命令

```tex
% 画出一条从第2列到第8列的横线段
\cline{2-8}
```

### 列表

#### 有序列表

```tex
\begin{enumerate}
    \item Java
    \item C++
\end{enumerate}
```

#### 无序列表

```tex
\begin{itemize}
    \item Java
    \item C++
\end{itemize}
```

### 章节

* 自动编号：`\section{}`、`\subsection{}`、`\subsubsection{}`。
* 不自动编号（且不加入目录中）:`\section*{}`

### 分栏

* 在\documentclass中指定分栏模式

```tex
\documentclass[twocolumn]{article}
```

* 在正文中使用命令切换。\\twocolumn进入双栏模式，\onecolumn进入单栏模式，两个命令都会先使用\clearpage换页，并不产生一页之内单双栏混合的效果。

### 参考文献

可以使用BIBTEX处理参考文献。

将所有可能会引用的文献放到以.bib结尾的文本文件中。

使用`\bibliographystyle`设定参考文献的格式，这通常在导言区完成。

使用`\bibliography`打印出参考文献列表。

例如，当前目录下有一个名为reference.bib的文献数据库，内容如下：

```tex
@inproceedings{He:2017:NCF:3038912.3052569,
 author = {He, Xiangnan and Liao, Lizi and Zhang, Hanwang and Nie, Liqiang and Hu, Xia and Chua, Tat-Seng},
 title = {Neural Collaborative Filtering},
 booktitle = {Proceedings of the 26th International Conference on World Wide Web},
 series = {WWW '17},
 year = {2017},
 isbn = {978-1-4503-4913-0},
 location = {Perth, Australia},
 pages = {173--182},
 numpages = {10},
 url = {https://doi.org/10.1145/3038912.3052569},
 doi = {10.1145/3038912.3052569},
 acmid = {3052569},
 publisher = {International World Wide Web Conferences Steering Committee},
 address = {Republic and Canton of Geneva, Switzerland},
 keywords = {collaborative filtering, deep learning, implicit feedback, matrix factorization, neural networks},
} 
```

指定数据库文件时，不带bib后缀。可以同时从多个文献数据库中提取文献，文件名用逗号分隔开即可。

```tex
\begin{document}

...
% 从文献数据库reference.bib中获取文献信息，打印参考文献列表
\bibliography{reference}
\end{document}
```

在正文中，使用`\cite`命令引用需要的文献，`\cite`命令引用的位置会出现文献的编号，同时将提示LATEX列出所引用的文献

```tex
\begin{document}
...
ncf\cite{He:2017:NCF:3038912.3052569}
% 从文献数据库reference.bib中获取文献信息，打印参考文献列表
\bibliography{reference}
\end{document}
```

### 引用与跳转

1.如果需要在论文中引用公式、图表、脚注等，可以使用`\label`和`\ref`。

```tex
\begin{equation}
\label{xxx}
\end{equation}

Equation \ref{xxx}
```

注意：ref中的内容必须与label中的内容一致，才能完成引用。

2.如果要支持引用跳转，则需要引入`hyperref`包

```tex
\usepackage{hyperref}
```

### 超链接

使用`\url{}`可以插入超链接。

### 特殊符号

| 特殊符号 |          代码           |
| :------: | :---------------------: |
|  破折号  | `---`（三个英文连字符） |

