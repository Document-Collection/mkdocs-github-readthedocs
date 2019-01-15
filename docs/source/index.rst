.. sphinx使用 documentation master file, created by
   sphinx-quickstart on Sun Dec 16 15:27:21 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

sphinx+github+readthedocs
======================================

.. toctree::
   :caption: 目录:
   :maxdepth: 1

   sphinx/Sphinx - 介绍
   sphinx/Sphinx - 新建文档工程
   sphinx/Sphinx - 目录树
   sphinx/reStructuredtext - 常用语法
   sphinx/Sphinx - html主题
   sphinx/Sphinx - Markdown
   readthedocs/ReadtheDocs - 介绍
   readthedocs/ReadtheDocs - 在线发布
   readthedocs/ReadtheDocs - 编译问题

Sphinx工程目前还没有完全支持markdown，尤其是对于数学公式

比如在Markdown中，行内数学符号用$...$，行外数学符号用$$...$$

但是在Sphinx工程中，无法实现行内数学符号效果，行外数学符号也只支持单行

所以如果有涉及数学公式的文章，还是使用其他方法好一点

在github上提了一个bug：[Sphinx Markdown MathJax doesn't work correctly #5957](https://github.com/sphinx-doc/sphinx/issues/5957)