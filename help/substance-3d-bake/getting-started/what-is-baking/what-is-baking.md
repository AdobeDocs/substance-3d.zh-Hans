---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/getting-started/what-is-baking.html"
breadcrumb-title: ''
description: 了解什么是烘焙，并了解如何将3D网格信息保存到纹理文件中，以增强您的Substance素材。
helpx_creative_field: ""
helpx_description: "bakers > Getting Started > What is Baking "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '正在烘焙 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# 烘焙是什么？

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

&#x200B;>> 

(来源：[Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0)

烘焙是有关&#x200B;**将与** 3D网格&#x200B;**相关的信息**&#x200B;保存到&#x200B;**纹理**&#x200B;文件（[位图](https://en.wikipedia.org/wiki/Raster_graphics)）中的进程名称。 大多数情况下，此过程涉及另一个网格。 在这种情况下，第一网格的信息被转移到第二网格UV上，然后存储到纹理中。

虽然某些应用程序可能支持将信息烘焙到网格属性中（如顶点颜色），但Substance Baker仅允许将信息烘焙到纹理中。 但是，他们可以读取网格属性并将它们分解为纹理（如顶点颜色）。

## 烘焙是必要的吗？

Substance软件可以生成纹理，这些纹理可以使用与网格几何相关的信息来增强。\
许多滤镜和材质都可以通过查看烘焙纹理来适应3D网格的特定几何形状。 烘焙可以提供有关环境阴影可以位于何处，几何图形的边在哪里，以及更多的信息。

例如：一辆旧车可能在其底部应用了铁锈，因为它在一段时间内没有移动。 烘焙所述位置映射将允许知道底部在网格上的位置，所述网格将馈送铁锈发生器并产生合适的纹理。

![](../../assets/examples.jpg){width="500px"}

## 烘焙是怎样工作的？

每个烘焙师执行特定操作以生成自己的结果，但烘焙过程通常涉及两种可能的方法：

* **生成一个网格** ：依靠当前网格生成信息。
* **从一个网格到另一个网格生成** ：从源网格计算信息并将结果转移到另一个网格上。

此烘焙过程依赖于网格属性，因此网格必须是干净的，并且其几何形状中不存在任何可能的错误。

## 你能烘焙什么信息？

许多类型的信息都可以被烘焙。 但是，通常只需要一个特定的集合，因为它们可以外推，以便以后创建更高级的结果。 这就是为何可以在多个软件中找到常见的烘焙过程类型的原因。

作为实例，Substance软件可以输出以下类型的信息：

* **环境遮蔽** （环境阴影）
* **法线**&#x200B;信息（作为矢量方向存储的表面细节变化）
* **方向**（向上或向下、向左或向右等）
* **曲率**（几何形状的边和腔）
* **位置**（规范化多维数据集内几何的相对位置）

有关详细信息，请参阅每个烘焙师[&#128279;](../../bakers-settings/bakers-settings.md)的文档。

## “常规”和“来自网格”面包师之间的差异

根据流程，烘焙师会使用各种实施。 一般来说，**来自网格**&#x200B;的烘焙师依靠光线追踪技术将数据从一个模型提取并投影到另一个模型。
