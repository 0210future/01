# git

## 安装步骤

1. 访问Git官方网站：https://git-scm.com/download/win。
2. 在下载页面，点击下载按钮以获取最新版本的Git安装程序。根据你的操作系统位数（32位或64位），选择相应的安装程序。
3. 下载完成后，运行安装程序。（基本上一直下一步就行）
4. 在安装程序的欢迎页面，点击“Next”继续。
5. 阅读并接受许可协议，然后点击“Next”。
6. 选择安装位置。默认情况下，将Git安装在"C:\Program Files\Git"目录下。也可以选择其他路径（我是改到了D盘），然后点击“Next”。
7. 选择组件。确保选中了“Git Bash Here”选项，它将安装一个强大的命令行工具，可以在Windows资源管理器中右键点击打开。根据个人需求，选择其他可选组件，然后点击“Next”。
8. 选择开始菜单文件夹名称。根据个人偏好，将Git添加到开始菜单中指定的文件夹，然后点击“Next”。
9. 选择默认编辑器。选择默认的“Use Vim (the ubiquitous text editor) as Git’s default editor”或者其他编辑器（如notepad++），然后点击“Next”。
10. 选择Git使用的默认终端仿真器。默认情况下，选择使用“Use Git from Git Bash only”选项，这意味着你只能使用Git Bash来执行Git命令。如果你有特定的需求，可以选择其他选项，然后点击“Next”。
11. 配置行尾转换符。默认情况下，选择“Checkout as-is, commit Unix-style line endings”，然后点击“Next”。
12. 配置终端仿真器的字符编码。默认情况下，选择“Use Windows' default console window”，然后点击“Next”。
13. 选择额外的选项。根据个人需求选择或保持默认选项，然后点击“Next”。
14. 检查安装设置。确保所显示的设置正确无误，然后点击“Install”开始安装Git。
15. 安装完成后，点击“Finish”完成安装过程。

## 安装后的目录

![](C:\Users\lenovo\Pictures\Microsoft.Windows.Photos_8wekyb3d8bbwe!App\QQ截图20230713103605.png)

## 使用git进行你版本管理过程

### 初始化仓库

在命令行中进入你的项目文件夹，运行git init命令来初始化一个新的Git仓库。

### 添加和提交文件

使用git add <文件名>命令将文件添加到暂存区，或者使用git add .命令添加所有文件。
使用git commit -m "提交信息"命令将暂存区的修改提交到本地仓库。

### 创建和切换分支

使用git branch命令可以列出当前仓库中的所有分支。带有星号*的分支表示当前所在分支。
使用git branch <分支名>命令创建一个新的分支。
使用git checkout <分支名>命令切换到指定的分支。

### 合并分支

首先，使用git checkout <目标分支>命令切换到你想要合并到的目标分支。
运行git merge <被合并的分支>命令，将指定分支的更改合并到目标分支。

### 远程仓库管理

使用git remote add <远程仓库名> <远程仓库URL>命令将本地仓库与远程仓库关联起来。
使用git remote -v命令可以查看与本地仓库关联的远程仓库列表。
使用git push <远程仓库名> <本地分支名>命令将本地仓库的更改推送到远程仓库。
使用git pull <远程仓库名> <远程分支名>命令从远程仓库拉取并合并更改到本地仓库。

### 解决冲突

当出现冲突时，你需要手动解决冲突。
使用git status命令查看有冲突的
 打开有冲突的文件，在标记的地方手动编辑以解决冲突。
使用git add <文件名>命令将解决冲突后  文件标记为已解决。
最后使用git commit -m "解决冲突"命令提交解决冲突后的文件。

### 版本回退和撤销

使用git log命令查看提交历史记录以获取要回退的提交的哈希值。
使用git reset <提交哈希值>命令将HEAD指针回退到指定的提交。
使用git checkout -- <文件名>命令撤销对某个文件的修改。