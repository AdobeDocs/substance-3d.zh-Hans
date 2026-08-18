---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-instance-definition-ue5.html"
breadcrumb-title: ''
description: 在Unreal Engine 5中使用Substance素材创建素材实例定义，以优化GPU渲染性能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Instance Definition - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物料实例定义 — UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# 物料实例定义 — UE5

您可以将UE5材质实例与Substance结合使用。 这样无需将新素材上传到GPU渲染流程，即可在GPU渲染流程中节省大量时间。 可以在运行时或在编辑器中创建MID。 在版本5.0.0中，我们添加了对材质实例化的完全支持。

## 在编辑器中创建材质实例

1. 右键单击Substance创建的UE5素材，然后选择“创建素材实例”。 这将创建UE5实例材质。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-31-at-6-07-08-pm?$png$&jpegSize=300&wid=1472)
1. 右键单击Substance实例工厂，然后选择“创建图形实例”。 这将创建图形的一个实例，并创建另一个UE5材质。 删除新创建的UE5材料，因为这将不会使用它。

   ![](../../../../assets/screen-shot-2022-03-31-at-6-10-38-pm.png)
1. 双击在步骤1中创建的材质实例，并为所有映射启用“纹理”参数。
1. 将纹理设置为从步骤2创建的新INST纹理。 这会将素材实例设置为使用实例图形中的Substance输出映射。

   ![](../../../../assets/screen-shot-2022-03-31-at-6-13-18-pm.png)

您现在有一个UE5材质实例，它使用一组特定的Substance纹理。 这是在UE5项目中处理多种物质的一种更优化的方式。 要了解如何使用蓝图创建MID，请查看此页面。 [蓝图(UE5)：动态素材实例](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
