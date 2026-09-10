---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-aggregate-substance.html"
breadcrumb-title: ''
description: 使用Blueprint聚合材料在高级工作流引擎5中的运行时合并多个Substance节点。
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

1. 使用“创建聚合Substance工厂”节点，并设置“输出工厂”和“输入工厂”。 “输出工厂”应具有一个纹理映射，该映射将用作“输入工厂”参数中的输入图像。
1. 使每个用作输入的输出纹理的SubstanceConnection对象具有相应值的名称（输出图形的输出名称和输入图形的输入参数名称）
1. 添加创建图形实例节点，并将“创建聚合Substance工厂”节点的结果与父材料一起插入工厂输入中，以充当模板（这可以是插件随附的默认\_substance材料之一）。
1. 创建一个Substance 图形实例变量并存储上一个node的结果。
1. 可选：设置任何所需的Substance参数（此示例为图形输出设置新的分辨率）。
1. 创建“异步”或“同步”渲染节点，并将要渲染的实例连接到Substance 图形实例变量。
1. 使用图形实例中的“获取动态材料实例”函数创建或获取现有材料实例。 将“名称”和“父材料中”留空将使用在步骤3中生成实例时使用的参数。
1. 添加一个“设置材料节点”，并将MID变量的值设置为“材料输入”。 对于目标，请将其设置为要应用材料的对象。
