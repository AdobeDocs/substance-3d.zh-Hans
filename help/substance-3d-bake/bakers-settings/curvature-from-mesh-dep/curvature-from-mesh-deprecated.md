---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Baker中弃用的弯曲的参考。 请改用Baker中的更新弯曲。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh (deprecated)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 从弯曲（已弃用）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 从弯曲（已弃用）

来自网格的弯曲Baker从高多边形网格生成弯曲纹理。 它比基[弯曲](../../bakers-settings/curvature/curvature.md)Baker速度慢，但生成的结果更准确。

**适用于：**

* Substance Designer
* Substance自动化工具包

>[!NOTE]
>
> 由于Substance Designer2019.3，此Baker已弃用，我们建议改用新的[来自网格](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md)的弯曲Baker。

## 参数

| *参数* | *描述* |
| --- | --- |
| **强度** | 弯曲细节的强度。 如果启用了&#x200B;**软饱和**，则会禁用此参数。 |
| **柔和** **饱和** | 如果启用，弯曲详细信息将被柔化。 |
| **最大化范围** | 如果启用，弯曲详细信息将放在纹理范围容量内。 这意味着非常强的值将被定义为最大值，而所有其他值将根据此极值进行缩放。 |
