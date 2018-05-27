# 如何安装本地包

> # How to install local packages

[![Install npm packages locally](http://img.youtube.com/vi/JDSfqFFbNYQ/0.jpg)](http://www.youtube.com/watch?v=JDSfqFFbNYQ "Install npm packages locally")

安装npm包有两种方式：本地安装或全局安装。请根据你使用包的方式来选择安装的类型。

> There are two ways to install npm packages: locally and globally. Choose which kind of installation to use based on how you want to use the package.

- 如果你想依赖你自己的模块中的包，则使用类似Node.js的require方式，然后以本地的方式安装。这是**npm install**的默认方式。
- 如果你想像命令行一样使用包，（例如grunt CLI），然后[全局安装](https://docs.npmjs.com/getting-started/installing-npm-packages-globally)。

> - If you want to depend on the package from your own module, using something like Node.js's **require**, then you want to install locally. This is **npm install**‘s default behavior.
> - If you want to use a package as a command line tool, (such as grunt CLI), then install it globally.

要了解更多相关**install**命令，请查看[CLI文档页面](https://docs.npmjs.com/cli/install)。

> To learn more about the **install** command, check out the CLI doc page.

## 安装一个包

> ## Install a package

包可以使用命令下载：

> A package can be downloaded with the command:

```
npm install <package_name>
```

这条命令会在你当前的目录创建一个**node_modules**文件夹（如果一个包都还没有的话）并将包下载到该文件夹中。

> This will create the **node_modules** directory in your current directory (if one doesn't exit yet) and will download the package to that directory.

### 测试：

> ### Test:

为了确认**npm install **已正确运行，查看**node_modules**文件夹下会存在一个包含你已经安装的包的目录。

> To confirm that **npm install** worked correctly, check to see that a **node_modules** directory exists and that it contains a directory for the package(s) you installed.

### 示例：

> Example:

安装一个名为**lodash**的包，通过从**node_modules**文件夹中列出的内容来确认已成功运行，在文件夹内你应该会看到一个名为**lodash**的文件夹。

> Install a package called **lodash**. Confirm that it ran successfully by listing the contents of **node_modules** directory, where you should see a directory called **lodash**.

#### 微软Windows

> #### Microsoft Windows

```
C:\ npm install lodash
C:\ dir node_modules

#=> lodash
```

#### macOS, Ubuntu, Debian

> #### macOS, Ubuntu, Debian

```
> npm install lodash
> ls node_modules

#=> lodash
```

## 包的哪个版本被安装了？

> ## Which Version of the Package is Installed?

如果本地目录中没有**package.json**文件，说明最新版的包已经被安装。

> If there is no **package.json** file in the local directory, the latest version of the package is installed.

如果本地目录中有**package.json**文件，npm安装的最新版本满足**package.json**文件中[semver 规则](https://docs.npmjs.com/getting-started/semantic-versioning)的声明。

>If there is a **package.json** file, npm installs the latest version that satisfies the semver rule declared in **package.json**.

## 在你的代码中使用已安装的包

> ## Using the Installed Package In Your Code

只要**node_modules**目录中有包，你就可以在你的代码中使用它。比如，如果你正在创建一个Node.js模块，你可以**引入**它。

> Once the package is in **node_modules**, you can use it in your code. For example, if you are creating a Node.js module, you can **require** it.

### 示例：

> ### Example:

使用以下代码创建一个名为**index.js**的文件：

> Create a file named **index.js**, with the following code:

```
// index.js
var lodash = require('lodash');

var output = lodash.without([1, 2, 3], 1);
console.log(output);
```

使用**node index.js**运行代码，将会输出**[2, 3]**。

> Run the code using **node index.js**, it should output **[2, 3]**.

如果你还没有正确安装**lodash**，你将会收到这个报错：

> If you had not properly installed **lodash**, you would receive this error:

```
module.js:340
	throw err:
		  ^
Error: Cannot find module 'lodash'
```

要修复这个错误，请在**index.js**目录中运行**npm install lodash**。

> To fix this, run **npm install lodash** in the same directory as your **index.js**.

