
# Markdown使用-2 页内跳转

之前学习总结过 `Markdown` 的语法，但是在 `CSDN` 上用 `Markdown` 写博客无法实现页内跳转，一直没有找到很好的解决方法，今天偶然在网上发现新的关于页内跳转的解决方法

---

主要内容:

* <a name="T0" href="#C0">使用 `HTML` 标签 `<a>`</a>
    * <a id="T0.1" href="#C0.1">使用 `id` 属性</a>
* <a id="T1" href="#C1" target="_self">属性 `target="_self"`</a>
* [生成目录](#3)

---

参考：

[MarkDown使用-1](https://blog.csdn.net/u012005313/article/details/53558570)

---

## <a name="C0" href="#T0">使用 `HTML` 标签 `<a>`</a>

因为 `Markdown` 可以嵌入 `HTML` 标签，所以最初我想到的是利用 `HTML` 的锚点标签 `<a>` 实现页内跳转

参考：[HTML <a> 标签](http://www.w3school.com.cn/tags/tag_a.asp)

`W3School` 中给出了业内跳转的示例：

参考：[链接到同一个页面的不同位置](http://www.w3school.com.cn/tiy/t.asp?f=html_link_locations)

使用方法如下，在 `A` 处设置锚点，定义锚点的名称

    <a name="锚点名称">A</a>

在 `B` 处设置锚点，定义链接指向的页内锚点

    <a href="#锚点名称">B</a>

不过在 `CSDN` 博客使用过程中，这种方式没有起作用

### <a id="C0.1" href="#T0.1">使用 `id` 属性</a>

后来又找到一种方法，是使用 `id` 属性替换 `name` 属性，这次可以跳转了，不过每次跳转操作都会打开一个新的页面

---

## <a id="C1" href="#T1" target="_self">属性 `target="_self"`</a>

今天很偶然的情况下，发现添加属性 `target` 可能会有用

参考：[使用Markdown实现页内跳转](https://blog.csdn.net/maomaolaoshi/article/details/78157676?locationNum=3&fps=1#1)

就是在跳转锚点的时候添加属性 `target="_self"`

在 `W3School` 上找到了相应的解释

参考：[HTML <a> 标签的 target 属性](http://www.w3school.com.cn/tags/att_a_target.asp)

> `<a>` 标签的 `target` 属性规定在何处打开链接文档。
>
>`_self`
>
>这个目标的值对所有没有指定目标的 `<a>` 标签是默认目标，它使得目标文档载入并显示在相同的框架或者窗口中作为源文档。这个目标是多余且不必要的，除非和文档标题 `<base>` 标签中的 `target` 属性一起使用。

---

## <h1 id="3"><center>生成目录</center></h1>

在网上还找到一种方法，就是生成目录语法，实现方式如下

参考：

[MarkDown技巧：两种方式实现页内跳转](https://www.cnblogs.com/JohnTsai/p/4027229.html)

[Markdown页内跳转实现方法](https://www.cnblogs.com/tocy/p/markdown-link-inner-page.html)

在 `A` 处设置目录 

    <h1 id="1">标题1</h1>
    <h1 id="2">标题2</h1>
    // 或
    ## 标题1
    。。。
    ## 标题2

在 `B` 处设置跳转目录

    * [标题1](#1)
    * [标题2](#2)
    // 或
    * [标题1](#标题1)
    * [标题2](#标题2)

**注意：标题名不能有中英文混杂，会造成跳转功能失效**

`sphinx`对于目录跳转语法失效