

[DeepLab系列的进击](https://zhuanlan.zhihu.com/p/38474698)

**DeepLab V2：** 

文章总结起来就是：空洞卷积+全连接CRF+ASPP模块， 主干网络从预训练的 VGG 变成了 ResNet。

总的来说算法为了对抗物体的多尺度做了很多文章，首先是提出了 ASPP 模块，然后是多尺度训练和测试，再者就是数据增强（对输入图片进行随机缩放）。

算法整体流程：首先在三个尺度上训练和测试，得到的概率是输入图片的八分之一大小，然后是将概率图进行双线性插值到原始输入图片大小，将三个尺度的概率图进行融合，融合策略是最简单的取最大值，最后将融合之后的和原始输入一样大小的概率图输入到全连接条件随机场中细化边缘细节得到最终的分割结果。训练的时候将 GT 降采样了 8 倍和 CNN 直接输出的概率图同样的大小计算 loss。

下图是对 ASPP 模块的说明，使用多尺度的卷积核来探测多尺度的物体：

![](https://pic1.zhimg.com/80/v2-6a6efd2f65b84eb71fb4367683944f18_hd.jpg)

文章提出了两种网络结构，如下，最终的效果当时是有 ASPP 模块的评分高。

![](https://pic4.zhimg.com/80/v2-52a8700a6236813bb8373d58cafc4b7f_hd.jpg)

**DeepLab V3：** 

讲道理，第三版相对于第二版的改动真不是很大，主要是借鉴了下面的两篇论文的思想，然后分别对之前的空洞卷积和 ASPP 模块就行了改进，然后整体加入了 BN。

- Understanding Convolution for Semantic Segmentation

- Pyramid Scene Parsing Network

另外文章指出了，在训练的时候将 GT 应该保持不动，将概率图插值之后再进行计算 loss，这样不会导致金标准在降采样过程中丢失细节，毕竟8倍的降采样还是很严重的。

![](https://pic3.zhimg.com/80/v2-ea0d8f1e7f280736fde7904e947e576e_hd.jpg)

**DeepLab V3+：** 

鉴于对最后的概率图依然使用大倍数的双线性插值恢复到与原图一样的大小还是过于简单了，因此在这个版本中，增加了一个恢复细节的解码器部分。然后大量的使用了 depthwise separable convolution 来减小参数量提高处理速度，减小过拟合，强化网络的性能。

![](https://pic1.zhimg.com/80/v2-7a581e2266a1cb3bc4d0a1837211cde0_hd.jpg)



---

比较全面的对 DeepLab 解读，来自机器之心文章：[语义分割网络DeepLab-v3的架构设计思想和TensorFlow实现](https://www.jiqizhixin.com/articles/deeplab-v3)  【荐】

作为一个例子，试想通过一系列的卷积来传递图像，而不是使用池化和全连接层。我们将每次卷积都设置成步长为 1，padding 为「SAME」。通过这种处理，每一次卷积都保留了输入的空间维度。我们可以堆叠很多这种卷积，并最终得到一个分割模型。

![](https://image.jiqizhixin.com/uploads/editor/9174de92-cec2-47e3-95b4-f19434cd8164/1522033431606.jpg)

​				*用于密集预测的全卷积神经网络。请注意，不存在池化层和全连接层。*

这个模型可以输出形状为 [W,H,C] 的概率张量，其中 W 和 H 代表的是宽度和高度，C 代表的是类别标签的个数。在第三个维度上应用最大化函数会得到形状为 [W,H,1] 的张量。然后，我们计算真实图像和我们的预测的每个像素之间的交叉熵。最终，我们对计算结果取平均值，并且使用反向传播算法训练网络。

然而，这个方法存在一个问题。正如前面所提到的，使用步长为 1，padding 为「SAME」，保留了输入的维度。但是，那样做的后果就是模型会极其耗费内存，而且计算复杂度也是很大的。

为了缓解这个问题，分割网络通常会有三个主要的组成部分：卷积层、降采样层和上采样层。

![](https://image.jiqizhixin.com/uploads/editor/226ec612-038e-4a3b-a4f0-904a8e314793/1522033432285.jpg)

​							*图像语义分割模型的编码器-解码器结构。*





---

### DeepLab v3

- [Semantic Segmentation -- (DeepLabv3)Rethinking Atrous Convolution for Semantic Image Segmentation论文解](https://blog.csdn.net/u011974639/article/details/79144773)

  输出步幅 output_stride：定义为输入图像的分辨率与最终输出分辨率的比值。







