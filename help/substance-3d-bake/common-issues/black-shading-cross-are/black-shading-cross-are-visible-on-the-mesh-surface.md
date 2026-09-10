---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: 通过更正着色空间和法向计算，修复网格表面上可见的黑色正切伪影。
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

在光照下时，网格的多个区域会出现黑色着色伪影。

![](../../assets/black-shading-cross.jpg)


## 说明

黑底十字通常表示法线图与网格不匹配，这通常是由于网格几何发生了变化，或者计算的方式与Baker执行的计算不同。 例如：网格的三角化在Baker和渲染网格及其法线图的视口之间是不同的。

## 解决方案

确保显示网格及其法线图的应用程序已与烘焙纹理的方式同步。 这意味着：

* 验证查看器和Baker之间的切线空间是否相同。
* 验证Baker和视图之间的“Normal（标准）”格式是否相同。
* 验证查看者和Baker之间的三角化是否相同。 有关详细信息，请参阅[此页面](../../guides/triangulating-before-bak/triangulating-before-baking.md)。
