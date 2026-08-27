---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-emissive.html"
breadcrumb-title: ''
description: 在MODO中配置材料的emissive属性，以控制发光量和颜色设置。
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

## 使用Emissive（发光量和颜色）

Substance可以具有可选的emissive输出。 您可以在MODO中将其用作发光量和颜色。 启用emissive输出时，它将设置为发光量效果。 默认情况下，此声道在“纹理图像静止图像”选项卡下解释为线性。\
在着色器树中右键单击该纹理，然后选择复制。 然后，将复制的纹理设置为发光色彩效果。 然后，您可以对驱动发光量效果的纹理的高值和低值作出更改，以进一步增强该值。

>[!NOTE]
>
> 对于发光颜色的纹理集，需要在“图像静止图像”选项卡中将解析设置为sRGB。

要获得开花效果，需要在渲染面板中启用开花，并设置阈值和半径。

![](../../../assets/bloom.png)

对于虚实和Unity材料，Emissive输出由材料专门处理。\
虚构=虚构Emissive\
Unity = Unity排放

需要在“图像静止”选项卡中将虚构Emissive和Unity发射纹理从“线性”更改为“sRGB”。
