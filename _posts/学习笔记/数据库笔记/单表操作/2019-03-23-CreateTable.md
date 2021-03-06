---
layout: post
title: '表的创建与修改'
date: 2019-03-23
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 表的创建与修改

1. 创建表

   ``` sql
   create table 表名（字段名 类型（长度）[约束],
   	字段名 类型（长度）[约束],
   	字段名 类型（长度）[约束],
   	字段名 类型（长度）[约束]
   ）;
   ```

2. 查看当前数据库的所有表

   `show tables;`

3. 查看表的结构

   `desc 表名;`

4. 删除表

   `drop table 表名;`

5. 修改表名

   * 方法一

     `alter table 表名 rename to 新表名`

   * 方法二

     `rename table 表名 to 新表名`

6. 修改表

* 添加一列

  `alter table 表名 add 字段名 类型(长度) [约束]`

* 修改列的类型(长度，约束)

  `alter table 表名 modify 要修改的字段名 类型(长度) [约束]`

* 修改列名(列名，长度，约束等)

  `alter table 表名 change 旧列名 新列名 类型(长度) [约束]`

* 删除列

  `alter table 表名 drop [colmun] 列名`

* 修改表的字符集

  `alter table 表名 character set 字符集`

* 查看表的信息

  `show create table 表名`

  

