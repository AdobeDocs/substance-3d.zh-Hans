---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-aggregate-substance.html"
breadcrumb-title: ''
description: 使用Blueprint聚合材料在高级工作流引擎4中的运行时合并多个Substance节点。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE4)聚合Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Blueprint(UE4)：聚合Substance

新的聚合Substance节点允许您采用两个Substance实例工厂，并在运行时创建新的实例工厂，该工厂可用于创建新图形实例。 这种特殊之处在于，您可以将其中一个组合图形实例的输出纹理连接到另一个组合图形实例的输入图像。 要从此新工厂创建Substance图形实例，请参阅我们的运行时图形实例文档。 [材料实例定义 — UE4](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/material-instance-definition-157352129.html)

1. 导入要使用的Substance。
1. 创建类型为&#x200B;**Substance 图形实例**&#x200B;的变量“AggregateGraphInstance”。
1. 创建类型为&#x200B;**材料**&#x200B;和&#x200B;**材料动态实例**&#x200B;的变量
1. 创建&#x200B;**建立Substance连接**&#x200B;并设置输出和输入标识符。
1. 创建&#x200B;**聚合Substance实例工厂**&#x200B;并设置输出和输入工厂。
1. 创建&#x200B;**图形实例**&#x200B;并设置实例名称。
1. 设置&#x200B;**聚合图形实例**&#x200B;变量。
1. 在步骤7中使用&#x200B;**获取纹理**&#x200B;从聚合图形实例获取SubstanceSubstance。
1. 使用步骤3中的材料作为父级创建&#x200B;**动态实例实例**。
1. 从步骤3设置MID变量。
1. 使用带MID材料的&#x200B;**设置材料**&#x200B;设置网格变量。

   ![](../../../../../assets/a2-3.png){width="800px"}
1. 按照动态材料文档中的说明设置实例通道（步骤11-19）\
   [蓝图(UE4)：动态素材实例](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)

   ![](../../../../../assets/a4-3.png){width="800px"}
