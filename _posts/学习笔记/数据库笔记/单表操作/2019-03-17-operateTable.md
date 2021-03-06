---
layout: post
title: '对数据库表记录操作'
date: 2019-03-17
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/database.jpg'
tags: database SQL
---

# 对数据库表记录操作

* **插入数据中文乱码问题解决**

  1. **方法一** 

     **修改数据库安装目录里面的 my.ini 文件 然后重启Mysql服务**

     在第57行添加：**default-character-set=utf8**

     ![图片](img\修改my.ini文件.png)

     2. **方法二**(<font color="green">建议</font>)

        使用命令：`set names 字符集`

* **插入记录**

  1. `insert into 表名 (列1，列2，列3) values (值1，值2，值3)`

     **注意前面的列与后面的值相对应前面的列可以自己指定**

  2. `insert into 表名 values(值1，值2，值3)`

     **后面的值必须要与全部的列相对应 如果某个列是自动增长的可以将值设置为null**

  

* **更新/修改记录**

  1. 不带条件

     `update 表名 set 字段名=值`

     结果会将表中该字段下所有的值都改变

  2. 带条件的

     `update 表名 set 字段名=值 where 条件`

     结构会将表中字段符合条件的内容改变

* **删除表记录**

  1. 带条件

     `delete from 表名 where 条件`

     会将符合条件的记录删除，id不会重置

  2. 不带条件的

     ` delete from 表名`

     会将表中所有记录都删除但表没有被删除

  3. 面试题

     说说delete与truncate的区别?

     delete 删除的时候是一条一条的删除记录配合事务可以将数据找回

     truncate是将整个表删除然后再新建一张符合条件的表找不回数据

     truncate删除table不能带条件：`truncate 表名`

* **事务**

  1. 开启事务

     `start transaction`

  2. 回滚事务

     `rollback`

* **查询操作**

  **语法**：`select [distinct]  | * 列名1，列名2 from 表名 [where 条件]`

  **以下列这个存储商品信息的表（product）为例**

  |  id  | name | price | date |
  | :--: | :--: | :---: | :--: |
  |      |      |       |      |

  

  1. 查询所有商品信息

     语法：`select * from product`

  2. 查询商品名和商品价格

     `select name, price from product `

  3. 查询所有商品信息使用表别名

     `select * from product [as] p`

  4. 查询商品名，使用列别名

     `select name [as] p `

  5. 去掉重复值(按照价格)

     `select distinct(price) from product`

  6.   所有商品价格＋10显示

     `select name , price + 10 from product`

