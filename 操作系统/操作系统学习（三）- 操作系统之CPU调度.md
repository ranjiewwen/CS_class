## 操作系统之进程与线程

### L14 CPU调度策略

- 如何设计调度算法？
![](http://i.imgur.com/XGH7d8U.png)

- 调度关键在：折中和综合
![](http://i.imgur.com/8tH5oLf.png)

- IO约束型的任务一般是前台任务，和用户交互；CPU约束型关注周转时间
- 进程切换过程需要系统内耗，切换时间长则系统内耗大

- 各种CPU调度算法
- `FCFS`先来先服务
- P3和P2交换，达到短作业优先
![](http://i.imgur.com/v27ZnHA.png)

- `SJF`短作业优先
- 该方法周转时间最短
![](http://i.imgur.com/1W7NsE0.png)

- `Robin` RR：按时间片来轮转调度---->提高响应时间
![](http://i.imgur.com/YQPPtLW.png)

- 响应时间和周转时间同时存在，怎么办？
- 优先级调度
- 如果固定优先级的时候，可能后台饥饿
- 后台任务优先级动态升高，但是前台的响应时间变长
- 矛盾
![](http://i.imgur.com/wx288Vp.png)

- 调度算法有一定的学习能力

### L15 一个实际的schedule函数

- 实时调度，低耗调度
- `TASK_RUNNIG`就绪队列
- `counter`最大就是优先级调度,`counter`本身也是时间片
- `c==0`就绪队列已完
- 执行IO阻塞进程完后，进入就绪队列的时候优先级升高
![](http://i.imgur.com/XL7W1kj.png)
- `counter`优先级,阻塞时间越长，优先级越高，而且执行时间越长
![](http://i.imgur.com/q8c9lsf.png)

- `counter`的作用
- 响应时间有界
![](http://i.imgur.com/YH1BS6i.png)