本系列关于AI/DeepLearning的大部分资料来源于Andrew NG在Coursera的讲课本内容，  
希望系统学习的同学请自行在Coursera注册学习或旁听： https://www.coursera.org  

接下来看看如何计算导数dw, db

## 导数
![img](https://huoqifeng.github.io/img/deeplearning/derivator.png)
 - 导数是导函数在某一点的值
 - 计算如上面的例子

## 高次函数的导数
![img](https://huoqifeng.github.io/img/deeplearning/derivator1.png)
![img](https://huoqifeng.github.io/img/deeplearning/derivator2.png)

## Computation Graph
要计算导数的计算先介绍computation Graph
![img](https://huoqifeng.github.io/img/deeplearning/computation-graph.png)
 - 蓝线是Forward Computation Graph
 - 红线代表Backward Computation Graph

## 用Computation Graph 计算导数
![img](https://huoqifeng.github.io/img/deeplearning/computation-graph-derivator.png)
 - 首先计算 dJ/dv = 3
 - 在计算 dv/da = 1
 - dJ/da = (dJ/dv)*(dv/da) = 1*3 = 3
