---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-normals.html"
breadcrumb-title: ''
description: 在MODO中配置法线映射方向设置，以确保使用Substance素材正确进行法线映射渲染。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Normals
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# 使用法线

使用正常数据 — 设置正确的方向

构建StockSubstance是为了使用DX法线方向。 但是，MODO使用OGL。 通过将“法线格式”参数设置为1.0，可以反向法线。 Substance增效工具将仅解释Substance中设置的参数。 您可能会遇到一个没有“normal\_format”参数的Substance，因为该控件要由Substance的作者添加到自定义Substance中。 如果遇到没有此参数的Substance，可以翻转法线贴图纹理图层上的绿色通道以修复方向。

>[!NOTE]
>
> 仅当Substance具有错误的法线方向且作者未创建在Substance参数中翻转法线的控件时，才需要翻转绿色通道

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/normal-1.png)

</td>
<td style="border: 0;" valign="top">

![](../../../assets/invert-2.png)

</td>
</tr>
</table>
