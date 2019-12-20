
# Markdown使用-4 表格

`Markdown`本身有表格语法，它也支持`HTML`表格

---

目录

1. <a id="T1" href="#C1" target="_self">`Markdown`表格语法</a>
2. <a id="T2" href="#C2" target="_self">`HTML`表格语法</a>
3. <a id="T3" href="#C3" target="_self">在线编辑</a>

---

## <a id="C1" href="#T1" target="_self">`Markdown`表格语法</a>

参考：[Tables](https://www.markdownguide.org/extended-syntax/#tables)

Markdown的表格语法如下：

    | Syntax      | Description | Description1 |
    | ----------- | ----------- | ------------ |
    | Header      | Title       | Title1       |
    | Paragraph   | Text        | Text1        |

    To add a table, use three or more hyphens (---) to create each column’s header, and use pipes (|) to separate each column. You can optionally add pipes on either end of the table.

| Syntax      | Description | Description1 |
| ----------- | ----------- | ------------ |
| Header      | Title       | Title1       |
| Paragraph   | Text        | Text1        |

使用3个或更多的连字符（`-`）来创建每列的头，使用竖线（`|`）来分离每列

### 对齐

    | Syntax      | Description | Test Text     |
    | :---        |    :----:   |          ---: |
    | Header      | Title       | Here's this   |
    | Paragraph   | Text        | And more      |

    You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

如果想要对齐每列（左，中，右），可以在连字符上加上分号（`:`），加在左边表示向左对齐，加在两侧表示居中对齐，加在右边表示向右对齐。

---

## <a id="C2" href="#T2" target="_self">`HTML`表格语法</a>

参考：[HTML 表格](http://www.w3school.com.cn/html/html_tables.asp)

同样的，在`Markdown`上也可以使用`HTML`表格语法，相比之下，使用`HTML`语法可以实现更多的样式。

    <table>
        <tr>
            <td>1行1列</td>
            <td>1行2列</td>
        </tr>
        <tr>
            <td>2行1列</td>
            <td>2行2列</td>
        </tr>
    </table>

<table>
    <tr>
        <td>1行1列</td>
        <td>1行2列</td>
    </tr>
    <tr>
        <td>2行1列</td>
        <td>2行2列</td>
    </tr>
</table>

标签`<table>`表示表格，标签`<tr>`表示行，标签`<td>`表示列

### 边界

如果想要显示边界，在`<table>`属性中设置`border`

    <table border="1">
        <tr>
            <td>1行1列</td>
            <td>1行2列</td>
        </tr>
        <tr>
            <td>2行1列</td>
            <td>2行2列</td>
        </tr>
    </table>

<table border="1">
    <tr>
        <td>1行1列</td>
        <td>1行2列</td>
    </tr>
    <tr>
        <td>2行1列</td>
        <td>2行2列</td>
    </tr>
</table>

### 表头

使用标签`<th>`表示表头

    <table border="1">
        <tr>
            <th>表头</a>
            <th>第二个表头</a>
        </tr>
        <tr>
            <td>1行1列</td>
            <td>1行2列</td>
        </tr>
        <tr>
            <td>2行1列</td>
            <td>2行2列</td>
        </tr>
    </table>

<table border="1">
    <tr>
        <th>表头</a>
        <th>第二个表头</a>
    </tr>
    <tr>
        <td>1行1列</td>
        <td>1行2列</td>
    </tr>
    <tr>
        <td>2行1列</td>
        <td>2行2列</td>
    </tr>
</table>

表头`<th>`即可用于行，也可表示列

    <table border="1">
        <tr>
            <th>姓名</th>
            <td>Bill Gates</td>
        </tr>
        <tr>
            <th>电话</th>
            <td>555 77 854</td>
        </tr>
        <tr>
            <th>电话</th>
            <td>555 77 855</td>
        </tr>
    </table>

<table border="1">
    <tr>
        <th>姓名</th>
        <td>Bill Gates</td>
    </tr>
    <tr>
        <th>电话</th>
        <td>555 77 854</td>
    </tr>
    <tr>
        <th>电话</th>
        <td>555 77 855</td>
    </tr>
</table>

### 标题

使用标签`<caption>`设置表格标题

    <table border="1">
        <caption>电话簿</caption>
        <tr>
            <th>姓名</th>
            <td>Bill Gates</td>
        </tr>
        <tr>
            <th>电话1</th>
            <td>555 77 854</td>
        </tr>
        <tr>
            <th>电话2</th>
            <td>555 77 855</td>
        </tr>
    </table>

<table border="1">
    <caption>电话簿</caption>
    <tr>
        <th>姓名</th>
        <td>Bill Gates</td>
    </tr>
    <tr>
        <th>电话1</th>
        <td>555 77 854</td>
    </tr>
    <tr>
        <th>电话2</th>
        <td>555 77 855</td>
    </tr>
</table>

### 跨越多行或多列

在标签`<td>`或者`<th>`上设置属性`colspan`表示跨越多列，设置属性`rowspan`表示跨越多行

    <table border="1">
        <caption>电话簿</caption>
        <tr align="center">
            <th>姓名</th>
            <td>Bill Gates</td>
            <td colspan="2">hehe</td>
        </tr>
        <tr>
            <th>电话</th>
            <td>555 77 854</td>
            <td>555 77 855</td>
            <td>555 77 856</td>
        </tr>
    </table>

<table border="1">
    <caption>电话簿</caption>
    <tr align="center">
        <th>姓名</th>
        <td>Bill Gates</td>
        <td colspan="2">hehe</td>
    </tr>
    <tr>
        <th>电话</th>
        <td>555 77 854</td>
        <td>555 77 855</td>
        <td>555 77 856</td>
    </tr>
</table>

    <table border="1">
        <caption>电话簿</caption>
        <tr align="center">
            <th>姓名</th>
            <th>电话</th>
        </tr>
        <tr>
            <td>Bill Gates</td>
            <td>555 77 854</td>
        </tr>
        <tr>
            <td rowspan="2" align="center">hehe</td>
            <td>555 77 855</td>
        </tr>
        <tr>
            <td>555 77 856</td>
        </tr>
    </table>

<table border="1">
    <caption>电话簿</caption>
    <tr align="center">
        <th>姓名</th>
        <th>电话</th>
    </tr>
    <tr>
        <td>Bill Gates</td>
        <td>555 77 854</td>
    </tr>
    <tr>
        <td rowspan="2" align="center">hehe</td>
        <td>555 77 855</td>
    </tr>
    <tr>
        <td>555 77 856</td>
    </tr>
</table>

### 对齐

使用属性值`align`设置对齐方式，它可以应用于每一种标签：

* 在标签`<table>`中设置，表示表格居中
* 在标签`<tr>`中设置，表示行文字对齐
* 在标签`<td>`中设置，表示列文字对齐

---

## <a id="C3" href="#T3" target="_self">在线编辑</a>

参考：[Tables Generator – 在线生成 LaTeX、HTML、Markdown 表格](https://www.appinn.com/tables-generator/)

有一个在线表格生成器：[Tables Generator](http://www.tablesgenerator.com/html_tables)，可用于生成`Markdown`表格和`HTML`表格

还有一个`W3C`的在线编辑器：[html_tables](http://www.w3school.com.cn/tiy/t.asp?f=html_tables)