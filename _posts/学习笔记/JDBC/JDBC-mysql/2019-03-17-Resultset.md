---
layout: post
title: 'JDBC_处理结果集'
date: 2019-03-17
author: 海
color: rgb(255,210,32)
cover: '../assets/bgimage/jdbc.jpg'
tags: JDBC
---

# 处理结果集

* **ResultSet**

  它内部有一个“行光标”，光标默认的位置在“第一行上方”，我们可以调用next()方法把“行光标”

  向下移动一行，当第一次调用next()方法时，“行光标”就到了第一行记录的位置，这时可以使用

  ResultSet提供的getXXX(int col) 方法来获取指定列的数据。

* 判断处理结果是否为空

  需要注意的是不管statement的executeQuery查询结果是否为空返回的ResultSet对象都会是null

  因此要判断结果是否为空需要调用ResultSet的next()方法如果为空会返回false反之true。

* ResultSet的getXXX(int col)方法

  * `Object getObject(int col)`, 获得任意对象

  * `String getString(int col)`，获得字符串

  * `int getInt(int col)`，获得整型

  * `double getDouble(int col)`，获得双精度浮点数

    **参数col对应表中的列（从1开始）**