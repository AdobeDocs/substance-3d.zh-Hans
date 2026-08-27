---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-substance-material-parameters.html"
breadcrumb-title: ''
description: 使用BlueprintSubstance进行动态材料控制，在运行时在不真实引擎4中更改材料参数。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Substance material parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE4)材料参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Blueprint(UE4)：材料参数Substance

## 更改浮点参数：

您将使用[设置输入Float节点](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-node-reference-151584784.html)来更改float、color(float4)和布尔值substance参数。

1. 创建类型为“Substance 图形实例”的变量作为引用。
1. 创建一个“设置输入Float节点”，并将目标设置为“Substance 图形实例”变量。
1. 在“设置输入Float”节点上，将标识符设置为要更改的Substance参数的名称。\
   *\*可以通过打开标识符INST并将鼠标悬停在参数名称上来查找Substance名称。 标识符名称将显示在工具提示弹出窗口中。*
1. 在“输入Float节点”上，拖出一个连接并创建一个Make Array Node。 Make Array节点的索引为0。 索引0对应于浮点值。
1. 创建“异步”或“同步”渲染节点，并将执行行从“设置输入”Float连接到“渲染节点”。 将要渲染的实例设置为Substance 图形实例变量。\
   *\*&#x200B;异步未阻止，同步正在阻止。*

![](../../../../../assets/steps.png){width="800px"}

## 布尔值参数

使用“设置输入布尔值”更改布尔值参数。

![](../../../../../assets/setbool.png){width="800px"}

## 颜色参数

颜色参数可使用“设置输入颜色”进行更改。

![](../../../../../assets/setcolor.png){width="800px"}

## 更改Integer参数：

整数参数的工作方式与“设置输入浮点”相同。 您将使用Set Input Integer节点。

![](../../../../../assets/int.png)

## 标识符

您可以在substance INST中找到参数的标识符。 将鼠标移到参数上，工具提示将显示标识符名称。 这是在Substance Designer输出的标识符字段中设置的名称。

![](../../../../../assets/indent-1.png){width="800px"}
