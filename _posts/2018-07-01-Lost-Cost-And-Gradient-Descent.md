本系列关于AI/DeepLearning的大部分资料来源于Andrew NG在Coursera的讲课本内容，  
希望系统学习的同学请自行在Coursera注册学习或旁听： https://www.coursera.org  

要计算W,b就需要不停的迭代，直到满意为止，这个就是个优化问题。
什么是满意呢？就是误差最小的时候，Lost, Cost就是定义误差的，经常采用的方法就是Gradient Descent
今天我们就来看Lost, Cost和Gradient Descent。

## 什么是Lost 和 Cost
![img](https://huoqifeng.github.io/img/deeplearning/lost-cost.png)
 - Lost 是一个样例上的误差（损失）
 - Cost 是所有m个样例的误差

## 什么是Gradient Descent
![img](https://huoqifeng.github.io/img/deeplearning/gradient-descent.png)
 - Gradient Descent 梯度下降， 是要找到下降最快的方向，也就是导数或导函数
 - 应用Gradient Descent 不停迭代计算dw, db得到不同的W, b,用不同时间的W,b重新计算Lost, Cost
 - 数学上可以证明对于凸函数一定能找到最优点或者局部最优点
 - 后续的课程会讲到如何如何找到全局最优点和避免过拟合

## 一次函数在某个点的导数
![img](https://huoqifeng.github.io/img/deeplearning/derivator.png)

## 高次函数在某个点的导数
![img](https://huoqifeng.github.io/img/deeplearning/derivator1.png)
![img](https://huoqifeng.github.io/img/deeplearning/derivator2.png)

## 如何实现Gradient Descent
![img](https://huoqifeng.github.io/img/deeplearning/implement-gradient-descent.png)
 - 在实现Gradient Descent的时候要用到导数。
 - 计算dw, db,后面讲完 Computatiom Graph 会详细描述
