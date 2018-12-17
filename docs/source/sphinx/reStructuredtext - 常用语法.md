
# 常用`reStructuredtext`语法

`sphinx`使用`reStructuredtext`作为标记语法，下面学习一些相关的内容

## 注释

使用..表示注释

    .. 注释内容

    或

    .. 注释1
        注释2
        注释3

## 列表和类引号块

列表和类引号块的使用和`markdown`类似

列表

    * This is a bulleted list.
    * It has two items, the second
    item uses two lines.

    1. This is a numbered list.
    2. It has two items too.

    #. This is a numbered list.
    #. It has two items too.

类引号块

    * this is
    * a list

        * with a nested list
        * and some subitems

    * and here the parent list continues

进行嵌套时，必须空一行

## 标题

段标题通过在标题下一行输入等于号（`'=='`）实现，注意：`==`至少和标题一样长

    这是一个标题
    ===========

还有其他符号表示不同的段落

    # with overline, for parts
    * with overline, for chapters
    =, for sections
    -, for subsections
    ^, for subsubsections
    ", for paragraphs







