---
layout: post
title: mongo查询技巧
date: 2018-09-07 18:11:26
forType: DB
category: mongoDB
tags: [mongoDB, 查询技巧]
---

* content
{:toc}

mongo检索
----------
模糊搜索：
```
db.getCollection('CollenctionName').find({"elementName":{$regex:"***"}});
```
时间段查询：
```
db.getCollection('CollenctionName').find({"elementName":{$gte: new Date("2018-01-01T00:00:00.000+08:00"), 
                                                         $lt: new Date("2018-01-01T23:59:59.000+08:00")}});
```

mongo去重统计
----------
db.CollectionName.distinct("elementName");