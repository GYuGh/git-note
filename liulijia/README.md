创建版本库
---
- git init    创建git可以管理的仓库，原来的空目录下回增加.git目录
- git add ＜file＞   将文件添加到暂存区
- git add .   将所有文件添加到暂存区
- git commit 将文件提交到仓库
- .gitignore   .gitignore可以忽略一些不能提交的文件，.gitignore文件本身要放到版本库里，并且对.gitignore做版本管理

版本回退
---
- git log   显示从近到远提交的历史记录，便于确定回退的版本
- git log --pretty=oneline   减少信息的显示，显示最主要的信息，包括commit id和提交的内容
- git reset   回退到上一个版本
- git reset --hard commit id   回到指定的版本
- HEAD   当前版本，HEAD∧   上一个版本，HEAD~100   往上100个版本（HEAD是指向当前版本的指针，指向哪个版本号，就把当前版本定位在哪）
- git reflog   想恢复到新版本时，git reflog可以记录用过的每一次命令，找到要回到版本的commit id

修改
---
- git status   文件被修改后，可以以此查看，时刻掌握仓库当前状态
- git diff   查看具体被修改的内容 
- git checkout --file   文件还未添加到暂存区，丢弃工作区的修改
- git reset HEAD file   文件被修改，且已添加到暂存区，要丢弃修改
- git rm   删除文件

分支管理
---
- git branch name   创建分支,在checkout后加上-d表示删除分支
- git checkout name   切换分支，在checkout 后加上-b表示创建并切换分支
- git branch   列出所有的分支，当前分支前会有一个*
- git merge name   合并指定分支到当前分支
- **解决冲突**
当master分支和一个新的分支分别有新的提交时，git的在合并时会产生冲突，需要手动改变内容再合并。
实际开发中，稳定的master分支仅用于开发新版本，平时的工作应在不稳定的新的分支上，当版本发布时，将新的分支合并到主分支。
合并分支时，加上--no--ff参数可以看出曾做过合并。
- **Bug分支**
开发过程中的bug可以通过临时分支修复，修复合并后，可以将临时分支删除。
手头有工作时，可以先把工作现场git stash（将工作现场储藏），bug修复后，用git stash pop,恢复stash的内容的同时将（也可先用git stash apply恢复，再用git stash drop删除）stash的内容删除，回到工作现场。
git stash list命令可以查看工作现场。
- **Feature分支，添加新功能**
新建分支添加新功能。
丢弃一个未被合并过的分支，git branch -D name强行删除。
- **多人协作**
多人协作工作模式:
用git push origin branch-name推送自己的修改。
若远程分支比本地更新，推送会失败，要先用git pull合并。再次推送。
git branch --set-upstream branch-name origin/branch-name   创建本地分支与远程分支的链接关系
git remove -v   查看远程库信息
git checkout -b branch-name origin/branch-name   建立本地分支和远程分支的关联

标签
---
在版本库中打标签可以唯一确定打标签时刻的版本。
- git tag name   创建新的标签
- git tag -a tagname -m   指定标签信息
- git tag   查看所有标签
- git push origin tagname   推送一个本地标签到远程
- git push origin --tags   推送全部未推送过的本地标签
- git tag -d tagname   删除一个本地标签
- git push origin :refs/tags/tagname   删除一个远程标签









