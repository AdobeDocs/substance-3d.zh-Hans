---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/world-space-direction.html"
breadcrumb-title: ''
description: 在世界空间中计算矢量方向，并将它们存储到纹理中用于方向效果和蒙版。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > World Space Direction
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 世界空间方向
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---


# 世界空间方向

Baker允许计算世界空间到纹理中的矢量方向。

**适用于：**

* Substance Designer
* Substance自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **输入方向** | 定义计算方向的输入。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>从纹理</strong>：矢量方向由输入纹理定义。</li><li data-preserve-html="true"><strong>从统一矢量</strong>（默认）：矢量方向用X、Y、Z滑块定义。</li></ul> |
| **正常方向** | 定义输出纹理的标准格式。 这会根据格式反转绿色通道。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li></ul> |
| **X Y Z** | 如果&#x200B;**输入方向**&#x200B;设置为&#x200B;**从统一矢量**，则使用滑块定义方向矢量的3个分量。 |
| **方向文件** | 输入纹理文件的路径，用于定义方向矢量（如果&#x200B;**输入方向**&#x200B;设置为&#x200B;**来自纹理**）。 |
