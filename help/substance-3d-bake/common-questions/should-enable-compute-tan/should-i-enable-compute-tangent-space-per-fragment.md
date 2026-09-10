---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/should-i-enable-compute-tangent-space-per-fragment.html"
breadcrumb-title: ''
description: 了解何时启用每个片段的计算正切空间以及它如何影响您的烘焙结果。
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Should I enable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 我是否应该启用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# 是否应该启用“计算每个片段的切线空间”？

>[!WARNING]
>
> **问题**
> 
> “计算每个片段的正切空间”设置的含义是什么，其用法是什么？

>[!NOTE]
>
> **说明**
> 
> 启用此设置后，将告知Baker在片段着色器（也称为像素着色器）中执行切线空间计算，而不是顶点着色器。 这意味着计算将按每个像素完成，而不是从顶点插入到顶点。 Baker使用此设置了解如何对纹理进行编码。 它以前还知道如何读取着色器所呈现的纹理。
> 
> 启用或禁用此参数通常需要重新生成纹理，以将其与3D视口和渲染引擎（如Iray）同步。

>[!NOTE]
>
> **解决方案**
> 
> 根据要渲染纹理的软件或游戏引擎，可能会禁用或启用此设置：
> 
> | *软件* | *计算每个片段的正切空间* |
> | --- | --- |
> | **虚构引擎4** | 启用 |
> | **统一** | 禁用 |
