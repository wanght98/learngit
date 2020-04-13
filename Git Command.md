# 常用Git指令

* `git init` 初始化仓库
* `git add new.md` 文件添加到暂存区
  `git check out new.md` 反向操作，从暂存区转移到工作区
* `git commit -m "create a new file"` 文件提交
* `git reset --hard HEAD^` 回退到上一个版本
  `git reset --hard HEAD~100` 回退到前一百个版本
  `git reset --hard 1094a`  回退/前进到1094a开头的版本号
* `git status` 查看状态
* `git diff new.md` 查看工作区和暂存区的区别
  `git diff --cached new.md` 查看暂存区和仓库区别
  `git diff HEAD new.md` 查看工作区和仓库的区别
* `git log` 显示提交日志
  `git log --pretty=online` 显示简洁
* `git reflog` 记录使用过的git指令