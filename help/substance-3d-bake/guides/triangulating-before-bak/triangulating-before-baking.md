---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/triangulating-before-baking.html"
breadcrumb-title: ''
description: 了解网格三角化如何影响烘焙结果，并了解准备几何图形的最佳做法。
helpx_creative_field: ""
helpx_description: bakers > Guides > Triangulating before baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙前三角化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# 烘焙前三角化

3D网格可以用多边形来定义，每个脸部有多个边界边。 通常通过四边形（4边），有时更多（n边）。\
但是，软件以后会将这些多边形变换为三角形，因为这样更容易管理和执行计算（特别是在GPU上）。

## 三角化如何影响网格？

![](../../assets/triangulation.jpg)

**没有将Quad/N-Gon转换为三角形的标准解决方案**。 如上图所示，多个选择是有效的。\
Baker不太可能像游戏引擎那样对网格进行三角划分，因为我们选择了特定的算法，而不是其他算法。

## 为什么在烘焙之前要三角化？

烘焙过程将读取几何，然后将信息编码到纹理中。\
由于这些信息基于UV，并且有时基于网格拓扑，因此如果其他软件未像应用纹理时那样读取几何图形，则可能会错误地解码信息。

在下图中，您可以看到左上角的低多边形网格和右上角的高多边形网格。\
底部是低多边形，法线图从高多边形烘焙。 左侧的网格使用的三角剖分与Substance Painter在烘焙时使用的三角剖分相同。 右侧的网格不会显示黑色伪像。 这是因为法线图的烘焙方式与当前的网格三角化方式不匹配。 此问题可以通过&#x200B;**更新网格和/或重新生成**&#x200B;来修复。

![](../../assets/example-triangulation-artifact.jpg)
