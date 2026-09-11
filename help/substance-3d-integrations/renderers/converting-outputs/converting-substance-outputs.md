---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/converting-substance-outputs.html"
breadcrumb-title: ''
description: 了解如何转换材料输出以匹配不同的渲染器要求和工作流程。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Converting Substance outputs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 转换Substance输出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# 转换Substance输出

## Substance Painter

您可以从Substance Painter中导出转换后的映射。 支持多种渲染预设，只需选择预设即可转换映射类型。 （转换基于metal/rough工作流程）。

![](../../assets/convertpainter.png){width="800px"}

## Substance增效工具

Substance增效工具将生成输出并自动为特定工作流创建材料。 但是，对于DCC应用程序和第三方渲染器，您可能需要手动转换金属/粗略输出。 以下集成支持自动渲染工作流程，并且将在需要时相应地转换任何映射类型：

* [玛雅Substance](../../3d-applications/maya/using-workflows/using-workflows.md)
* [3ds Max中的Substance](../../3d-applications/3ds-max/3ds-max.md)

## 自定义Substance

如果要构建自定义Substance，则可以创建渲染器所需的特定输出，例如Vray和Corona。 使用金属/粗糙度转换节点（“库”>“PBR实用程序”），您可以轻松地将base color、粗糙度和金属映射转换为特定的渲染器。

![](../../assets/convert-designer.png){width="600px"}
