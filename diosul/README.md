#GIT(伪)笔记

******************

##关于版本控制    
* 程序员必备的技能，调编程效率和更加专业的代码管理
* GIT采用分布式管理系统，更加安全，保证离线的可操作

##一个GIT实例
* 在本地完成代码readme.md
* 命令行cd至目录下
* git init 在此创建git仓库
* git add readme.md 添加代码到版本库的暂存区
* git commit -m "关于修改的标签" 提交代码至版本库
* git staut 查看当前版本库信息
* git branch test 创建test分支
* git checkout test 转到此分支同时修改本地代码
* git add readme.md 添加修改过的代码到test分支
* git commit -m "...." 提交至test
* git checkout master / git merge 合并分支
* git log 查看提交历史
* git branch 查看分支
* git add remote origin www.xxxx.com:git  设置origin
* git push origin master 上传到远程代码仓库
