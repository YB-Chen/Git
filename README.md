### 如何修改Git Bash的默认启动路径 ###

1. 选择Git Bash图表，右键属性；
2. 将“目标”中的“--cd-to-home”删除；
3. 用仓库路径代替“起始位置”中的内容；
4. 点击确定，重启Git Bash即进入所设定的路径。

点击进入[图片示例](https://github.com/YB-Chen/GitCommend/blob/master/git-bash%E5%B1%9E%E6%80%A7.JPG?raw=true)

### 创建SSH Key ###
**ssh-keygen -t rsa -C "youremail@example.com"**

### 关联和删除远程库 ###
**关联方法一：git remote add origin git@github.com:< username of github > / < name of repository >.git**

**关联方法二：git remote add origin http://github.com:/< username of github >/< name of repository >.git** 

Git支持多种协议，默认的git://使用ssh，但也可以使用https等其他协议，使用https除了速度慢以外，还有个最大的麻烦是每次推送都必须输入口令，但是在某些只开放http端口的公司内部就无法使用ssh协议而只能用https。

**删除远程库**

git remote rm origin

其中，origin为远程库的别名

### 推送本地库/拉取远程库 ###

**推送本地库：git push -u origin master**   
  
用git push命令，实际上是把当前分支master推送到远程。由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令（去掉-u）。

**拉取远程库：git clone git@github.com:< username of github >/< name of repository >.git**






