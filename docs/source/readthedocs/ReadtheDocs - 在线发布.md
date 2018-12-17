
#　在线发布

在本地新建`sphinx`工程后，将本地文档发送到`github`上，然后就可以在`readthedocs`上发布在线文档

`readthedocs`在`github`有一个模板文档工程

[rtfd/template](https://github.com/rtfd/template)

生成的在线文档：[Welcome to Read the Docs Template’s documentation!](https://zjzstu-demo.readthedocs.io/en/latest/index.html)

## 上传文档

参考：[Importing Your Documentation](https://docs.readthedocs.io/en/latest/intro/import-guide.html#)

上传地址：[import](https://readthedocs.org/dashboard/import/)

如果使用`github`账号登录，那么可以直接在页面上显示你的工程（需要刷新）；否则，需要手动导入

## 编译过程

参考：[Build Process](https://docs.readthedocs.io/en/latest/builds.html)

根据参考文字可知，如果你上传的是`sphinx`工程，那么`readthedocs`首先会在doc或docs文件夹内搜索`conf.py`文件，然后是在其他位置，如果没有会自动生成一个




