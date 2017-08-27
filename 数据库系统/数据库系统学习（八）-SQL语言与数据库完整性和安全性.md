
## 第八讲 SQL语言与数据库完整性

- 重难点
![](http://i.imgur.com/2pO0uhV.png)

### 数据库完整性的概念

- 关系数据库
![](http://i.imgur.com/efzvWBJ.png)

- 防止和避免数据库中不合理数据的出现
- 输入错误，操作失误，程序处理错误等
![](http://i.imgur.com/T1oKktP.png)

- 完整性约束条件的一般形式
- 对O操作集合，当出现A情况时，检查P约束是否满足，当不满足时进行R处理
![](http://i.imgur.com/eSkhCUf.png)

### 数据库完整性的分类

- 按约束对象分类
![](http://i.imgur.com/XrqFQFu.png)

- 按约束来源分类
![](http://i.imgur.com/npOH3Dn.png)

- 按约束状态分类
![](http://i.imgur.com/Kuf2xP9.png)

### SQL语言实现静态完整性

- 约束类别
![](http://i.imgur.com/NYiAyLR.png)

- SQL实现约束方法`Create Table`
- 列完整性和表完整性
![](http://i.imgur.com/i4uXqcD.png)

- `table_constr`表约束
![](http://i.imgur.com/JC9d7Tp.png)
![](http://i.imgur.com/ZIQxwCO.png)
![](http://i.imgur.com/IlEitGX.png)

- 撤销和追加约束的语句
![](http://i.imgur.com/B3NGsG7.png)

### SQL的断言及应用

- 断言也会影响数据库的效率
- 断言谓词
![](http://i.imgur.com/zFL5fGr.png)

### SQL实现动态完整性

- 触发器`Trigger`
![](http://i.imgur.com/YWe4UWU.png)

- 基本语法
![](http://i.imgur.com/lEJoeGd.png)

- 事件
![](http://i.imgur.com/E9b1jxm.png)

- 示例
![](http://i.imgur.com/oeQ27pZ.png)
![](http://i.imgur.com/hgsjier.png)


## 第八讲 SQL语言与数据库安全性

- 数据库安全性概念
- 免受非法，非授权用户的使用，泄露，更改，破坏等...
![](http://i.imgur.com/wIn8Udz.png)

- 划分好数据库的安全级别以及用户的安全级别

### 自主安全性机制

- 概念
![](http://i.imgur.com/tdFF9O6.png)

- DBMS怎么样自动实现自主安全性
![](http://i.imgur.com/RTamWXc.png)

- 安全性访问规则
- `P`谓词：即条件
![](http://i.imgur.com/d88y1fg.png)

- 示例
![](http://i.imgur.com/NH1A12o.png)

- 按名控制安全性：存储矩阵
![](http://i.imgur.com/Pd0PKT4.png)

- 视图实现自主安全性
![](http://i.imgur.com/6rUVLL0.png)

### SQL语言实现安全性控制

- SQL语言的用户与权力
![](http://i.imgur.com/lECFQP6.png)

- 授权命令
![](http://i.imgur.com/JscEwXu.png)

- 收回授权命名
![](http://i.imgur.com/DwhM7K1.png)

### 自主安全性的授权过程及其问题

- 授权过程
![](http://i.imgur.com/h3n23OP.png)
![](http://i.imgur.com/0HnGcDO.png)

### 强制安全性机制

- 访问规则
![](http://i.imgur.com/bBQ0MiK.png)

- 强制安全性机制的实现
![](http://i.imgur.com/RLHF3ub.png)




