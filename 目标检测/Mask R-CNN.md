# Mask R-CNN

![mask-rcnn](../assets/mask-rcnn.svg)

如 :numref:`fig_mask_r-cnn`所示，Mask R-CNN是基于Faster R-CNN修改而来的。

具体来说，Mask R-CNN将兴趣区域汇聚层替换为了

**兴趣区域对齐**层，使用**双线性插值**（bilinear interpolation）来保留特征图上的空间信息，从而更适于像素级预测。

兴趣区域对齐层的输出包含了所有与兴趣区域的形状相同的特征图。

它们不仅被用于预测每个兴趣区域的类别和边界框，还通过额外的全卷积网络预测目标的像素级位置。

本章的后续章节将更详细地介绍如何使用全卷积网络预测图像中像素级的语义。