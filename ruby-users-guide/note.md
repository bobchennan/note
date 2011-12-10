What is ruby?
=============

Getting started
===============

Simple examples
===============

* 函数返回最后一次计算的值，允许使用return但是不必要

* ARGV[]，命令行参数数组

* to_i，把字符串转换为数字

* 内置高精度

String
======

* 双引号字符串支持反斜杠转义，以及#{}内嵌表达式

* 单引号字符串不进行转义

* 可以用+和*进行字符串的连接和重复

* 在ruby中，字符是数字

* []用来取字符，负指标表示从末尾开始数，这点和python一致

* [a, b]对应与python中的切片，[a..b]是取第a和第b个字符之间的字符串

Regular expressions
===================

* 一个正则表达式例子：/\<0(x|X)(\d|[a-f]|[A-F])+\>/

* 用=~来测试，返回第一个匹配的下标或者nil

Arrays
======

* 一个数组[1, 2, "3"]

* 同字符串一样，支持连接和重复，取址和切片

* 可以用join()和split()和字符串互相转化

* 一个哈希表{1 => 2, "2" => "4"}

* 使用delete()方法删除某个键值

Back to the simple examples
===========================

* 使用def来定义函数

* case ... when ... when ... end

* case利用===进行测试，例如(2..5) === i，以及/\d/ === "1"

* while ... end

* while和if可以写成后缀格式，例如puts "is zero" if a == 0，或者puts i += 1 while i < 3

* unless是if的反面，until是while的反面

* break是C里面的break，next是C里面的continue，redo是再来一发（当前循环），还可以直接return

* ruby的for是foreach，还等价于each方法，例如for e in c ... end等价于c.each {|e| ... }

Iterators
=========

* string提供each_byte和each_line迭代器，each实现的是each_line

* retry可以重来整个循环

* yield用来调用作为参数的语句块

Object-oriented thinking
========================

Methods
=======

* 函数调用的括号可以省略

* 可以用self来指代实例，而且可以省略

Classes
=======

* 使用class来定义类，def来定义其成员函数

* new方法用来创建实例

Inheritance
===========

* 使用\<来表示继承

Redefinition of methods
=======================

* 可以直接重写成员函数

* 使用super来调用父类的同名函数

Singleton methods
=================

* 可以为实例定义方法

Modules
=======

* 使用.或者::来调用

* 使用include来导入

* 可以利用include来实现多继承

Procedure objects
=================

* proc{}用来定义过程对象

* 过程对象通过call方法执行

* trap用于响应系统调用

Variables
=========

* $表示全局变量，@表示实例变脸，小写字母表示实例变量，大写字母表示常量

* self和nil是例外，self是个全局变量，而nil是个常量

Global variables
================

* 可以使用trace_var来跟踪变量改变

Instance variables
==================

Local variables
===============

* 对于局部变量，第一次赋值等于声明

Class constants
===============

Exception processing: rescue
============================

* 使用open来打开文件

* rescue相当于except，使用retry再来一发

Exception processing: ensure
============================

* 搞不定就fail吧

* ensure相当于finally

Accessors
=========

* 可以定义attr=和attr方法来实现setter和getter

* 定义inspect来代替默认返回值

* 使用attr_reader, attr_writer, attr_accessor来快速定义setter和getter

Object initialization
=====================

* 使用initialize定义构造函数
