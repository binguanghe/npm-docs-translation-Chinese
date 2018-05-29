# 如何更新本地包

> # How to Update Local Packages

[![Updating local packages](http://img.youtube.com/vi/HRudtPGcOt4/0.jpg)](http://www.youtube.com/watch?v=HRudtPGcOt4 "Updating local packages")

定期更新你应用的依赖包是一个不错的做法。这样，如果原来的开发者们改进了他们的代码，你的代码也将得到改进。

> It's a good practice to update the packages your application depends on. Then, if the original developers have improved their code, your code will be improved as well.

要做这个：

1. 在你想要更新的应用里的**package.json**文件的相同路径中运行**npm update**。
2. 运行**npm outdated**，将不会有任何结果显示。

> To do this:
>
> 1. Run **npm update** in the same directory as the **package.json** file of the application that you want to update.
> 2. Run **npm outdated**, there should not be any results.

## 了解更多

> Learn More

- [npm-update](https://docs.npmjs.com/cli/update)
- [npm-outdated](https://docs.npmjs.com/cli/outdated)