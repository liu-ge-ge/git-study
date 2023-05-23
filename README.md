>git是一个分布式的版本管理系统,每个人的电脑都有一个完整的版本库
1. git init #初始化一个仓库
2. git status #查看当前文件夹下的所有文件状态
3. git add . #提交所有改动的文件到暂存区
4. git add 文件名 #提交指定的文件
5. git commit -m '备注' # 将在暂存区的内容提交的到当前分支
6. git diff # 查看修改
7. git log #查看现在所有的版本
8. git reset --hard HEAD^ 回退到上一个版本 ^^上上个 前100就是 HEAD~100
9. git reset --hard 'commitId' #回到最新的版本需要找到它的commit id
10. git reflog #查看命令历史记录
11. git restore --staged 文件名 #将暂存区的文件撤销