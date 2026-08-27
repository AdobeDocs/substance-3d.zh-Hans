---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/curvature-from-mesh.html"
breadcrumb-title: ''
description: 使用射线追踪从高多边形网格生成精确的弯曲纹理以进行精确的边缘检测。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格的曲率
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# 网格的曲率

来自网格烘焙器的曲率从高多边形网格生成曲率纹理。 速度比基本[曲率](../../bakers-settings/curvature/curvature.md)面包机慢，但生成的结果更准确。

**适用于：**

* Substance Designer
* Substance自动化工具包
* Substance Painter

## 参数

| *参数* | *描述* |
| --- | --- |
| **次生射线** | 读取附近几何图形所发射的光线量。 较高的值会产生较少的杂色，但计算时间较长。 默认值为32。 |
| **采样半径** | 计算几何曲面处的弯曲时，将附近的几何考虑到多远。 较高的值可能产生较强边缘，而较低的值可能产生较细的边缘，但会丢失信息。 |
| **相对于定界框** | 定义采样半径是相对于网格的大小，还是定义为基于单位的距离。 |
| **自交集** | 按弯曲射线名称匹配。 指示Baker应如何匹配低多边形和高多边形几何。 它可用于过滤烘焙过程，而无需手动分离（分解）网格。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>始终</strong>（默认）：低多边形网格与每个高多边形网格匹配。</li><li data-preserve-html="true"><strong>按网格名称</strong>：按网格名称过滤网格，以避免与不需要的几何相匹配。</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md)。 |
| **自动色调映射边界** | 控制曲率值应如何写入纹理。 如果启用，将根据在烘焙过程中找到的最小值和最大值在0和1之间规范化值范围。 如果禁用，则手动定义最小值和最大值。  **注意：**&#x200B;在烘焙UDIMs/UV拼贴时，应禁用此参数以使色调映射一致而不是针对每个拼贴，否则可能会在每个纹理之间创建接缝。 要手动查找合适的最小值/最大值，请先在启用此设置的情况下进行烘焙，然后查看控制台/日志，以了解烘焙器输出的值。 |
| **色调映射最小值** | 如果禁用了&#x200B;**自动色调映射边界**，请定义最小值以缩放曲率结果以适应纹理。 |
| **最大色调映射** | 如果禁用了&#x200B;**自动色调映射边界**，请定义最大值以缩放曲率结果以适应纹理。 |
| **法线图** | 指向正常纹理的可选路径。 可用于代替面包机内部计算。 |
| **世界空间** | 如果启用，则正常纹理将被解释为世界空间法向，而不是切线空间。 |
| **正常方向** | 法向纹理的格式（如果位于相切空间中）。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
