---
layout: post
title: '表与表之间的关系'
date: 2019-03-24
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 表与表之间的关系

* 一对多关系

  > **建表原则**：在多的一方创建一个字段，字段作为外键指向一的一方的字段(unique)

  `alter table 从表名 add [constraint] [外键名] foreign key (外键字段名) references 主表名(主表字段)`

* 多对多关系

  > **建表原则**：需要创建第三张表，中间表中至少两个字段，这两个字段分别作为外键指向各自一方的字段(unique)

