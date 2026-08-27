---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/corona.html"
breadcrumb-title: ''
description: 在3ds Max中使用Substance材质，并采用“Specular/光泽度”工作流程和所需的映射，制作电晕渲染器。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Corona
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 科罗纳
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# 科罗纳

要使用Corona进行渲染，您可以使用从Substance Painter或Substance增效工具导出的映射。 Corona使用Specular/光泽度工作流程和1/IOR映射。 您需要以下地图：

* Diffuse
* 反射(Specular)
* Glossiness
* 1/IOR（已转换）

1/IOR映射只能从金属/粗糙度工作流程中转换，后者是Substance Designer和Substance Painter的默认工作流程。

1. 使用Corona预设从Substance Painter导出地图。
1. 对于自定Substance，可以使用设置为Vray预设的basecolor\_metallic\_roughness转换节点来创建自定义输出。
1. 对于3ds Max和Cinema 4D，使用层状电晕材料处理金属和介电材料，并绕过转换1/IOR映射的需要。

## 目录

* [用于3ds Max的电晕显示器](../../renderers/corona/corona-for-3ds-max/corona-for-3ds-max.md)
* [Corona -Substance Painter](../../renderers/corona/corona-painter/corona-substance-painter.md)
