---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/arnold/arnold-substance-painter.html"
breadcrumb-title: ''
description: 将Arnold渲染器的输出模板与aiStandard材料结合使用以进行基于物理的渲染。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Arnold > Arnold - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arnold -Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# Arnold -Substance Painter

Substance Painter2020.1 (6.1.0)附带使用[aiStandard材料](https://docs.arnoldrenderer.com/display/A5AFMUG/Standard+Surface)的Arnold的[输出模板](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/getting-started/export/output-templates/export-presets)。

![](../../../assets/arnold-export.png){width="800px"}

## Arnold Standard着色器（Arnold 5及更高版本）

| Substance Painter导出 | Arnold AiStandardSurface |
| --- | --- |
| 底色 | 基色/颜色 |
| 粗糙度 | Specular/粗糙度 |
| 金属度 | 基本/金属性 |
| 法线 | (**Maya**)几何/凹凸映射/凹凸2d（用作切线空间法线） （**3ds** **最大**）位图→法线 |
| 高度 | (**Maya**)着色器/位移(**3ds** **Max**)对象修饰符→Arnold属性→位移→使用映射 |
| 放射 | 发射/颜色（发射重量= 1.0） |
| anisotropy level（未包含在默认Arnold输出模板中） | (**Maya**)外套/各向异性(**3ds** **Max**)外套/各向异性 |
| anisotropy level（未包含在默认Arnold输出模板中） | (**Maya**)外套/旋转（**3d** **最大**）外套/旋转 |

>[!NOTE]
>
> 需要正确解释表示数据的地图。 有关详细信息，请参阅[色彩管理](../../../renderers/color-management/color-management.md)页面。
