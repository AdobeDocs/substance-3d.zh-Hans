---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/guides/triangulating-before-baking.html"
breadcrumb-title: ''
description: 了解网格三角化如何影响烘焙结果并了解准备几何图形的最佳实践。
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

可以使用每个表面具有多个边界边的多边形来定义3D网格。 通常通过四边形（4边），有时更多（n边）。\
但是，软件稍后会将这些多边形转换为三角形，因为管理和执行计算更容易（特别是在GPU上）。

## 三角化如何影响网格？

![](../../assets/triangulation.jpg)

**没有将Quad/N-Gon转换为三角形的标准解决方案**。 如上图所示，多个选择是有效的。\
面包师们不太可能像游戏引擎那样对网格进行三角剖分，因为我们选择了特定的算法，而不是其他算法。

## 为什么在烤前要三角剖分？

烘焙过程将读取几何图形，然后将信息编码到纹理中。\
由于这些信息基于UV，并且有时基于网格拓扑，因此如果其他软件未像应用纹理时那样读取几何图形，则可能会错误地解码这些信息。

在下图中，您可以在左上角看到低多边形网格，在右上角看到高多边形网格。\
底部是低多边形，标准地图来自高多边形。 左侧的网格使用的三角剖分与Substance Painter在烘焙时使用的三角剖分相同。 右侧的网格不显示黑色伪影。 这是因为生成法线映射的方式与当前三角化网格的方式不匹配。 可通过&#x200B;**更新网格和/或重制**&#x200B;来修复此问题。

![](../../assets/example-triangulation-artifact.jpg)
