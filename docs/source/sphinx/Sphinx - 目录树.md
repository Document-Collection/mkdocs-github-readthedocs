

# sphinx目录树

参考：

[Directives](http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#table-of-contents)

[Defining document structure](http://www.sphinx-doc.org/en/master/usage/quickstart.html#defining-document-structure)

[目录树](https://zh-sphinx-doc.readthedocs.io/en/latest/markup/toctree.html#toctree-directive)

---

## 指令

reStructuredtext包含了多种指令，其格式如下：

    .. directive_name::arguments
       :option1:
       :option2:

       content

directive_name表示指令名

arguments表示指令参数，直接跟在双冒号之后，由指令觉得是否有参数，有多少个

options表示指令选项，以字段列表的形式存在

content表示指令内容，跟在指令和选项之后，间隔一行进行，由指令确定是否允许内容，以及做什么

常见问题：**内容应该缩进到与选项相同的级别**，比如

    .. toctree::
       :maxdepth: 2
       
       usage/installation
       usage/quickstart

---

## toctree

使用sphinx-quickstart生成工程后，index.rst文档如下：

    .. sphinx使用 documentation master file, created by
    sphinx-quickstart on Sun Dec 16 15:27:21 2018.
    You can adapt this file completely to your liking, but it should at least
    contain the root `toctree` directive.

    Welcome to sphinx使用's documentation!
    ======================================

    .. toctree::
       :maxdepth: 2
       :caption: Contents:

    Indices and tables
    ==================

    * :ref:`genindex`
    * :ref:`modindex`
    * :ref:`search`

其中toctree表示一个指令，它用于生成目录树（table of content tree）

toctree有几个特殊选项：maxdepth、caption、readonly

### 添加文档

在toctree指令中可以添加文档，将文档名添加到指令内容即可，比如

    .. toctree::
       :maxdepth: 2
       :caption: Contents:

       Sphinx使用 - html主题
       zj_rst

其中Sphinx使用 - html主题和zj_rst就是文档名

**注意1：文档内容要和选项相同级别（同一条竖线下）**

**注意2：文档中必须要有标题**

### maxdepth

maxdepth表示目录树显示的标题深度，maxdepth=1表示显示第一级标记，maxdepth=2表示显示第一和第二级标题，默认情况下所有级别标题都会列出

:maxdepth: 1的情况

    Contents:

    Sphinx使用 - html主题
    zj_rst

:maxdepth: 2的情况

    Contents:

    Sphinx使用 - html主题
        * 内置主题
        * 修改
        * 自定义
    zj_rst

### caption

caption用于生成目录树标题，当前是Content，比如，修改成“目录树”

    目录树:

    Sphinx使用 - html主题
    zj_rst
