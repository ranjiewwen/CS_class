## 操作系统之外设

### L26 IO与显示

- 操作系统整体框图
![](http://i.imgur.com/2u6B7G2.png)
- 让外设工作起来，就是向外设寄存器谢命令
- 需要查寄存器地址，内容的格式和语义...操作系统要给用户提供一个简单视图--文件视图
![](http://i.imgur.com/wK60KP6.png)
- 一段操作外设的程序
![](http://i.imgur.com/dGC1EnH.png)
- 文件视图
![](http://i.imgur.com/KzqrdIe.png)

- `printf`实际就是向设备`write`，写之前要打开设备文件
![](http://i.imgur.com/jUT8tJH.png)

- open系统调用
- open的时候，找到inode文件信息，放在PCB中，然后write的时候利用这些信息写文件
![](http://i.imgur.com/US8InA6.png)
- 向屏幕写内容
- `crw_table`函数指针
![](http://i.imgur.com/fMnisbS.png)
- `sleep_if_full()`缓冲区队列，之前再内存中执行很快，屏幕显示慢些，所以先放在缓冲区中，形成一个生产者和消费者模型，进行同步
![](http://i.imgur.com/w15bTkv.png)

- 文件接口write,里面调用open文件描述符,对应设备文件的信息inode,一点一点选择对应什么设备，最后到真真的设备
- 做设备驱动就是写好核心函数，注册到相应的表中

- printf的整个过程
![](http://i.imgur.com/mgxnSZ3.png)

### L27 键盘

- 操作系统将外部设备都当做文件，通过文件描述符确定向哪种外设发指令
- `outb`输出，`inb`输入，这里和寄存器交互
- 键盘的故事，键盘中断
- 根据不同的扫描码，执行不同的`key_table`函数
![](http://i.imgur.com/kn4Yk16.png)
![](http://i.imgur.com/S4Rxv0o.png)
- 输入也要放入缓冲队列中`read_q`,上层再从缓冲队列中读数据
![](http://i.imgur.com/wnDfl2p.png)
- IO读写整体框架
![](http://i.imgur.com/TUDMKza.png)