
# Markdown使用-5 数学公式

`Markdown`标准语法中没有数学公式编辑的内容，之前都是通过图片的形式插入数学公式，现在学会了通过编辑`LaTex`语法的数学公式，然后插入到`Markdown`文件中

---

目录

1. <a id="T1" href="#C1" target="_self">`LaTex`简介</a>
2. <a id="T2" href="#C2" traget="_self">如何编辑数学公式</a>
3. <a id="T3" href="#C3" traget="_self">如何在`Markdown`文件中插入数学公式</a>

---

## <a id="C1" href="#T1" target="_self">`LaTex`简介</a>

参考：

[TeX](http://www.ctex.org/TeX)

[LaTeX](http://www.ctex.org/LaTeX)

[LATEX](https://en.wikibooks.org/wiki/LaTeX)

`Tex`是由`Donald Knuth`创造的一个排版计算机程序（`a typesetting computer program`），它能够将文本文件编译成高质量的文档。

`LaTex`是基于`Tex`的宏定义系统，其目的是为了简化`Tex`的指令操作，使用`LaTex`可以生成复杂的数学公式。

---

## <a id="C2" href="#T2" traget="_self">如何编辑数学公式</a>

`LaTex`为编辑数学公式提供了简单的指令，**但我并不想在这里介绍哪些指令可以实现哪种数学公式**，可以通过公式编辑器，使用图形化的方式编辑数学公式

[LaTeX公式编辑器](http://www.codecogs.com/latex/eqneditor.php)

如果遇到哪个符号没有找到，可以去下面链接快速搜索

[LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)

[MarkDown Latex公式，矩阵，表格等使用](https://blog.csdn.net/u014228934/article/details/78223442#11-%E5%A6%82%E4%BD%95%E8%BE%93%E5%85%A5%E7%9F%A9%E9%98%B5)

*`Markdown`编辑器必须包含`MathJax`引擎来支持`LaTex`数学公式*

---

## <a id="C3" href="#T3" traget="_self">如何在`Markdown`文件中插入数学公式</a>

分为两种情况：

* 对于行内公式而言，在公式两边各一个美元符号（`$`）
* 对于单独一行公式而言，在公式两边各两个美元符号（`$$`）

比如

    $$y(n)=(f\ast g)(n)=\sum_{\tau =\infty}^{\infty}f(\tau )g(n-\tau )d\tau $$

$$y(n)=(f\ast g)(n)=\sum_{\tau =\infty}^{\infty}f(\tau )g(n-\tau )d\tau $$

其中符号$\ast$表示卷积操作，它的实现方式是其中一个函数$f(\tau )$在另一个函数$g(n-\tau )$上的加权求和的过程


    $$H(x,y) = \sum_{i=0}^{M_{i} - 1} \sum_{j=0}^{M_{j}-1} I(x+i - a_{i}, y + j - a_{j})K(i,j)$$


$$H(x,y) = \sum_{i=0}^{M_{i} - 1} \sum_{j=0}^{M_{j}-1} I(x+i - a_{i}, y + j - a_{j})K(i,j)$$

    $$\frac{1}{9}\begin{bmatrix}
    1 & 1 & 1\\ 
    1 & 1 & 1\\ 
    1 & 1 & 1
    \end{bmatrix}$$

$$\frac{1}{9}\begin{bmatrix}
1 & 1 & 1\\ 
1 & 1 & 1\\ 
1 & 1 & 1
\end{bmatrix}$$

    $$\begin{bmatrix}
    1& 2& 3\\ 
    4& 5& 6\\ 
    7& 8& 9
    \end{bmatrix}\Rightarrow \begin{bmatrix}
    3& 2& 1\\ 
    6& 5& 4\\ 
    9& 8& 7
    \end{bmatrix}\Rightarrow \begin{bmatrix}
    9& 8& 7\\ 
    6& 5& 4\\ 
    3& 2& 1
    \end{bmatrix}$$

$$\begin{bmatrix}
1& 2& 3\\ 
4& 5& 6\\ 
7& 8& 9
\end{bmatrix}\Rightarrow \begin{bmatrix}
3& 2& 1\\ 
6& 5& 4\\ 
9& 8& 7
\end{bmatrix}\Rightarrow \begin{bmatrix}
9& 8& 7\\ 
6& 5& 4\\ 
3& 2& 1
\end{bmatrix}$$