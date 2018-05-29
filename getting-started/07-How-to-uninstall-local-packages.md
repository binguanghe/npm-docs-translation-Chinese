# 如何卸载本地包

> # How to Uninstall Local Packages

[![Uninstalling local packages](http://img.youtube.com/vi/Z-BpYj6cSoQ/0.jpg)](http://www.youtube.com/watch?v=Z-BpYj6cSoQ "Uninstalling local packages")

要从你的node_modules目录中移除一个包，请使用：

> To remove a package from your node_modules directory, use:

```
npm install lodash
```

要从**package.json**的依赖中移除一个包，你需要使用保存标志。

> To remove it from the dependencies in **package.json**, you will need to use the save flag.

```
npm unistall --save lodash
```

注意：如果你安装了“开发依赖”包（也就是使用 **--save-dev**），**--save**标志的命令将不会从**package.json**移除该包。你必须使用**--save-dev**来卸载它。

#### 测试：

> #### Test:

为了确保**npm uninstall**命令正确运行，请查找**node_modules**目录。以确认里面不再包含一个你卸载的包的目录。

> To confirm that **npm install** work correctly, find the **node_modules** directory. Be sure that it no longer contains a directory for package(s) you uninstalled.

你可以通过运行：

- **ls node_modules** 在Unix系统上，比如“OSX”
- **dir node_modules** 在Windows上

#### 举例

> #### Example:

安装一个名为**lodash**的包来确认命令成功运行，即通过列出**node_modules**的内容并看到一个名为**lodash**的包的文件夹。

> Install a package called **lodash**. Confirm that it ran successfully by listing the contents of the **node_modules** directory and seeing a directory called **lodash**.

使用**npm uninstall**来卸载**lodash**。以确认命令成功运行，即通过列出**node_modules**的内容并确认名为**lodash**的目录的不存在。

> Uninstall **lodash** with **npm uninstall**. Confirm that it ran successfully by listing the contents of the **node_modules** directory and confirming the absence of a directory called  **lodash**.

##### 安装Lodash

> Install Lodash

```
> npm install lodash
> dir node_modules     # use 'ls node_modules' for Unix
```

##### 卸载Lodash

> Uninstall Lodash

```
#=> lodash

> npm uninstall lodash
> dir node_modules     # use 'ls node_modules' for Unix

#=>
```

