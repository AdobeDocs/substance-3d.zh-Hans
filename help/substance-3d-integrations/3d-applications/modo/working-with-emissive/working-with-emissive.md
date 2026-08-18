---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-emissive.html"
breadcrumb-title: ''
description: 在MODO中为Substance素材配置发射率属性，以控制发光量和颜色设置。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Emissive
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用发射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 使用发射器

## 使用发射度（发光量和颜色）

Substance可以具有可选的发射输出。 您可以在MODO中将其用作发光量和颜色。 启用发射输出时，它将设置为发光量效果。 默认情况下，此通道在“纹理图像静止”选项卡下被解释为“线性”。\
右键单击“着色器”树中的纹理，然后选择复制。 然后，将复制的发射纹理设置为发光颜色效果。 然后，您可以对驱动发光量效果的纹理的高值和低值作出更改，以进一步增强该值。

>[!NOTE]
>
> 对于设置为发光颜色的纹理，需要将解析设置为“图像静止图像”选项卡中的sRGB。

要获得开花效果，需要在渲染面板中启用开花，并设置阈值和半径。

![](../../../assets/bloom.png)

对于虚实和统一素材，发射输出由素材具体处理。\
虚构=虚构\
Unity = Unity排放

需要在“Image Still”（图像静止）选项卡中将虚发光和Unity Emission（统一发光）纹理从“Linear”（线性）更改为“sRGB”。
