---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/mesh-parts-bleed-between-each-other.html"
breadcrumb-title: ''
description: 通过使用“按名称匹配”或调整距离来防止网格部分在烘焙过程中相互渗透。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Mesh parts bleed between each other
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格部分之间出血
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# 网格部分之间出血

>[!WARNING]
>
> **问题**
> 
> 网格几何出血在其他部分上，并创建伪像。
> 
> ![](../../assets/bleed-example.png)

>[!NOTE]
>
> **说明**
> 
> 烘焙过程从低多边形网格表面发送光线以入射到高多边形网格以创建匹配。 有时，光线会射得太远，导致错误的几何形状，从而产生出血和伪影。

>[!NOTE]
>
> **解决方案**
> 
> 有几种解决方案可避免此问题：
> 
> * 使用[按名称匹配](../../features/matching-by-name/matching-by-name.md)功能隔离网格
> * 使用[笼子](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html)限制光线距离。
> * 将常用烘焙器设置中的默认光线距离更改为较低的值。
