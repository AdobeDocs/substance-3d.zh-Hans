---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-aggregate-substance.html"
breadcrumb-title: ''
description: 使用Blueprint聚合Substance实现高级工作流程，在虚幻引擎5的运行时组合多个工作流素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE5)聚合Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Blueprint(UE5)：聚合Substance

1. 使用“创建聚合Substance工厂”节点，并设置“输出工厂”和“输入工厂”。 “输出工厂”应具有纹理映射，该映射在“输入工厂”参数中用作输入图像。
1. 使每个输出纹理的SubstanceConnection对象用作具有相应值的名称（输出图表的输出名称和输入图表的输入参数名称）的输入
1. 添加一个“创建图形实例”节点，并将“创建聚合Substance工厂”节点的结果连同父材料一起插入工厂输入中，以充当模板（这可以是插件随附的默认\_substance材料之一）。
1. 创建一个Substance 图形实例变量并存储上一个node的结果。
1. 可选：设置任何所需的Substance参数（此示例为图形输出设置新的分辨率）。
1. 创建“异步”或“同步”渲染节点，并将要渲染的实例连接到Substance 图形实例变量。
1. 使用图形实例中的“获取动态素材实例”功能创建或获取现有素材实例。 将“名称”和“父材中”留空将使用在步骤3中生成实例时使用的参数。
1. 添加“设置材质节点”，并将MID变量的值设置为“材质输入”。 对于目标，请将其设置为要应用素材的对象。
