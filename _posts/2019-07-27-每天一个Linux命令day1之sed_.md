---
layout:      post
title:       每天一个Linux命令之sed
subtitle:    day1
date:        2019-07-27
author:      Mingke Fan
header-img:  img/post-bg-e2e-ux.jpg
tags:
    - Linux
---

## sed替换第一个匹配

写一个sed脚本，只会用“Banana”替换第一次出现的“Apple”
示例输入：输出：
     Apple       Banana
     Orange      Orange
     Apple       Apple
这是一个简单的脚本： 编者注：适用于 GNU  sed 只要。
sed '0,/Apple/{s/Apple/Banana/}' filename

来自 <http://landcareweb.com/questions/1393/ru-he-shi-yong-sedzhi-ti-huan-wen-jian-zhong-de-di-yi-ge-pi-pei-xiang>

sed '0,/pattern/s/pattern/replacement/' filename
这对我有用。
例
sed '0,/<Menu>/s/<Menu>/<Menu><Menu>Sub menu<\/Menu>/' try.txt > abc.txt
编者注：两者兼容 GNU  sed 只要。

来自 <http://landcareweb.com/questions/1393/ru-he-shi-yong-sedzhi-ti-huan-wen-jian-zhong-de-di-yi-ge-pi-pei-xiang>

* -i 可以将修改内容持久化到文件
