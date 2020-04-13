# 常用Git指令

* `git init` 初始化仓库
* `git add new.md` 文件添加到仓库
* `git commit -m "create a new file"` 文件提交
* `git status` 查看状态
* `git diff new.md` 查看修改前后区别
* `git log` 显示提交日志
  `git log --pretty=online` 显示简洁
* `git reset --hard HEAD^` 回退到上一个版本
  `git reset --hard HEAD~100` 回退到前一百个版本
  `git reset --hard 1094a`  回退/前进到1094a开头的版本号
* `git reflog` 记录使用过的git指令