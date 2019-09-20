
# sphinx-github-readthedocs

[![Documentation Status](https://readthedocs.org/projects/zj-sphinx-github-readthedocs/badge/?version=latest)](https://zj-sphinx-github-readthedocs.readthedocs.io/en/latest/?badge=latest) [![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme) [![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

> sphinx文档制作，github远程托管，readthedocs在线发布

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

# 安装

需要预先安装以下工具：

```
$ pip install -U Sphinx
$ sudo apt-get install make
```

## 用法

有两种使用方式

1. 在线浏览文档：[sphinx+github+readthedocs](https://zj-sphinx-github-readthedocs.readthedocs.io/en/latest/index.html)

2. 本地生成文档，实现如下：

    ```
    $ git clone https://github.com/zjZSTU/sphinx-github-readthedocs
    $ cd sphinx-github-readthedocs/docs
    $ make html
    ```
    编译完成后进入`docs/build/html`目录，打开`index.html`文件

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
