本系列关于AI/DeepLearning的大部分资料来源于Andrew NG在Coursera的讲课本内容，  
希望系统学习的同学请自行在Coursera注册学习或旁听： https://www.coursera.org  

机器学习的问题可以归结为识别问题，识别其实就是归结为分类问题，分类又分为是否的二分类和多对象的分类。
我们从二分类Binary Classification来开始我们的学习，多分类的问题只是在输出用Softmax替代Sigmoid,会在以后的文章提到。
Binary Classification是一个True/False问题，比如对于一个图片，图片中的是不是一只猫，对于一个邮件，是不是对你很重要等等。
以下图来说：

![img](https://github.com/huoqifeng/huoqifeng.github.io/blob/master/img/deeplearning/binary-classification.png)


 - 每一个图片都是一个64x64像素的图
 - 每一个像素都可以分解成R,G,B三基色，三个Channel。
 - 那么特征向量X就是64x64x3 = 12288
 - 对应的Y，可能是Cat(1),不是Cat(0)
 
在Binary Classification中用的Notation如下图：
![img](https://github.com/huoqifeng/huoqifeng.github.io/blob/master/img/deeplearning/notation-binary-classification.png) 
 - 对于每一个数据样本（x,y）,x是一个n维向量，n是特征数，y是0或1
 - m是样本数量
 - 总的样本的特征X 是m列的矩阵，每一列是一个样本的特征向量
 - 总的样本的Y也是一个m列的矩阵，每一列是一个1维向量，[0] 或 [1]
 

那么机器学习就是要通过对m个样例的分析和学习，得到一个模型（Model）,对于新的图片，应用这个模型来判断，新的图片是不是一只猫（1或者0）。
Logistic Regression就是这样的一种算法，基本的算法就是给每一个特征分配一个权重w，这样W就是一个n维的向量，n是特征的数量，
算法通过学习（迭代）得到W,那么对新的图片应用W就可以得到预测值，下面是Logistic Regression用到的Notation:
![img](https://github.com/huoqifeng/huoqifeng.github.io/blob/master/img/deeplearning/notation-logistic-regression.png)  
 - 需要注意的是常数b，是一个正则化因子，后面的文章会提到
 - W是一个n维向量，由样例通过迭代得到。
 - W + b 就是Model
 - 因为通过W,b计算的结果并不是1,0， 所以要应用一个Sigmoid 函数，使得计算结果在0,1之间
 - 后面会有讲到，W,b计算的直接结果是Z，应用Sigmoid函数之后的结果记为A，Sigmiod函数叫做Activation函数