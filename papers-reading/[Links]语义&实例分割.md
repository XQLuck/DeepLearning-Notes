

### 基于监督下的图像分割

资料&干货：

- [语义分割相关资料总结](https://zhuanlan.zhihu.com/p/41976717)
  > 看完里面的资料后，基本对语义分割可以蛮清楚了。

- 知乎：[当前主流的图像分割研究方向都有哪些？](https://www.zhihu.com/question/33599013)

综述类：

- [语义分割 | 发展综述](https://zhuanlan.zhihu.com/p/37618829)
- [十分钟看懂图像语义分割技术](https://www.leiphone.com/news/201705/YbRHBVIjhqVBP0X5.html)
  > 这篇文章介绍了“Normalized cut”的图划分方法，简称“N-cut”，还介绍到 Grab Cut，以及神经网络、FCN、条件随机场 CRF 等内容。（一篇很全面且易懂的好文）

- 知乎_魏秀参：[从特斯拉到计算机视觉之「图像语义分割」](https://zhuanlan.zhihu.com/p/21824299)
  > 看完上面那篇再看这篇吧，内容大部分差不多，但值得看看。

- [资源 | 从全连接层到大型卷积核：深度学习语义分割全指南](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728920&idx=4&sn=3c51fa0a95742d37222c3e16b77267ca&scene=21#wechat_redirect)
- [一文概览主要语义分割网络：FCN,SegNet,U-Net...](https://www.tinymind.cn/articles/410)
- [分割算法——可以分割一切目标（各种分割总结）](https://mp.weixin.qq.com/s/KcVKKsAyz-eVsyWR0Y812A)



---

传统分割方法：

- [图像分割技术（1）](https://blog.csdn.net/zizi7/article/details/50950494)

  > 介绍了一些传统的图像分割技术。一般有 4 种分割思路：基于点线、边缘的分割；基于阈值的分割（二值化）；基于区域的分割；基于分水岭的分割

语义分割专栏：

- 知乎_stone：[图像语义分割](https://zhuanlan.zhihu.com/c_197474183)
- 知乎_学海无涯乐为舟：[语义分割的学习](https://zhuanlan.zhihu.com/c_1008415414103203840)
- 知乎_加油可好：[语义分割刷怪进阶](https://zhuanlan.zhihu.com/c_156519173)

语义分割相关研究：

- [图像语义分割之FCN和CRF](https://blog.csdn.net/u012759136/article/details/52434826#t9)


语义分割模型讲解：

- [全卷积网络 FCN 详解](https://zhuanlan.zhihu.com/p/30195134)

论文汇总：

- [语义分割 - Semantic Segmentation Papers](https://www.aiuai.cn/aifarm62.html)



#### 实例分割

相较于语义分割，实例分割不仅要做出像素级别的分类，还要在此基础上将同一类别不同个体分出来，即做到每个实例的分割。这对分割算法提出了更高的要求。好在我们此前积累足够的目标检测算法基础。实例分割的基本思路就是在语义分割的基础上加上目标检测，先用目标检测算法将图像中的实例进行定位，再用语义分割方法对不同定位框中的目标物体进行标记，从而达到实例分割的目的。

实例分割算法也有一定的发展历史但其中影响深远且地位重要的算法不多，以 Mask R-CNN 为例进行介绍。

Mask R-CNN 是 2017 年何恺明等大佬基于此前的两阶段目标检测算法推出的顶级网络。Mask R-CNN 的整体架构如图所示：

![](http://p35l3ejfq.bkt.clouddn.com/20181031203911.png)

Mask R-CNN 将 Fast R-CNN 的 ROI Pooling 层升级成了 ROI Align 层，并且在边界框识别的基础上添加了分支 FCN 层，即 mask 层，用于语义 Mask 识别，通过 RPN 网络生成目标候选框，然后对每个目标候选框分类判断和边框回归，同时利用全卷积网络对每个目标候选框预测分割。Mask R-CNN 本质上一个实例分割算法（Instance Segmentation），相较于语义分割（Semantic Segmentation），实例分割对同类物体有着更为精细的分割。

Mask R-CNN 在 COCO 测试集上的图像分割效果如下：![](http://p35l3ejfq.bkt.clouddn.com/20181031204014.png)

*Mask R-CNN 论文：https://arxiv.org/abs/1703.06870*

*MaskR-CNN 开源实现参考：https://github.com/matterport/Mask_RCNN*



### 基于弱监督学习的图像分割

最近基于深度学习的图像分割技术一般依赖于卷积神经网络 CNN 的训练，训练过程中需要非常大量的标记图像，即一般要求训练图像中都要有精确的分割结果。

对于图像分割而言，要得到大量的完整标记过的图像非常困难，比如在 ImageNet 数据集上，有 1400 万张图有类别标记，有 50 万张图给出了 bounding box，但是只有 4460 张图像有像素级别的分割结果。对训练图像中的每个像素做标记非常耗时，特别是对医学图像而言，完成对一个三维的 CT 或者 MRI 图像中各组织的标记过程需要数小时。如果学习算法能通过对一些初略标记过的数据集的学习就能完成好的分割结果，那么对训练数据的标记过程就很简单，这可以大大降低花在训练数据标记上的时间。这些初略标记可以是：

1. 只给出一张图像里面包含哪些物体，
2. 给出某个物体的边界框，
3. 对图像中的物体区域做部分像素的标记，例如画一些线条、涂鸦等（scribbles)。



参考文章：

- [CNN在基于弱监督学习的图像分割中的应用](https://zhuanlan.zhihu.com/p/23811946)
- [一文概览主要语义分割网络：FCN,SegNet,U-Net...](https://www.tinymind.cn/articles/410)

