
# markdown配置

sphinx支持markdown，使用的是[CommonMark](https://commonmark.org/)语法

## 配置

需要安装recommonmark

    pip install recommonmark

然后在配置文件conf.py中添加Markdown解析器

    source_parsers = {
    '.md': 'recommonmark.parser.CommonMarkParser',
    }

增加'.md'作为扩展名

    source_suffix = ['.rst', '.md']


