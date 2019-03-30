---
layout: post
title: '聚合函数'
date: 2019-03-23
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 聚合函数

> **聚合函数定义**：
>
> ​	聚合函数对一组值执行计算并返回单一的值。**聚合函数会忽略空值(null)**。聚合函数经常与 SELECT 语句的 GROUP BY 子句一同使用。
>
> ​													------引自百度

**注意：**聚合函数不能作为条件放在where语句的后面，可以作为条件放在having的后面

**常用函数：**

| 聚合函数 | 功能   |
| :------: | ------ |
|  sum()   | 求和   |
|  avg()   | 平均   |
|  max()   | 最大值 |
|  min()   | 最小值 |
| count()  | 记数   |



* 获得所有商品价格的总和

  `select sum(price) from product`

* 获得所有商品的平均价格

  `select avg(price) from product`

* 获得所有商品的个数

  `select count(*) from product`

  

