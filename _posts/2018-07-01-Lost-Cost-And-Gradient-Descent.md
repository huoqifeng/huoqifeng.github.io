本系列关于AI/DeepLearning的大部分资料来源于Andrew NG在Coursera的讲课本内容，  
希望系统学习的同学请自行在Coursera注册学习或旁听： https://www.coursera.org  

要计算W,b就需要不停的迭代，知道满意为止，什么是满意呢？就是Lost, Cost都比较低的时候，经常采用的方法呢就是Gradient Descent
今天我们就来看Lost, Cost和Gradient Descent。

## 什么是Lost 和 Cost
![img](https://huoqifeng.github.io/img/deeplearning/lost-cost.png)
 - Lost 是一个样例上的偏差（损失）
 - Cost 是所有m个样例的偏差

## 什么是Gradient Descent
![img](https://huoqifeng.github.io/img/deeplearning/gradient-descent.png)
 - Gradient Descent 是要找到上升或者下降最快的方向，也就是导数

## 如何实现Gradient Descent
![img](https://huoqifeng.github.io/img/deeplearning/implement-gradient-descent.png)
 - 在实现Gradient Descent的时候要计算dw, db,后面讲完Computing Graph会详细描述
