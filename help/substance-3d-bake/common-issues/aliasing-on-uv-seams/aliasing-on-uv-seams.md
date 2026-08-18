---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/aliasing-on-uv-seams.html"
breadcrumb-title: ''
description: 通过调整消除锯齿和填充设置，修复烘焙期间UV接缝上出现的锯齿伪影。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Aliasing on UV Seams
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV接缝上的锯齿
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# UV接缝上的锯齿

>[!WARNING]
>
> **问题**
> 
> 烘烤后，UV接缝的边界上出现黑点或点：
> 
> ![](../../assets/edge-aliasing.png)

>[!NOTE]
>
> **说明**
> 
> 当贝克将信息写入纹理时，它必须从几何转换为像素。 此信息的处理可能会导致[锯齿](https://en.wikipedia.org/wiki/Aliasing)。 出现锯齿的原因通常是UV的几何形状与像素网格不对齐，或者UV覆盖的像素不足以提供足够的分辨率。
> 
> 在下图中，几何形状为红色叠加。 如果几何形状覆盖面包师表面的一半以上（白色正方形是满像素，黑色正方形是空像素），面包师会将像素标记为满像素。 在右图像中，像素网格的分辨率是它的两倍，因此可以更精确地表示几何形状。
> 
> ![](../../assets/aliasing-example-large.png)
> 
> ![](../../assets/aliasing-example-small.png)

>[!NOTE]
>
> **解决方案**
> 
> * 提高面包师的输出纹理分辨率。
> * 增加“消除锯齿”设置（注意：计算起来可能需要较长时间）。
> * 在3D建模软件的UV编辑器中，将UV对齐像素网格。
> * 提供更好的UV纹理比。
