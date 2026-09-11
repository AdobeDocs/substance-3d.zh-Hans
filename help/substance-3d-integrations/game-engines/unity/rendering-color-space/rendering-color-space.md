---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/rendering-color-space.html"
breadcrumb-title: ''
description: 配置Unity的色彩空间设置，以确保使用基于物理的着色器正确渲染材料。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Rendering Color Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渲染色彩空间
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# 渲染色彩空间

纹理设计为与基于物理的着色器一起使用。 为获得最佳效果，您应该在Unity播放器设置中将色彩空间设置为线性。

1. 转到“编辑”>“项目设置”>“播放器”
1. 在渲染部分中，将色彩空间更改为线性。 （Unity默认为灰度系数空间，该空间不正确，并且会导致纹理颜色看起来不正确）。

   >[!NOTE]
   >
   > **信息**
   > 
   > 如果Unity中的“色彩空间设置”设置为“灰度系数”，则会禁用纹理上的sRGB选项

   ![](../../../assets/rendering-4.png){width="600px"}
