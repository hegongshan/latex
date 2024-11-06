### 准备工作

第一步，导入fancyhdr包

```tex
% 导入宏包
\usepackage{fancyhdr}
```

第二步，将页面样式设置为`fancy`，并清空页眉和页脚

```tex
% 将页面样式设置为fancy
\pagestyle{fancy}
% 清除页眉和页脚
\fancyhf{}
```

### 设置页眉

```tex
\fancyhead[positions]{header}
```

其中，`positions`表示页眉的位置，可选值有：

* `L`：left，位于页面左侧
* `C`：center，位于页面中间
* `R`：right，位于页面右侧
* `O`：odd，奇数页
* `E`：even，偶数页

对于header

* `\thesection`表示当前节的节号
* `\leftmark`表示当前章标题
* `\rightmark`表示当前节标题

调整页眉下面的那条横线宽度：

```tex
\renewcommand{\headrulewidth}{2pt}
```

如果需要区分奇偶页，需要将当前文档设置为双面文档

```tex
\documentclass[twoside]{article}

% 使用中文
\usepackage{ctex}

\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\fancyhead[RO]{奇数页右页眉}
\fancyhead[LE]{偶数页左页眉}
```

### 设置页脚

```tex
\fancyfoot[positions]{footer}
```

`positions`的可选值与页眉相同。

对于footer，使用`\thepage`表示当前页的页号

例如：

```tex
\fancyfoot[C]{\thepage}
```

调整页脚上面的那条横线宽度

```tex
\renewcommand{\footrulewidth}{2pt}
```

### 示例

```tex
\documentclass[twoside]{article}

% 使用中文
\usepackage{ctex}

\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\fancyhead[RO]{奇数页右页眉}
\fancyhead[LE]{偶数页左页眉}
\fancyfoot[C]{\thepage}
\renewcommand{\headrulewidth}{2pt}
\renewcommand{\footrulewidth}{2pt}

\begin{document}
	\section{第1节}
	\clearpage
	\section{第2节}
	\clearpage
\end{document}
```
