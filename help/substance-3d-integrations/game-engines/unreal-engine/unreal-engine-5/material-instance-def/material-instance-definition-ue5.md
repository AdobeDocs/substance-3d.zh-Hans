---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-instance-definition-ue5.html"
breadcrumb-title: ''
description: 使用虚实引擎5中的Substance材料创建材料实例定义，以优化GPU渲染性能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Instance Definition - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料实例定义 — UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# 材料实例定义 — UE5

可以将UE5材料实例与Substance一起使用。 这样无需将新材料上传到GPU渲染过程，即可节省该过程的一大步。 可以在运行时或在编辑器中创建MID。 在版本5.0.0中，我们增加了对材料实例化的完全支持。

## 在编辑器中创建材料实例

1. 右键单击Substance创建的UE5材料，然后选择“创建材料实例”。 这将创建一个UE5实例材料。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-31-at-6-07-08-pm?$png$&jpegSize=300&wid=1472)
1. 右键单击Substance实例工厂，然后选择“创建图形实例”。 这将创建该图形的一个实例，并创建另一个UE5材料。 删除新创建的UE5材料，因为这将不会使用它。

   ![](../../../../assets/screen-shot-2022-03-31-at-6-10-38-pm.png)
1. 双击在步骤1中创建的材料实例，然后为所有映射启用纹理参数。
1. 将纹理设置为在步骤2中创建的新INST纹理。 这将设置材料实例以使用实例图形中的Substance输出映射。

   ![](../../../../assets/screen-shot-2022-03-31-at-6-13-18-pm.png)

您现在有一个UE5材料实例，它使用一组特定的Substance纹理。 这是在UE5项目中处理多种物质的一种更优化的方式。 要了解如何使用蓝图创建MID，请查看此页面。 [蓝图(UE5)：动态材料实例](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
