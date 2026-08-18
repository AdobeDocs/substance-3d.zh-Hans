---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: 通过检查网格颜色属性和UV映射，从网格烘焙失败解决颜色映射。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baking failed with Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 无法通过网格中的颜色映射进行烘焙
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# 无法通过网格中的颜色映射进行烘焙

>[!WARNING]
>
> **问题**
> 
> 可能的错误消息：
> 
> &#x200B;> > > 
> 
> [烘焙]烘焙失败（来自网格的颜色图）\
> 找不到顶点颜色

>[!NOTE]
>
> **说明**
> 
> 来自网格[&#128279;](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md)的颜色映射的默认设置是根据网格UV将高多边形网格顶点颜色烘焙到纹理中。 但是，通常情况下，高多边形网格没有任何顶点颜色信息。 因此，面包师无法写入不存在的信息。

>[!NOTE]
>
> **解决方案**
> 
> 有不同的解决方案可避免此错误消息：
> 
> * 使用具有顶点颜色的高多边形网格
> * 使用不同的设置从网格烘焙器设置颜色图
> * 如果不需要颜色图，请不要使用网格烘焙器中的颜色图
