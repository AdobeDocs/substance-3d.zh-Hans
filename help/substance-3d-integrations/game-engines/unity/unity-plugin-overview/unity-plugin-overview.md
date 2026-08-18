---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-plugin-overview.html"
breadcrumb-title: ''
description: 了解适用于Unity的Substance 3D插件，包括版本支持、功能和集成功能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Plugin Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity插件概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Unity插件概述

## Unity版本支持

Substance 3D for Unity增效工具版本3.0.0目前支持Unity 2020 LTS及更高版本。

## 正在下载Substance包

1. 可从Unity Asset Store下载该插件： <https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208>

## 导入Substance材料

1. 在“项目”窗口中单击鼠标右键，然后选择“导入资源”，或将要导入的Substance素材拖动到“项目视图”面板中。
1. 浏览要导入的Substance素材。 Substance素材的文件扩展名为“.sbsar”。
1. Substance材料将导入到您的Unity项目中。

   1. sbsar资源将创建一个主导入文件以及一个文件夹，其中包含输出纹理和生成的Unity素材。
1. 然后，可以将素材拖放到“场景”视图的网格上，然后在“检查器”中编辑参数。

   ![](../../../assets/window-overview.png){width="1000px"}

>[!NOTE]
>
> **法线图转换**
> 
> Unity增效工具中的Substance将自动将DirectX转换为OpenGL。 使用[Substance Source](https://source.substance3d.com/)中的材质时，无需将法线方向更改为OGL。 如果要在Substance Designer中创建自己的素材，请确保使用默认DirectX着色器，因为增效工具将自动处理常规转换。 有关更多信息，请查看在Unity中使用法线。

## 更改参数

可以在“检查器”窗口中设置参数和分辨率。 请参阅[更改参数](../../../game-engines/unity/changing-parameters/changing-parameters.md)。

[unity\_tweaking\_parameters.mp4](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/download/attachments/186056716/unity-tweaking-parameters.mp4)

## Unity渲染管道支持

Substance 3D增效工具支持HDRP和URP。 更多信息即将发布。

## 如何学习教程
