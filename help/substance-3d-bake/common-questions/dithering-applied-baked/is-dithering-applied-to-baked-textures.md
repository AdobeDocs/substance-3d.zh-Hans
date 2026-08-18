---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-questions/is-dithering-applied-to-baked-textures.html"
breadcrumb-title: ''
description: 了解是否对烘焙纹理应用抖动以及它如何影响纹理质量。
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Is dithering applied to baked textures "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '是否对烘焙纹理应用抖动 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# 是否将抖动应用于烘焙纹理？

>[!WARNING]
>
> **问题**
> 
> 面包师是否支持纹理[抖动](https://en.wikipedia.org/wiki/Dither)？如果支持，何时应用？

>[!NOTE]
>
> **说明**
> 
> 应用抖动可避免8位正常映射中出现条纹，例如：
> 
> ![](../../assets/dither.jpg)

>[!NOTE]
>
> **解决方案：Substance Designer**
> 
> 抖动在以下情况下自动应用：
> 
> * 将贝克输出保存到8位纹理文件时
> * 在设置为8位的图形的位图节点中使用Baker输出时。

>[!NOTE]
>
> **解决方案：Substance Painter**
> 
> 抖动是一个可以在导出过程中启用或禁用的选项。 该功能仅在“正常”、“位移”和“Height”声道导出为8位文件格式时应用。

>[!NOTE]
>
> **解决方案：Substance自动化工具包**
> 
> 目前不支持抖动。
