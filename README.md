git-note
===
在这里大家把任务做完，即用git命令将自己的笔记（到自己的文件夹（自己拼音为文件夹名）里的README里面）上传到github上。


注意
----
- 在clone以后，先git fetch origin，再一定记住**要创建一个以自己名字拼音的分支**，然后在这个分支上将笔记弄到README.md里面。
- 在自己的分支上把任务完成后，请切换到note分支，然后merge自己的分支（**记住要带--no-ff**,这样就有merge的记录，如果有人没按照这个流程来，很容易就可以看出来）
- 然后再将note分支push
- **master分支将由我来merge，其他人禁止在master分支上做任何修改**

工作流
---
- 每个人需要有自己的分支，所有的工作需要在自己分支上完成。
- 是分支保持最新（与开发版一致），当要开始工作的时候，先在自己的分支上fetch开发版分支（这次的开发板分支叫note），然后完成一个任务后，在开发板分支（也是先要fetch一下，**保持最新**）merge，最后push到远程仓库。

保持note最新的步骤
---
方法1：

git checkout note

git fetch origin note:tmp

git diff tmp（审查diff，一般没冲突的话就可以忽视）

git merge tmp

方法二（不安全，不推荐，以后禁止使用）：

git checkout note

git pull origin note
