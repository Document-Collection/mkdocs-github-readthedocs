
# Sphinx-bug

`Sphinx`工程目前还没有完全支持`markdown`，尤其是对于数学公式。比如在`Markdown`中，行内数学符号用`$...$`，行外数学符号用`$$...$$`，但是在`Sphinx`工程中，无法实现行内数学符号效果，行外数学符号也只支持单行

所以如果有涉及数学公式的文章，还是使用其他方法好一点。在`github`上提了一个`bug`：[Sphinx Markdown MathJax doesn't work correctly #5957](https://github.com/sphinx-doc/sphinx/issues/5957)