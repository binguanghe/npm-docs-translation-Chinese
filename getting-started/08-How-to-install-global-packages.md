# 如何安装全局包

> # How to Install Global Packages

npm包有两种安装方式：本地安装和全局安装。选择哪一种安装类型取决于你如何使用包。

> There are two ways to install npm packages: locally and globally. Choose which kind of installation to use based on how you want to use the package.

- 如果你想像使用命令行工具一样使用包，那就全局安装。不管是否在当前目录都可以运行。比如你正在安装grunt，你可以选择这个方式。

> - If you want to use a package as a command line tool, then install it globally. This way, it works no matter which directory is current. This is the choice you would use if you were installing grunt, for example.

- 如果你想依赖你自己模块中的包，那就[本地](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)安装。比如你使用require语句，你可以选择这个方式。

> - If you want to depend on the package from your module, then install it locally. This is the choice you would use if you are using require statements, for example.

要全局下载包，使用**npm install -g < 包名 >**命令, 例如：

> To download packages globally, use the command **npm install -g < package >**, e.g.:

```
npm install -g jshint
```

如果你得到一个EACCES（权限）错误，请查看[see this chapter about permission](https://docs.npmjs.com/getting-started/fixing-npm-permissions)。

> If you get an EACCES error, see this chapter about permission.

*小提示：如果你安装了npm 5.2或更高版本，可以考虑使用npx全局运行包*

> *Tip: Consider using npx to run packages globally, if you have npm 5.2 or greater installed.*

