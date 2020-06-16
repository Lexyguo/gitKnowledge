# gitKnowledge
git使用中一些常用、好用的命令

检出仓库：$ git clone ...(需要克隆的地址)

查看远程仓库：$ git remote -v

查看远程库：$ git remote show

添加远程仓库：$ git remote add [name] [url]

删除远程仓库：$ git remote rm [name]

修改远程仓库：$ git remote set-url --push [name] [newUrl]

拉取远程仓库：$ git pull [remoteName] [localBranchName]

推送远程仓库：$ git push [remoteName] [localBranchName]

查看本地分支：$ git branch

查看所有的分支：$ git branch -a

查看远程分支：$ git branch -r

创建本地分支：$ git branch [name]

切换分支：$ git checkout [name]

切换到本地dev分支：$ git checkout dev

创建新分支并立即切换到新分支：$ git checkout -b [name]

删除分支：$ git branch -d [name] （-d选项只能删除已经参与了合并的分支，对于未有合并的分支是无法删除的。如果想强制删除一个分支，可以使用-D选项）

合并分支：$ git merge [name]

创建远程分支(本地分支push到远程)：$ git push origin [name]

删除远程分支：$ git push origin :heads/[name] 或者 $ gitpush origin :[name] 

查看当前状态：$ git status

提交：$ git commit

添加commit信息：$ git commit -m

查看commit的差异：$ git commit -v

提交并且加注释：$ git commit -am "init"

把所有的change加到git index里然后再commit：$ git commit -a

查看commit的日志：$ git log

查看尚未暂存的更新：$ git diff 

查看尚未提交的更新：$ git diff --cached 或 $ git diff --staged

将文件给push到一个临时空间中：$ git stash push

将文件从临时空间pop下来：$ git stash pop

相当于是从远程获取最新版本到本地，不会自动merge：$ git fetch

看已经被提交的：$ git ls-files

看所有用户：$ git config --list

合并某个分支提交的内容到当前分支并提交：$ git cherry-pick <commit id>

合并某个分支提交的内容到当前分支但不提交：$ git cherry-pick -n <commit id>

继续cherry-pick操作：$ git cherry-pick --continue

取消cherry-pick操作：$ git cherry-pick --abort

中断cherry-pick操作：$ git cherry-pick --quit

该分支顶端提交进cherry-pick：$ git cherry-pick <branch name>

查看版本：$ git tag

创建版本：$ git tag [name]

删除版本：$ git tag -d [name]

查看远程版本：$ git tag -r

创建远程版本(本地版本push到远程)：$ git push origin [name]

删除远程版本：$ git push origin :refs/tags/[name]

合并远程仓库的tag到本地：$ git pull origin --tags

上传本地tag到远程仓库：$ git push origin --tags

创建带注释的tag：$ git tag -a [name] -m '注释信息'

