---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/normal-map-has-strange-colorful-gradients.html"
breadcrumb-title: ''
description: 通过检查网格法线、平滑组和UV映射，修复正常映射中奇异的彩色渐变。
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

烘焙器的输出是一组非常强的彩色渐变。

![](../../assets/color-gradient.png)


## 说明

烘烤过程中，当高多边形网格与低多边形网格不匹配时，通常会产生彩色渐变。 这种不匹配可以由以下原因解释：

* 高多边形和低多边形网格<b>不能正确重叠</b>（请参阅下图）。
* 高多边形是<b>缺少几何</b>，而低多边形尝试覆盖它。
* 高多边形或低多边形网格具有反转的顶点法线。

当发生这种情况时，烘焙过程会尝试匹配不存在的几何形状，从而导致一些空的东西。 烘焙器使用从纹理中的相邻像素提取的颜色填充此空白区域，以创建彩色渐变（除非禁用了<b>扩散</b>）。

## 解决方案

由于导致网格之间不重叠的可能原因很少，因此需要考虑几种解决方案：

* 确保冻结/重置网格变换（重置x形等）以确保所有网格一致
* 在3D建模软件中导入低多边形和高多边形网格以验证它们正确重叠
* 如果使用[按名称匹配](../../features/matching-by-name/matching-by-name.md)功能，请确保命名约定有效（可以通过烘焙进行验证，然后查看日志文件，该文件应打印网格名称）。

### 示例

以下是一个高多边形球体和低多边形球体的示例。 左侧的网格没有重叠，因为高多边形已被移走：

![](../../assets/baking-gradients.jpg)
