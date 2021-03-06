
# 在线发布

在本地新建`sphinx`工程后，将本地文档发送到`github`上，然后就可以在`readthedocs`上发布在线文档

`readthedocs`在`github`有一个模板文档工程

[rtfd/template](https://github.com/rtfd/template)

生成的在线文档：[Welcome to Read the Docs Template’s documentation!](https://zjzstu-demo.readthedocs.io/en/latest/index.html)

## 上传文档

参考：[Importing Your Documentation](https://docs.readthedocs.io/en/latest/intro/import-guide.html#)

上传地址：[import](https://readthedocs.org/dashboard/import/)

如果使用`github`账号登录，那么可以直接在页面上显示你的工程（需要刷新）；否则，需要手动导入

**注意１：不需要上传`build`目录，在`readthedocs`导入时会自动编译**

**注意２：对于已经导入的工程，只要`github`上有更新，那么会自动触发`readthedocs`更新，不再需要手动操作**

## 编译过程

参考：[Build Process](https://docs.readthedocs.io/en/latest/builds.html)

如果你上传的是`sphinx`工程，那么`readthedocs`首先会在`doc`或`docs`文件夹内搜索`conf.py`文件，然后是在其他位置，如果没有会自动生成一个

`readthedocs`完整的编译流程如下：

* 从`github`中`check out`代码，如果已经下载，那么更新代码
* 根据你选择的生成格式（比如`sphinx html`）进行编译
* 将编译完成后的文件从构建服务器复制到应用服务器，复制完成后，就开始工作

**如果要修改为`mkdocs`工程，可以在高级设置中选择文档类型为`Mkdocs`**

### 编译问题

参考：

[解决UnicodeDecodeError: 'ascii' codec can't decode byte 0xe5 in position 108: ordinal not in range(128](https://blog.csdn.net/lengyuewusheng99/article/details/52822450)

[Python3异常-AttributeError: module 'sys' has no attribute 'setdefaultencoding'](https://blog.csdn.net/fly910905/article/details/74922378)

编译`conf.py`文件时，发生中文格式问题

    Running Sphinx v1.7.9
    WARNING: the config value 'epub_title' is set to a string with non-ASCII characters; this can lead to Unicode errors occurring. Please use Unicode strings, e.g. u'Content'.
    WARNING: the config value 'project' is set to a string with non-ASCII characters; this can lead to Unicode errors occurring. Please use Unicode strings, e.g. u'Content'.
    loading translations [en]... done
    making output directory...

    ...
    ...
    UnicodeDecodeError: 'ascii' codec can't decode byte 0xe5 in position 0: ordinal not in range(128)

    Encoding error:
    'ascii' codec can't decode byte 0xe5 in position 0: ordinal not in range(128)
    The full traceback has been saved in /tmp/sphinx-err-VIWOpI.log, if you want to report the issue to the developers.

有两种解决方法：

第一种是针对`python2`，在`conf.py`中如下代码，将编码格式改为`utf-8`

    import sys 
    reload(sys) 
    sys.setdefaultencoding('utf8')

第二种是修改`readthedocs`编译环境，在`Admin->Advanced Settings->Python interpreter:`

将选项修改成`CPython 3.x`




