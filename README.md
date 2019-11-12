### 如何修改Git Bash的默认启动路径 ###

1. 选择Git Bash图表，右键属性；
2. 将“目标”中的“--cd-to-home”删除；
3. 用仓库路径代替“起始位置”中的内容；
4. 点击确定，重启Git Bash即进入所设定的路径。

点击进入[图片示例](https://github.com/YB-Chen/GitCommend/blob/master/git-bash%E5%B1%9E%E6%80%A7.JPG?raw=true)

### 创建SSH Key ###
**$ ssh-keygen -t rsa -C "youremail@example.com"**

### 关联和删除远程库 ###
**关联方法一：$ git remote add origin git@github.com:< username of github >/< name of repository >.git**

**关联方法二：$ git remote add origin http://github.com:/< username of github >/< name of repository >.git**

**删除远程库：$ git remote rm origin**

### 修改和提交 ###



### 推送本地库/拉取远程库 ###

**推送本地库：$ git push -u origin master**

**拉取远程库：$ git clone git@github.com:< username of github >/< name of repository >.git**

### 分支管理 ###

**创建分支：$ git branch < name of branch >**

**切换分支：$ git checkout < name of branch >**

**创建并切换分支：$ git checkout -b < name of branch >**

**查看分支：$ git branch**

**合并指定分支到当前分支：$ git merge < name of branch >**

**删除分支：$ git branch -d < name of branch >**