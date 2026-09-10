---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/normal-map-from-mesh.html"
breadcrumb-title: ''
description: 使用Baker从高多边形网格创建正切空间或来自网格的法线图映射。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Normal Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格中的法线贴图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 7%

---


# 网格中的法线贴图

通过“从法线图”Baker，可以从高模网格创建正切空间或世界空间法线映射。**适用于：**

* Substance Painter
* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **映射类型** | 控制Baker应输出的常规纹理类型。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>世界空间</strong></li><li data-preserve-html="true"><strong>切线空间</strong>（默认）</li></ul>*在Substance Painter中，无法控制此参数，且此参数设置为切线空间。* |
| **正常方向** | 在&#x200B;**映射类型**&#x200B;参数设置为切线空间时定义法向纹理的格式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li></ul>*在Substance Painter中，此参数由[项目设置](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/interface/project-configuration)控制。* |
