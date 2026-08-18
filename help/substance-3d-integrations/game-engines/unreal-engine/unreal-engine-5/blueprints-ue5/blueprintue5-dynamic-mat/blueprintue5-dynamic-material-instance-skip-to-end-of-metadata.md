---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-dynamic-material-instance-skip-to-end-of-metadata.html"
breadcrumb-title: ''
description: 使用蓝图，在Unreal Engine 5的运行时从Substance素材创建动态素材实例。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Dynamic Material Instance Skip to end of metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE5)动态素材实例跳到元数据结尾
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Blueprint(UE5)：动态素材实例跳到元数据结尾

1. 创建类型为“Substance实例工厂”的变量，并将默认值设置为“导入Substance工厂”。
1. 添加一个“创建图形实例”节点，并将Substance实例工厂与父材料一起插入工厂输入，以充当模板（这可以是插件随附的默认\_substance材料之一）。
1. 创建另一个变量，以存储在上一步中创建的Substance 图形实例对象。
1. 使用图形实例中的“获取动态素材实例”功能创建或获取现有素材实例。 将“名称”和“父材中”留空将使用在步骤2中生成实例时使用的参数。
1. 创建“材料”类型的变量。 这将是“材料实例动态”(Material Instance Dynamic，MID)。 将“获取动态素材实例”的返回值设置为变量。

   ![](../../../../../assets/dynamic-material-annotated-1.png)
1. 添加“设置材质节点”，并将MID变量的值设置为“材质输入”。 对于目标，请将其设置为要应用素材的对象。
1. 可选：设置任何所需的Substance参数（此示例使用预先存在的Substance Graph实例并将值复制到新实例）。
1. 创建“异步”或“同步”渲染节点，并将要渲染的实例连接到Substance 图形实例变量。
