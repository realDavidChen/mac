## 一. 按常规，打开vs code，按f1，搜索 code，选择安装code命令选项，完成基本安装
## 二. 为了在termina1一直可以使用code命令打开vs code，我们需要做如下设置：
在terminal中，输入
```
mdfind "kMDItemCFBundleIdentifier == 'com.microsoft.VSCode'"
```
会得到如下的反馈
```
/Users/你的计算机名/Downloads/Visual Studio Code.app
```

在你的 .zshrc 文件中，你可以添加如下的别名行(不知道自己的计算机名也可以用 $ whoami 命令在terminal中查到)：

```
alias code="/Users/你的计算机名/Downloads/Visual\\ Studio\\ Code.app/Contents/Resources/app/bin/code"
```

或者将路径添加到 $PATH 变量：
```
export PATH="/Users/你的计算机名/Downloads/Visual Studio Code.app/Contents/Resources/app/bin:$PATH"

```
记得在更新 .zshrc 文件后，重新启动终端或者运行 source ~/.zshrc 以使更改生效。之后，你应该能够在终端中成功运行 code 命令了。
