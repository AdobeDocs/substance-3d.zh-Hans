---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: 通过更正切线空间和法线计算，修复在网格曲面上可见的黑色着色伪像。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Black shading cross are visible on the mesh surface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 黑着色十字在网格表面上可见
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# 黑着色十字在网格表面上可见

在光照下网格的多个区域上出现黑色着色伪影。

![](../../assets/black-shading-cross.jpg)


## 说明

黑色阴影交叉通常表示法线映射与网格不匹配，这通常是因为网格几何发生了变化，或者网格的计算方式不同于面包师进行的计算。 例如：网格的三角化在渲染网格及其法线图的面包师和视窗之间不同。

## 解决方案

确保显示网格及其法线映射的应用程序与烘焙纹理的方式已同步。 这意味着：

* 验证查看器和烘焙器之间的相切空间是否相同。
* 验证视图和面包机之间的“Normal”（法线）格式是否相同。
* 验证查看者和烘焙师之间的三角划分是否相同。 有关详细信息，请参阅[此页面](../../guides/triangulating-before-bak/triangulating-before-baking.md)。
