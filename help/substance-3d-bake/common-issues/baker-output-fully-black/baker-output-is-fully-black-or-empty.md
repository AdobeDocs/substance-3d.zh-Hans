---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/baker-output-is-fully-black-or-empty.html"
breadcrumb-title: ''
description: 诊断Baker输出完全为黑色或空的原因，并了解如何修复网格和UV问题。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baker output is fully black or empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Baker输出完全为黑色或为空
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# Baker输出完全为黑色或为空

>[!WARNING]
>
> **问题**
> 
> Baker的结果是黑色或空纹理：
> 
> ![](../../assets/black.png)

>[!NOTE]
>
> **说明**
> 
> 黑色纹理表示Baker找不到输出结果所需的信息。 例如，烘焙过程未找到与低多边形匹配的高多边形网格，因此没有可与之比较的颜色。

>[!NOTE]
>
> **解决方案**
> 
> * 验证是否正确加载了Baker必需的高多边形网格（有关任何错误，请参阅日志文件/窗口）。
> * 验证低多边形或高多边形网格不会太大（大于1公里）或太小（小于1厘米）。
> * 验证Baker是否可以读取/处理网格（有关任何错误，请参阅日志文件/窗口）。
> * 验证[按名称匹配](../../features/matching-by-name/matching-by-name.md)功能是否设置不正确（某些对象可能相互排除且从不重叠）。
> * 验证低多边形UV是否在0-1范围内。
