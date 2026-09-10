---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/world-space-normals.html"
breadcrumb-title: ''
description: 使用高级网格的世界空间坐标将法线、正切和二项式保存到纹理中。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > World Space Normals
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 世界空间法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 世界空间法线

Baker允许将网格的正常格式、正切格式和二项式格式保存到纹理中。

**适用于：**

* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **烘焙类型** | 定义Baker将执行的计算类型。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>正常</strong>（默认）</li><li data-preserve-html="true"><strong>正切</strong></li><li data-preserve-html="true"><strong>次法线</strong></li></ul> |
| **法线图** | 输入普通纹理的路径，在计算期间将使用该路径添加详细信息。 |
| **正常方向** | 如果&#x200B;**烘焙类型**&#x200B;设置为&#x200B;**正常**，则定义输入纹理的正常格式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li></ul> |
