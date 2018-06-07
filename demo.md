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
  + 执行上面的命令，没有任何显示，这就对了，Unix的哲学是“没有消息就是好消息”，说明添加成功
- 第二步：用命令git commit告诉git，把文件提交到仓库
  + $ git commit -m "wrote a readme file"  
  [master (root-commit) eaadf4e] wrote a readme file  
   1 file changed, 2 insertions(+)  
   create mode 100644 readme.txt  
  + -m后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。
  + 1 file changed：1个文件被改动（我们新添加的readme.txt文件）
  + 2 insertions：插入了两行内容（readme.txt有两行内容）

### 版本回退
- HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id
- 穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
- 要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。