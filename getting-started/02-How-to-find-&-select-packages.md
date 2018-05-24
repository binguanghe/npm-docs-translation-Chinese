# 查找和选择包

> # Finding and Selecting Packages

要查找包，可以从[搜索栏](https://npmjs.com)开始。

## 例如：查找一个包

> ## Example: Finding a Package

你想在你的应用里使用条形码或者二维码。而不是花上数周的时间来解决它，为什么不看一下，如果别人已经发布的创建好的二维码包了呢？从搜索栏输入一个值开始吧：

> You want to use bar codes (QR codes) in your application. Rather than spend weeks figuring out how to do this, why not see if someone has posted a package that creates QR codes? Start by entering a value in the search bar:

![search bar](https://docs.npmjs.com/images/small-search-bar-qr.png)

当你输入时，可能显示的选择有：

> As you type, possible choices appear:

![search result](https://docs.npmjs.com/images/search-results-qr-scanner-what-is-npm.png)

### 如何在相似的包之间做出选择

> ### How to Choose Between Similar Packages

当你在搜索栏输入一个搜索项后，按回车键查看排名以帮助你在相似的包之间做出选择：

> After entering a search term in the search bar, press Enter to see rankings that will help you choose between similar packages:

![choose your package](https://docs.npmjs.com/images/qr-image-help-u-choose.png)

通常情况下，会出现数十个或者甚至数百个有着相似名字或相似用途的包。为了帮助你决定想要浏览的最好的包，每个包都已经使用npms分析器根据四个标准来排名：

> Often, there are dozens or even hundreds of packages with similar names and/or similar purposes. To help you decide the best ones to explore, each package has been ranked according to four criteria using the **npms analyzer**:

- 理想程度
- 受欢迎程度
- 质量
- 维护情况

> - Optimal
> - Population
> - Quality
> - Maintenance

**受欢迎程度**表示这个包已经被下载的次数。这是一个很重要的包指标，在被找到的包中尤其有用，但也不完全正确。

> **Popularity** indicates how many times the package has been downloaded. This is a good indicator of packages that others have found to be especially useful, but not foolproof.

**质量**包括考虑到的条件有，比如是否有readme文件，稳定性，测试例子，更新的依赖数，自定义网站以及代码复杂度。

> **Quality** includes considerations such as the presence of a readme file, stability, tests, up-to-date dependencies, custom website, and code complexity.

**维护情况**根据开发者们的关注度来对包进行排名。例如，在当前或即将发布的npm版本中，越被频繁更新的包质量可能越好。

> **Maintenance** ranks packages according to the attention given by developers. Packages that are maintained more frequently are more likely to work well with the current or upcoming versions of npm, for example.

**理想程度**则使用一种有意义的方式结合其他三个标准来衡量。

> **Optimal** combines the three other criteria in a meaningful way.

想要根据特定的标准来列出包，则点击**排序包**下面的标签。例如，想要根据受欢迎度来搜索，则点击**受欢迎度**。

> To list packages according to a specific criteria, click its label under **Sort Packages**. For example, to search by Popularity, click **Popularity**.

![sort example](https://docs.npmjs.com/images/qr-sort-criteria-blowup.png)



### 包页面


> ### The Package Page

当你选择一个包的时候，会显示很多信息。这是包作者写的各种详细信息。这里你可以知道如何来使用这个包。开发者们通常也会提供联系信息。

> When you choose a package, more information appears. This information is written by the package author(s) so details vary. This is where you can discover how to use this package. Developers often provide contact information as well.

这里有一些你找到的包页面相关信息的类型的例子。

> Here are some examples of the type of information you will find on the package page.

##  包页面组成的部分


> ## Parts of the Package Page:

在包页面上有一些可用的标签。

> These are the tabs available on the package page.

![tabs example](https://docs.npmjs.com/images/package-choices.png)

### 查看Readme

> ### Viewing Readme

readme文件由包开发者们创建。如果完成得不错，上面会解释包的用途以及如何使用这个包。

> The readme file is created by the package developer. If done well, it explains the purpose of the package, and how to use it.

### 查看依赖

> ### Viewing Dependencies

很多包由其他包组成。这些其他包被成为依赖。

> Many packages are made up of other packages. These packages are called dependencies.

![viewing dependecies](https://docs.npmjs.com/images/package-viewing-dependencies.png)

### 查看关联

> ### Viewing Dependents

那些包含这个包并以某种方式显示的包被称为关联。

> Packages that incorporate the package shown in some way are called dependents.

### 查看版本
> ### Viewing Versions

当一个包被更新，上一个版本的列表会展示出来。

> When a package is updated, a list of previous versions appear.

![view versions](https://docs.npmjs.com/images/package-viewing-versions.png)



#### 下载一个包
> #### Download a package

下一章会说明如何安装npm。当你安装npm之后，你就可以使用终端控制台来下载包。这个已经在下一章说明。

>  The next chapter explains how to install npm. After you install npm, you will use a terminal console to download packages. This is explained in later chapters.

## 了解更多
> ## Learn More

获取更多关于npms和npms分析器的运行方式，点击[这里](https://npms.io/about) 。

> For more information about how npms and the npms analyzer work, click here.