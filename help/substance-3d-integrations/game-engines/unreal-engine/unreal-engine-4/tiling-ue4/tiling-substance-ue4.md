---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/tiling-substance-ue4.html"
breadcrumb-title: ''
description: 通过将纹理Substance坐标节点和标量参数添加到材质中，在Unreal Engine 4中拼贴纹理节点。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Tiling Substance - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拼贴Substance- UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# 拼贴Substance- UE4

要平铺Substance纹理，您需要添加纹理坐标节点，并将其乘以标量参数。

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/ExpressionReference/Coordinates/#texturecoordinate>

要为U和V拼贴创建参数，您可以使用“追加矢量”并将此矢量乘以TexCoord。 这允许您单独设置U和V磁贴数量。

![](../../../../assets/tiling-3.png){width="800px"}
