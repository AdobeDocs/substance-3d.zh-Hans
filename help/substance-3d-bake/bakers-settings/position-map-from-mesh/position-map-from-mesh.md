---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/position-map-from-mesh.html"
breadcrumb-title: ''
description: 从高多边形网格计算精确的位置图以获取精确的几何位置信息。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Position map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 来自网格的位置图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# 来自网格的位置图

来自网格烘焙器的位置映射计算高多边形网格几何的位置并存储到纹理中。 它与基本位置烘焙机相似，但可以产生更精确的结果。

**适用于：**

* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **模式** | 控制将哪些信息计算到位置纹理中。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>所有轴：</strong>将X、Y和Z轴的位置粘贴到输出纹理的RGB通道中。</li><li data-preserve-html="true"><strong>一个轴：</strong>将单个轴作为灰度图像烘焙到输出纹理中。</li></ul> |
| **轴** | 定义在&#x200B;**Mode**&#x200B;参数设置为&#x200B;**One axis**&#x200B;时应计算哪个轴。 |
| **规范化类型** | 定义如何按轴缩放位置值。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>边界：</strong>根据网格体积（定界框长度）规范化每个轴。</li><li data-preserve-html="true"><strong>BSphere：</strong>根据网格体积半径（边界球面）规范化所有轴。</li></ul> |
| **标准化比例** | 定义如何根据网格缩放位置值。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>每个材质</strong>：将每个材质（纹理集）的值缩放为0到1之间。</li><li data-preserve-html="true"><strong>完整场景</strong>（默认）：缩放值以考虑整个网格。 这允许在对象和材质（纹理集）之间使用连续的位置值。</li></ul> |
