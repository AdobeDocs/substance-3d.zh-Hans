---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/color-map-from-mesh.html"
breadcrumb-title: ''
description: 将颜色属性从高多边形网格投射到纹理中，以便为选区蒙版烘焙多边形颜料或材质ID。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格中的颜色贴图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# 网格中的颜色贴图

网格烘焙器的此颜色图将颜色属性从高清晰度网格投射到纹理中。 该功能可用于烘焙聚合颜料或材料ID以创建选区蒙版。

**适用于：**

* Substance Designer
* Substance自动化工具包
* Substance Painter

## 参数

| *参数* | *描述* |
| --- | --- |
| **颜色源** | 控制颜色生成应基于高多边形网格的哪个属性。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>顶点颜色</strong>：读取保存到纹理中的顶点颜色。 颜色从顶点插入到顶点。</li><li data-preserve-html="true"><strong>材质颜色</strong>：读取分配给多边形表面的材质颜色。</li><li data-preserve-html="true"><strong>网格ID</strong>：为每个找到的对象分配颜色。</li><li data-preserve-html="true"><strong>多边形组/子网格ID</strong>：为每个子对象（也称为元素）分配颜色。</li></ul> |
| **颜色生成器** | 定义当&#x200B;**颜色源**&#x200B;设置为&#x200B;**网格ID**&#x200B;或&#x200B;**多边形组/子网格ID**&#x200B;时如何生成颜色。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>随机</strong>：每个对象或子对象均使用随机生成的颜色着色。</li><li data-preserve-html="true"><strong>色相偏移</strong>：每个对象或子对象均根据色相用一种唯一的颜色着色。</li><li data-preserve-html="true"><strong>灰度</strong>：每个对象或子对象都使用唯一的灰度值着色。</li></ul> |
