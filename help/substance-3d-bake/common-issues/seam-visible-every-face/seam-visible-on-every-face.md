---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/seam-visible-on-every-face.html"
breadcrumb-title: ''
description: 通过检查展开、平滑组和网格拓扑问题，修复每个脸部上可见的接缝。
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
> 即使没有接缝，几何图形的几条边上也仍然可见UV接缝：
> 
> ![](../../assets/seam-every-face.jpg)

>[!NOTE]
>
> **说明**
> 
> 如果不使用[笼子](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html)，则烘焙过程将沿低多边形网格的顶点法线方向发射光线。 如果每个顶点法线都拆分（即每个脸部与相邻顶点不共享相同的脸部法线），则不会在边缘上以相同的方向发送光线。 这会导致拆分，因为每一边上的信息不同。
> 
> 如[本页](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)中所述，锯齿还会加剧此问题。

>[!NOTE]
>
> **解决方案**
> 
> 此处只能提供两种解决方案：
> 
> * 使用[笼子](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html)控制光线方向，而不是让Baker从低多边形几何形状计算它。
> * 将低多边形网格的顶点法线合并在一起（柔化它们/应用常见的平滑组）。
