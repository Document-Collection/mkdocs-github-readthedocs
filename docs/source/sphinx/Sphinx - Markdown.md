
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


