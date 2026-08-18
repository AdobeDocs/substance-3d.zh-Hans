---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/home.html"
breadcrumb-title: ''
description: 了解如何使用Substance Bakers将基于网格的信息计算到纹理文件中，并增强您的纹理化工作流程。
helpx_creative_field: ""
helpx_description: bakers > Home
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance Bakers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 13%

---


# Substance Bakers

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<b>Substance Bakers</b>是一组高级算法，用于将基于网格的信息计算到纹理文件中。 任何拥有3D网格的艺术家都可以使用它们来利用高级纹理方法。 烘焙过程是Substance软件工作流程的核心，旨在提供<b>强大的工具</b>和<b>自动纹理化</b>。

本文档介绍了烘焙</b>的<b>基础知识和<b>常见问题</b>以及处理此流程时可能遇到的错误。

</td>
<td width="58.30%" style="border: 0;" valign="top">

![](../assets/optim-baker-home.png){width="400px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 快速入门

* [烘焙是什么？](../getting-started/what-is-baking/what-is-baking.md)
* 烘焙方式：
  * [Substance 3D Painter](../getting-started/software-interface/3d-painter/substance-3d-painter.md)
  * [Substance 3D Designer](../getting-started/software-interface/3d-designer/substance-3d-designer.md)
  * [Substance 3D自动化工具包](../getting-started/software-interface/3d-automation-toolkit/substance-3d-automation-toolkit.md)
* [每个软件的可用性](../getting-started/availability-per-software/availability-per-software.md)
* [兼容的3D软件](../getting-started/compatible-3d-software/compatible-3d-software.md)
* [教程](../getting-started/tutorials/tutorials.md)

</td>
<td style="border: 0;" valign="top">

### 面包师设置

* [通用参数](../bakers-settings/common-parameters/common-parameters.md)
* [环境光遮蔽](../bakers-settings/ambient-occlusion/ambient-occlusion.md)
* [来自网格的环境遮蔽](../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)
* [从网格弯曲法线](../bakers-settings/bent-normals-from-mesh/bent-normals-from-mesh.md)
* [网格中的颜色贴图](../bakers-settings/color-map-from-mesh/color-map-from-mesh.md)
* [Convert UV to SVG](../bakers-settings/convert-uv-to-svg/convert-uv-to-svg.md)
* [弯曲](../bakers-settings/curvature/curvature.md)
* [网格的曲率](../bakers-settings/curvature-from-mesh/curvature-from-mesh.md)
* [网格的曲率（已弃用）](../bakers-settings/curvature-from-mesh-dep/curvature-from-mesh-deprecated.md)
* [网格中的高度贴图](../bakers-settings/height-map-from-mesh/height-map-from-mesh.md)
* [网格中的法线贴图](../bakers-settings/normal-map-from-mesh/normal-map-from-mesh.md)
* [Opacity Mask from Mesh](../bakers-settings/opacity-mask-from-mesh/opacity-mask-from-mesh.md)
* [位置](../bakers-settings/position/position.md)
* [来自网格的位置图](../bakers-settings/position-map-from-mesh/position-map-from-mesh.md)
* [网格中的厚度贴图](../bakers-settings/thickness-map-from-mesh/thickness-map-from-mesh.md)
* [已从网格中转移纹理](../bakers-settings/transferred-texture-from/transferred-texture-from-mesh.md)
* [世界空间方向](../bakers-settings/world-space-direction/world-space-direction.md)
* [世界空间法线](../bakers-settings/world-space-normals/world-space-normals.md)

</td>
<td style="border: 0;" valign="top">

### 参考线

* [错误和警告消息](../guides/error-and-warning-mes/error-and-warning-messages.md)
* [性能和优化](../guides/performances-and-opt/performances-and-optimizations.md)
* [烘焙前三角化](../guides/triangulating-before-bak/triangulating-before-baking.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 功能

* [几何缓存](../features/geometry-cache/geometry-cache.md)
* [GPU 射线追踪](../features/gpu-raytracing/gpu-raytracing.md)
* [按名称匹配](../features/matching-by-name/matching-by-name.md)
* [切线空间](../features/tangent-space/tangent-space.md)

</td>
<td style="border: 0;" valign="top">

### 常见问题

* [如何导出已烘焙贴图？](../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md)
* [是否将抖动应用于烘焙纹理？](../common-questions/dithering-applied-baked/is-dithering-applied-to-baked-textures.md)
* [是否应该启用“计算每个片段的切线空间”？](../common-questions/should-enable-compute-tan/should-i-enable-compute-tangent-space-per-fragment.md)
* [在Substance软件外部烘焙的纹理看起来不正确](../common-questions/texture-baked-outside-sof/texture-baked-outside-of-substance-software-looks-incorrect.md)
* [什么是Asbin文件？](../common-questions/what-are-assbin-files/what-are-assbin-files.md)
* [烘焙纹理的位深度是什么？](../common-questions/what-the-bit-depth-baked/what-is-the-bit-depth-of-baked-textures.md)
* [OpenGL和DirectX标准格式有何区别？](../common-questions/what-the-difference-bet/what-is-the-difference-between-the-opengl-and-directx-normal-format.md)
* [为什么烘焙或导出后的纹理会出现奇怪的拉伸？](../common-questions/why-are-there-strange-str/why-are-there-strange-stretches-in-my-textures-after-baking-or-exporting.md)
* [为什么“按名称匹配”无法用于环境遮蔽/Thickness？](../common-questions/why-matching-name-not-wor/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.md)
* [为什么烘焙后我的网格完全变黑了？](../common-questions/why-mesh-fully-black-aft/why-is-my-mesh-fully-black-after-baking.md)

</td>
<td style="border: 0;" valign="top">

### 常见问题

* [UV接缝上的锯齿](../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)
* [面包机输出完全为黑色或为空](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/baker-output-is-fully-black-159451835.html)
* [无法通过网格中的颜色映射进行烘焙](../common-issues/baking-failed-with-color/baking-failed-with-color-map-from-mesh.md)
* [黑着色十字在网格表面上可见](../common-issues/black-shading-cross-are/black-shading-cross-are-visible-on-the-mesh-surface.md)
* [网格部分之间出血](../common-issues/mesh-parts-bleed-between/mesh-parts-bleed-between-each-other.md)
* [正常地图具有奇怪的彩色渐变](../common-issues/normal-map-has-strange/normal-map-has-strange-colorful-gradients.md)
* [正常纹理看起来是多面的](../common-issues/normal-texture-looks-fac/normal-texture-looks-faceted.md)
* [烘焙常规纹理后，接缝可见](../common-issues/seams-are-visible-after/seams-are-visible-after-baking-a-normal-texture.md)
* [每张脸上都可以看到接缝](../common-issues/seam-visible-every-face/seam-visible-on-every-face.md)

</td>
</tr>
</table>
