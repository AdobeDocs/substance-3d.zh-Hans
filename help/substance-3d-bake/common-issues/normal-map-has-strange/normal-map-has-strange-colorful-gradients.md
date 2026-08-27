---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/normal-map-has-strange-colorful-gradients.html"
breadcrumb-title: ''
description: 通过检查网格法线、平滑组和UV映射，修复法线图中奇怪的彩色渐变。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal map has strange colorful gradients
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常地图具有奇怪的彩色渐变
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 正常地图具有奇怪的彩色渐变

Baker的输出是一组色彩非常浓烈的渐变。

![](../../assets/color-gradient.png)


## 说明

在烘焙过程中，当高多边形区域与低多边形网格不匹配时，通常会产生彩色渐变。 这种不匹配可以由以下原因解释：

* 高多边形和低多边形网格<b>不能正确重叠</b>（请参阅下图）。
* 高多边形是<b>缺少几何</b>，而低多边形尝试覆盖它。
* 高多边形或低多边形网格具有反转顶点法线。

当发生这种情况时，烘焙过程会尝试匹配不存在的几何，从而导致一些空值。 该Baker使用从纹理的相邻像素中提取的颜色填充此空白区域，从而创建彩色渐变（除非禁用了<b>漫射</b>）。

## 解决方案

由于导致网格之间不重叠的可能原因很少，因此必须考虑几种解决方案：

* 确保冻结/重置网格转换（重置X形等）以确保所有网格一致
* 在3D建模软件中同时导入低多边形和高多边形网格以验证它们正确重叠
* 如果使用[按名称匹配](../../features/matching-by-name/matching-by-name.md)功能，请确保您的命名约定有效（您可以通过烘焙进行验证，然后查看应打印网格名称的日志文件）。

### 示例

以下是一个高多边形球体和低多边形球体的示例。 左侧网格不重叠，因为高多边形已被移开：

![](../../assets/baking-gradients.jpg)
