---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/seams-are-visible-after-baking-a-normal-texture.html"
breadcrumb-title: ''
description: 通过调整填充、消除锯齿和UV布局，消除烘焙普通纹理中的可见接缝。
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seams are visible after baking a normal texture
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙常规纹理后，接缝可见
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# 烘焙常规纹理后，接缝可见

>[!WARNING]
>
> **问题**
> 
> 即使在干净的烘焙后，在UV网格边界处也可以看到法线映射接缝。

>[!NOTE]
>
> **说明**
> 
> 即使在完美的烘焙后，接缝仍然可见。 其主要原因是法向近似曲面信息转化为纹理。 有时，纹理会缺乏精度，或者必须在低多边形几何和高多边形几何之间补偿过多，以便达到足够的精度。 在其它情况下，几何与其法线图的渲染方式会影响其外观效果。

>[!NOTE]
>
> **解决方案**
> 
> 有几种可能的解决方案可以用来降低正常地图接缝的强度：
> 
> * 通常UV不会与像素对齐，这会导致锯齿并产生接缝。 有关详细信息，请参阅[此页面](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)。
>   * 增加纹理分辨率可能是减少此效果的一种方法。
>   * 将UV边界与像素对齐是减少此效果的另一种方法。
> * 增加着色器&#x200B;**品质**&#x200B;设置。 着色器品质会影响Specular反射的计算方式。 如果旋转了某些UV 岛，并且该参数太低，则可能产生可见的接缝。 有关详细信息，请参阅[此页面](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/pbr-metal-rough-172818827.html)。
