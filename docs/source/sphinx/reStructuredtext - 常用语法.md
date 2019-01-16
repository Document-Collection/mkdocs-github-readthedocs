
# `reStructuredtext`语法

`sphinx`使用`reStructuredtext`作为标记语法，下面学习一些相关的内容

* 注释
* 列表
* 类引号块
* 标题
* 源文件引用
* 超链接

## 注释

使用`..`表示注释

    .. 注释内容

    或

    .. 注释1
        注释2
        注释3

## 列表

    * This is a bulleted list.
    * It has two items, the second
    item uses two lines.

    1. This is a numbered list.
    2. It has two items too.

    #. This is a numbered list.
    #. It has two items too.

## 类引号块

    * this is
    * a list

        * with a nested list
        * and some subitems

    * and here the parent list continues

进行嵌套时，必须空一行

## 标题

段标题通过在标题下一行输入等于号（`'=='`）实现（**注意：`==`至少和标题一样长**）

    一级标题
    ===========

    ===========
    二级标题
    ===========

    三级标题
    ^^^^^^^^

    四级标题
    ---------

    五级标题
    >>>>>>>>>

    六级标题
    :::::::::

## 源文件引用

    .. include:: 源文件路径

## 超链接

页内链接

    # 设置锚点
    链接名_
    # 引用锚点
    .. _锚点:

外部链接

    # 在一行内 
    链接名_
    # 单独一行
    .. _reference: 链接名










