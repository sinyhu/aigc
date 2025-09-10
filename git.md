# git 的命令记录

git branch -r  查询有哪些远程分支
git checkout -b AIBrush orign/AIBrush   创建并切换分支​	git checkout -b <本地分支名> origin/<远程分支名>	​常用方法​：创建本地分支并跟踪远程分支，然后切换到该分支。

git 服务器上执行下面两个命令
git init --bare androidAIBrush
chown -R git:git androidAIBrush

本地获取然后创建远程分支
git pull origin master

git add 1.txt 

git commit -m "提交1.txt"

git push origin master
