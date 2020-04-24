# 常用Git指令

* `git init` 初始化仓库

* `git add new.md` 文件添加到暂存区
  `git checkout -- new.md` 反向操作，从暂存区转移到工作区
  `git restore new.md` 新版指令，同`git checkout` 
  
* `git commit -m "create a new file"` 文件提交

* `git reset --hard HEAD^` 回退到上一个版本
  `git reset --hard HEAD~100` 回退到前一百个版本
  `git reset --hard 1094a`  回退/前进到1094a开头的版本号
  `git restore --staged` 新版指令，同`git reset HEAD` 
  
* `git status` 查看状态

* `git diff new.md` 查看工作区和暂存区的区别
  `git diff --cached new.md` 查看暂存区和仓库区别
  `git diff HEAD new.md` 查看工作区和仓库的区别
  
* `git log` 显示提交日志
  `git log --pretty=online` 显示简洁
  `git log --graph` 可以看到分支合并图
  
* `git reflog` 记录使用过的git指令

* `git rm new.md` 从版本库中删除文件

* `git remote add origin ...` 本地库关联远程库

* `git push -u origin master` 将本地库的内容push到远程库（第一次）
  `git push origin master` 后期使用时可以用这个指令
  `git push origin dev` 讲本地分支推到远程分支
  
* `git clone ...` 将远程库克隆到本地

* `git checkout -b dev` 创建dev分支并切换
  等同于以下操作
  `git branch dev` 创建dev分支
  `git checkout dev` 切换到dev分支
  `git switch -c dev` 新版指令，创建并切换到dev分支
  `git switch -c dev origin/dev` 本地创建dev分支并与远程仓库dev分支同步
  
  `git branch --set-upstream dev origin/dev`建立本地分支与远程分支的关联
  `git switch dev` 新版指令，切换到dev分支
  
* `git branch` 查看分支

* `git branch -d dev` 删除dev分支
  `git branch -D dev` 强行删除dev分支（如果想要删除没有合并过的分支）
  
* `git merge dev` 合并dev分支到当前分支
  `git merge --no--ff dev`禁用fast forward模式，在merge时生成新的commit,可以从log中看到分支信息即使分支后面被删除
  
* 修复bug时，会创建新的bug分支，合并后删除

* `git stash`保存工作现场，以后恢复
  `git stash list`查看保存了哪些存储
  `git stash pop` 恢复现场并删除stash内容
  `git stash apply` 恢复现场但不删除stash内容 `git stash drop`删除stash内容
  
* `git cherry-pick 34ec....`复制这个提交到当前的分支

* `git tag v1.0` 打标签
  `git tag` 查看标签
  `git tag v0.9 xxxx` 给某一次commit打标签
  `git tag -a v0.1 -, "version 0.1 released" 1094adb` 创建带有说明的标签
  `git show <tag name>` 显示说明文字
  `git tag -d v0.1` 删除
  `git push origin :refs/tags/v0.9` 删除本地标签后用这条指令删除远程标签
  `git push origin <tagname>` 标签推送到远程
  `git push origin --tags` 推送所有本地标签到远程
