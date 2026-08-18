---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/convert-uv-to-svg.html"
breadcrumb-title: ''
description: 将网格UV转换为可用于创建精确蒙版和叠加的矢量图形文件。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Convert UV to SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convert UV to SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 6%

---


# Convert UV to SVG

“将UV转换为SVG”烘焙器将低多边形网格UV转换为矢量图形文件。 此矢量图形文件可用于创建蒙版。

**适用于：**

* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **填充** | 控制要为SVG形状添加多少几何边距。 |
| **颜色模式** | 定义SVG形状的着色方式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>随机：</strong>每个UV壳层都用随机颜色着色。</li><li data-preserve-html="true"><strong>色相偏移：</strong>每个UV壳层均用唯一的色相值着色。</li><li data-preserve-html="true"><strong>灰度：</strong>每个UV外壳都使用唯一的灰度值着色。</li><li data-preserve-html="true"><strong>统一颜色：</strong>所有UV外壳均使用50%灰度值着色。</li><li data-preserve-html="true"><strong>材质ID颜色</strong>：UV外壳由场景视图中定义的材质颜色着色。</li></ul> |
