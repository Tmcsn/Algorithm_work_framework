# 常用git 命令最小集

## git stash

应用场景：

今天在更新github上Algorithm_work_framework项目时遇到如下情景，我习惯开辟多个分支，多个develop分支以及master分支(这么做主要是模拟平时工作中的环境，方便真实应用场景，结合场景对不同git 命令进行分析与使用)，平时在对应功能的develop分支进行开发，今天在开发到一半时，想要切换到其他develop分支进行开发，此时遇到如下问题：

```
在切换前需要提交您的修改或者保存进度
```

git stash可以对当前修改进行保存，使用命令

git stash or git stash save "message"  就可以将我们本分支的修改暂存起来

git stash pop 还原最新保存的修改

git stash list 显示所有分支的暂存信息

git stash apply stash@{0}  选择某个暂存信息进行恢复

（需要注意的是git stash 是对整个工程进行保存的，在ａ分支上保存的修改，在切换到ｂ分支之后，还可以在ｂ分支上将ａ分支保存的修改还原）