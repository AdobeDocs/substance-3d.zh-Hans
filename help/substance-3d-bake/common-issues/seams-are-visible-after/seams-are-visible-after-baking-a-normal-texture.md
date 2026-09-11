---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-issues/seams-are-visible-after-baking-a-normal-texture.html"
breadcrumb-title: ''
description: 通过调整填充、消除锯齿和UV布局，消除烘焙的正常纹理中的可见接缝。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seams are visible after baking a normal texture
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙普通纹理后，接缝可见
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# 烘焙普通纹理后，接缝可见

>[!WARNING]
>
> **问题**
> 
> 接缝在网格的UV边界处可见，即使进行了一次干净的烘焙。

>[!NOTE]
>
> **说明**
> 
> 即使在完美烘焙后，仍然可以看到接缝。 其主要原因是法线逼近曲面信息转化为纹理。 有时，纹理精度不高或需要在低多边形和高多边形几何之间补偿过多，以致于不够精确。 在其它情况下，几何与其法线图的渲染方式会影响其外观效果。

>[!NOTE]
>
> **解决方案**
> 
> 我们可以通过几种可能的解决方案来降低接缝的强度：
> 
> * 通常UV不会与像素对齐，这会导致锯齿并生成接缝。 有关详细信息，请参阅[此页面](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)。
>   * 提高纹理分辨率可能会降低这种效果。
>   * 将UV边框与像素对齐是减少这种效果的另一种方法。
> * 增加着色器&#x200B;**质量**&#x200B;设置。 着色器质量会影响Specular反射的计算方式。 如果某些UV 岛被旋转，并且该参数太低，则可能产生可见的接缝。 有关详细信息，请参阅[此页面](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/spdoc/pbr-metal-rough-172818827.html)。
