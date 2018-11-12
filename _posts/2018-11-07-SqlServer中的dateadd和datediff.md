---
layout:      post
title:       SQL Server
subtitle:    dateadd和datediff详解
date:        2018-08-13
author:      Mingke Fan
header-img:  img/post-bg-e2e-ux.jpg
tags:
    - sql
---

# 日期相关Sql总结

## datediff

```sql
datediff(datepart,start,end)
求出end时间同start时间之间的间隔
```

例：

```sql
datediff(month,0,getdate())
求出当前时刻同0之间的月份间隔
```

## dateadd

```sql
dateadd(datepart,number,date)
date + number之后的datetime
```

dateadd和datediff通常搭配使用，如下：

```sql
dateadd(mm,datediff(month,0,getdate()),0)
当前月份的第一天的00:00:00.000时刻
```

```sql
dateadd(ms,-3,dateadd(mm,datediff(month,0,getdate()),0))
上个月的最后一天的23:59:59.997时刻
```

## reference

[datediff官方文档](https://docs.microsoft.com/en-us/sql/t-sql/functions/datediff-transact-sql?view=sql-server-2017)