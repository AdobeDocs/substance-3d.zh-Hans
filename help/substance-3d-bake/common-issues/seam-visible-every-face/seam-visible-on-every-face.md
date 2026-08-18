---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/seam-visible-on-every-face.html"
breadcrumb-title: ''
description: 通过检查UV展开、平滑组和网格拓扑问题，修复每个人脸上可见的接缝。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seam visible on every face
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 每张脸上都可以看到接缝
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# 每张脸上都可以看到接缝

>[!WARNING]
>
> **问题**
> 
> 即使没有UV接缝，也可以在几何图形的一些边缘看到接缝：
> 
> ![](../../assets/seam-every-face.jpg)

>[!NOTE]
>
> **说明**
> 
> 如果不使用[笼子](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html)，烘焙过程将沿低多边形网格的顶点法线的方向发射光线。 如果分割每个顶点法线（即每个表面不与相邻表面共享相同的顶点法线），则光线不会在边缘上以相同的方向发送。 这会导致拆分，因为每一边上的信息不同。
> 
> 如[本页](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)中所述，锯齿还会加剧此问题。

>[!NOTE]
>
> **解决方案**
> 
> 此处只能提供两种解决方案：
> 
> * 使用[笼](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html)控制光线方向，而不是让烘焙师从低多边形几何计算它。
> * 将低多边形网格的顶点法向合并在一起（柔化它们/应用通用平滑组）。
