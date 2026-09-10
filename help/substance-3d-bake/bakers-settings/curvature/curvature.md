---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature.html"
breadcrumb-title: ''
description: 从网格中提取弯曲信息以创建纹理来加亮几何图形的型腔和边缘。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弯曲
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 3%

---


# 弯曲

曲率烘焙器允许提取曲率纹理。 此纹理包含与几何相关的型腔和边信息。

纹理属性定义为：

* 黑色值表示凹形区域。
* 白色值表示凸形区域。
* 灰度值表示中性区域（主要是平坦）。

**适用于：**

* Substance Designer
* Substance自动化工具包
* Substance Painter

## 参数

| *参数* | *描述* |
| --- | --- |
| **算法** | 定义如何在网格上计算弯曲信息。 |
| **详细信息** | 控制弯曲中信息的强度。 较高的值可能产生更多的细节，但不太精细。 |
| **启用接缝** | 如果启用，烘焙师将尝试通过将边框处的纹理从一侧复制到另一侧来减少UV 岛之间的接缝。 |
| **接缝** **强度** | 如果已启用&#x200B;**启用接缝**，则此参数将控制接缝修复的强度。 |
