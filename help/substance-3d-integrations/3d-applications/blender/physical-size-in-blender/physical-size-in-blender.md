---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/blender/physical-size-in-blender.html"
breadcrumb-title: ''
description: 使用物理尺寸设置，根据Blender中的真实维度缩放Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Physical size in Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blender中的物理尺寸
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Blender中的物理尺寸

Substance素材中的物理尺寸允许根据素材在世界上的大小对其进行缩放。 尺寸在Designer等Substance应用程序中设置，并显示在“插件”面板的“物理尺寸”部分中。

![](../../../assets/blender-physical-size.png)

启用物理尺寸后，素材将根据实际大小（以厘米为单位）进行平铺。 无论对象缩放程度如何，素材拼贴都将保持不变。 该功能可以通过在加载项面板中切换到物理尺寸着色器来启用。 调整对象比例后，应按ctrl/cmd+A应用比例以准确平铺物理尺寸纹理。

## 调整物理尺寸

可以调整映射节点中的值，以便对物理尺寸拼贴进行艺术控制。 此外，可以将对象（如“空”）用于“纹理坐标”输入，以使用输入对象的变换来控制纹理映射（请参阅下面的示例）。

![](../../../assets/blender-physical-szie-empty.gif)
