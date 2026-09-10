---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/redshift/redshift-substance-painter.html"
breadcrumb-title: ''
description: 使用Substance Painter和适当的纹理设置导出Redshift渲染器的输出模板材料。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Redshift > Redshift - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Redshift -Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Redshift -Substance Painter

Substance Painter2020.1 (6.1.0)支持Redshift [输出模板](https://docs.substance3d.com/display/SPDOC/Export)用于金属/粗糙度(rsMaterial)。 只需使用Redshift模板导出即可生成与Redshift材料兼容的纹理。

![](../../../assets/rs-export.png)

## Redshift材料设置

| Substance Painter导出 | Redshift材料 |
| --- | --- |
| Color | Diffuse/颜色 |
| 粗糙度 | 反射/粗糙度(BRDF = GGX) |
| 金属度 | 反射/金属度（菲涅尔类型=金属度） |
| 法线 | 总体/凹凸图/rsBumpMap（输入图类型=切线空间法线 — Height比例= 1.0） |
| DisplaceHeightField | 着色器/ rsDisplacement TexMap（映射编码=Height字段） |
| 发射颜色 | 总体/排放（排放重量= 1.0） |

>[!NOTE]
>
> 需要正确解释表示数据的地图。 有关详细信息，请参阅[色彩管理](../../../renderers/color-management/color-management.md)页面。

## Maya/Redshift示例

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maya-example?$pjpeg$&jpegSize=300&wid=1583){width="800px"}
