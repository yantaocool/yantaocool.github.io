---
layout:     post
title:      "git 更新代码到本地"
subtitle:   " \"Git update code to local\""
date:       2018-11-23 12:01:00
author:     "吴庆宝"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 工具
---

> “JUST DO IT. ”


## 正规流程
```
git status（查看本地分支文件信息，确保更新时不产生冲突）

git checkout – [file name] （若文件有修改，可以还原到最初状态; 若文件需要更新到服务器上，应该先merge到服务器，再更新到本地）

git branch（查看当前分支情况）

git checkout remote branch (若分支为本地分支，则需切换到服务器的远程分支)

git pull
```
若命令执行成功，则更新代码成功！

## 快速流程
上面是比较安全的做法，如果你可以确定什么都没有改过只是更新本地代码 
```
git pull (一句命令搞定)
git branch 看看分支 
git chechout aaa 切换分支aaa 
git branck aaa 创建aaa分支 
git chechout -b aaa 本地创建 aaa分支，同时切换到aaa分支。只有提交的时候才会在服务端上创建一个分支
``` 

—— wuxiumu 后记于 2018.11


