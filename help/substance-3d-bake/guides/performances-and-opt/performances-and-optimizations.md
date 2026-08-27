---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/performances-and-optimizations.html"
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

* 良好的CPU将提供减少的计算时间（多核将加快使用光线追踪的网格&#x200B;**烘焙器的**&#x200B;计算）。
* 充足的内存(RAM)将允许载入包含大量细节（多边形）的网格。
* 良好的GPU将允许以大分辨率（例如8K）生成纹理。

## 三角化

烘焙师在内部使用三角化网格；如果3D模型（低多边形和高多边形）未进行三角化，则烘焙师将自行三角化网格。 此过程可能耗时较长，并且随着模型中包含的多边形数量将线性增加。 通常建议对网格（特别是高多边形网格）进行三角化以避免烘烤过程中发生此过程。

如果您的工作流程基于FBX，则可以在导出时使用DCC应用程序中的选项三角化网格。

## 几何缓存

有关详细信息，请参阅以下页面： [几何缓存](../../features/geometry-cache/geometry-cache.md)

## 消除锯齿

烘焙师可以使用超采样来执行消除锯齿。 超取样意味着烘焙师将在每个像素投射更多光线以平滑结果。 烘焙时间可能受此设置影响很大；对于需要大量光线的烘焙师（例如来自网格烘焙器的环境遮蔽）尤其如此。

例如：

* AA设置为2x2时，烘焙师投射的光线将是初始光线总量的4倍。 对于2048\*2048 px纹理，计算所得的结果相当于烘焙4096\*4096px纹理，并且计算时间应增加4倍左右。
* AA设置为8x8时，烘焙师投射的光线将是初始光线总量的64倍。 对于2048\*2048 px的纹理，计算时间相当于生成16384\*16384px的纹理，计算时间大约增加64倍。

**考虑到这些数字，应该谨慎使用8x8设置**。

为了减少噪音的存在，通常建议增加次生射线的数量（对于环境遮蔽、Thickness和弯曲的法向烘焙器）并保持2x2或4x4 AA设置，而不是使用少量次生射线和高AA设置。

>[!NOTE]
>
> 对于来自网格的环境遮蔽，良好的性能/质量设置是使用AA 2x2和至少128次生射线。

## 文件格式

在磁盘上导出文件可能需要很长时间，具体取决于文件格式、分辨率、位深度和压缩设置。 可以在“首选项”/“项目”/“常规”/“文件格式”选项中修改压缩设置。 禁用压缩功能可在扩展较大文件时减少导出时间。

## 崩溃和TDR

崩溃可能由多种因素引起，其中之一是TDR（超时检测恢复）。 TDR是一个Windows机制，用于在GPU似乎没有响应的情况下进行检测和恢复。 由于TDR延迟检测的默认值较低，因此在某些情况下使用特定烘焙器时可能会发生崩溃：

* 使用环境遮蔽烘焙器烘焙密集网格时
* 使用具有非常密集的高多边形网格（超过60,000,000个三角形）的DXR加速面包时

您可以在以下位置找到有关TDR的其他信息以及有关如何修改其关联设置的分步指南： [GPU驱动程序崩溃导致计算时间过长（TDR崩溃）](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)
