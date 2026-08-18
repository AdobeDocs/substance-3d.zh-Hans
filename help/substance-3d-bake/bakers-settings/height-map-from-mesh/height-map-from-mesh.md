---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/height-map-from-mesh.html"
breadcrumb-title: ''
description: 从高多边形网格创建Height贴图，以获取用于纹理化的表面细节和几何信息。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Height Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格中的高度贴图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 8%

---


# 网格中的高度贴图

使用来自网格烘焙器的Height映射，可以从高多边形网格创建Height映射。**适用于：**

* Painter
* Designer
* 自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| ****标准化**** | 定义应如何将Height范围的值向下保存到纹理中。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>相对于光线距离</strong>：</li><li data-preserve-html="true"><strong>相对于低多边形网格（每个UV图块）</strong>（默认）</li><li data-preserve-html="true"><strong>相对于最小/最大（每个UV图块）</strong></li><li data-preserve-html="true"><strong>手动</strong></li></ul> |
| **缩放除数** | 定义Height值应相乘或相除的量。仅在&#x200B;**标准化**&#x200B;设置为&#x200B;**手动**&#x200B;时可用。 |
