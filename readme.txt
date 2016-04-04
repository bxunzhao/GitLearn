git start
git init 新建项目管理

git add <file> 添加修改的文件，添加新的文件
git commit -m "提交说明"，修改文件过后必须要add后才能讲修改的部分提交

git status 查看被修改过的文件
git diff 查看修改内容

git log 查看提交日志
	--pretty=oneline 参数设置为以列表显示日志

HEAD 指向当前的版本，Head^指向上一个版本
git reset --hard ID 指向ID的版本

git reflog 查看所有的历史命令纪录 

git add 就是把文件添加到暂存区
git commit 将暂存区的内容提交到当前分支
	初始化项目的时候，git会创建一个master分支

git checkout -- file 注意格式，丢弃工作区的内容（没有提交到暂存区）
git reset HEAD file 丢弃暂存区内容（没有提交）
git reset HEASD ID 回退版本

git rm file 从版本库中删除文件，但也可以意见还原，checkout reset。。

将项目推送到远程，如Github.com
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

git 分支branch
git checkout －b branchname git创建并切换分支，
	git branch branchname  创建分支
	git checkout branchname  切换分支
git branch －d branchname 删除分支
git merge branchname 合并指定分支到当前分支

git 冲突解决后才能提交，合并分支
git 分支管理策略，　--no-ff 禁用Fast forward 合并分支模式 
	准备合并dev分支，请注意--no-ff参数，表示禁用Fast forward：


查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。