>   git是一个分布式的版本管理系统,每个人的电脑都有一个完整的版本库
1.  git init #初始化一个仓库
2.  git status #查看当前文件夹下的所有文件状态
3.  git add . #提交所有改动的文件到暂存区
4.  git add 文件名 #提交指定的文件
5.  git commit -m '备注' # 将在暂存区的内容提交的到当前分支
6.  git diff # 查看修改
7.  git log #查看现在所有的版本
8.  git reset --hard HEAD^ 回退到上一个版本 ^^上上个 前100就是 HEAD~100
9.  git reset --hard 'commitId' #回到最新的版本需要找到它的commit id
10. git reflog #查看命令历史记录
11. git restore --staged 文件名 #将暂存区的文件撤销

12. git remote add origin git@github.com:liu-ge-ge/git-study.git 添加地址
13. git push -u origin master 把master推送到远程库
14. git remote -v #查看远程信息
15. git clone '地址' #克隆远程库

16. git checkout -b '分支名称' #创建dev分支，并切换 / git switch -c '分支名称'
17. git branch '分支名称' #创建分支 
18. git checkout '分支名称' #切换分支 /git switch '分支名称'
19. git merge '分支名称' #合并分支 使用的是Fast forward模式
20. git merge --no-ff -m '备注' '分支名称' #禁用Fast forward模式
21. git branch -d '分支名称' #删除分支
22. git log --graph --pretty=oneline --abbrev-commit # 查看分支合并情况



### 分支管理策略
1.首先,master分支应该非常稳定,仅用来发布新版本，平时不能在上面干活，干活都在dev分支上，也就是说dev是不稳定的到发布时再合并到master上

### Bug分支
> 如果你需要暂时到别的分支处理bug但是当前分支工作没有完成，可以使用git stash可以把当前工作现场储存起来，等处理完bug在回到当前分支使用
> git stash pop 回复并删除stash
> git cherry-pick 'commit id' 将在master分支上修复的bug复制到dev分支上