---
layout: post
title: Mysql定义类型与查询类型不一致问题处理
date: 2018-08-29 14:27:25
forType: DB
category: Mysql
tag: [Mysql, 问题处理]
---

* content
{:toc}

问题描述
-----------------------------------------------------------------
Mysql中某一字段定义成int类型，查询时传入String，会截取字符串


解决
-----------------------------------------------------------------
```
1. SELECT COLUMN_NAME FROM TABLE_NAME t WHERE CONCAT(t.int_id) = '***' ;
2. SELECT COLUMN_NAME FROM TABLE_NAME t WHERE CAST(t.int_id as char) = '***' ;
```

引用
-----------------------------------------------------------------
原文地址：[Mysql 一个字段定义成int类型，查询时传入String，会截取字符串](https://blog.csdn.net/xiaolyuh123/article/details/64441817?locationNum=3&fps=1)