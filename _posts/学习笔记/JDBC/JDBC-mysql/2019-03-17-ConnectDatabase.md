---
layout: post
title: 'JDBC_连接数据库'
date: 2019-03-17
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/jdbc.jpg'
tags: JDBC
---

# 连接数据库

   **连接数据库所需的参数**

|            参数            |                             内容                             |
| :------------------------: | :----------------------------------------------------------: |
| Driver（驱动的完全限定名） |                    com.mysql.jdbc.Driver                     |
|            URL             | url = jdbc:mysql://localhost:3306/数据库名?useUnicode=true&characterEncoding=UTF-8 |
|            user            |                          你的用户名                          |
|            pass            |                         用户名的密码                         |



1. **注册驱动**

   `Class.forName("com.mysql.jdbc.Driver");`

   **解释**：JDBC规范中明确要求**Driver**类必须想DriverManager

   ​	    注册自己，当调用`Class.forname()`时JVM会查找并加

   ​	    载driver,Mysql的driver类中含有静态代码块,代码块中

   ​	    的内容是向DriverManager注册自己，当driver被加载时

     	  静态块中的代码将会执行。

2. 获得连接

   `Connection con = DriverManager.getConnection(url,user,pass);`

