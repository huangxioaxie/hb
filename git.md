![image-20201120083614767](C:\Users\hb\AppData\Roaming\Typora\typora-user-images\image-20201120083614767.png)

git status 查看整个仓库的状态

git add 文件名：工作区到暂存区

git reset -- 文件名 ：撤销，从暂存到工作区

git diff 查看工作区被跟踪文件的修改详情

git commit 暂存到版本区

git log 

​			分支名

​			--oneline

​			-n

​			--author

​			--graph



git branch -avv  查看全部分支的信息

git reset --soft HEAD~[n]  n表示撤退的步数

git reflog  记录本地仓库所有分支的每一次版本变化 可以看到每个版本的版本号和步数

git reset --hard [版本号] 或[步数] 强制退回





git config --global alias.[简称] [原命令]

git config -l  查看版本信息



***GIT 分支管理(最强大的功能)***

> git fetch 刷新本地分支，与仓库同步但暂不更新  
>
> git rebase origin/master 更新本地分支

> 上述等价于 git pull



> 创建新的分支 git branch [分支名]   
>
> 从master切换到新分支 git checkout [分支名]
>
> 上述等价于 git checkout -b [分支名]   



> 将新分支提交推送给远程仓库 	git push [主机名]  [本地分支名] :[远程分支名]
>
> 简写 git push [本地分支名]



> 本地分支跟踪(通过pull获取更新)远程分支  	git branch -u [主机名/远程分支名] [本地分支名]
>
> 或者  git push -u [主机名] [远程分支名]
>
> 撤销 本地分支对远程分支的跟踪 git branch --unset-upstream [分支名]



> 删除远程分支  	git push [主机名]:[远程分支名]  比如： git push origin :dev
>
> 给当前分支改名  git branch -m [新名字]
>
> 删除本地分支  	git branch -D [本地分支名1] [本地分支名2]  //删除当前分支要去上一分支
>
> 