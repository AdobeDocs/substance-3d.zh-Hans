---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/position.html"
breadcrumb-title: ''
description: 计算网格的几何位置并将其保存到纹理中，以创建基于体积的效果和渐变蒙版。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Position
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 位置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---


# 位置

“位置”Baker计算网格几何的位置并存储到纹理中。 该位置对于计算对象体积中的信息或创建渐变蒙版非常有用。

**适用于：**

* Substance Painter
* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **模式** | 控制将哪些信息计算到位置纹理中。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>所有轴：</strong>将X、Y和Z轴的位置烘焙到输出纹理的RGB通道中。</li><li data-preserve-html="true"><strong>一个轴：</strong>将单个轴作为灰度图像烘焙输出纹理。</li></ul> |
| **轴** | 定义在&#x200B;**Mode**&#x200B;参数设置为&#x200B;**一个轴**&#x200B;时应计算哪个轴。 |
| **规范化类型** | 定义如何缩放每个轴的位置值。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>框：</strong>根据轴量（定界框长度）规范化每个网格。</li><li data-preserve-html="true"><strong>BSphere：</strong>根据轴体积半径（边界球面）规范化所有网格。</li></ul> |
| **标准化比例** | 定义如何根据网格缩放位置值。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>每个材料</strong>：对于每个材料(纹理集)，值将缩放为介于0和1之间。</li><li data-preserve-html="true"><strong>完整场景</strong>（默认）：将缩放值以将整个网格考虑在内。 这允许在对象和材料(纹理集)之间使用连续的位置值。</li></ul> |
