---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/guides/performances-and-optimizations.html"
breadcrumb-title: ''
description: 了解如何优化硬件设置和网格准备以实现更快的烘焙性能。
helpx_creative_field: ""
helpx_description: bakers > Guides > Performances and optimizations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 性能和优化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---


# 性能和优化

## 最低硬件要求

使用Substance Bakers没有最低要求，但请务必注意以下几点：

* 良好的CPU将减少计算时间（多内核将加快使用射线追踪的网格&#x200B;**Baker中**&#x200B;的计算）。
* 充足的内存(RAM)能够加载包含大量细节（多边形）的网格。
* 良好的GPU将允许以大分辨率（例如8K）生成纹理。

## 三角化

Baker在内部使用三角化网格；如果3D模型（低多边形和高多边形）未进行三角化，则Baker将自行对网格进行三角化。 此过程可能耗时较长，并且随着模型中包含的多边形数量将线性增加。 通常建议对网格（尤其是高模网格）进行三角化以避免在烘焙期间发生此过程。

如果您的工作流程基于FBX，您可以在导出时使用DCC应用程序中的选项三角化网格。

## 几何缓存

有关详细信息，请参阅以下页面： [几何缓存](../../features/geometry-cache/geometry-cache.md)

## 消除锯齿

Baker可以使用超采样执行消除锯齿操作。 超取样意味着Baker将在每个像素强制转换更多光线，以便让结果更加平滑。 此设置可能会显着影响烘焙时间；此设置对于需要大量光线的Baker（例如，来自网格Baker的ambient occlusion）尤其有用。

例如：

* AA设置2x2意味着Baker的强制转换是初始光线量的4倍。 对于2048\*2048 px纹理，生成的计算等同于烘焙4096\*4096px纹理，计算时间应多出4倍。
* AA设置为8x8时，表示Baker的强制转换是初始光线量的64倍。 对于2048\*2048 px纹理，生成的计算时间相当于烘焙16384\*16384px纹理，计算时间应多大约64倍。

**考虑到这些数字，应该谨慎使用8x8设置**。

为了减少噪声的存在，通常建议增加次生射线的数量（针对ambient occlusion、Thickness和bent normalsBaker）并保持2x2或4x4 AA设置，而不是使用少量次生射线和高AA设置。

>[!NOTE]
>
> 从ambient occlusion的一种较好的性能/质量设置是使用AA 2x2和至少128次生射线。

## 文件格式

在磁盘上导出文件可能需要很长时间，具体取决于文件格式、分辨率、位深度和压缩设置。 可以在“首选项”/“项目”/“常规”/“文件格式”选项中修改压缩设置。 禁用压缩功能可在扩展较大文件时减少导出时间。

## 崩溃和TDR

崩溃可能由多种因素引起，其中之一是TDR（超时检测恢复）。 TDR是一个Windows机制，用于在GPU似乎没有响应的情况下进行检测和恢复。 由于TDR延迟检测的默认值较低，因此在某些情况下，使用特定Baker时会遇到崩溃：

* 使用Baker烘焙密集网格时
* 使用具有非常密集的高多边形（超过6,000万个三角形）的DXR加速Baker时

有关TDR的其他信息，以及有关如何修改其关联设置的分步指南，请参阅此处： [带有长计算的GPU驱动程序崩溃(TDR崩溃)](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)
