---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/renderman/renderman-substance-painter.html"
breadcrumb-title: ''
description: 使用pxrSurfaceSubstance Painter和适当的输出转换导出Renderman的材料纹理。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Renderman > Renderman - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderman -Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Renderman -Substance Painter

Substance Painter2020.1 (6.1.0)支持&#x200B;[**pxrSurface**](https://rmanwiki.pixar.com/display/REN/PxrSurface)和pxrDisney [输出模板](https://docs.substance3d.com/display/SPDOC/Export)。

![](../../../assets/renderman.png)

建议使用&#x200B;**pxrSurface**&#x200B;进行输出。

![](../../../assets/pxrsurface.png)

## Renderman Shader (Maya - RM 23.1)

| Substance Painter导出 | PxrSurface |
| --- | --- |
| 漫射颜色 | 扩散/颜色 |
| 镜面粗糙度 | 主要Specular/粗糙度 |
| SpecularFaceColor | 主要Specular/脸部颜色 |
| 法线 | 全局/凹凸/PxrNormalMap →方向(Open GL) |
| 位移 | （红色通道） PxrDispTransform （结果F） → （显示标量） PxrDisplace （输出颜色） → (位移着色器) PxrSurfaceSG |
| GlowColor | 发光/颜色（增益= 1.0） |
| Presence | 全球/在线状态 |

>[!NOTE]
>
> 需要正确解释表示数据的地图。 有关详细信息，请参阅[色彩管理](../../../renderers/color-management/color-management.md)页面。
