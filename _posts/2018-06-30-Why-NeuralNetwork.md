本系列关于AI/DeepLearning的大部分资料来源于Andrew NG在Coursera的讲课本内容，  
希望系统学习的同学请自行在Coursera注册学习或旁听： https://www.coursera.org  

在AI盛行的今天，DeepLearning和Neural Network几乎可以说是Machine Learning的代名词，  
尽管机器学习涵盖很多的领域，比如KNN, SVM,为什么NN占据了统治地位呢？下面Andrew NG的这张图可以说的很明白：  


![img](https://huoqifeng.github.io/img/deeplearning/scale-drive-nn.png)


 - 当数据集比较小的时候，传统机器学习的结果和NN的结果是差不多的
 - 当数据集逐渐增加，传统机器学习的结果达到一个平台，而NN还有提升的空间
 - 当数据集再增加，小规模的NN逐渐达到一个平台，而中等规模和大规模的NN还有提升空间
 - 数据集还在增加，中等规模的NN的结果也会达到一个平台，而大规模的NN还能有比较好的提高
 - 随着数据的增加，超大规模的NN可以带来巨大的performance的提升，当然，这个是以现代计算机的计算能力为基础的

总结起来，DeepLearning 和 Neural Network近几年大规模的流行和应用依赖两个条件：
 - 大规模的数据
 - 飞快提升的计算能力 