---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/bump-and-displacement.html"
breadcrumb-title: ''
description: 使用MODO中材料的凹凸和位移贴图将表面细节和深度添加到模型中。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Bump and Displacement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 凹凸和位移
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# 凹凸和位移

使用凹凸和位移

Substance可以具有可选的Height输出。 您可以将其用作位移或凹凸。 启用Height后，它将设置为凹凸纹理效果。 对于Unity来说，它将会变成Unity Bump，而Unreal Bump将变成Unreal Bump。 然后，您可以选择Substance项材料并相应地设置凹凸振幅。 如果要将Height用作位移，可将材料图层效果更改为表面着色>位移。 然后在“材料参考”中，设置适当的“位移距离”。

![](../../../assets/bump-1.png)

在本例中，我使用虚构材料，但将虚构“Bump Layer”（凹凸图层）效果更改为“位移”。 然后在Substance项材料上，设置位移距离并相应地渲染细分级别。

![](../../../assets/dis.png)
