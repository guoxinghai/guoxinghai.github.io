---
layout: post
title: '嵌套查询'
date: 2019-03-24
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 嵌套查询

> 定义：一条查询(select) 语句结果作为另一条查询(select)语句的 一部分(查询条件，查询结果，表等)。

案例：查询**product**表中属于化妆品的商品信息

* 解决方法一（嵌套查询）

  `select product.* from product where category_id = (select cid from category where cname='化妆品')`

* 解决方法二（内连接）

  `select product.* from product , category where category_id = cid and cname = '化妆品'`

