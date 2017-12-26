
# 第六讲 SQL语言概述

- [基本命名操作](http://www.cnblogs.com/qinqinmeiren/archive/2011/05/21/2151693.html)

- 关系代数是集合的思想
- 关系演算是逻辑的思想（数学公式）

- `SQL-86,SQL-89,SQL-92,SQL-99,SQL-2003,2008...`发展过程标准
- SQL是`DDL,DML,DCL`于一体的数据库语言
- DDL:`Create,Alter,Drop(撤销)`
![](http://i.imgur.com/Oj8X58J.png)

- 语法和语义的精确表达

- 常用数据库系统：Student,Dept（院系）,Course,Teacher,SC(选课)

## 利用SQL建立数据库 

- 创建数据库
![](http://i.imgur.com/sBHsTg7.png)

- `create database`
- `create table`
![](http://i.imgur.com/FoPsEnm.png)
- 数据类型
![](http://i.imgur.com/OORVwmL.png)

## 利用SQL进行基本查询

- `Select- from - where`
![](http://i.imgur.com/nx99jz3.png)
![](http://i.imgur.com/CyapZlv.png)

- `where`子句检查表中的每个元组
- 关系是不允许重复的，但现实DBMS是可以重复的
![](http://i.imgur.com/tq5PUr3.png)

- 对检索结果排序`select -from -where-order by`
![](http://i.imgur.com/TXULRPv.png)

- 模糊查询问题`select from where (not)like`
![](http://i.imgur.com/GeXPYoh.png)
![](http://i.imgur.com/c5O6yqP.png)

### 利用SQL语言进行多表联合查询

- 连接条件放在where条件中
![](http://i.imgur.com/NHVtVTs.png)
![](http://i.imgur.com/BWIRCKV.png)

- 重名处理
![](http://i.imgur.com/c7F9q6E.png)
- from中定义了T1,T2，在select，where中就能使用
![](http://i.imgur.com/uwXZRmI.png)

- 多表联合查询训练
- `as`省略
- 用的theta连接而不是等值连接
- 等值连接是特殊的theta连接，当A=B时才能连接，自然连接有默认的连接条件，自然连接为特殊的等值连接
![](http://i.imgur.com/i5fVow3.png)

## 605结合SELECT的INSERT语句

- 一些，某些处理，插入一批数据`insert into 表名`
![](http://i.imgur.com/E11DbzR.png)

## 605结合SELECT的DELETE语句

- 删除满足指定条件的元组`delete from 表名`

- `Updata 表名`
![](http://i.imgur.com/j9ZwBIB.png)

## 数据库的修正和撤销

- `alter table tablename ***`
![](http://i.imgur.com/J9LcdMw.png)
- `Drop Table student`
- 数据库指定和关闭
![](http://i.imgur.com/e8tiqnz.png)

- 数据库的备份和恢复
- 数据库的授权`grant 权限 on 表名 to 用户名`
- 创建修改约束
![](http://i.imgur.com/fwokHSe.png)

- 总结
![](http://i.imgur.com/tiNbxUd.png)