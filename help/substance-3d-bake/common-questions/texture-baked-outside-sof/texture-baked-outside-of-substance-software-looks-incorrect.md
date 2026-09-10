---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/common-questions/texture-baked-outside-of-substance-software-looks-incorrect.html"
breadcrumb-title: ''
description: 解决Substance软件之外的纹理看起来不正确的原因，并了解如何修复色彩空间问题。
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Texture baked outside of Substance software looks incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在Substance软件外部烘焙的纹理看起来不正确
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 在Substance软件外部烘焙的纹理看起来不正确

>[!WARNING]
>
> **问题**
> 
> 为什么使用外部应用程序生成的纹理在Substance Painter中看起来不正确，而非Substance Bakers？

>[!NOTE]
>
> **解决方案**
> 
> 这个问题没有立即的解决方案，因为许多因素都可能导致这一问题：
> 
> * 验证Substance软件与外部应用程序之间的标准格式是否相同。 OpenGL为[X+， Y+， Z+]，DirectX为[X+， Y-， Z+]
>   * 在Substance Painter中，可以在[项目配置](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/interface/project-configuration)中更改正常格式。
>   * 在Substance Designer中，可以在[项目首选项](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-designer/using/workspace/preferences/project-settings)中更改常规格式。
> * 在网格并将其导入Substance软件之前，验证是否已对其进行三角化处理。 有关详细信息，请参阅[此页面](../../guides/triangulating-before-bak/triangulating-before-baking.md)。
