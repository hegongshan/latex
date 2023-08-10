使用`$`或者`$$`来标明需要解析的公式。`$`表示行内公式，而`$$`表示的数学公式会独占一行，如

`$y=ax+b$`： $y=ax+b$

`$$y=ax+b$$`：
$$
y=ax+b
$$

<!--more-->

#### 输入分数

示例：`$\frac{1}{3}$` 或者　`$1 \over 3$`

显示：$\frac{1}{3}$

#### 开根号

示例：`$\sqrt{3}$` 或者 `$\sqrt[n]{3}$`

显示：$\sqrt{3}$、$\sqrt[n]{3}$

#### 上下标

^表示上标，_表示下标。如果上下标的内容多于一个字符，则需要用{ }括起来。

示例：`$e^2$`、`$e^{ax+b}$`、

显示：$e^2$、$e^{ax+b}$

#### 对数

* 普通对数：`$\log_2{8}$` => $\log_2{8}$
* 自然对数：`$\ln 8$` => $\ln 8$
* 常用对数：`$\lg 100$` => $\lg 100$\

#### 取模

`a \mod b` => $a \mod b$

#### 累加、累乘

* 累加：`$\sum_{i=1}^n (i^2+2i+1)$`　=> $\sum_{i=1}^n (i^2+2i+1)$
* 累乘：`$\prod_{i=1}^n \frac{1}{i^2}$` => $\prod_{i=1}^n \frac{1}{i^2}$

#### 向量

示例：`$\vec x$` => $\vec x$

#### 积分

示例：`$\int_a^b sinx dx$` => $\int_a^b sinx dx$

#### 无穷

示例：`$\infty$` $\Rightarrow$  $\infty$

#### 偏导数

示例：`$\frac{\partial f(x,y)}{\partial x}$` => $\frac{\partial f(x,y)}{\partial x}$

#### 梯度

示例：`$\nabla f$` => $\nabla f$

#### 标签

示例：`$$(a+b)(a-b)=a^2-b^2 \tag{1.1}$$`
$$
(a+b)(a-b)=a^2-b^2 \tag{1.1}
$$

#### 最大、最小

最大：`$$\max_{x} y$$`
$$
\max_{x} y
$$
最小：`$$\min_{x} y$$`
$$
\min_{x} y
$$

arg max：`$$\mathop{\arg\max}_{x} y$$`
$$
\mathop{\arg\max}_{x} y
$$
arg min：`$$\mathop{\arg\min}_{x} y$$`
$$
\mathop{\arg\min}_{x} y
$$

#### 统计估计

示例：`$$\hat y$$ `
$$
\hat y
$$

#### 向上（下）取整

向上取整：`$$\left \lceil \frac{a}{b} \right \rceil$$`
$$
\left \lceil \frac{a}{b} \right \rceil
$$
向下取整：`$$\left \lfloor \frac{a}{b} \right \rfloor$$`
$$
\left \lfloor \frac{a}{b} \right \rfloor
$$

#### 空格

空一格：`a\ b ` => $a \ b$

空四格：`a \quad b` => $a \quad b$

空八格：`a \qquad b` $\Rightarrow$ $a \qquad b$

#### 绝对值、范数

绝对值：`\lvert x \rvert` $\Rightarrow$ $\lvert x \rvert$

范数：`\lVert x \rVert` $\Rightarrow$ $\lVert x \rVert$

#### 对齐

```
$$
\begin{align}
y &= (a-b)(a+b) \\
&= a^2 - b^2
\end{align}
$$
```

$$
\begin{align}
y &= (a-b)(a+b) \\\
&= a^2 - b^2
\end{align}
$$

#### 分段函数

```latex
$$
y=
\begin{cases}
0,& x < 0 \\
0.5,& x = 0 \\
1,& x > 0
\end{cases}
$$
```

$$
y=
\begin{cases}
0,& x < 0 \\\
0.5,& x = 0 \\\
1,& x > 0
\end{cases}
$$

#### 矩阵

* 不带括号的矩阵

