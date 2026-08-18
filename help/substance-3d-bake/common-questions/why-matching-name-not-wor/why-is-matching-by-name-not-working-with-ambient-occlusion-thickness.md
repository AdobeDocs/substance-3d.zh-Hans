---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.html"
breadcrumb-title: ''
description: 了解为什么按名称匹配无法用于环境遮蔽和Thickness烘焙师，并查找替代项。
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Why is Matching by Name not working with Ambient OcclusionThickness "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '为什么“按名称匹配”无法与“环境光遮蔽”“厚度”一起使用 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# 为什么“按名称匹配”无法用于环境遮蔽/Thickness？

>[!WARNING]
>
> **问题**
> 
> 我在[常用参数](../../bakers-settings/common-parameters/common-parameters.md)中启用了[按名称匹配](../../features/matching-by-name/matching-by-name.md)来筛选和排序我的低多边形网格和高多边形网格，为什么环境遮蔽烘焙商忽略它？

>[!NOTE]
>
> **说明**
> 
> “环境遮蔽”、“Thickness”和“弯曲法线”烘焙机在计算纹理时启动次生射线。 这些光线具有自己的“按名称匹配”设置。

>[!NOTE]
>
> **解决方案：Substance Painter**
> 
> 解决方案：为面包机参数中的次生射线启用按名称筛选。
