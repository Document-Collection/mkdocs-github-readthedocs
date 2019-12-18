
# MathJax支持

参考：

[Math support for HTML outputs in Sphinx](http://www.sphinx-doc.org/en/master/usage/extensions/math.html)

[Creating equations in Sphinx](https://build-me-the-docs-please.readthedocs.io/en/latest/Using_Sphinx/UsingMathEquationsInSphinx.html)

`Sphinx`教程介绍的是在配置工程时加入`mathjax`选项就可以将公式编辑成图片

我用`markdown`写文档时，在本地生成的文档中无法正确显示公式，但是在首页（`index.rst`）中加入一句

    :math:`\sigma_{1}`

就好了。母鸡？

不过在`readthedocs`中可以正常显示的

$$
\begin{bmatrix} 1& 2& 3\ 4& 5& 6\ 7& 8& 9 \end{bmatrix}\Rightarrow \begin{bmatrix} 3& 2& 1\ 6& 5& 4\ 9& 8& 7 \end{bmatrix}\Rightarrow \begin{bmatrix} 9& 8& 7\ 6& 5& 4\ 3& 2& 1 \end{bmatrix}
$$

---

## `MathJax`不支持

在`sphinx`上使用`markdown`编写数学公式时，扩展`mathjax`的效果很差

比如行间公式`$...$`就无法使用，得用`\\(...)\\`

另外对于另起一行插入数学公式`$$...$$`，如果是单行公式能够支持，但是对于多行公式无法渲染