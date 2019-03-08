# 记录DeepLearning学习过程

## 目录

<!-- TOC -->

- [1. Learning](#1-Learning)
- [2. Questions](#2-Questions)
- [3. Competition](#3-Competition)
- [4. Papers](#4-Papers)
- [5. Interview](#5-Interview)
- [6. Resources](#6-Resources)
- [7. Thinking](#7-Thinking)
- [Journals](#Journals)

<!-- /TOC -->

👉 推荐该系列文章：[关于神经网络模型&TensorFlow学习&目标检测模型等内容的系列文章.md](./Notes/关于神经网络模型&TensorFlow学习&目标检测模型等内容的系列文章.md)

:point_right: 关于图像分割（Image segmentation，含语义/实例/场景分割）的学习见：[图像分割专题](./Notes/images-segmentation/README.md)  &&  本文 [1.3 语义/实例/场景分割(Images segmentation)](#13-语义实例场景分割images-segmentation) 节内容~

- 语义/实例/场景分割 paper 以及代码实现见本文：[4.3 Images segmentation](#43-images-segmentation) 节
- 这里顺带插播下关于弱监督下的语义分割的研究和工作：[JackieZhangdx/WeakSupervisedSegmentationList](https://github.com/JackieZhangdx/WeakSupervisedSegmentationList)

👉 这里记录一些在学习过程的要点梳理和个人理解：[深度学习要点梳理和个人理解](./Notes/keypoints/README.md)  [推荐]

:point_right: 深度学习之框架学习，传送门：

- [tensorflow-learning](https://github.com/strivebo/tensorflow-learning)
- [pytorch-learning](https://github.com/strivebo/pytorch-learning)

:point_right: 关于目标检测（Object Detection）的学习见：[目标检测专题](./Notes/object-detection/README.md)

---

人工智能最新学术研究和技术实现追寻，可关注：

- [量子位 - 知乎 - 专栏](https://zhuanlan.zhihu.com/qbitai)
- [机器之心 - 知乎 - 专栏](https://zhuanlan.zhihu.com/jiqizhixin)
- [计算机视觉论文速递 - 知乎 - 专栏](https://zhuanlan.zhihu.com/c_172507674)
- [PaperWeekly - 知乎 - 专栏](https://zhuanlan.zhihu.com/paperweekly)
- [计算机视觉life - 知乎 - 专栏](https://zhuanlan.zhihu.com/c_150246914)
- ……

---

领域人物及事迹，了解下：

- 孙剑、何恺明：
  - [谁说高考状元高分低能，24岁时以去雾算法一举成名](https://baike.baidu.com/tashuo/browse/content?id=84a16c8986a54a4bf83ddebc)
- ……

## 1. Learning

### 1.1 深度学习基础

科普文章：

- [推荐 | 机器学习经典总结，入门必读【17000字，可下载PDF】](https://mp.weixin.qq.com/s?__biz=MzIxODM4MjA5MA==&mid=2247485716&idx=1&sn=5b182c1c0b6578b1b1f3b75878ec1364&chksm=97ea2371a09daa6713afbe506d2bc40a7b2062be151c58425cefabf6cb3c41de37e9f51fdb0b&mpshare=1&scene=1&srcid=1209sLVUbZIHaCnoa9sLlfZ4#rd)
- [一图看懂| 人工智能知识体系大全](https://mp.weixin.qq.com/s?__biz=MzU2MDc1MjEyMQ==&mid=2247486182&amp;idx=1&amp;sn=6174593f5862193e98cda311022aeb94&source=41#wechat_redirect)
- [云计算、大数据和人工智能这么火，究竟是什么关系？](https://mp.weixin.qq.com/s?__biz=MzU2MDc1MjEyMQ==&mid=2247486185&amp;idx=1&amp;sn=0690fac9da75b1ea9f44c4f79df461a9&source=41#wechat_redirect)

机器学习：

- [机器学习中常见4种学习方法、13种算法和27张速查表！](https://cloud.tencent.com/developer/article/1029070)

深度学习：

- 阮一峰：[神经网络入门](http://www.ruanyifeng.com/blog/2017/07/neural-network.html)
- 阮一峰：[如何识别图像边缘](http://www.ruanyifeng.com/blog/2016/07/edge-recognition.html)
- Charlotte77：[【深度学习系列】卷积神经网络CNN原理详解(一)——基本原理](https://www.cnblogs.com/charlotte77/p/7759802.html)
- Charlotte77：[一文弄懂神经网络中的反向传播法——BackPropagation](https://www.cnblogs.com/charlotte77/p/5629865.html )

深度学习系列文章：

- MachineLP：[MachineLP博客目录](https://blog.csdn.net/u014365862/article/details/78422372)
- hanbingtao：[《零基础入门深度学习》系列文章](https://www.zybuluo.com/hanbingtao/note/433855)

其他文章：

- [变形卷积核、可分离卷积？卷积神经网络中十大拍案叫绝的操作。](https://zhuanlan.zhihu.com/p/28749411)

### 1.2 常见模型的讲解及实现

#### (0) Paper讲解

- B 站视频：[深度学习顶级论文算法详解](https://www.bilibili.com/video/av30271782?from=search&seid=9462295319719088186)（含 Faster-RCNN、ResNet 论文讲解）

#### (1) ResNet

讲解

- [深度残差网络（ResNet）](https://ylhao.github.io/2018/05/25/%E6%AE%8B%E5%B7%AE%E7%BD%91%E7%BB%9C%EF%BC%88ResNet%EF%BC%89/)

实践

- 代码：[chaipangpang/ResNet_cifar](https://github.com/chaipangpang/ResNet_cifar)
- ResNet 代码讲解：
  - [理解ResNet结构与TensorFlow代码分析](https://blog.csdn.net/chaipp0607/article/details/75577305)
  - [TF官方的ResNet代码详解](https://zhuanlan.zhihu.com/p/32194105)

关于残差连接：[resnet中的残差连接，你确定真的看懂了？](https://zhuanlan.zhihu.com/p/42833949)

更多内容请看我单独写的一个文档：[ResNet(残差网络).md](./papers-reading/经典神经网络模型解读/ResNet(残差网络).md)

### 1.3 语义/实例/场景分割(Images segmentation)

#### (1) 图像分割基础

①什么是图像分割？

- [图像分割 传统方法 整理](https://zhuanlan.zhihu.com/p/30732385)  [荐看完]

  图片分割根据灰度、颜色、纹理、和形状等特征将图像进行划分区域，让区域间显差异性，区域内呈相似性。主要分割方法有：

  ``` xml
  基于阈值的分割
  基于边缘的分割
  基于区域的分割
  基于图论的分割
  基于能量泛函的分割
  ```

- [十分钟看懂图像语义分割技术 | 雷锋网](https://www.leiphone.com/news/201705/YbRHBVIjhqVBP0X5.html)  [荐看完]

②综述类/总结类：

- [从全连接层到大型卷积核：深度学习语义分割全指南](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728920&idx=4&sn=3c51fa0a95742d37222c3e16b77267ca&scene=21#wechat_redirect)

- [分割算法——可以分割一切目标（各种分割总结）](https://mp.weixin.qq.com/s/KcVKKsAyz-eVsyWR0Y812A)  [荐]

  深度学习最初流行的分割方法是，打补丁式的分类方法 (patch classification) 。逐像素地抽取周围像素对中心像素进行分类。由于当时的卷积网络末端都使用全连接层 (full connected layers) ，所以只能使用这种逐像素的分割方法。

  但是到了 2014 年，来自伯克利的 Fully Convolutional Networks（FCN）卷积网络，去掉了末端的全连接层。随后的语义分割模型基本上都采用了这种结构。除了全连接层，语义分割另一个重要的问题是池化层。池化层能进一步提取抽象特征增加感受域，但是丢弃了像素的位置信息。但是语义分割需要类别标签和原图像对齐，因此需要从新引入像素的位置信息。有两种不同的架构可以解决此像素定位问题。

  第一种是`编码-译码架构`。编码过程通过池化层逐渐减少位置信息、抽取抽象特征；译码过程逐渐恢复位置信息。一般译码与编码间有直接的连接。该类架构中 U-net 是最流行的。

  第二种是`膨胀卷积` (dilated convolutions) 【这个核心技术值得去阅读学习】，抛弃了池化层。

- [一文概览主要语义分割网络：FCN,SegNet,U-Net...](https://www.tinymind.cn/articles/410)

  该文为译文，介绍了很多语义分割的深度学习模型，包括半监督下的语义分割，可以大致看下。

③深度学习语义分割模型的介绍：

- [语义分割(semantic segmentation) 常用神经网络介绍对比-FCN SegNet U-net DeconvNet](https://blog.csdn.net/zhyj3038/article/details/71195262)
- [深度学习（十九）——FCN, SegNet, DeconvNet, DeepLab, ENet, GCN](https://blog.csdn.net/antkillerfarm/article/details/79524417)

④图像分割的衡量指标：

- [图像分割的衡量指标详解](https://blog.csdn.net/qq_37274615/article/details/78957962)

语义分割其实就是对图片的每个像素都做分类。其中，较为重要的语义分割数据集有：VOC2012 以及 MSCOCO。

#### (2) 图像分割仓库

- [semseg](https://github.com/guanfuchen/semseg)

  > 常用的语义分割架构结构综述以及代码复现

- [DeepNetModel](https://github.com/guanfuchen/DeepNetModel)

  > 记录每一个常用的深度模型结构的特点（图和代码）
  >
  > 大佬的博客：[计算机视觉相关资源整理](https://guanfuchen.github.io/post/markdown_blog_ws/markdown_blog_2017_11/%E8%AE%A1%E7%AE%97%E6%9C%BA%E8%A7%86%E8%A7%89%E7%9B%B8%E5%85%B3%E8%B5%84%E6%BA%90%E6%95%B4%E7%90%86/)

- [Semantic-Segmentation-Suite](https://github.com/GeorgeSeif/Semantic-Segmentation-Suite)

  > Semantic Segmentation Suite in TensorFlow. Implement, train, and test new Semantic Segmentation models easily!

- [mrgloom/awesome-semantic-segmentation](https://github.com/mrgloom/awesome-semantic-segmentation)（图像分割论文下载及实现可以在这里找到~）

#### (3) 图像分割论文及最新研究

论文汇集：

- [语义分割 - Semantic Segmentation Papers](https://blog.csdn.net/zziahgf/article/details/72639791)



#### (4) 图像分割讲解视频

- [浙大博士生刘汉唐：带你回顾图像分割的经典算法](http://www.mooc.ai/course/414/learn#lesson/2266)（需要注册才能观看~）
- [197期\_张觅\_基于深度卷积网络的遥感影像语义分割层次认知方法](https://www.bilibili.com/video/av24599502?from=search&seid=11210211322309323243)（关于遥感图像语义分割的，但听得不是很清楚~）

### 1.4 目标检测(Object Detection)

（待更……）


### 1.5 强化学习/增强学习(Reinforce Learning)

#### (1) 基础

- 雷锋网：[深度学习新星：GAN的基本原理、应用和走向](https://www.leiphone.com/news/201701/Kq6FvnjgbKK8Lh8N.html)



## 2. Questions

（1）如何免费云端运行 Python 深度学习框架：[如何在免费云端运行 Python 深度学习框架？-红色石头的个人博客](http://redstonewill.com/1493/?tdsourcetag=s_pcqq_aiomsg)

（2）什么学习中网络不收敛指的是什么？——①误差一直来回波动，进入不到容忍度内。②跟迭代不收敛或者系统不稳定差不多，上下波动不能趋近一个定值。



## 3. Competition

(1) Kaggle官网：https://www.kaggle.com/

(2) 天池AI开发者社区：https://tianchi.aliyun.com/home/



## 4. Papers

### 4.1 Basic

- 《A guide to convolution arithmetic for deep》[[Paper](https://arxiv.org/abs/1603.07285)]
- 《Bag of Tricks for Image Classification with Convolutional Neural Networks》[[Paper](https://arxiv.org/abs/1812.01187)]
- （待更。。。

### 4.2 Models

- [1989] LeNet：《Gradient-Based Learning Applied to document Recognition》[[Paper](http://vision.stanford.edu/cs598_spring07/papers/Lecun98.pdf)]
- [2012] AlexNet：《ImageNet Classification with Deep Convolutional
  Neural Networks》[[Paper](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)]
- [2014] Inception v1：《Going deeper with convolutions》[[Paper](https://arxiv.org/abs/1409.4842)]

  注：先前叫 GoogLeNet，现在简单地被称为 Inception vN，其中 N 指的是由 Google 定的版本号。
- [2014] VGGNet：《Very Deep Convolutional Networks for Large-Scale Image Recognition》[[Paper](https://arxiv.org/abs/1409.1556v6)]
- [2015] Inception v2：《Batch Normalization Accelerating Deep Network Training by Reducing Internal Covariate Shift》[[Paper](https://arxiv.org/abs/1502.03167)]
- [2015] Inception v3：《Rethinking the Inception Architecture for Computer Vision》[[Paper](https://arxiv.org/abs/1512.00567)]
- [2015] ResNet：《Deep Residual Learning for Image Recognition》[[Paper](https://arxiv.org/abs/1512.03385)]
- [2016] Inception v4：《Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning》[[Paper](https://arxiv.org/abs/1602.07261)]

### 4.3 Images segmentation

- **FCN：**《Fully Convolutional Networks for Semantic Segmentation》 [[Paper-v1](https://arxiv.org/abs/1411.4038v1)]  [[Paper-v2](https://arxiv.org/abs/1411.4038v2)]（最新提交时间：2015.03.08）	
- **U-Net：**《U-Net: Convolutional Networks for Biomedical Image Segmentation》[[Paper](https://arxiv.org/abs/1505.04597)]（最新提交时间：2015.05.18）
- **SegNet：**《SegNet: A Deep Convolutional Encoder-Decoder Architecture for Image Segmentation》[[Paper-v1](https://arxiv.org/abs/1511.00561v1)]  [[Paper-v2](https://arxiv.org/abs/1511.00561v2)]  [[Paper-v3](https://arxiv.org/abs/1511.00561v3)]（最新提交时间：2016.11.10）
- Dilated Convolutions：《Multi-Scale Context Aggregation by Dilated Convolutions》[[Paper-v1](https://arxiv.org/abs/1511.07122v1)]  [[Paper-v2](https://arxiv.org/abs/1511.07122v2)]  [[Paper-v3](https://arxiv.org/abs/1511.07122v3)]（最新提交时间：2016.04.30）
- DeconvNet：《Learning Deconvolution Network for Semantic Segmentation》[[Paper](https://arxiv.org/abs/1505.04366)]（最新提交时间：2015.05.17）
- RefineNet：《RefineNet: Multi-Path Refinement Networks for High-Resolution Semantic Segmentation》[[Paper-v1](https://arxiv.org/abs/1611.06612v1)]  [[Paper-v2](https://arxiv.org/abs/1611.06612v2)]  [[Paper-v3](https://arxiv.org/abs/1611.06612v3)]（最新提交时间：2016.11.25）
- PSPNet：《Pyramid Scene Parsing Network》[[Paper-v1](https://arxiv.org/abs/1612.01105v1)]  [[Paper-v2](https://arxiv.org/abs/1612.01105v2)]（最新提交时间：2017.04.27）
- Large Kernel Matters：《Large Kernel Matters -- Improve Semantic Segmentation by Global Convolutional Network》[[Paper](https://arxiv.org/abs/1703.02719)]（最新提交时间：2017.03.08）
- **DeepLab 系列：** 
  - DeepLab v1：《Semantic Image Segmentation with Deep Convolutional Nets and Fully Connected CRFs》[[Paper-v1](https://arxiv.org/abs/1412.7062v1)]  [[Paper-v2](https://arxiv.org/abs/1412.7062v2)]  [[Paper-v3](https://arxiv.org/abs/1412.7062v3)]  [[Paper-v4](https://arxiv.org/abs/1412.7062v4)]（最新提交时间 ：2016.06.07）
  - DeepLab v2：《DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs》[[Paper-v1](https://arxiv.org/abs/1606.00915v1)]  [[Paper-v2](https://arxiv.org/abs/1606.00915v2)]（最新提交时间：2017.05.12）
  - DeepLab v3：《Rethinking Atrous Convolution for Semantic Image Segmentation》[[Paper-v1](https://arxiv.org/abs/1706.05587v1)]  [[Paper-v2](https://arxiv.org/abs/1706.05587v2)]  [[Paper-v3](https://arxiv.org/abs/1706.05587v3)]（最新提交时间：2017.12.05）
  - DeepLab v3+：《Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation》[[Paper-v1](https://arxiv.org/abs/1802.02611v1)] [[Paper-v2](https://arxiv.org/abs/1802.02611v2)] [[Paper-v3](https://arxiv.org/abs/1802.02611v3)]（最新提交时间：2018.08.22）
- NAS：《Searching for Efficient Multi-Scale Architectures for Dense Image Prediction》[[Paper-v1](https://arxiv.org/abs/1809.04184)]（提交时间：2018.09.11） 相关文章：[语义分割领域开山之作：Google提出用神经网络搜索实现语义分割 | 雷锋网](https://www.leiphone.com/news/201810/hPe93A6N0YSQPF7y.html)
- （待更。。。

语义分割类的论文合集：

- [语义分割 - Semantic Segmentation Papers - CSDN博客](https://blog.csdn.net/zziahgf/article/details/72639791) | [语义分割 - Semantic Segmentation Papers - AIUAI](https://www.aiuai.cn/aifarm62.html)  | [分类 语义分割 下的文章 - AIUAI](https://www.aiuai.cn/category/segmentation/)
- [Segmentation - handong1587](https://handong1587.github.io/deep_learning/2015/10/09/segmentation.html)

关于图像分割的代码实现，见：[2-图像分割仓库](#2-图像分割仓库)

- [mrgloom/awesome-semantic-segmentation](https://github.com/mrgloom/awesome-semantic-segmentation)（图像分割论文下载及实现可以在这里找到~）
- [GeorgeSeif/Semantic-Segmentation-Suite](https://github.com/GeorgeSeif/Semantic-Segmentation-Suite)
- [guanfuchen/semseg](https://github.com/guanfuchen/semseg)
- [AstarLight/Satellite-Segmentation](https://github.com/AstarLight/Satellite-Segmentation)
- （待补充…

一些新的研究：

- [学界 | 上海交大卢策吾团队开源PointSIFT刷新点云语义分割记录](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650745253&idx=5&sn=05ff84805817d2d2a61a36a313d6cff8&chksm=871aeddbb06d64cdd93ff5b62a169084c0f3ed9e2395415e1d435c28f7168e4deb69102c1fa7&mpshare=1&scene=23&srcid=0721mm9a22Lw3RJZvLkWRbZb#rd)

### 4.4 Object Detection

- R-CNN：《Rich feature hierarchies for accurate object detection and semantic segmentation》[[Paper](https://arxiv.org/abs/1311.2524)]
- Fast R-CNN：《Fast R-CNN》 [[Paper](https://arxiv.org/abs/1504.08083)]
- Faster R-CNN：《Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks》 [[Paper](https://arxiv.org/abs/1506.01497)]
- Yolo
- SSD
- Mask R-CNN ：《Mask R-CNN》 [[Paper](https://arxiv.org/abs/1703.06870)]

一些新的研究：

- [优于Mask R-CNN，港中文&腾讯优图提出PANet实例分割框架](https://www.jiqizhixin.com/articles/2018-03-12-6)

### 4.5 Others



## 5. Interview

- 陈恩加：[自己整理的一点和深度学习相关的面试考点 - 知乎](https://zhuanlan.zhihu.com/p/48374690)
- 


## 6. Resources

### 6.1 Books

这两年关于人工智能特别是深度学习的书如雨后春笋很多。下面列举一些被大家普遍评价较高以及我有大概浏览过觉得不错的书，当个参考和记录：

**1.机器学习**

- 《写给人类的机器学习》译者：[飞龙](https://github.com/wizardforcel)（等）；原书：[Machine Learning for Humans](https://medium.com/machine-learning-for-humans/)
- 周志华《机器学习》，2016年1月
- Peter Harrington 《机器学习实战》，中文版译者：李锐/李鹏/曲亚东/王斌 ，2013年6月  [[GitHub代码仓库](https://github.com/pbharrin/machinelearninginaction)]

**2.深度学习**

- Michael Nielsen[《Neural Networks and Deep Learning》](http://neuralnetworksanddeeplearning.com/index.html)，中文版《神经网络与深度学习》
- 弗朗索瓦•肖莱 《Python深度学习》，中文版译者：张亮，2018年8月  
- 张玉宏《深度学习之美：AI时代的数据处理与最佳实践》，2018年6月
- 张平《图解深度学习与神经网络：从张量到TensorFlow实现》，2018年09月
- 李沐、Aston Zhang 等人《动手学深度学习》预览版：[《动手学深度学习》](https://zh.d2l.ai/)
- 邱锡鹏《神经网络与深度学习》：[在线阅读](https://nndl.github.io/)

**3.深度学习框架** 

- 泽宇/顾思宇 《Tensorflow：实战Google深度学习框架》
- 黄文坚/唐源《TensorFlow实战》
- 廖星宇《深度学习入门之PyTorch》 [[代码仓库](https://github.com/L1aoXingyu/code-of-learn-deep-learning-with-pytorch)]
- 陈云《深度学习框架PyTorch：入门与实践》 [[代码仓库](https://github.com/chenyuntc/pytorch-book)]

### 6.2 Videos

- [Video]偏科普入门，莫烦机器学习教程：<https://morvanzhou.github.io/tutorials/machine-learning/>
- [Video]适合入门，吴恩达机器学习课程：<https://www.coursera.org/learn/machine-learning>、或 B 站：<https://www.bilibili.com/video/av9912938/>
- [Video]吴恩达深度学习课程：<https://mooc.study.163.com/smartSpec/detail/1001319001.htm>（中英文字幕）
- [Video]林轩田《机器学习基石》，B 站观看：<https://www.bilibili.com/video/av1624332>
- [Video]林轩田《机器学习技法》，B 站观看：<https://www.bilibili.com/video/av12469267/>
- [Video]李宏毅《一天搞懂深度学习》，B 站观看：<https://www.bilibili.com/video/av16543434/>
- [Video]李宏毅_机器学习，B 站观看：<https://www.bilibili.com/video/av10590361/>
- [Video]李宏毅_深度学习，B 站观看：<https://www.bilibili.com/video/av9770302/>
- [Video]深度学习计算机视觉课程，李飞飞_斯坦福 CS231n 课程，B 站观看：<https://www.bilibili.com/video/av13260183/>（中文字幕）
- [Videos]李沐《动手学深度学习》：<https://space.bilibili.com/209599371/channel/detail?cid=23541>，书籍预览版：[《动手学深度学习》](https://zh.d2l.ai/)，代码GitHub地址：[d2l-ai/d2l-zh](https://github.com/d2l-ai/d2l-zh)

### 6.3 GitHub

- [apachecn/AiLearning](https://github.com/apachecn/AiLearning)

- [DeepLearning-500-questions](https://github.com/scutan90/DeepLearning-500-questions)

  深度学习500问，以问答形式对常用的概率知识、线性代数、机器学习、深度学习、计算机视觉等热点问题进行阐述，以帮助自己及有需要的读者。 全书分为15个章节，近20万字。由于水平有限，书中不妥之处恳请广大读者批评指正。 未完待续...

- [AI初学者--（机器学习爱好者）](http://www.ai-start.com/)

  本网站是一个公益性网站，致力于人工智能（AI）方面的课程的翻译、笔记分享等。

  本人2014年下半年开始翻译吴恩达老师的机器学习课程字幕，并写了课程的中文笔记。笔记被下载了几万次，应该帮助了不少人，也有很多人一直在帮助我，现在我把笔记的word原稿和markdown原稿分享给大家。

  …… ——By 黄海广

- [daily-paper-computer-vision](https://github.com/amusi/daily-paper-computer-vision)

  记录每天整理的计算机视觉/深度学习/机器学习相关方向的论文。

## 7. Thinking

- [周志华：关于机器学习的一点思考](https://mp.weixin.qq.com/s/sEZM_o5D6AhyMgvocbsFhw)（周老师的观点客观诚恳~）
- [你知道为什么说深度学习是这时代的炼金术吗？](https://mp.weixin.qq.com/s/y3KqZi68uoWnW_VHV-dtTg)
- [关于对人工智能的思考和看法随记.md](./Notes/关于对人工智能的思考和看法随记.md)



## Journals

对期刊和会议的认识：

- [论文收录平台 ( SCI、EI 等 ) 详细说明 | jiyiren](https://jiyiren.github.io/2017/11/18/papersci/)
- [SCI、EI、核心期刊 这些东西等级是怎么区分的？ - 知乎](https://www.zhihu.com/question/31558495)
- [SCI索引、SCI-E索引、SSCI和EI索引的区别，期刊验证查询 | 数据学习（DataLearner）](https://www.datalearner.com/journal_confirm)
- [计算机学术期刊、会议分类等级 - 小白 - CSDN博客](https://blog.csdn.net/zhouxinxin0202/article/details/79489977)

计算机视觉方向（CV）三大顶级会议：

- ICCV（IEEE International Conference on Computer Vision，国际计算机视觉大会）
- CVPR（IEEE Conference on Computer Vision and Pattern Recognition，IEEE国际计算机视觉与模式识别会议）
- ECCV（European Conference on Computer Vision，欧洲计算机视觉国际会议）

其他顶会：

- AAAI
- NeurIPS 
- ……

Q：什么是影响影子？

> 影响因子（Impact Factor，IF）是汤森路透（Thomson Reuters）出品的期刊引证报告（Journal Citation Reports，JCR）中的一项数据。 即某期刊前两年发表的论文在该报告年份（JCR year）中被引用总次数除以该期刊在这两年内发表的论文总数。这是一个国际上通行的期刊评价指标。——from：[影响因子_百度百科](https://baike.baidu.com/item/%E5%BD%B1%E5%93%8D%E5%9B%A0%E5%AD%90)

一些网上的分享：

- [发表一篇顶会论文的经验分享 - 勋爵 - 博客园](https://www.cnblogs.com/X-knight/p/9281538.html)

更多的了解：[对期刊和会议的认识](./journals/对期刊和会议的认识.md)

News：

- [1300篇！CVPR 2019论文接收结果公布，你上榜了吗？](https://mp.weixin.qq.com/s/uzcEXQ1ePfDEFB2PRmlAbw)


<div align="right">
    <a href="#记录DeepLearning学习过程">回到顶部</a>
</div>