---
layout:      post
title:       gitignore正确使用方法
subtitle:    git相关
date:        2018-11-13
author:      Mingke Fan
header-img:  img/post-bg-e2e-ux.jpg
tags:
    - git
---

# .gitignore正确使用方法

```shell
git rm --cached 要忽略的文件(git rm --cached .是忽略所有文件)
git add .gitignore(添加过滤规则)
git add .(重新根据过滤规则追踪文件)
git commit -m "make .gitignore working"
git push
```

- .gitignore文件针对未追踪的文件进行过滤，所以需要`git rm --cached 文件`从Git的数据库中删除对某些文件的追踪.  
- git rm删除的是追踪状态，而不是物理文件（本地依然存在物理文件），同时git rm可以记录删除的动作。

## reference

[git忽略已经被提交的文件](https://segmentfault.com/q/1010000000430426)

["git rm"和"rm"的区别](https://blog.csdn.net/jfkidear/article/details/12152167)