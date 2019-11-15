### 如何修改Git Bash的默认启动路径 ###
	1. 选择Git Bash图表，右键属性；
	2. 将“目标”中的“--cd-to-home”删除；
	3. 用仓库路径代替“起始位置”中的内容；
	4. 点击确定，重启Git Bash即进入所设定的路径。

点击进入[图片示例](https://github.com/YB-Chen/GitCommend/blob/master/git-bash%E5%B1%9E%E6%80%A7.JPG?raw=true)

### 配置相关指令 ###
    创建SSH Key
	$ ssh-keygen -t rsa -C "youremail@example.com"
    初始化仓库
    $ git init
	本地库与远程库关联方法一
    $ git remote add origin git@github.com:< username of github >/< name of repository >.git
	本地库与远程库关联方法二
    $ git remote add origin http://github.com:/< username of github >/< name of repository >.git
	解除本地库与远程库的关联
    $ git remote rm origin

### 创建和添加 ###
    创建文件夹
	$ mkdir <文件夹名>
    创建文件
	$ touch <文件名>
	创建一个文本文件并进入编辑状态
	$ vi <文件名>  //vi其实是linux的一个文本编辑器，此命令是进入vi程序。vi有两种模式：编辑模式（默认）和命令模式
	添加单个文件
	$ git add <文件名.扩展名>
	添加某类文件
	$ git add *.<扩展名>
	添加所有状态的文件
	$ git add -A
	添加修改和删除状态的文件（不包括新建状态）
	$ git add -u
	添加修改和新建状态文件（不包括删除文件）
	$ git add .

### 远程库 ###
	把远程库clone到本地
    $ git clone git@github.com:< username of github >/< name of repository >.git
	推送本地库分支到远程库分支
    $ git push -u origin < branch name>(远程库有对应分支时，不需要-u)
    拉取远程库分支到本地库
    $ git pull origin < branch name>
	查看远程库地址
    $ git remote -v
	查看所有分支
    $ git branch -a


### 分支管理 ###
	创建分支
    $ git branch < name of branch >
	切换分支
    $ git checkout < name of branch >
    创建并切换分支
    $ git checkout -b < name of branch >
	由远程dev分支创建（并切换）本地dev分支
    $ git checkout -b dev origin/dev
	合并指定分支到当前分支
    $ git merge < name of branch >(默认以fast forward模式合并)
    合并时禁用fast forward模式
    $ git merge --no-ff -m "merge with no-ff" < name of branch >
	删除本地分支
    $ git branch -d < name of branch >
	删除远程分支
    $ git push origin --delete < branch name >

### 合并远程分支 ###
	1、在本地创建dev分支并与远程dev分支对应
    $ git checkout -b dev origin/dev
	2、切换到master分支
    $ git checkout master
	3、本地的dev合并到master上（遇到冲突解决完后再次提交）
    $ git merge dev(默认以fast forward模式合并)
	4、推送到远程的master分支
    $ git push origin master 

### 信息查看 ###
	查看历史提交信息
    $ git log
	查看修改内容
    $ git status
	查看当前仓库的基本信息
    $ git remote show origin
	查看本地分支
    $ git branch
    查看本地分支详情
    $ git branch -v
	查看本地及远程分支
    $ git branch -a
	查看本地及远程分支详情
    $ git branch -av
    查看详细分支历史
    $ git log --graph --pretty=oneline --abbrev-commit
    

