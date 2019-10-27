---
layout:     post
title:      "Git使用中的问题 更新中"
subtitle:   " \"Problems in Git usage Update\""
date:       2018-11-23 20:01:00
author:     "吴庆宝"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 工具
---

> “JUST DO IT. ”


**git add . 的时候遇到warning: LF will be replaced by CRLF in ...... 解决办法**

输 入 git add . 后出现
```
git add -A
warning: LF will be replaced by CRLF in _config.yml.
The file will have its original line endings in your working directory.
```
解决方法：
```
git config --global core.autocrlf false
```
就可以解决了。

原因就是：

原因是路径中存在 / 的符号转义问题，false就是不转换符号默认是true，相当于把路径的 / 符号进行转义，这样添加的时候就有问题

**git commit 报 "Changes not staged for commit:"是怎么回事?**

你 git add 了吗

—— wuxiumu 后记于 2018.11
