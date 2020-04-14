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
* `git reflog` 记录使用过的git指令
* `git rm new.md` 从版本库中删除文件
* `git remote add origin ...` 本地库关联远程库
* `git push -u origin master` 将本地库的内容push到远程库（第一次）
  `git push origin master` 后期使用时可以用这个指令
* `git clone ...` 将远程库克隆到本地
* `git checkout -b dev` 创建dev分支并切换
  等同于以下操作
  `git branch dev` 创建dev分支
  `git checkout dev` 切换到dev分支
* `git branch` 查看当前分支
* `git branch -d dev` 删除dev分支
* `git merge dev` 合并dev分支到当前分支

