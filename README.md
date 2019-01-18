# 记录DeepLearning学习过程

## Learning

#### CNN学习过程

- [变形卷积核、可分离卷积？卷积神经网络中十大拍案叫绝的操作。](https://zhuanlan.zhihu.com/p/28749411)



### DL-常见模型讲解及实现

##### paper讲解

- B 站视频：[深度学习顶级论文算法详解](https://www.bilibili.com/video/av30271782?from=search&seid=9462295319719088186)（含 Faster-RCNN、ResNet 论文讲解）



##### ResNet

(1) 讲解

- [深度残差网络（ResNet）](https://ylhao.github.io/2018/05/25/%E6%AE%8B%E5%B7%AE%E7%BD%91%E7%BB%9C%EF%BC%88ResNet%EF%BC%89/)

(2) 实践

- 代码：[chaipangpang/ResNet_cifar](https://github.com/chaipangpang/ResNet_cifar)
- ResNet 代码讲解：
  - [理解ResNet结构与TensorFlow代码分析](https://blog.csdn.net/chaipp0607/article/details/75577305)
  - [TF官方的ResNet代码详解](https://zhuanlan.zhihu.com/p/32194105)

关于残差连接：[resnet中的残差连接，你确定真的看懂了？](https://zhuanlan.zhihu.com/p/42833949)

更多内容请看我单独写的一个文档：[ResNet(残差网络).md](./papers-reading/经典神经网络模型解读/ResNet(残差网络).md)

### Semantic segmentation(语义分割)

#### semseg-Aticles

传统分割方法：[图像分割 传统方法 整理](https://zhuanlan.zhihu.com/p/30732385)

> 图片分割根据灰度、颜色、纹理、和形状等特征将图像进行划分区域，让区域间显差异性，区域内呈相似性。主要分割方法有：
>
> - 基于阈值的分割
> - 基于边缘的分割
> - 基于区域的分割
> - 基于图论的分割
> - 基于能量泛函的分割

还不懂什么是语义分割，先看这篇文章：[十分钟看懂图像语义分割技术](https://www.leiphone.com/news/201705/YbRHBVIjhqVBP0X5.html)

(1) 综述类/总结类：

- [从全连接层到大型卷积核：深度学习语义分割全指南](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728920&idx=4&sn=3c51fa0a95742d37222c3e16b77267ca&scene=21#wechat_redirect)

- [分割算法——可以分割一切目标（各种分割总结）](https://mp.weixin.qq.com/s/KcVKKsAyz-eVsyWR0Y812A)

  > 第一种是**编码-译码架构**。编码过程通过池化层逐渐减少位置信息、抽取抽象特征；译码过程逐渐恢复位置信息。一般译码与编码间有直接的连接。该类架构中 U-net 是最流行的。
  >
  > 第二种是**膨胀卷积** (dilated convolutions) 【这个核心技术值得去阅读学习】，抛弃了池化层。

- [一文概览主要语义分割网络：FCN,SegNet,U-Net...](https://www.tinymind.cn/articles/410)

  > 该文为译文，介绍了很多语义分割的深度学习模型，包括半监督下的语义分割，可以大致看下。

(2) 深度学习语义分割模型的介绍：

- [语义分割(semantic segmentation) 常用神经网络介绍对比-FCN SegNet U-net DeconvNet](https://blog.csdn.net/zhyj3038/article/details/71195262)
- [深度学习（十九）——FCN, SegNet, DeconvNet, DeepLab, ENet, GCN](https://blog.csdn.net/antkillerfarm/article/details/79524417)

图像分割的衡量指标：

- [图像分割的衡量指标详解](https://blog.csdn.net/qq_37274615/article/details/78957962)

语义分割其实就是对图片的每个像素都做分类。其中，较为重要的语义分割数据集有：VOC2012 以及 MSCOCO。

#### semseg-Repositories

- [semseg](https://github.com/guanfuchen/semseg)

  > 常用的语义分割架构结构综述以及代码复现

- [DeepNetModel](https://github.com/guanfuchen/DeepNetModel)

  > 记录每一个常用的深度模型结构的特点（图和代码）
  >
  > 大佬的博客：[计算机视觉相关资源整理](https://guanfuchen.github.io/post/markdown_blog_ws/markdown_blog_2017_11/%E8%AE%A1%E7%AE%97%E6%9C%BA%E8%A7%86%E8%A7%89%E7%9B%B8%E5%85%B3%E8%B5%84%E6%BA%90%E6%95%B4%E7%90%86/)

- [Semantic-Segmentation-Suite](https://github.com/GeorgeSeif/Semantic-Segmentation-Suite)

  > Semantic Segmentation Suite in TensorFlow. Implement, train, and test new Semantic Segmentation models easily!

#### semseg-Papers

论文汇集：

- [语义分割 - Semantic Segmentation Papers](https://blog.csdn.net/zziahgf/article/details/72639791)



#### semseg-Videos

- [浙大博士生刘汉唐：带你回顾图像分割的经典算法](http://www.mooc.ai/course/414/learn#lesson/2266)（需要注册才能观看）

遥感图像分割：

- [197期\_张觅\_基于深度卷积网络的遥感影像语义分割层次认知方法](https://www.bilibili.com/video/av24599502?from=search&seid=11210211322309323243)




### Reinforce Learning(强化学习/增强学习)

#### RL-Articles

- 雷锋网：[深度学习新星：GAN的基本原理、应用和走向](https://www.leiphone.com/news/201701/Kq6FvnjgbKK8Lh8N.html)



## Questions





Competition
===

Kaggle：https://www.kaggle.com/

天池AI开发者社区：https://tianchi.aliyun.com/home/



## Papers-download-links







## Resources

### Articles

- 阮一峰：[神经网络入门](http://www.ruanyifeng.com/blog/2017/07/neural-network.html)
- 阮一峰：[如何识别图像边缘](http://www.ruanyifeng.com/blog/2016/07/edge-recognition.html)
- hanbingtao 《零基础入门深度学习》系列文章：https://www.zybuluo.com/hanbingtao/note/433855
- Charlotte77：[【深度学习系列】卷积神经网络CNN原理详解(一)——基本原理](https://www.cnblogs.com/charlotte77/p/7759802.html)
- Charlotte77：[一文弄懂神经网络中的反向传播法——BackPropagation](https://www.cnblogs.com/charlotte77/p/5629865.html )

（updating…）

### Books

这几年，关于人工智能、机器学习、深度学习的书如雨后春笋般，真的很多。下面列举一些大家普遍评价很高以及我有大概浏览过觉得不错的书，当个参考和记录：

1、机器学习

- 周志华《机器学习》2016年1月
- 译书：《机器学习实战》2013年6月

2、深度学习

- Michael Nielsen[《Neural Networks and Deep Learning》](http://neuralnetworksanddeeplearning.com/index.html)，中文版《神经网络与深度学习》
- 中文译本：《Python深度学习》2018年8月
- 张玉宏《深度学习之美：AI时代的数据处理与最佳实践》2018年6月

3、深度学习框架

- 泽宇/顾思宇 《Tensorflow：实战Google深度学习框架》
- 黄文坚/唐源《TensorFlow实战》
- 廖星宇《深度学习入门之PyTorch》 [[代码仓库]](https://github.com/L1aoXingyu/code-of-learn-deep-learning-with-pytorch)
- 陈云《深度学习框架PyTorch：入门与实践》 [[代码仓库]](https://github.com/chenyuntc/pytorch-book)

### Videos

- [Video]偏科普入门，莫烦机器学习教程：<https://morvanzhou.github.io/tutorials/machine-learning/>
- [Video]适合入门，吴恩达机器学习课程：<https://www.coursera.org/learn/machine-learning>、或 B 站：<https://www.bilibili.com/video/av9912938/>
- [Video]吴恩达深度学习课程：<https://mooc.study.163.com/smartSpec/detail/1001319001.htm>（中英文字幕）
- [Video]林轩田《机器学习基石》，B 站观看：<https://www.bilibili.com/video/av1624332>
- [Video]林轩田《机器学习技法》，B 站观看：<https://www.bilibili.com/video/av12469267/>
- [Video]李宏毅《一天搞懂深度学习》，B 站观看：<https://www.bilibili.com/video/av16543434/>
- [Video]李宏毅_机器学习，B 站观看：<https://www.bilibili.com/video/av10590361/>
- [Video]李宏毅_深度学习，B 站观看：<https://www.bilibili.com/video/av9770302/>
- [Video]深度学习计算机视觉课程，李飞飞_斯坦福 CS231n 课程，B 站观看：<https://www.bilibili.com/video/av13260183/>（中文字幕）
- [Videos]李沐《动手学深度学习》：<https://space.bilibili.com/209599371>，GitHub地址：<https://github.com/diveintodeeplearning/d2l-zh>


### GitHub-Repositories

- [DeepLearning-500-questions](https://github.com/scutan90/DeepLearning-500-questions)

  > 深度学习500问，以问答形式对常用的概率知识、线性代数、机器学习、深度学习、计算机视觉等热点问题进行阐述，以帮助自己及有需要的读者。 全书分为15个章节，近20万字。由于水平有限，书中不妥之处恳请广大读者批评指正。 未完待续...

- 吴恩达的机器学习&深度学习课程笔记：http://www.ai-start.com/

  > 本网站是一个公益性网站，致力于人工智能（AI）方面的课程的翻译、笔记分享等。
  >
  > 本人2014年下半年开始翻译吴恩达老师的机器学习课程字幕，并写了课程的中文笔记。笔记被下载了几万次，应该帮助了不少人，也有很多人一直在帮助我，现在我把笔记的word原稿和markdown原稿分享给大家。
  >
  > ……
  >
  > ——By 黄海广

- [daily-paper-computer-vision](https://github.com/amusi/daily-paper-computer-vision)

  > 记录每天整理的计算机视觉/深度学习/机器学习相关方向的论文。



<div align="right">
    <a href="#记录DeepLearning学习过程">回到顶部</a>
</div>











