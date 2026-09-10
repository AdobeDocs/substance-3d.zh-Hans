---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/gpu-raytracing.html"
breadcrumb-title: ''
description: 支持硬件加速GPU 射线追踪，将烘焙计算速度提高25倍或更多，从而加快工作流程。
helpx_creative_field: ""
helpx_description: bakers > Features > GPU Raytracing
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU 射线追踪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 18%

---


# GPU 射线追踪

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

一些烘焙器支持在GPU上实现光线追踪的硬件加速，这通常可将计算速度提高25倍或以上。

## 硬件要求

如果系统符合以下要求，则会自动启用光线追踪：

* 安装了兼容的GPU\*（RTX系列、Titan V或GeForce 10xx）
* GPU驱动程序是最新版本
* 已安装Windows 10“Fall Creator”/ 10月更新（1809版）或更高版本\*\*

</td>
<td style="border: 0;" valign="top">

![GPU 射线追踪开/关比较](../../assets/rtx-ao-demo.gif "GPU 射线追踪开/关比较"){zoomable="yes"}

</td>
</tr>
</table>

\*：兼容的NVIDIA GPU包括使用Pascal体系结构或更高版本的所有GPU。 即GTX 10系列、Titan V系列、RTX 20系列或更新版本。

\*\*：要检查您的Windows版本，请单击“开始”菜单，键入“winver”并按Enter键。\
您可以通过Microsoft支持网站上的[专用页面](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update)获取更新。

>[!TIP]
>
> 如果您遇到问题，可以在应用程序首选项中禁用GPU 射线追踪。

## 支持的烘焙师

根据Substance 3D面包师版本，下表列出了每个面包师的GPU 射线追踪支持：

+++版本3及更高版本

| 烘焙 | 支持GPU 射线追踪 |
| --- | --- |
| 环境光遮蔽 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 弯曲法线 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| Color | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 弯曲 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 高度 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 法线 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 法线世界空间 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |



| 烘焙 | 支持GPU 射线追踪 |
| --- | --- |
| 不透明度蒙版 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 位置 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 位置低 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 厚度 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 已传输纹理 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 世界空间到切线空间 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |


+++

+++版本2

| 烘焙 | 支持GPU 射线追踪 |
| --- | --- |
| 环境光遮蔽 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 网格中的环境光遮蔽 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> \* |
| 网格中的弯曲法线 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> \* |
| 网格中的颜色 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |
| Convert UV to SVG | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 网格中的曲率 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> \* |
| 网格中的高度 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |
| 网格中的法线 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |



| 烘焙 | 支持GPU 射线追踪 |
| --- | --- |
| 来自网格的不透明度蒙版 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |
| 网格中的布局 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |
| 位置 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 网格中的厚度 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> \* |
| 已转移网格中的纹理 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> \* |
| 世界空间方向 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 世界空间法线 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |


\*：支持CPU射线追踪，该速度明显低于GPU 射线追踪。

+++
