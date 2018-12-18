
# `markdown`配置

`sphinx`支持`markdown`，使用的是[CommonMark](https://commonmark.org/)语法

## 配置

需要安装`recommonmark`

    pip install recommonmark

然后在配置文件`conf.py`中添加`Markdown`解析器

    source_parsers = {
    '.md': 'recommonmark.parser.CommonMarkParser',
    }

增加`'.md'`作为扩展名

    source_suffix = ['.rst', '.md']

## MathJax

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