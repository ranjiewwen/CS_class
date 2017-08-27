
# 第十讲 嵌入式SQL语言之动态SQL

- 静态SQL
- 区别变量和属性；高级语言向嵌入式SQL传递变量的方法
![](http://i.imgur.com/f3ZLz2L.png)

- 动态SQL
![](http://i.imgur.com/Ma1U1E1.png)

- 动态构造SQL语句是应用程序员必须掌握的重要手段

## SQL语句的动态构造示例

- 根据界面搜索条件，传入条件构造语句中，然后执行
- 关键在构造查询动态语句
![](http://i.imgur.com/iopf8Dl.png)
- 动态SQL语句构造小结
![](http://i.imgur.com/rde7kc0.png)

- SQL字符串的构造
- 数值型变量转换为字符型，然后是否加引号，比较大小前的转换
![](http://i.imgur.com/A5NTItE.png)

- 动态SQL的两种执行方式
![](http://i.imgur.com/C3ZwEvG.png)

## 数据字典及其作用

- 数据字典
![](http://i.imgur.com/O4CGkNG.png)
- 数据字典的内容跟构成
![](http://i.imgur.com/Mfoibq2.png)
- 数据字典的表结构或视图
- 也是存储在磁盘上的关系，专为内存高效访问设计的特定的数据结构
- 系统目录就是记录数据库的信息
- SQLDA：储存数据库中表的，列的，完整性的定义信息
![](http://i.imgur.com/mndphEl.png)

## ODBC/JDBC使用

- `open database connection`
![](http://i.imgur.com/Q1ENAyh.png)
- 应用程序如何通过ODBC连接一个数据库服务器？
![](http://i.imgur.com/z0PRKBM.png)
- 应用程序如何通过ODBC与数据库服务器进行通信？
![](http://i.imgur.com/z1gg9NI.png)
![](http://i.imgur.com/fHMoVXV.png)

- `Java database connection`
![](http://i.imgur.com/jO04wIt.png)
- 应用程序使用JDBC API访问数据库的过程
![](http://i.imgur.com/UN4fuqb.png)
![](http://i.imgur.com/9wpJCeH.png)

- 比较
- 嵌入式SQL思维
![](http://i.imgur.com/xqIddTl.png)
- ODBC的思维模式
![](http://i.imgur.com/ebKRmNv.png)
- JDBC的思维模式
![](http://i.imgur.com/Ujl1NtH.png)