---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/plugin-overview-ue4.html"
breadcrumb-title: ''
description: 了解如何通过Substance增效工具概述指南，在Unreal Engine 4中导入和使用Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Plugin Overview - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 增效工具概述 — UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# 增效工具概述 — UE4

## 导入Substance

1. 在“Content Browser”（内容浏览器）中，点击“Import”（导入）按钮，然后浏览找到Substance.sbsar文件。
1. 在“Substance导入”选项中，您可以设置将创建的INST和材质名称。 导入操作将创建SubstanceINST和Factory以及生成的纹理。 将使用Substance纹理创建UE4素材作为素材通道的输入。

## 更改参数

1. 双击SubstanceINST项以打开“参数”窗口。
1. 重置按钮会将Substance参数重置为默认值。 导出和导入预设将使用编辑器中设置的值导出Substance预设文件(.sbspr)。 您也可以导入预设。
1. 在“输出”中，可以禁用和启用生成纹理的输出。
1. 输出大小允许您更改纹理大小。
1. 随机植入将更改种子值以生成纹理。 这有利于随机化材料。
1. “参数”部分允许您扭曲材料。

![](../../../../assets/param.png){width="600px"}
