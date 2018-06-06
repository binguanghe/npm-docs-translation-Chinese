# 如何创建Node.js模块

> # How to Create Node.js Modules

[Youtube: Creating Node.js modules](https://youtu.be/3I78ELjTzlQ)

Node.js模块是一种可以发布到npm上的包。要创建一个新的模块，请从创建一个**package.json** 文件开始。

> Node.js modules are a type of packages that can published to npm. To create a new module, start by creating a **package.json** file.

使用**npm init**来创建**package.json**。它会提示你为字段输入值。两个必须的字段是“名称”和“版本”。你还需要为“main”设置一个值。这些步骤在[第五章](https://docs.npmjs.com/getting-started/using-a-package.json)

> Use **npm init** to create **package.json**. It will prompt you for values for fields. The two required fields are 'name' and 'version'. You'll also need to set a value for 'main'. You can use the default, **index.js**. These steps are described in detail in Chapter 5.

如果你想为作者字段添加信息， 请使用以下格式（电子邮件和网站都是可选的）：

> If you want to add information for the author field, use the following format (email and website are optional):

```
Your name < email@example.com > (http://example.com)
```

一旦**package.json**被创建，你将需要创建一个当你的模块被需要加载的文件。

在那个文件里，添加一个函数作为**出口**对象的一个属性。这将使该函数适用于其它代码。

> Once your **package.json** file is created, you'll want to create the file that will be loaded when your modules is required. The default name for this file is **index.js**.
>
> In that file, add a function as a property of the **export** object. This will make the function available to other code.

```
export.printMsg = function() {
   console.log("This is a message from the demo package");
}
```

测试：

 	1. 发布你的包到npm。
	2. 在你的项目外面创建一个新的目录。
	3. 切换到新的目录（**cd**）。
	4. 运行**npm install <package>**.
	5. 创建一个需要引用包的test.js文件并调用方法。
	6. 运行**node test.js**。发送到console.log的信息将会显示。

> Test:
>
>  	1. Public your package to npm.
> 	2. Make a new directory outside of your project.
> 	3. Switch to the new directory(**cd**).
> 	4. Run **npm install < package >**.
> 	5. Create a test.js file which requires the package and calls the method.
> 	6. Run **node test.js**. The message sent to the console.log should appear.

## 了解更多

> ## Learn More

要了解包的类型，点击[这里](https://docs.npmjs.com/getting-started/packages)

> To understand types of packages, click here.