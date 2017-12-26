
# 第九讲 嵌入式SQL语言之基本技巧

## 901 什么是嵌入式SQL语言

- 交互式SQL语言的局限性
![](http://i.imgur.com/vKqrmuT.png)

- 嵌入式SQL语言
![](http://i.imgur.com/zwEjqkc.png)

- 交互式和嵌入式语言的对比
![](http://i.imgur.com/GtXqmev.png)

- 高级语言中使用嵌入式语言需要解决的问题
![](http://i.imgur.com/rRf6gRE.png)

## 902 程序与数据库连接

- 变量的声明与使用
- 嵌入式SQL的可变化性
![](http://i.imgur.com/v0oODxO.png)
- 程序与数据库的连接与断开
![](http://i.imgur.com/2bt3Z0V.png)
![](http://i.imgur.com/qXqcqT2.png)

- SQL执行过程中，必须有提交与撤销语句才能确认其操作结果！
![](http://i.imgur.com/z0NhwHe.png)

## 事务的概念与特性

- 事务的概念`transaction`
- 事务的开始和结束由应用程序员决定
- 因为任何一条 SQL 语句都可告诉 DBMS 开始一个新事务
![](http://i.imgur.com/vzAf3zG.png)
- DBMS提供一致性状态转换
![](http://i.imgur.com/K5xWiuC.png)
- 事务的特性`ACID`
![](http://i.imgur.com/X01NqjE.png)
- `SQL communication area`和SQL错误捕获语句

## 数据集和游标

- 如何读取单行数据和多行数据
- 单行结果直接赋给宿主程序的变量即可
![](http://i.imgur.com/Sjny1V0.png)
- 检索多行结果，需要用游标`Cursor`
![](http://i.imgur.com/sPh0gFI.png)
![](http://i.imgur.com/KzBdGeJ.png)
- 游标的使用
![](http://i.imgur.com/tw6g7z7.png)
- 游标的定义
![](http://i.imgur.com/6bnoo35.png)

## 可滚动游标

- 可滚动游标的概念
![](http://i.imgur.com/EXrbOzw.png)
- `open database connectivity`odbc是一种跨DBMS的DB操作平台
- 可滚动游标的使用
![](http://i.imgur.com/oGpnDi2.png)
![](http://i.imgur.com/inDotYF.png)

## 数据库的增删改

- 数据库记录的删除
![](http://i.imgur.com/K5fCopH.png)
- 数据库的更新
![](http://i.imgur.com/wzO7XNW.png)
- 数据库的插入
![](http://i.imgur.com/7ploxjw.png)

## 异常状态捕获机制

- 基本机制
- 设置SQL通信区，设置状态捕获语句，状态处理语句
![](http://i.imgur.com/APZ923x.png)
- SQL通信区：SQLCA
![](http://i.imgur.com/Mx166FG.png)
- 状态捕获语句
- `SQL error;not found;sqlwarning`
- `continue;goto 标号；stop；Do/Call func`
![](http://i.imgur.com/FRH1bGx.png)
- 作用范围
![](http://i.imgur.com/ragWRfn.png)
- 状态捕获语句whenever的使用容易引发无限循环
- 此时用`exec sql whenever sqlerror continue`控制是否无限循环
- 典型DBMS系统记录状态信息的三种方法
![](http://i.imgur.com/kBXIVv7.png)
- 程序处理，对错误信息的处理
![](http://i.imgur.com/IcMQnM4.png)
![](http://i.imgur.com/Dg8EQmO.png)

