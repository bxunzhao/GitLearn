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