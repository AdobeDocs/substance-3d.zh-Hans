---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/material-instance-definition-ue4.html"
breadcrumb-title: ''
description: 在Unreal Engine 4中使用Substance素材创建素材实例定义，以优化GPU渲染性能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Material Instance Definition - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物料实例定义 — UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# 物料实例定义 — UE4

您可以将UE4材质实例与Substance结合使用。 这样无需上传新素材即可处理，从而节省了GPU渲染流程中的一个大步骤。 可以在运行时或在编辑器中创建MID。 在版本4.24.0.3中，我们添加了对素材实例化的完全支持，并引入了一个新的素材模板Substance 引擎，其中具有模板支持的数字输出。 材质模板允许您确切定义要在UE4中配置Substance材质着色器的方式。

导入sbsar文件时，可选择要使用的模板。

![](../../../../assets/ue4-material-templates.png)

我们随附了用于处理位移、折射和世界对齐素材的模板，这些模板内置了用于调整拼贴、纹理大小、位移和发射参数的控件。 材质模板系统还允许您提供自己的自定义模板。

![](../../../../assets/ue4-material-instance-params.png)

## 在编辑器中创建材质实例

1. 右键单击Substance创建的UE4素材，然后选择“创建素材实例”。 这将创建UE4实例化素材。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/01-12?$png$&jpegSize=100&wid=592){width="560px"}
1. 右键单击Substance实例工厂，然后选择“创建图形实例”。 这将创建图形的一个实例，并创建另一个UE4材质。 删除新创建的UE4材料，因为这将不会使用它。

   ![](../../../../assets/02-10.png){width="300px"}
1. 双击在步骤1中创建的材质实例，并为所有映射启用“纹理”参数。
1. 将纹理设置为从步骤2创建的新INST纹理。 这会将素材实例设置为使用实例图形中的Substance输出映射。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/03-6?$png$&jpegSize=200&wid=1011){width="800px"}

您现在有一个UE4材质实例，它使用一组特定的Substance纹理。 这是在UE4项目中处理多种物质的一种更优化的方式。 要了解如何使用Blueprint创建MID，请查看此页面。 [蓝图(UE4)：动态素材实例](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
