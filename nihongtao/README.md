Note
========

*quotes*
-------
- Unix的哲学是“没有消息就是好消息”
- Software is like sex: it's better when it's free.

**本机操作**
-

- git status<br>*查看仓库状态。*
- git diff<br>*查看修改的部分。*<br>**p.s:git diff HEAD -- readme.txt**
- git log<br>*显示从最近到最远到最近的日志（下键切换更远的日志）*
- git reset --hard HEAD^/HEAD+number<br>*HEAD^^表示上上个版本，HEAD表示当前版本。*
- git reset --hard+number<br>/HEAD file*数字没必要完全符合。*可以撤销add的误操作，重新放回工作区。
- git reflog<br>*记录每一次操作。*
- git add<br>*add与commit要对应*
- git commit -m ""<br>*提交，引号内容是备注。*
- git checkout -- file<br>*让文件回到最近一次add，或者commit状态，直接丢弃工作区的修改，如果没有“--”就创建了一个新的分支,用版本库里的版本替代工作区内的版本，可以一键还原。*
- git rm file<br>*删除一个文件。*
- git stash<br>*存储工作场地。*
- git stash list<br>*查看存储列表*
- git stash apply/pop<br>*恢复存储内容，恢复存储内容并删除stash。apply stash@{0}恢复指定的文件。*
- git pull<br>抓取远程的新提交。
- git tag <name><br>打开新标签
- git show <tagname>
- git tag -a <tagname> -m<br>指定标签信息
- git tag -s <tagname> -m<br>PGP签名标签。
- git push origin :refs/tags/<tagname>
- git config --global color.ui true<br>显示颜色

**远程操作**
-
- git remote add origin
- git push(p.s:git push origin master)
- git clone + url
- git remote -v<br>显示远程仓库的地址。

**创建与合并分支**
--
- git checkout -b ‘dev’==git branch dev + git checkoout dev。<br>创建+切换分支
- git branch<br>（查看当前分支）
- git branch + name<br>（创建分支）
- git merge dev<br>合并分支*fast-forward快进模式*
- git branch -d dev<br>删除dev**相当于把文件从一个容器转换到另一个中。**
- git merge --no--ff <br>不使用Fast forward能看到曾经做过的合并


原理
--
- **版本库**（.git）<br>暂存区的概念：由工作区->暂存区->master。
- **远程仓库**<br>一台电脑上可以克隆多个版本库，可以实现本机远程库（**超级装逼**）Github做为服务器，作为远程仓库。注册账号需要一个ssh key来确认用户身份。
- **分支管理**<br>在上传之前建立自己的分支，保证了代码的完整性，同时可运行。
- **创建与合并分支**<br>HEAD->master->提交，每次提交master分支的线会向前移，分支线越来越长。dev指针沟通HEAD和master，工作区的修改和提交针对dev分支，但是如果dev指针移动时master并不会从动，需要合并master，合并完成后，删除dev指针，那么剩下的HEAD便指向master，同时master也会前移。
- **解决冲突**<br> <<<<<<<，=======，>>>>>>><br>标记不同的内容。
<br>*git log --graph --pretty=oneline --abbrev-commit*<br>查看合并情况（每行~**这个好有逼格！**）。
- **修复bug**<br>通过merge解决方案到dev并删除出现的bug来解决。
- **标签管理**<br>标签就是某个commit的指针。
- **忽略文件**<br>编写。gitignore文件，并放到库里，但是我还没学会。
