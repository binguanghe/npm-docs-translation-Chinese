# 开始

> # Getting Started

1. 从[npmjs.com](http://npmjs.com)创建一个账户。
2. 从终端控制台安装npm。
3. 使用你的新的用户名登录到终端。

> 1. Creat an account from [npmjs.com](http://www.npmjs.com/).
> 2. Install npm from terminal console.
> 3. Login to terminal with your new username.

注意：很多可以从浏览器获取的步骤你也可以直接从命令行界面获取。跳过[这里](https://docs.npmjs.com/getting-started/installing-node#Related-CLI-Commands)了解更多。

> Note: Many of the steps that you can take from the browser can also be taken directly from the Command Line Interface. Skip [here](https://docs.npmjs.com/getting-started/installing-node#Related-CLI-Commands) to learn more.

## 创建一个账户

> ## Create an Account

1. 访问[http://npmjs.com](http://npmjs.com)并点击“登录”。

> 1. Go to [http://www.npmjs.com](http://www.npmjs.com/) and click 'log in'.

![login](https://docs.npmjs.com/images/first-screen.png)

2. 完成注册页面。

> complete the sign up page.

![signUp](https://docs.npmjs.com/images/npm-signup-page-comp.png)

**全名**即名字和姓氏。（你也可以填写中间的名字）。

> **Full name** First name and Last name. (You can enter middle name(s) as well).

**公开电子邮件**填写一个电子邮件账户。当你发布一个包的时候这个电子邮件地址将会被添加到元数据中。这意味着这个电子邮件地址会被所有下载你的包的人看到。此外，当你更新包的时候npm会把邮件发送到这个账户，也包括偶尔的产品更新和信息。

> **Public Email** Enter an email account. This email address will be added to the metadata when you publish a package. This means that the email address can be discovered by anyone who downloads your packages. In addition, npm will send email to this account when you update packages, as well as occassional product and information.

**用户名**填写用户名，当你在npm里发布一个包或者与与其他用户交流的时候将会显示。请选择一个不会违反我们协议指导方针的名字。名字必须是小写。它可以带有数字和短横杠，但有相关的限制以防止假冒账号。

>  **Username** Enter the username that will be shown when you publish packages or interact with other users within npm. Choose a name that doesn't violate our policy guidelines. The name must be lower case. It can be dashes and numerals, but there are restrictions in order to prevent fake accounts.

**密码**按照屏幕上的密码指导来填写。

> **Password** Follow the password guidelines on the screen.

3. 根据你的想法来点击两个选择框。然后点击“创建一个账户”。

> 3. Click the two boxes according to your wishes. Then click the "Create an Account".

4. 打开你输入你的电子邮件地址。

> Open the email address that you entered.

5. 查找一封标题带有*欢迎来到npm*的信件（如果收件箱中没有找到邮件则搜索全部邮件）。

> Find a message with the title *Welcome to npm*(search *All email* in case the email doesn't appear in the inbox).

![inbox](https://docs.npmjs.com/images/welcome-letter-snippet.png)

欢迎信息内有帮助资源链接。作为后期的参考你可能会标记它。

> Welcome message has links to helpful recourses; you might want to flag it for later reference.

*注意：如果你找不到欢迎信息，请点击从新发送：*

> Note: If you can't find the welcome message, please click resend:

![resend](https://docs.npmjs.com/images/email-notif.png)

6. 点击邮件里的链接。成功了！你将会被跳转到你新的登录页面。

> Click the link in your email. Success! You will be sent to your new landing page.

请注意这个URL：

> Notice the URL

**https://www.npmjs.com/~yourusername**

以后这是快速访问你的页面的方法。

> This is a quick way to get to your page in the future.

![yourPage](https://docs.npmjs.com/images/first-page-b4-setup.png)

###当你设置完登录账户之后

> ### After you set up your Login Account

现在有你有了一个登录账户。这里有一些你可以在安装npm之前（或者之后）做的事情：

- 添加/修改你的资料
- 设置双向认证
- 创建一个组织，添加成员以及组织团队等
- 了解关于支付账户和账单

> You now have a login account. Here are a few things you can do before (or later) you install npm:
>
> - Create/Edit your profile
> - Set up two-factor Authentication
> - Create an Organization, Add members, and Form Teams
> - Learn about Paid Accounts and Billing

或者你可以在终端控制台里安装npm，像下面说明的，然后回到这些步骤。

> Or you can install npm in the terminal console, as explained below, the come back to these steps.

如果你想浏览网站，设置你的资料以及快速开始，下面的屏幕截图显示相关的菜单。

> The following screen shot shows where the menu is if you want to explore the website, set up your profile, and get started right way:

![menu](https://docs.npmjs.com/images/profile-menu.png)

## 终端，编辑器以及Git(初学者)

> Terminals, Editors, and Git (For Beginners)

*如果你之前用过终端或者编辑器，可以跳过本章。*

> *Skip this section if you've worked with terminals or editors in the past.*

在npm，我们非常高兴欢迎众多新的开发者来到JavaScript世界。在你使用npm之前，你需要知道设置终端，编辑器以及git。欢迎！

> At npm, we are thrilled to welcome many brand new coders to the JavaScript world. Before you begin using npm, you need to know about setting up terminal, an editor, and git. Welcome!

首先：

1. 为你的电脑找终端模拟器：
   - 使用苹果[终端](https://support.apple.com/guide/terminal/welcome/mac)的帮助。
   - 使用微软Windows [PowerShell](https://docs.microsoft.com/en-us/powershell/)的帮助。
   - Linux[终端模拟器](https://opensource.com/life/17/10/top-terminal-emulators)
2. 查找并选一个你喜欢的文本编辑器。
3. 如果你还没有准备好请考虑一下注册一个[git账户](https://help.github.com/articles/set-up-git/)

> Fisrt:
>
> 1. Find the terminal emulator for your computer:
>    - Help with Apple's Terminal.
>    - Help with Microsoft Windows PowerShell.
>    - Linux terminals emulators.
> 2. Find and pick a text editor that you like.
> 3. Consider signing up for a git account if you haven't already.

本章最后的“了解更多”部分有单独的资源供初学者和所有人使用。

> There are additional resources for beginners and for everyone at the end of this chapter in the "Learn More" section.

## 安装npm和管理npm版本

> ## Install npm and Manage npm Versions

npm由Node.js编写，因此要使用npm你需要安装Node.js。你可以从Node.js网站或者通过安装一个Node版本管理器（NVM）来安装npm。本章将说明这两个方法。

> npm is written in Node.js, so you need to install Node.js in order to use npm. You can install npm via the Node.js website, or by installing a *Node Version Manager* or NVM. This chapter explains both options.

如果你只是想开始浏览npm，使用Node.js安装方法是最快的方式。如果你是一名高级开发者准备加入并使用版本，请使用node版本管理器。如果你不确定，在你选择之前请先阅读本章。以后你可以随时改变如何运行npm。

> If you just want to get started exploring npm, using the Node.js installation method is fastest. If you are an advanced developer ready to jump in and work with versions, use the node version manager. If you aren't sure, please read this chapter before you decide. You can always change how you run npm in the future.

### 从Node.js安装npm

> ### Installing npm from Node.js site

#### 1. 安装Node.js和npm

> #### 1. Install Node.js & npm

##### OS/X 或者Windows

> ##### OS/X or Windows

如果你正在使用OS X或者Windows，请从[Node.js download page](https://nodejs.org/en/download/)使用其中一个安装器。确保安装带有LTS标签的版本。其他版本还没使用npm版本测试。

![download npm](https://docs.npmjs.com/images/win-installing-node-lts.png)

##### Linux

如果你正在使用Linux,请选择其中的一个选项：

- 点击[这里](https://nodejs.org/en/download/package-manager/)以很多Linux开发者喜欢的方式安装npm。
- 在[Node.js下载页面](https://nodejs.org/en/download/)滚动到安装器。
- 查看[NodeSource's binary distributions](https://github.com/nodesource/distributions)是否有一个适合你的系统的最近的版本。

> Linux 
>
> If you're using Linux, choose one of these options:
>
> - click here to install npm for Linux in the way many Linux developers prefer.
> - scroll through the installation on the Node.js download page.
> - check NodeSource's binary distributions to see if there's a more recent version that works with your system.

##### 不常见的操作系统

> ##### Less-Common Operating Systems

点击[这里](https://nodejs.org/en/download/package-manager/)了解更多关于此类操作系统的安装Node.js的信息。

> Click here to learn about installation node.js for a variety of operating systems.

#### 2. 测试你的安装

> #### 2. Test your installation

安装之后，运行**node -v**。版本号应为v8.9.1或更高。

#### 3. 更新npm

> #### 3. Update npm

当你安装Node.js时，npm会被自动安装。但是，npm比Node.js更新得要频繁，因此请确保你是最新的版本。

> When you install Node.js, npm is automatically installed. However, npm gets updated more frequently than Node.js, so be sure that you have the latest version.

要进行测试，则运行**npm -v**。

> To test, run **npm -v**.

为了确保安装的是最新的版本，请滚动到本页的底部。如果你看到的版本号与最新的版本不一致，则运行：

**npm install npm@latest -g**。

> To be sure that this mathes the latest version, scroll to the bottom of this page. If the version you see does not match the latest version, run:
>
> **npm install npm@latest -g**.

### 使用版本管理器来安装Node.js和npm

> ### Using a Version manager to install Node.js and npm

自从npm和Node.js产品由不同的机构管理开始，更新和维护变得复杂起来。不仅如此，Node.js安装进程在一个目录中安装npm只有本地权限。当你尝试以全局方式运行包的时候会引起权限报错。

> Since npm and Node.js products are managed by different entities, updates and maintenance can become complex. Also, the Node.js installation process installs npm in a directory that only has local permissions. This can cause permissions errors when you attempt to run packages globally.

为了解决这些问题，很多开发者选择使用node版本管理器，或者nvm来安装npm。这个版本管理器可以避免权限错误问题，以及解决Node.js和npm更新的复杂问题。

> To solve both these issues, many developers opt to use a *node version manager, or nvm*, to install npm. The version manager will avoid permission errors, and will solve the complexities of updating Node.js and npm.

此外，开发者可以在npm多版本上使用npm来测试他们的应用。nvm允许你轻松地切换npm和node版本。这让切换版本变得十分便捷以确保你的应用可以让大多数用户运行，即使他们正在使用别的版本。如果你决定要安装一个版本管理器，请使用你选择的版本管理器的说明来选择如何切换版本，并学习如何与最新版本的npm保持同步。

> In addition, developers can use an nvm to test their applications on multiple versions of npm. The nvm enables you to easily switch npm as well as node versions. This makes it easier to ensure that your applications work for most users, even if they are instructions for the version manager you select to learn how to switch versions, and to learn how to keep up-to-date with the latest version of npm.

#### 苹果 MacOS

> #### Apple MacOS

点击[这里](https://github.com/creationix/nvm/blob/master/README.md#installation)了解如何为MacOS安装nvm。

> Click here to learn how to install nvm for MacOS.

#### 微软Windows

> #### Microsoft Windows

在Windows上安装和管理npm和Node.js，我们推荐[nvm-Windows](https://github.com/coreybutler/nvm-windows)。

> To install and manage npm and Node.js on Windows, we suggest nvm-windows.

#### Linux

> #### Linux

点击[这里](https://github.com/creationix/nvm/blob/master/README.md#installation)了解如何为Linux安装nvm。

> Click here to learn how to install nvm for Linux.

## 从终端登录到npm

> ##Login to npm from a terminal

要测试你新的账户，请输入：

**npm login**

> To login your new account, type:
>
> **npm login**

你会被提示输入用户名，密码以及电子邮件。请务必确保拼写你的用户名与你之前在网站填写的保持一致，否则你讲会创建一个新的账户。

> You will prompted for your username, password, and email. Be sure to spell your username exactly the same way as you entered it on the website, or you will create a new  account.

![npmLogin](https://docs.npmjs.com/images/npm-login.png)

如果你已经设置好双向验证，当你登录的时候你将会被要求输入一次性密码。如果你需要更多信息请查看[the chapter about two-factor authentication](https://docs.npmjs.com/getting-started/using-two-factor-authentication)。

> If you have already set up two-factor authentication, you will be asked for a one-time password when you login. Please see the chapter about two-factor authentication if you need more information.

要测试你是否已经成功登录，请输入**npm whoami**。

> To test that you have successfully logged  in, type **npm whoami**.

## 试验下一个版本

> ## Experimenting with the next Release

*提供给更多高级用户使用*

*For more advanced users*

如果你想尝试一个未发布的npm版本，以测试你创建的软件包将与计划的npm下一版本一起使用，请使用这个命令：

**npm install npm@next -g**

> If you want to try the next, unreleased version of npm to test the packages you have created will work with the planned next release of npm, use this command:
>
> **npm install npm@next -g**

这可能只是重装当前版本，具体取决于开发周期。除此之外，这个早期的版本不是最终版本。因此那些功能有可能或者没有可能匹配最终发布的版本。

## 了解更多

> ## Learn More

要了解更多关于如何使用node版本管理器，nvm，请点击[这里](https://github.com/creationix/nvm/blob/master/README.md#usage)。

> To learn more about how to use node version manager, nvm, click here.

需要教程，一个可以与其他人见面并且一步步浏览**node学院**以及它的帮助[网站](https://nodeschool.io/)。

> For tutorials, a chance to meet others, and step-by-steps, explore **node school **and its helpful site.

如果你在开发学习中不知所措，请查看npm的Laurie Voss 在“[除了你每个人都知道的东西](https://www.youtube.com/watch?v=JIJZnF_L5KI)”。它会让你意识到你不再感到孤单！

> See npm's Laurie Voss on "Stuff Everybody Knows Except You" if you are feeling overwhelmed in your dev learning. It will make you realize you are not alone!

如何使用苹果的终端[终端](https://support.apple.com/guide/terminal/welcome/mac)。

> How to use Apple's terminal

如何使用微软Windows [PowerShell](https://docs.microsoft.com/en-us/powershell/)。

> How to use Microsoft Windows PowerShell.

如何查找Linux[终端仿真器](https://opensource.com/life/17/10/top-terminal-emulators)。

> How to find Linux terminal emulators.

*注意：虽然在本用户文档中包含了相关的CLI命令，但是CLI也包含了命令行帮助信息，它也有[文档章节以及紧急帮助（帮助页面）](https://docs.npmjs.com/cli/help)*。

> *Note: While relevant CLI commands are covered throughout this user documentation, the CLI includes command line help, its own documentation section, and instant help(man page)*.



