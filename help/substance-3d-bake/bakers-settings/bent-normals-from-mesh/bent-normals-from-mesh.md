---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/bent-normals-from-mesh.html"
breadcrumb-title: ''
description: 计算描述高多边形网格中环境光照平均方向的bent normals纹理。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Bent Normals from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 从网格弯曲法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 3%

---


# 从网格弯曲法线

来自Baker的Bent normals计算一个描述环境光照平均方向的纹理。 此Baker派生自网格[&#128279;](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)Baker的Ambient occlusion。

**适用于：**

* Painter
* Designer
* 自动化工具包

## 参数

| *参数* | *描述* |
| --- | --- |
| **次生射线** | 遮蔽光线的数量。 较高的值会产生较少的噪声，但计算时间将较长。 |
| **分钟遮挡距离** | 遮挡射线将到达高多边形几何的最小距离&#x200B;**.** |
| **最大遮挡距离** | 遮蔽光线将照射到高多边形几何的最大距离。 |
| **相对于定界框** | 如果启用，则光线距离计算基于低多边形网格的归一化空间（0到1）。 如果禁用，则光线距离计算基于导出时在低多边形网格中指定的单位（米、厘米等）。 |
| **扩散角度** | 遮蔽射线的最大扩散角度。 默认值为180。 |
| **分发** | 遮蔽射线的角度分布。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>余弦</strong>（默认）</li><li data-preserve-html="true"><strong>一致</strong></li></ul> |
| **忽略背面** | 如果启用，遮挡射线将忽略背面的点击（如果高多边形法线与发射光线的低多边形脸部相反的方向）。 大多数情况下，应启用此设置以避免出现伪影。 |
| **自遮蔽** | 按名称匹配遮挡射线。 指示Baker应如何匹配低多边形和高多边形几何。 它可用于过滤烘焙过程，而无需手动分离（分解）网格。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>始终</strong>（默认）：低多边形网格与每个高多边形网格匹配。</li><li data-preserve-html="true"><strong>按网格名称</strong>：按网格名称过滤网格，以避免与不需要的几何相匹配。</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md)。 |
| **映射类型** | 定义输出纹理的类型。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>世界空间</strong></li><li data-preserve-html="true"><strong>正切空间</strong> （默认）</li></ul> |
| **正常方向** | 将&#x200B;**Mat类型**&#x200B;设置为切线空间时，控制输出纹理的常规格式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong> <strong> <br/></strong></li><li data-preserve-html="true"><strong>DirectX</strong>（默认）<strong> <br/></strong></li></ul> |
