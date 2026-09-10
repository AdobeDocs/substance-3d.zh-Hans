---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5.html"
breadcrumb-title: ''
description: 在Unreal引擎5中创建和使用材料模板，以定义Substance输出节点如何连接到材料输入。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物料模板用途 — UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 物料模板用途 — UE5

材料模板允许用户为物质创建基础材质，以用作将输出节点连接到材料中输入的模板。\
将自动使用与材料输入具有相同名称和类型的输出。 此父材料示例包含一个“baseColor”纹理示例节点，如果Substance具有也名为“baseColor”的纹理输出，则会填充此节点。\
![](../../../../assets/parent-material-sample.png)

Substance输出支持更新纹理、单个浮点或int标量值以及矢量(2-4)值。 要在运行时使用float或int输出，必须从图形获取dynamicMaterialInstance，因为constantMaterialInstances（在编辑器中生成的任何材料）无法在运行时更改标量值。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/scalar-value?$png$&jpegSize=100&wid=245)

Substance图形实例将尝试在创建时填写所有相关输出值。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-04-01-at-4-38-31-pm?$png$&jpegSize=200&wid=1076)
