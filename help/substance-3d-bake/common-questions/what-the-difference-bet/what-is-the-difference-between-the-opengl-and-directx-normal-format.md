---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-questions/what-is-the-difference-between-the-opengl-and-directx-normal-format.html"
breadcrumb-title: ''
description: 了解OpenGL与法线贴图格式之间的差异以及何时使用它们。
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What is the difference between the OpenGL and DirectX normal format "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'OpenGL和DirectX标准格式有何区别 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# OpenGL和DirectX标准格式有何区别？

>[!WARNING]
>
> **问题**
> 
> OpenGL和DirectX标准格式有何区别？

>[!NOTE]
>
> **说明**
> 
> OpenGL和DirectX是两个图形API（函数集），程序员可在应用程序中使用，与GPU（图形处理单元）对话。 从法线图的角度来看，这种差异导致了如何解释RGB纹理的绿色通道。 OpenGL期望第一个像素位于底部，而DirectX期望第一个像素位于顶部。 这通常是在各种技术讨论中建议尝试反转法线图的绿色通道，以查看在反转像素值（第一个变为最后一个）时它是否表现更好。 OpenGL可称为&#x200B;**Y+**（自下而上），而DirectX称为&#x200B;**Y-**（自上而下）。
> 
> 要了解使用哪种格式，请参阅将在其中使用您的纹理的目标应用程序。
