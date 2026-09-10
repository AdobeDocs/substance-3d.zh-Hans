---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/normal-texture-looks-faceted.html"
breadcrumb-title: ''
description: 通过平滑网格法线和调整平滑组设置，修复正常纹理中多面外观的问题。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal texture looks faceted
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常纹理看起来是多面的
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 正常纹理看起来是多面的

>[!WARNING]
>
> **问题**
> 
> 烘焙“正常”纹理后，该网格看起来呈多面状态，或者每个脸部在其中都可见。
> 
> ![](../../assets/normal-faceted.jpg)

>[!NOTE]
>
> **说明**
> 
> 烘焙法线会产生这种结果的主要原因是低模网格法线设置不正确。 每个脸部的每一边都是一个硬边，使得与高多边形网格匹配时的光线投影忽略邻域信息，产生接缝或无意识信息。 虽然在网格上显示的结果可能不错，但这可能会导致稍后出现着色问题，应予以解决。

>[!NOTE]
>
> **解决方案**
> 
> 主要解决的方法是对顶点法则或低模网格进行重做，准确的命名过程取决于3D建模软件：
> 
> * 在胡迪尼的Maya使用&#x200B;**平均法线**。
> * 在3DS Max中使用&#x200B;**一个平滑组**。
> * 在混合器中使用&#x200B;**平滑阴影**。
> * 从zBrush导出的网格将始终刻面并且应在其他软件中进行清理。
> 
> 请注意，这可能不够：请确保这些设置还在导出网格时保存/生成顶点常规或着色信息。
