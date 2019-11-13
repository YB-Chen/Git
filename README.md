### 如何修改Git Bash的默认启动路径 ###
	1. 选择Git Bash图表，右键属性；
	2. 将“目标”中的“--cd-to-home”删除；
	3. 用仓库路径代替“起始位置”中的内容；
	4. 点击确定，重启Git Bash即进入所设定的路径。

点击进入[图片示例](https://github.com/YB-Chen/GitCommend/blob/master/git-bash%E5%B1%9E%E6%80%A7.JPG?raw=true)

### 配置相关指令 ###
    创建SSH Key
	$ ssh-keygen -t rsa -C "youremail@example.com"
	本地库与远程库关联方法一
    $ git remote add origin git@github.com:< username of github >/< name of repository >.git
	本地库与远程库关联方法二
    $ git remote add origin http://github.com:/< username of github >/< name of repository >.git
	解除本地库与远程库的关联
    $ git remote rm origin

### 远程库 ###
	推送本地库到远程
    $ git push -u origin master
	拉取远程库到本地
    $ git clone git@github.com:< username of github >/< name of repository >.git
	查看远程库地址
    $ git remote -v
	查看所有分支
    $ git branch -a


### 修改和删除 ###
    增加一行


### 分支管理 ###
	创建分支
    $ git branch < name of branch >
	切换分支
    $ git checkout < name of branch >
    创建并切换分支
    $ git checkout -b < name of branch >
	查看分支
    $ git branch
	合并指定分支到当前分支
    $ git merge < name of branch >
	删除本地分支
    $ git branch -d < name of branch >
	删除远程分支
    $ git push origin --delete < branch name >

### 合并远程分支 ###
	1、把代码clone到本地仓库
    $ git clone git@github.com:< username of github >/< name of repository >.git
	2、在本地创建dev分支并与远程dev分支对应
    $ git checkout -b dev origin/dev
	3、切换到master分支
    $ git checkout master
	4、本地的dev合并到master上（遇到冲突解决完后再次提交）
    $ git merge dev
	5、推送到远程的master上
    $ git push origin master 

### 仓库信息查看 ###
	查看历史提交信息
    $ git log
	查看修改内容
    $ git status
	查看当前仓库的基本信息
    $ git remote show origin

