---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/physical-size-ue5.html"
breadcrumb-title: ''
description: 使用物理尺寸设置可根据虚构引擎5中的真实维度缩放Substance材料。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Physical Size - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物理尺寸- UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# 物理尺寸- UE5

Substance素材中的物理尺寸允许根据素材在世界上的大小对其进行缩放。 该值在Substance Designer中设置，并通过材料模板系统读入Unreal。\
父项中的[Substance\_Triplanar\_Template](../../../../game-engines/unreal-engine/unreal-engine-5/material-template-usage/out-the-box-material-tem/out-of-the-box-material-templates.md)材料包含如何使用物理尺寸缩放虚形材料的示例。



无论网格的放大值如何，材料都将根据其在世界范围内所占用的大小（以厘米为单位）进行平铺。 对于岩石材料（图1），每次测量为1.8米（180厘米）。

![](../../../../assets/rock-material-parameters.png)

包含物理尺寸数据的Substance材料的值将复制到任何名为physicalsize的现有材料矢量参数节点中。



由于UE5中的材料中没有位移值，因此物理尺寸模板会将三平面映射的值复制为X、Y、X。
