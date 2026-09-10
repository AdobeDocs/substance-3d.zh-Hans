---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/what-are-assbin-files.html"
breadcrumb-title: ''
description: 了解什么是Assbin文件以及如何将其用作几何缓存文件以加快烘焙操作。
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What are Assbin files "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '什么是阿斯宾文件 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# 什么是Asbin文件？

>[!WARNING]
>
> **问题**
> 
> 在Substance Painter中烘焙后，我在文件扩展名为“assbin”的高多边形网格旁边找到一个或多个文件，它们是什么？ 我可以安全地移除它们吗？

>[!NOTE]
>
> **解决方案**
> 
> Assbin文件在烘焙过程中使用的高多边形网格的预处理版本。 与原始网格文件相比，它们读取速度更快，从而允许在迭代Baker设置时更快地重新烘焙。 可以安全地将其移除。 如有必要，Substance Painter将重新生成它们。 然而，这可能影响烘焙业绩。
> 
> 如果进入Substance Painter[主首选项](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/general-71008262.html)并禁用“保存预处理的场景文件”选项，则可能永远不会生成这些文件。
