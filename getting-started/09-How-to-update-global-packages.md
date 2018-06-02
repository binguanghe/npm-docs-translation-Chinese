# 如何更新全局包

> # How to Update Global Packages

*需要2.6.1或更高版本。如果你正在使用一个更低的版本，请往下查看。*

> *Requires version 2.6.1 or greater. See below if you are using older version.*

要更新全局包，请输入：

> To update global packages, type:

```
npm update -g < package >
```

例如，要更新一个叫jshint的包，你就输入：

> For example, to update a package called jshint, you'd type:

```
npm update -g jshint
```

要找出哪些包需要更新，输入：

> To find out which packages need to be update, type:

```
npm outdated -g --depth=0
```

要更新所有的全局包，输入：

> To update all global packages, type:

```
npm update -g
```

#### 如果你正在使用2.6.0或更低版本

> #### If you are using version 2.6.2 or less

对于低于2.6.1的npm版本，请运行[这个脚本](https://gist.github.com/othiym23/4ac31155da23962afd0e)来更新所有旧的全局包。前提情况是，请考虑升级到最新的npm版本。为此，请输入：

```
npm install npm@latest -g
```

