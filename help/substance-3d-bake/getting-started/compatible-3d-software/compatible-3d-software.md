---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/getting-started/compatible-3d-software.html"
breadcrumb-title: ''
description: 了解哪些3D软件与Substance Bakers兼容，并了解如何准备网格以获得最佳烘焙效果。
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Compatible 3D software
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 兼容的3D软件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---


# 兼容的3D软件

大多数3D软件都与Substance Baker兼容，只要它们以应用程序支持的文件格式将网格几何导出为多边形即可。

但是，在导出这些网格时，并非所有软件在功能和质量方面都是相同的。 因此，正确清理网格并确保其与Baker兼容非常重要。 有关如何准备网格的详细信息，请参阅各种[指南](../../guides/performances-and-opt/performances-and-optimizations.md)。

## 软件兼容性

下面列出了常见的3D软件及其与Baker的兼容性：

| *名称* | *状态* |
| --- | --- |
| **混合器** | 兼容：需要先拼合修饰符，然后再导出。 |
| **Maya** | 兼容：要求在导出前冻结变换和删除历史记录。 |
| **3DS最大值** | 兼容：在导出前需要重置xForm。 |
| **MODO** | 兼容：建议使用“游戏选项卡”导出器设置为“非真实静态网格”。 |
| **Cinema 4D** | 兼容：需要先拼合修饰符，然后再导出。 |
| **zBrush** | 不兼容：首先需要在另一个3D应用程序中处理和清理低多边形网格。 兼容：用于烘焙的高多边形网格。 |

## 文件格式

在烘焙几何时，还必须考虑所使用的文件格式。 文件格式将定义要保存在网格中的信息量。

信息过多有时可能有害并导致错误。 我们通常建议在出现错误时尝试使用不同的文件格式，因为这是解决问题的一种简单方法，并可以确定问题出在Baker中还是来自3D软件。

下面简要介绍这些Baker支持的两种最常见的文件格式：

| 文件格式 | 信息 |
| --- | --- |
| **FBX** | Autodesk FBX (Filmbox)是Autodesk Software使用的主要文件格式，它可以写为文本或二进制。  它支持：<ul data-preserve-html="true"><li data-preserve-html="true">UV（多组）</li><li data-preserve-html="true">顶点、正切和二项式</li><li data-preserve-html="true">顶点颜色</li><li data-preserve-html="true">三角形脸部、四边脸部和N-Gon脸部</li><li data-preserve-html="true">相机</li><li data-preserve-html="true">光源</li><li data-preserve-html="true">网格子分区</li><li data-preserve-html="true">平滑组</li><li data-preserve-html="true">材料信息（如颜色）</li><li data-preserve-html="true">位图</li></ul> |
| **对象** | Wavefront OBJ是一种非常简单的基于文本的文件格式，它支持：<ul data-preserve-html="true"><li data-preserve-html="true">UV（仅一套）</li><li data-preserve-html="true">顶点法线</li><li data-preserve-html="true">顶点颜色（仅适用于从Pixologic zBrush导出的颜色）</li><li data-preserve-html="true">三角形脸部、四角脸部和N-Gon脸部</li><li data-preserve-html="true">材料颜色（如果存在<strong>mtl</strong>文件）</li></ul> |