```latex
$$
A = 
\begin{matrix}
2 & 0 \\
0 & 5
\end{matrix}
$$
```

$$
A = 
\begin{matrix}
2 & 0 \\\\
0 & 5
\end{matrix}
$$

* 带括号的矩阵

1.`\begin{vmatrix}...\end{vmatrix}` 
$$
A = 
\begin{vmatrix}
2 & 0 \\\\
0 & 5
\end{vmatrix}
$$


2.`\begin{bmatrix}...\end{bmatrix}` 
$$
A = 
\begin{bmatrix}
2 & 0 \\\\
0 & 5
\end{bmatrix}
$$

3.`\begin{Bmatrix}...\end{Bmatrix}`
$$
A = 
\begin{Bmatrix}
2 & 0 \\\
0 & 5
\end{Bmatrix}
$$
4.`\begin{pmatrix}...\end{pmatrix}`
$$
A = 
\begin{pmatrix}
2 & 0 \\\
0 & 5
\end{pmatrix}
$$

#### 省略号

|       省略号        |   符号   |
| :-----------------: | :------: |
| 水平省略号 $\cdots$ | `\cdots` |
| 垂直省略号 $\vdots$ | `\vdots` |
| 对角省略号 $\ddots$ | `\ddots` |

#### 括号

|          括号          |          符号          |
| :--------------------: | :--------------------: |
|  $\overbrace{x,y,z}$   |  `\overbrace{x,y,z}`   |
| $\underbrace{x_1,x_2}$ | `\underbrace{x_1,x_2}` |

#### 箭头

|       箭头        |       符号        |
| :---------------: | :---------------: |
|    $\uparrow$     |    `\uparrow`     |
|    $\Uparrow$     |    `\Uparrow`     |
|   $\downarrow$    |   `\downarrow`    |
|   $\Downarrow$    |   `\Downarrow`    |
|   $\rightarrow$   |   `\rightarrow`   |
|   $\Rightarrow$   |   `\Rightarrow`   |
|   $\leftarrow$    |   `\leftarrow`    |
|   $\Leftarrow$    |   `\Leftarrow`    |
| $\leftrightarrow$ | `\leftrightarrow` |
| $\Leftrightarrow$ | `\Leftrightarrow` |
|    $\nearrow$     |    `\nearrow`     |
|    $\searrow$     |    `\searrow`     |
|    $\swarrow$     |    `\swarrow`     |
|    $\nwarrow$     |    `\nwarrow`     |

#### 四则运算

| 四则运算 |   符号   |
| :------: | :------: |
|    +     |    +     |
|    -     |    -     |
| $\times$ | `\times` |
|  $\div$  |  `\div`  |

#### 特殊乘法

- `$x \cdot y$` => $x \cdot y$
- `$x \bullet y$` => $x \bullet y$
- `$x \odot y$` => $x \odot y$
- `$x \otimes y$` => $x \otimes y$

#### 关系运算符

|      关系运算       |      符号      |
| :-----------------: | :------------: |
|       $\leq$        |     `\leq`     |
|       $\geq$        |     `\geq`     |
|       $\neq$        |     `\neq`     |
|      $\approx$      |   `\approx`    |
|        $\ll$        |     `\ll`      |
|        $\gg$        |     `\gg`      |
|    相似于$\sim$     |     `\sim`     |
|      $\simeq$       |    `\simeq`    |
|     全等$\cong$     |    `\cong`     |
|    恒等$\equiv$     |    `\equiv`    |
| 定义为$\triangleq$  |  `\triangleq`  |
|       $\prec$       |    `\prec`     |
|       $\succ$       |    `\succ`     |
|   正比于$\propto$   |   `\propto`    |
| 推出 $\to$、$\gets$ | `\to`、`\gets` |

#### 逻辑运算符

| 逻辑运算  |   符号    |
| :-------: | :-------: |
| $\forall$ | `\forall` |
| $\exists$ | `\exists` |
|  $\land$  |  `\land`  |
|  $\lor$   |  `\lor`   |
|  $\lnot$  |  `\lnot`  |

