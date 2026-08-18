---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-aggregate-substance.html"
breadcrumb-title: ''
description: 使用Blueprint聚合Substance实现高级工作流，在虚幻引擎4的运行时组合多个工作流素材。
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

新的聚合Substance节点允许您采用两个Substance实例工厂，并在运行时创建新的实例工厂，该工厂可用于创建新的图形实例。 这种特殊之处在于，您可以将其中一个组合图形实例的输出纹理连接到另一个组合图形实例的输入图像。 要从此新工厂创建Substance图形实例，请参阅我们的运行时图形实例文档。 [材质实例定义 — UE4](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/material-instance-definition-157352129.html)

1. 导入要使用的Substance。
1. 创建类型为&#x200B;**Substance 图形实例**&#x200B;的变量“AggregateGraphInstance”。
1. 创建类型为&#x200B;**材质**&#x200B;和&#x200B;**材质实例动态**&#x200B;的变量
1. 创建&#x200B;**建立Substance连接**&#x200B;并设置输出和输入标识符。
1. 创建&#x200B;**聚合Substance实例工厂**&#x200B;并设置输出和输入工厂。
1. 创建&#x200B;**Graph实例**&#x200B;并设置实例名称。
1. 设置&#x200B;**聚合图形实例**&#x200B;变量。
1. 在步骤7中使用&#x200B;**获取Substance纹理**&#x200B;从聚合图形实例获取Substance纹理。
1. 使用步骤3中的素材变量作为父级创建&#x200B;**动态素材实例**。
1. 从步骤3设置MID变量。
1. 使用带MID变量的&#x200B;**设置材质**&#x200B;来设置网格的材质。

   ![](../../../../../assets/a2-3.png){width="800px"}
1. 如“动态素材实例”文档中所示设置素材的通道（步骤11-19）\
   [蓝图(UE4)：动态素材实例](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)

   ![](../../../../../assets/a4-3.png){width="800px"}
