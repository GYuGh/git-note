GitHub 笔记
---
基础知识
---
- **在git中有3个区：工作区，暂存区和仓库**
- **在刚开始使用git命令时，要先配置身份**
    git config --global user.name “wangli”
    git config --global user.email “wangli@gmail.com”**
- cd ..\ 到上一级目录
- cd +磁盘:  进入某一磁盘
- cd +仓库名 进入自己的仓库
- git add ＜file＞   将该文件从工作区添加到暂存区
- git add .   将所有文件添加到暂存区
- git commit -m “”将文件以某一个名字从暂存区添加到仓库，每一次名字都可以换，感觉最好把自己的修改操作作为名字
- git diff   查看比对被修改的内容 
- **如果只add而没有commit，将报错，但如果反过来，git diff 以后将没有修改差异，也就说git diff实际上比对的是工作区和暂存区的不同**
- git diff-cached 是查看working tree 和index file的差别
- git diff HEAD 是查看working tree 和commit的差别
- git log   显示从近到远提交的仓库的历史记录
- git init    创建git可以管理的仓库
- git checkout +分支名   文切换到某一分支
- git reset HEAD file   文件被修改，且已添加到暂存区，要丢弃修改
- git rm   删除文件

分支管理
---
- git branch  查看所有分支,*后面的是当前所在的分支，master是主分支
- git branch +文件名  创建分支
- git checkout name   切换分支，在checkout 后加上-b表示创建并切换分支
- git merge name   合并指定分支到当前分支

对于本次任务操作起来的步骤
---
- 先把远程仓库克隆到本地，形成自己的本地仓库
  git clone +仓库地址，仓库地址在github的网页中“ATPS clone URL  ”处。
- 在把note分支从远程仓库上抓下来，抓之前应先切换到note分支
  git checkout note
  git fetch origin note
- 再将写的内容提交到本地仓库 保存为md格式
- 下一步是合并自己的分支到note分支中，建立在当前分支是note的基础上
  git merge wangli --no-ff  **“--no-ff”可以使得在远程仓库可以看到自己分支合并的记录**
- 最后一步便是推送，需要分别将自己的分支和note分支推送到远程仓库
  **注意，要推送哪个分支，首先就要将其切换到哪个分支！**
    git push origin note
    git checkout wangli
    git push origin wangli
    







