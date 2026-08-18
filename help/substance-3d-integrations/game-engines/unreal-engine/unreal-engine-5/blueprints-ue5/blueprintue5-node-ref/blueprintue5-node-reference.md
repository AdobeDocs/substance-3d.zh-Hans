---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-node-reference.html"
breadcrumb-title: ''
description: Unreal Engine 5中可用于物料操作的所有SubstanceBlueprint节点的参考指南。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Node Reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE5)节点引用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 0%

---


# Blueprint(UE5)：节点引用

## 常规Substance节点：

| 名称 | 输入 | 描述 |
| --- | --- | --- |
| **GetSubstances** | 输入： **材质** | 返回材料使用的Substance 图形实例数组。 如果您创建使用来自两个不同图形实例的纹理输出的材质，此函数将返回这两个图形实例。 |
| **GetSubstanceTextures** | 输入： **SubstanceGraphInstance** | 从Substance 图形实例输入参数返回所有已启用纹理和当前计算的纹理的数组。 |
| **GetGraphName** | 输入： **SubstanceGraphInstance** | 返回Designer中设置的图形名称。 |
| **GetFactoryName** | 输入： **SubstanceGraphInstance** | 返回用于创建传递到此节点的&#x200B;**SubstanceGraphInstance**&#x200B;的&#x200B;**GraphInstanceFactory**&#x200B;的名称。 |
| **GetSubstanceLoadingProgress** | 无 | 返回一个介于0和1之间的浮点，该浮点表示已完全装载的物质所占的百分比。 |
| **CreateGraphInstance** | 输入： **SubstanceInstanceFactory** — 要从中创建图形实例的工厂。输入： **GraphIndex** (int) — 要创建的图形的索引。 输入： **InstanceName** (FString) — 希望新实例具有的名称。 | 返回新的独立图形实例，该实例将一直持续到应用程序关闭。 |
| **DuplicateGraphInstance** | **SubstanceGraphInstance** — 要创建副本的图形实例。 | 返回新的独立图形实例，该实例将一直持续到应用程序关闭。 |
| **EnableInstanceOutputs** | 输入： **SubstanceGraphInstance** — 包含要启用输入的输出的图形实例： **OutputIndices** （int32数组） — 要启用的输出的索引。 | 如果之前已禁用，则创建在&#x200B;**SubstanceGraphInstance**&#x200B;中传递的纹理输出。 此功能与从&#x200B;**SubstanceGraphInstance**&#x200B;编辑器启用输出相同。 *注意：这不会使用新创建的纹理更新您的材质。 这需要在运行时使用新输出设置sampler参数来处理。* |
| **DisableInstanceOutput** | 输入： **SubstanceGraphInstance** — 包含要禁用输入的输出的图形实例： **OutputIndices** （int32数组） — 要禁用的输出的索引 | 如果启用，将禁用并删除在图形对象中传递的纹理输出 |
| **CopyInputParameters** | 输入： **SubstanceGraphInstance** — 要将值应用于Input的图形实例： **SubstanceGraphInstance** — 要从中获取值的图形实例 | 恢复Substance 图形实例输入参数的所有已更改输入值。 |
| **ResetInputParameters** | 输入：SubstanceGraphInstance | 将Substance 图形实例的输入值重置为默认值 |
| **SetGraphInstanceOutputSize** | 输入： **SubstanceGraphInstance**&#x200B;输入：宽度 — X坐标的纹理分辨率输入：Height- Y坐标的纹理分辨率 | 使用从参数传入的大小设置从此图形实例生成的所有输出的纹理分辨率。 注意：在CPU引擎上为Max 2048注意：在GPU引擎上为Max 4096 |
| **异步渲染** | **SubstanceGraphInstance** | 重新计算Substance 图形实例输入的输出纹理。 （非阻塞） |
| **同步渲染** | **SubstanceGraphInstance** | 重新计算Substance 图形实例输入的输出纹理。 （阻止） |

## 图形实例特定函数：

只能从图形实例调用

| 名称 | Input | 描述 |
| --- | --- | --- |
| GetDynamicMaterialInstance | 输入：名称（字符串） | 返回Substance的运行时动态素材实例，或者创建一个（如果不存在）。 对于来自substance值输出的大多数运行时值更改，需要动态素材实例。 |
| **GetInputNames** | 无 | 返回包含所有输入参数名称的字符串数组。 |
| **GetInputType** | 无 | 返回与此输入关联的数据类型。 |
| **SetInputInt** | 输入： **标识符** （字符串）输入： **输入值** （int数组） | 更改由标识符找到的输入值。 若要应用更改，必须使用&#x200B;**AyncRender**&#x200B;或&#x200B;**SyncRender**&#x200B;从游戏中渲染素材。 |
| **SetInputFloat** | 输入： **标识符** （字符串）输入： **输入值** （浮点数组） | 更改由标识符找到的输入值。 若要应用更改，必须使用&#x200B;**AyncRender**&#x200B;或&#x200B;**SyncRender**&#x200B;从游戏中渲染素材。 |
| **GetInputInt** | 输入： **标识符** （字符串） | 返回具有输入参数的当前值的ints数组。 |
| **GetInputFloat** | 标识符（字符串） | 返回具有输入参数的当前值的浮点数组。 |
| **SetInputBool** | 输入： **Bool** （布尔值）输入： **标识符** （字符串） | 采用布尔值以分配可切换输入值类型。 以前，只有将int值设置为1或0并铸造到布尔值才能实现此目的。 |
| **GetInputBool** | 输入： **标识符** （字符串） | 返回输入的当前布尔值。 |
| **SetIputColor** | 输入： **颜色** （线性颜色）输入： **标识符** (FString) | 输入FLinitialColor值以将颜色输入值类型指定给。 以前，只有通过设置浮点值并传入浮点数组，才能实现此目的。 |
| **GetInputColor** | 输入：标识符(FString) | 以UE4格式返回当前颜色值。 |
| **CreateAggregateSubstanceFactory** | 输入： **输出工厂** (SubstanceInstanceFactory)*创建输出并将用作输入工厂的输入的工厂。*&#x200B;输入： **输出工厂图形索引** （整数）*要合并的实体中的哪个图形。* 输入： **输入工厂** (SubstanceInputFactory)*将输出用作输出工厂的输入图像的工厂。*输入：**连接**（SubstanceConnections数组）*可使用Blueprint节点Make Array创建此库。 Substance连接是如何将输入链接到哪个输出的聚合节点的。* ** Return (SubstanceInstanceFactory)***可用于创建新组合实例的图形实例。* | 新的聚合Substance节点允许您采用两个Substance实例工厂并在运行时创建新的实例工厂，该工厂可用于创建新的图形实例。 这种特殊之处在于，您可以将其中一个组合图形实例的输出纹理连接到另一个组合图形实例的输入图像。 要从此新工厂创建Substance图形实例，请参阅我们的运行时图形实例文档。 |
| **SubstanceConnectionStruct** | 输入： **输出标识符** (FString)*要链接到输入中的纹理输出的标识符。* 输入： **输入标识符** (FString) | 由“创建聚合Substance工厂”用于指定如何使用新的输入纹理链接每个输出纹理。 |
