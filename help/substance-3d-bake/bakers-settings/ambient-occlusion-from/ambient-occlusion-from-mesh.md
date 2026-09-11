---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/bakers-settings/ambient-occlusion-from-mesh.html"
breadcrumb-title: ''
description: 使用ambient occlusion技术从高多边形网格中烘焙精确的射线追踪纹理，以增强真实感。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 来自网格的环境遮蔽
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---


# 来自网格的环境遮蔽

通过“从BakerAmbient occlusion”，可以从高多边形网格烘焙Ambient occlusion纹理。 它比基[ambient occlusion](../../bakers-settings/ambient-occlusion/ambient-occlusion.md)Baker速度慢，但生成的结果更准确。

**适用于：**

* Substance Designer
* Substance自动化工具包
* Substance Painter

## 参数

| *参数* | *描述* |
| --- | --- |
| **次生射线** | 遮蔽光线的数量。 较高的值会产生较少的杂色，但计算时间较长。 默认值为64。 |
| **分钟遮挡距离** | 遮蔽光线将照射到高多边形几何的最小距离。 默认值为0.00001。 |
| **最大遮挡距离** | 遮蔽光线将照射到高多边形几何的最大距离。 默认值为0.1。 |
| **相对于定界框** | 如果启用，单位将相对于对象的定界框（1.0是定界框的对角长度）。 如果禁用，则用于最小和最大遮挡板距离的单位为导出网格时定义的单位（米、厘米或导出的场景的任何单位）。 |
| **扩散角度** | 遮蔽射线的最大扩散角度。 默认值为180。 |
| **分发** | 遮蔽射线的角度分布。 定义光线在扩散角大小的圆锥内的散射方式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>余弦</strong>（默认）：真实，但可能会导致极细的遮挡区域出现白线。 更适合着色和光照。</li><li data-preserve-html="true"><strong>一致</strong>：用于创建线性渐变。 更适用于图层蒙版和其他筛选。</li></ul> |
| **忽略背面** | 此参数定义遮挡射线是否忽略背面的点击（如果高多边形法线与发射光线的低多边形脸部相反的方向）。 大多数情况下，应启用此设置以避免出现伪影。 可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Nevers</strong>（默认）：绝不会忽略背面</li><li data-preserve-html="true"><strong>始终</strong>：始终忽略背面</li><li data-preserve-html="true"><strong>按网格名</strong>：只有与后缀关键字匹配的网格才会忽略后缀。 请参阅[常用参数](../../bakers-settings/common-parameters/common-parameters.md)。</li></ul> |
| **自遮蔽** | 按名称匹配遮挡射线。 指示Baker应如何匹配低多边形和高多边形几何。 它可用于过滤烘焙过程，而无需手动分离（分解）网格。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>始终</strong>（默认）：低多边形网格与每个高多边形网格匹配。</li><li data-preserve-html="true"><strong>按网格名称</strong>：按网格名称过滤网格，以避免与不需要的几何相匹配。</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md)。 |
| **法线图** | 指向普通纹理的可选路径。 可用于代替面包机内部计算。 |
| **世界空间** | 如果启用，则正常纹理将被解释为世界空间法向，而不是切线空间。 |
| **正常方向** | 法向纹理的格式（如果位于相切空间中）。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong>（默认）</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
| **衰减** | 定义如何通过遮挡距离衰减遮蔽。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>：无衰减。</li><li data-preserve-html="true"><strong>线性</strong>（默认）：渐进衰减。</li><li data-preserve-html="true"><strong>平滑</strong>：软衰减。</li></ul> |
| **地平面** | 如果启用，在XZ轴的网格边界框下模拟与次生射线冲突的平面。 此模拟阴影来自不可见的平面图。 |
| **地平面偏移** | 允许将计划移离网格以降低效果的强度。 该值为绝对值，与网格大小无关。 |