#### 集合运算符

|       集合运算       |    符号     |   集合运算    |     符号      |   集合运算    |     符号      |
| :------------------: | :---------: | :-----------: | :-----------: | :-----------: | :-----------: |
|        $\cup$        |   `\cup`    |  $\subseteq$  |  `\subseteq`  |     $\in$     |     `\in`     |
|        $\cap$        |   `\cap`    | $\subseteqq$  | `\subseteqq`  |   $\notin$    |   `\notin`    |
|      $\subset$       |  `\subset`  | $\subsetneq$  | `\subsetneq`  | $\varnothing$ | `\varnothing` |
|      $\supset$       |  `\supset`  | $\subsetneqq$ | `\subsetneqq` |  $\emptyset$  |  `\emptyset`  |
| 集合相减 $\setminus$ | `\setminus` |  $\supseteq$  |  `\supseteq`  | $\supsetneqq$ | `\supsetneqq` |

#### 希腊字母

|          小写字母          |            符号            | 大写字母  |   符号    |
| :------------------------: | :------------------------: | :-------: | :-------: |
|          $\alpha$          |          `\alpha`          |           |           |
|          $\beta$           |          `\beta`           |           |           |
|          $\gamma$          |          `\gamma`          | $\Gamma$  | `\Gamma`  |
|          $\delta$          |          `\delta`          | $\Delta$  |  `Delta`  |
|         $\lambda$          |         `\lambda`          | $\Lambda$ | `\Lambda` |
|           $\eta$           |           `\eta`           |           |           |
| $\epsilon$   $\varepsilon$ | `\epsilon`   `\varepsilon` |           |           |
|           $\rho$           |           `\rho`           |           |           |
|          $\zeta$           |          `\zeta`           |           |           |
|           $\xi$            |           `\xi`            |   $\Xi$   |   `\Xi`   |
|           $\pi$            |           `\pi`            |   $\Pi$   |   `\Pi`   |
|          $\theta$          |          `\theta`          | $\Theta$  | `\Theta`  |
|         $ \sigma $         |          `\sigma`          | $\Sigma$  | `\Sigma`  |
|      $\phi$ $\varphi$      |     `\phi`  `\varphi`      |  $\Phi$   |  `\Phi`   |
|           $\psi$           |           `\psi`           |  $\Psi$   |  `\Psi`   |
|           $\mu$            |           `\mu`            |           |           |
|          $\omega$          |          `\omega`          | $\Omega$  | `\Omega`  |
|           $\tau$           |           `\tau`           |           |           |

#### 字体

* 粗体（boldface）：`\mathbf{X}` => $\mathbf{X}$

* 罗马体（roman）：`\mathrm{d}x` => $\mathrm{d}x$

导数的正式写法：`\frac{\mathrm{d} y } {\mathrm{d} x }`
$$
\frac{\mathrm{d} y } {\mathrm{d} x }
$$
以下三种字体仅支持大写字母

* 书写体（calligraphic）：`\mathcal{X}` => $\mathcal{X}$

* script：`\mathscr{X}` => $\mathscr{X}$
* 黑体（Blackboard bold）：`\mathbb{X}` => $\mathbb{X} $

#### 特殊符号

|               特殊符号               |        代码        |
| :----------------------------------: | :----------------: |
|          反斜杠$\backslash$          |    `\backslash`    |
|             星号$\star$              |      `\star`       |
|         度数，例如$30^\circ$         |     `30^\circ`     |
|      手写体$\ell$，区别于数字1       |       `\ell`       |
|         导数简写，撇$\prime$         |      `\prime`      |
|           波浪号$\tilde x$           |    ` \tilde x`     |
| $\overset{def}{=}$、$\overset{b}{a}$ | `\overset{def}{=}` |
|          $\underset{b}{a}$           | `\underset{b}{a}`  |
|       单个字符上划线 $\bar b$        |      `\bar b`      |
|    多个字符上划线 $\overline{ab}$    |  `\overline{ab}`   |
|           微分算子$\nabla$           |      `\nabla`      |



