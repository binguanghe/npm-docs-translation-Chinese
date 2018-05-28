# 使用package.json工作

> # Working with package.json

创建一个**package.json**文件是本地化管理已安装npm包的最好方式。

> The best way to manage locally installed npm packages is to create a **package.json** file.

一个**package.json**文件。

- 列出你的项目依赖的所有包。
- 允许你使用[语义版本规则](https://docs.npmjs.com/getting-started/docs.npmjs.com/getting-started/semantic-versioning)来指定你项目中可以使用的包的版本。
- 使你的构建可以重复使用，并且这样更容易与其他开发者分享。

> A **package.json** file.
>
> - lists the packages that your project depends on.
> - allows you to specify the version of a package that your project can use using semantic versioning rules.
> - makes you build reproducible, and therebefore *before* much easer to share with other developers.

## 前提条件

> # Requirements

一个**package.json**文件必须包含：

- **名称**
  - 全部小写
  - 只有一个词，不允许出现空格
  - 允许有横杠和下划线
- **版本**
  - 以**x.x.x**的形式
  - 需遵循[语义版本规范](https://docs.npmjs.com/getting-started/semantic-versioning)

> A **package.json** must hava:
>
> - **name**
>   - all lowercase
>   - one word, no spaces
>   - dashes and underscores allowed
> - **version**
>   - in the form of **x.x.x**
>   - follows semver spec

例如：

> For example:

```
{
  "name": "my-awesome-package",
  "version": "1.0.0"
}
```

## 创建一个package.json

> ## Creating a package.json

创建一个**package.json**文件有两种基本方式。

> There are two basic ways to create a **package.json** file.

### 1. 运行一个CLI窗口 

如果要使用你提供的值来创建**package.json**文件，请运行：

> ### 1. Run a CLI questionnaire
>
> To create a **package.json** with values that you supply, run:

```
> npm init
```

这将启动一个命令行窗口，即在你启动命令行窗口的目录会创建一个**package.json**文件。

> This will initiate a command line questionnaire that will conclude with the creation of a **package.json** in the directory which you initiated the command.

### 2. 创建一个默认的 package.json 文件 

> ### Create a default package.json

要得到一个默认的**package.json**文件，请以**--yes**或者**--y**为标记运行**npm init**命令 

```
> npm init --yes
```

此方法将使用从当前目录中提取的信息生成默认的package.json。

> This method will generate a default **package.json** using information extracted from the current directory.

```
> npm init --yes
Wrote to /home/ag_dubs/my_package/package.json:

{
  "name": "my_package",
  "description": "",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/ashleygwilliams/my_package.git"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/ashleygwilliams/my_package/issues"
  },
  "homepage": "https://github.com/ashleygwilliams/my_package"
}
```

- 名称：当前路径名
- 版本：总为**1.0.0**
- 描述：来自readme的信息，或者是一个空字符串“”
- 主要文件：**index.js**
- 脚本：通过默认创建一个空的**测试**脚本
- 关键词：空
- 作者：空
- 开源许可证：ISC
- 错误漏洞：如果存在，则来自当前路径的信息
- 主页：如果存在，则来自当前路径的信息

>- **name**: the current directory name
>- **version**: always **1.0.0**
>- **description**: info from the readme, or an empty string ""
>- **main**: always **index.js**
>- **scripts**: by default creates an empty **test** script
>- **keyword**: empty
>- **author**: empty
>- **license**: **ISC**
>- **bugs**: info from the current directory, if present
>- **homepage**: info from the current directory, if present

你也可以为初始化命令设置一些配置选项。比如下面几个有用的：

> You can also set several config options for the init command. Some useful ones:

```
> npm set init.author.email "wombat@npmjs.com"
> npm set init.author.name "ag_dubs"
> npm set init.license "MIT"
```

#### 注意：

> #### NOTE:

如果**package.json**文件里没有描述项，npm会以**README.md**文件的第一行或者README来替代。当别人搜索npm的时候描述项会帮助他们找到你的包，因此，为了让你的包更容易被找到，在**package.json**文件里定义好描述项是相当有用的。

> If there is no description field in the **package.json**, npm uses the first line of the **README.md** or README instead. The description helps people find your package when searching npm, so it's definitely useful to make a custom description in the **package.json**  to make your package easier to find.

### 如何自定义**package.json**

> ### How to Customize the **package.json** questionnaire

如果你想创建多个package.json文件，并且你可能想要在初始进程运行时自定义被问到的问题，那么这些文件会一直包含你想要的信息。只要是被提问的问题你都可以自定义那些字段。

> If you expect to create many package.json files, you might wish to customize the questions asked during the init process, so that the files always contain key information that you expect. You can customize the fields as well as the questions that are asked.

要想这么做，你可以在主目录 **~/ .npm-init.js** 建立一个自定义**.npm-init.js** .文件。

> To do this, you create a custom **.npm-init.js** in your home directory **~/ .npm-init.js** .

一个简单的**.npm-init.js**文件大概是这样：

> A simple **.npm-init.js** might look something like this:

```
module.export = {
  customField: 'Custom Field',
  otherCustomField: 'This field is really cool'
}
```

你的主目录中有这个文件，运行**npm init** 将会输出一个包含以下几行信息的**package.json**文件。

> Running **npm init** with this file in your home directory would output a **package.json** that included these lines:

```
{
  customField: 'Custom Field',
  otherCustomField: 'This field is really cool'
}
```

你也可以使用**提示**函数自定义问题。

> You can also customize the questions by using the **prompt** function.

要了解如何创建高级自定义此文件，请查看[init-package-json](https://github.com/npm/init-package-json)文档。

> To learn more about how to create advanced customizations, check out the docs for init-package-json

## 指定依赖

> ## Specifying Dependencies

要指定你项目中的依赖，你需要列出你想要在**package.json**中使用的包。你可以列出的包有两种：

> To specify the packages your project depends on, you need to list the packages you'd like to use in your **package.json** file. There are 2 types packages you can list:

- **“dependencies”**: 这些包是在你的应用在生产中需要的。
- **devDependencies**: 这些包只需用于开发和测试。


> - **"dependencies"**: These packages are required by your application in production.
> - **"devDependencies"**: These packages are only needed for development and testing.

### 手动编辑你的**package.json**

> ### Manually editing your **package.json**

你可以手动编辑你的**package.json**。你需要在包对象中设置一个名为**dependencies**的属性来指向一个对象。这个对象将保存相关的属性，即你希望使用的包的名称。它会指向一个[**语义化版本**](https://docs.npmjs.com/getting-started/docs.npmjs.com/getting-started/semantic-versioning)表达式，该表达式指定该项目与你的项目兼容的版本。

> You can manually edit your **package.json**. You'll need to create an attribute in the package object called **dependencies** that points to an object. This object will hold attributes that name the packages you'd like to use. It will point to a **semver** expression that specifies the versions of that project that are compatible with your project.

如果你有那些只用于本地开发的依赖，请参照以下以上相同的结构，但是要使用名为**devDependencies**的属性。

> If you have dependencies you only use during the local development, follow the same instructions as above but use the attribute called **devDependencies**.

例如，下面的项目使用与生产中的主要版本1相匹配的任何版本的包**my_dep**，并需要与主版本3相匹配的包**my_test_framework**的任何版本，但是仅用于开发。

> For example, the project below uses any version of the package **my_dep** that matches major version 1 in production and requires any version of the package **my_test_framework** that matches major version 3, but only for development:

```
{
  "name": "my_package",
  "version": "1.0.0",
  "dependencies": {
    "my_dep": "^1.0.0"
  },
  "devDependencies" : {
    "my_test_framework": "^3.1.0"
  }
}
```

### **--save** 与**--save-dev** 安装标志

> ### **The --save** and **--save-dev** install flags

添加依赖到你的**package.json**中更简单（并且更好）的方式是使用命令行，使用**--save**或者**-save-dev**标记来**npm install**命令，取决于你想如何使用这中依赖关系。

> The easier (and more awesome) way to add dependencies to your **package.json** is to do so from the command line, flagging the **npm install** command with either **--save** or **--save-dev**, depending on how you'd like to use that dependency.

添加一个入口到你的**package.json**的**dependencies**:

> To add an entry to your **package.json**'s **dependencies**:

```
npm install <package_name> --save
```

添加一个入口到你的**package.json**的**devDependencies**:

> To add an entry to your **package.json**'s **devDependencies**:

```
npm install <package_name> --save-dev
```

## 管理依赖版本

> ## Managing dependency versions

npm使用语义版本，或者像我们通常提到的那样使用SemVer来管理版本以及包版本的范围。

> npm uses Semantic Versioning, or, as we often refer to it, SemVer, to manage versions and ranges of versions of packages.

如果你目录里有一个**package.json**文件并且运行**npm install**， npm会使用语义版本规则来寻找文件里列出的依赖并下载最新的版本。

> If you have a **package.json** file in your directory and you run **npm install**, npm will look at the dependencies that are listed in that file and download the latest versions, using semantic versioning.

## 了解更多

> ## Learn More

要了解更多关于package.json的魅力，请观看你可以在[第八章](https://docs.npmjs.com/getting-started/installing-npm-packages-globally)中找到的"Installing npm packages locally"的视频。

> To understand more about the power of package.json, see the video "Installing npm packages locally" which you can find in Chapter 8.

要了解更多关于语义化版本的规则，请查看[Getting Started "Semver page"](https://docs.npmjs.com/getting-started/docs.npmjs.com/getting-started/semantic-versioning)。

> To learn more about semantic versioning, see Getting Started "Semver page.