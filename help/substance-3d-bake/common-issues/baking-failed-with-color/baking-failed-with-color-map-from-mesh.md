---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: 通过检查烘焙属性和网格映射来解决UV映射失败问题。
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
> [烘焙]烘焙失败(来自网格的色图)\
> 找不到顶点颜色

>[!NOTE]
>
> **说明**
> 
> [来自网格的色图](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md)的默认设置是根据顶点UV将高多边形网格纹理烘焙为网格。 但是，通常情况下，高多边形网格没有任何顶点颜色信息。 因此，Baker无法写入不存在的信息。

>[!NOTE]
>
> **解决方案**
> 
> 有不同的解决方案可避免此错误消息：
> 
> * 使用具有网格的高多边形颜色
> * 使用其他设置设置Baker
> * 如果您不需要Baker，请不要使用它
