---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers.html"
breadcrumb-title: ''
description: 在3D工作流程中将主要渲染器（例如Arnold、V-Ray、Redshift等）与Substance素材结合使用。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渲染器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---


# 渲染器

[Substance Source](https://source.substance3d.com/)中提供的Substance素材包含基于物理的着色器的输出，并支持[金属/粗糙度（默认工作流程）和Specular/光泽度](https://academy.substance3d.com/courses/pbrguides)。 了解渲染器素材支持的工作流程很重要。 根据渲染器，您可能可以直接使用Substance材质输出，或者可能需要转换输出纹理。 从Substance share下载的自定义Substance素材或素材可能不包含给定渲染器所需的适当输出。

![](../assets/outputs.png){width="200px"}

例如，对于“Arnold”或“Vray Next”，可以直接使用金属/粗糙度输出。 但是，使用Renderman的pxrSurface时，基色/金属输出需要转换为漫射和Specular表面颜色。 如果支持渲染器，Substance集成增效工具将自动处理这些转换。

使用Substance Painter，您可以选择一个[输出模板](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/export/export-window/export-window)，它将创建给定渲染器所需的适当映射类型。 如果默认情况下不支持渲染器，您还可以创建自定义输出模板。

**输出模板**

![](../assets/output-template.png){width="500px"}

## 渲染器参考线

* [转换Substance输出](../renderers/converting-outputs/converting-substance-outputs.md)
* [色彩管理](../renderers/color-management/color-management.md)
* [Arnold](../renderers/arnold/arnold.md)
* [弗赖](../renderers/vray/vray.md)
* [Renderman](../renderers/renderman/renderman.md)
* [Redshift](../renderers/redshift/redshift.md)
* [Maxwell](../renderers/maxwell/maxwell.md)
* [科罗纳](../renderers/corona/corona.md)
* [辛烷值](../renderers/octane/octane.md)
* [Keyshot](../renderers/keyshot/keyshot.md)
* [Thea](../renderers/thea/thea.md)
* [特立克](../renderers/maverick/maverick.md)
* [工具袋](../renderers/toolbag/toolbag.md)
* [周期和事件](../renderers/cycles-and-eevee/cycles-and-eevee.md)
