---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion.html"
breadcrumb-title: ''
description: 了解如何使用Baker通过快速GPU加速算法生成环境阴影纹理。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境光遮蔽
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 4%

---


# 环境光遮蔽

Baker允许烘焙环境阴影纹理。 本Baker使用了一种在GPU上执行的快速算法。

**适用于：**

* Substance Designer
* Substance自动化工具包

>[!WARNING]
>
> * 旧GPU上可能不支持此Baker。
> * 在低端/移动GPU上以高分辨率进行烘焙可能会导致崩溃。

## 参数

| *名称* | *描述* |
| --- | --- |
| **法线图** | 输入法线图文件，可用于在Baker计算期间提供要考虑的网格曲面上的附加几何细节。 此参数是可选的。 |
| **世界空间** | 如果启用，请指定输入法线图为世界空间（而不是切线空间）。 如果未提供输入法线图，则此参数将被忽略/禁用。 |
| **反相正常** | 使用反法线计算ambient occlusion图（可用于生成厚度图）。 |
| **使用未选择的网格部件** | 使用网格中未选择的网格部分烘焙ambient occlusion映射。 |
| **质量** | 选择Ambient occlusion图的质量。 计算质量越高，速度越慢。可用值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>低</strong>（3遍）</li><li data-preserve-html="true"><strong>中</strong>（默认，5遍）</li><li data-preserve-html="true"><strong>高</strong> （10次）</li><li data-preserve-html="true"><strong>非常高</strong>（16次）</li></ul> |
| **精度偏差** | ambient occlusion的精度。 值越低，精度越高，但可能会产生较大的伪影。 |
| **距离淡化** | 环境光遮蔽的扩散。 |
