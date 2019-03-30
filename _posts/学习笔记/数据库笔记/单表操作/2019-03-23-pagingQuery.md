---
layout: post
title: '分页查询'
date: 2019-03-23
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 分页查询

**使用Limit 关键字进行分页查询操作**

* **limit 关键字两个参数的含义(limit m, n)**

  n 代表每页含有的记录条数

  m 代表起始位置(例如要查询第x页则 m = n*(x-1) )

* **limit关键字查询语句**(例如要查询student表中的学生信息 每页3条记录，第5页)

  `select * from student limit 12, 3`