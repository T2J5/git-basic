## git 的首次配置

git 包含一个 git config 的工具，可以用来获取和设置配置变量，这些变量控制 git 的外观和操作。可以将配置变量存储在三个不同的位置

1. /etc/gitconfig: 包含了系统中所有用户及其仓库的值。如果你向 git config 传入--system 选项，那么它就会专门从该文件中读写配置变量

2. ~/.gitconfig 或~/.config/git/config 文件，针对的时你自己。可以通过传入--global 选项使 git 专门从该文件中读写配置变量

3. 当前仓库的 git 目录(也就是.git/config)中的 config 文件：针对单个仓库

每一级都会覆盖上一级中的设置，因此.git/config 中的值要优于/etc/gitconfig 中的值

在 windows 系统中，git 会在$HOME 目录中(C:\User\$USER)查找.gitconfig 文件。它也查找/etc/gitconfig。不过这是相对于 MSys 的根目录，该目录是在安装程序运行时你所选择的安装目录

## 用户身份

```bash
git config --global user.name "username"
git config --global user.email 12345@qq.com
```

## 检查个人设置

```bash
git config --list
```
