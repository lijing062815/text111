### 安装git
- 在git官网直接下安装
- 下载后在菜单中找打git - > git bash  
- 在命令行输入
  + git config --global user.name "your name"
  + git config --global user.email "email@example.com"

注意:git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址

### 创建版本库
- 第一步：选择一个合适的地方，创建一个空目录
  + $ mkdir learngit
  + $ cd learngit
  + $ pwd
  + /Users/michael/learngit
- 第二步：通过git init命令把这个目录变成Git可以管理的仓库：
  + $ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
  + 如果你没有看到.git目录，那是因为这个目录默认是隐藏的，用ls -ah命令就可以看见。

### 将文件放到git仓库
- 第一步：用命令git add告诉git，把文件添加到仓库
  + $ git add readme.tex;