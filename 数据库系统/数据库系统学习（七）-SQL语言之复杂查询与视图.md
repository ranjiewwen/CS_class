
# 第七讲 SQL语言之复杂查询与视图

- 基本内容
![](http://i.imgur.com/uewQTs3.png)

- **子查询**
![](http://i.imgur.com/9Rs0Kx8.png)

- IN与NOT IN谓词子查询
- 判断某一表达式的值是否在子查询的结构中
![](http://i.imgur.com/A1qhd0m.png)
![](http://i.imgur.com/kJQlv4T.png)

- 非相关子查询
![](http://i.imgur.com/77xASFs.png)
- 相关子查询
![](http://i.imgur.com/piuet23.png)

- theta some /theta all谓词子查询
![](http://i.imgur.com/XnrCwsf.png)
![](http://i.imgur.com/mGI7FJc.png)

- 需要注意的
![](http://i.imgur.com/V0bfhXa.png)
![](http://i.imgur.com/ZIgYTTI.png)
![](http://i.imgur.com/NvFcqdy.png)

- EXIST与NOT EXIST子查询
- 对`所有或者全部`词有用处，做否定的否定转化
![](http://i.imgur.com/XEITYI3.png)

### 704-结果计算和聚集计算

- 结果计算
![](http://i.imgur.com/K3TAxeZ.png)
![](http://i.imgur.com/Pw7hRg4.png)

- 聚集函数
![](http://i.imgur.com/wN3ataf.png)
![](http://i.imgur.com/NGTS24o.png)

### 分组聚集计算和分组过滤

- 分组查询
![](http://i.imgur.com/chbVwjA.png)
![](http://i.imgur.com/15W1zeX.png)

- `where`查询是对表的每个元组查询，`count`是聚集函数，对每个组操作

- 分组过滤，**聚集函数不允许用于where子句中**

![](http://i.imgur.com/rAeyH2K.png)
![](http://i.imgur.com/2DZrmX2.png)
![](http://i.imgur.com/qdo5IrI.png)
![](http://i.imgur.com/wjnnhUG.png)

### 用SQL表达并交差操作

- 并交差处理
![](http://i.imgur.com/985EXrN.png)
![](http://i.imgur.com/woFiRkQ.png)
![](http://i.imgur.com/5mfzsDk.png)
![](http://i.imgur.com/9lPEmOd.png)

### 用SQL处理空值处理

- 空值处理
![](http://i.imgur.com/pKQOT6Q.png)
- `null`不能和任何表达式进行运算
![](http://i.imgur.com/YQ1fMjc.png)
![](http://i.imgur.com/Mc4dZXB.png)

### 用SQL语句表达连接和外连接操作

- 内外连接
![](http://i.imgur.com/uEAFLF0.png)
![](http://i.imgur.com/7LgrxZ4.png)
![](http://i.imgur.com/3ycx9fO.png)
![](http://i.imgur.com/bFkLWks.png)

### SELECT小结

- 基本用法
![](http://i.imgur.com/OEWE82J.png)
- `OQL`面向对象数据库，语法更加复杂

### SQL语言视图

- 视图的基本概念和结构
- 基本表（存储数据）和视图（存储公式）
![](http://i.imgur.com/HupdV2Y.png)

- 视图的定义
![](http://i.imgur.com/I913B56.png)

- 回顾一下as用法
![](http://i.imgur.com/jTTKepa.png)

- 实例
![](http://i.imgur.com/A7ahILY.png)

- 定义好的视图，可以像Table一样，在各种SQL语句中使用

- 视图的更新，带有聚集函数的更新不行
![](http://i.imgur.com/SrmR7Wo.png)
- 视图更新的可执行性
![](http://i.imgur.com/PC38fiF.png)

