---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/transferred-texture-from-mesh.html"
breadcrumb-title: ''
description: 根据网格的UV在法线图之间转移纹理，包括支持UV转换。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Transferred Texture from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 已从网格中转移纹理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 3%

---


# 已从网格中转移纹理

该Baker允许基于各自UV将纹理从一个网格转换为另一个文档。 此Baker还支持传输或法线图（需要特殊转换）。 为了起作用，两个网格都需要UV定义。

**适用于：**

* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **纹理的文件** | 要传输的输入纹理文件的路径。 |
| **UV 集** | 网格要在高多边形网格上使用的UV，以读取纹理并将其投影到低多边形网格上。 |
| **筛选模式** | 定义应如何进行纹理的像素插值。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>最接近</strong>：无插值，使用找到的最接近给定位置的像素。 精确，但可能会产生锯齿。</li><li data-preserve-html="true"><strong>双线性</strong>（默认）：使用给定位置最近的四个像素。 没有锯齿，但可能会模糊。</li></ul> |
| **法线图** | 如果启用，则向Baker指示要传输的输入纹理是法线图。 这表示有Baker对纹理应用特殊转换以使其与目标网格兼容。 |
| **映射类型** | 定义输入纹理的法线图类型。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>世界空间</strong></li><li data-preserve-html="true"><strong>相切空间</strong> （默认）</li></ul> |
| **正常方向** | 如果&#x200B;**映射类型**&#x200B;设置为&#x200B;**相切空间**，则定义输入纹理的常规格式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li></ul> |
