
# mkdocs-github-readthedocs

[![Documentation Status](https://readthedocs.org/projects/zj-sphinx-github-readthedocs/badge/?version=latest)](https://zj-sphinx-github-readthedocs.readthedocs.io/en/latest/?badge=latest) [![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme) [![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

>  mkdocs文档制作，github远程托管，readthedocs在线发布

## 内容列表

- [背景](#背景)
- [安装](#安装)
- [用法](#用法)
- [主要维护人员](#主要维护人员)
- [参与贡献方式](#参与贡献方式)
- [许可证](#许可证)

## 背景

[sphinx-github-readthedocs](https://blog.csdn.net/u012005313/article/details/85055398)：

```
CSDN编辑、发布文章不方便，想要找一个本地文档生成工具，最好支持Markdown，同时能够找一个在线发布网站，方便浏览
Sphinx+Github+Readthedocs能够满足要求
```

参考[MkDocs vs Sphinx](https://zhujian.tech/posts/50a5fdf2.html)，使用`MkDocs`替换`Sphinx`

# 安装

文档本地编译需要预先安装以下工具：

```
$ pip install mkdocs
```

## 用法

有两种使用方式

1. 在线浏览文档：[mkdocs+github+readthedocs](https://zj-sphinx-github-readthedocs.readthedocs.io/en/latest/index.html)

2. 本地浏览文档，实现如下：

    ```
    $ git clone https://github.com/zjZSTU/mkdocs-github-readthedocs.git
    $ cd mkdocs-github-readthedocs
    $ mkdocs serve
    ```
   启动本地服务器后即可登录浏览器`localhost:8000`

## 主要维护人员

* zhujian - *Initial work* - [zjZSTU](https://github.com/zjZSTU)

## 参与贡献方式

欢迎任何人的参与！打开[issue](https://github.com/zjZSTU/sphinx-github-readthedocs/issues)或提交合并请求。

注意:

* `GIT`提交，请遵守[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.4/)规范
* 语义版本化，请遵守[Semantic Versioning 2.0.0](https://semver.org)规范
* `README`编写，请遵守[standard-readme](https://github.com/RichardLitt/standard-readme)规范

## 许可证

[Apache License 2.0](LICENSE) © 2019 zjZSTU
