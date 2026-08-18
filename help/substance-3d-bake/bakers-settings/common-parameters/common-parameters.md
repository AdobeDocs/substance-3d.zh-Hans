---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/common-parameters.html"
breadcrumb-title: ''
description: 了解适用于所有烘焙师的常见参数，以及如何配置这些参数以优化纹理生成。
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Common Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通用参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---


# 通用参数

常用参数适用于所有烘焙师。 这些参数通常定义烘焙师将怎样行为以及如何处理高多边形网格，但如何生成最终纹理。 这些参数中的某些参数可以由特定的面包师覆盖。

虽然这些参数中的大部分在所有软件（包括Substance自动化工具包）中均可使用，但它们的行为可能略有不同；或者根据软件工作流程和实施情况，有些参数可能不可用。

## 常规参数

这些参数会影响烘焙师生成纹理的方式。

| *名称* | *描述* |
| --- | --- |
| **大小**（默认大小或输出大小） | 控制烘焙输出纹理分辨率（以像素为单位）。可用值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>32</strong></li><li data-preserve-html="true"><strong>64</strong></li><li data-preserve-html="true"><strong>128</strong></li><li data-preserve-html="true"><strong>256</strong></li><li data-preserve-html="true"><strong>512</strong></li><li data-preserve-html="true"><strong>1024</strong></li><li data-preserve-html="true"><strong>2048</strong>（默认）</li><li data-preserve-html="true"><strong>4096</strong></li><li data-preserve-html="true"><strong>8192</strong></li></ul>还支持非方形分辨率，例如：2048x1024（2:1比率）。 在Substance Designer中，此参数可由面包机本身覆盖。 |
| **格式** | 烘焙纹理的文件格式。*在Substance Painter中不可用。* 请参阅： [如何导出已烘焙贴图](../../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md)。 |
| **消除锯齿** | 控制消除锯齿，以提高烘焙纹理的质量，并减少不同几何连接处的锯齿。要了解有关锯齿的更多信息，请参阅[UV接缝上的锯齿](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)和[维基百科上的锯齿](https://en.wikipedia.org/wiki/Aliasing)。可用值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>（默认）</li><li data-preserve-html="true"><strong>次取样2x2</strong></li><li data-preserve-html="true"><strong>对4x4</strong>进行次采样</li><li data-preserve-html="true"><strong>次取样8x8</strong></li></ul>  **注意：**&#x200B;启用消除锯齿功能可以显着增加烘焙时间，因为消除锯齿功能是通过计算更高分辨率的纹理，然后将其缩小到最初选择的大小来起作用的。 这意味着具有2x2次采样的2K纹理将实际计算4K纹理。有时，增加烘焙机中的光线数量而不是增加次采样会更好。 它可以在无需等待太长时间的情况下取得更好的结果。 |
| **UV集** | 控制将使用来自低多边形网格的哪些UV来计算烘焙纹理。*在Substance Painter中不可用。* |
|  |  |
| **扩展(px)** | 按给定的像素量扩展UV外部或其边框的像素。 当这些边界没有与纹理像素完全对齐或纹理分辨率降低时（例如：中间映射），此操作可以避免在UV边界处接缝。 这是烘焙过程之后应用的后处理。 有时也可以称为“填充”。要了解有关膨胀的更多信息，请参阅[UV接缝](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)上的锯齿和[填充](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/padding-134643719.html)。 |
| **应用扩散** | 如果启用，UV外部将填充基于UV边框的平滑渐变颜色。 此过程可确保当纹理大小减小时，它保持稳定，而不会创建过度可见的接缝（例如：mipmaps）。 这是烘焙过程之后应用的后处理。 |
| **平均法线** | 如果启用，则在烘焙的网格匹配过程中计算顶点的平均法线，以确定在哪个方向发送光线。 如果禁用，光线将遵循网格的原始顶点法线。 |

## 高多边形参数

以下参数用于控制高多边形到低多边形网格烘焙（“从网格”烘焙）。

| *名称* | *描述* |
| --- | --- |
| **高清网格** | 包含高多边形网格的文件（或Substance包资源）的列表。 当烘焙过程开始计算不同信息并将网格信息保存到纹理中时，烘焙商将网格信息加载到内存中。 如果启用“**使用低作为高清**”，则会忽略此列表。 |
| **使用低作为高清**&#x200B;或&#x200B;**使用低多边形网格作为高多边形网格** | 如果启用，提供给烘焙师的高多边形网格列表将被忽略，而低多边形网格将自行烘焙。直接处理高多边形网格时，此参数非常有用。 例如，在启用此设置的情况下烘焙高多边形汽车的环境遮蔽纹理时，将忽略光线距离，烘焙器将生成完美的烘焙（无光线缺失或几何不匹配）。 |
|  |  |
| **设置与笼子的距离**&#x200B;或&#x200B;**使用笼子** | 指示在烘焙过程中是否使用笼形网格文件，而不是使用光线距离值。 笼子控制光线的最大距离和方向。 |
| **Cage文件** | 包含笼架的网格文件的路径。 |
| **正面值**&#x200B;或&#x200B;**最大正面距离** | 控制光线应从距离低多边形表面多远处开始，沿其路径查找任何高多边形几何形状。*使用Cage时，此设置无效。* |
| **后置值**&#x200B;或&#x200B;**最大后距** | 控制光线应停留在低多边形表面下方的距离，以便沿其路径查找任何高多边形几何形状。*使用Cage时，此设置无效。* |
| **相对于定界框** | 如果启用，则光线距离和其他基于大小的计算将基于低多边形网格的归一化空间。 如果禁用，则光线距离计算将基于导出时在低多边形网格中指定的单位（米、厘米等）。禁用此设置并在对象具有精确测量时手动输入光线距离有时可能非常有用。 |
|  |  |
| **匹配** | 指示面包师应如何匹配低多边形和高多边形几何。 它可用于过滤烘焙过程，而无需手动分离（分解）网格。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>始终</strong>（默认）：低多边形网格与每个高多边形网格匹配。</li><li data-preserve-html="true"><strong>按网格名称</strong>：按网格名称过滤网格，以避免与不需要的几何相匹配。</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md)。 |
| **匹配后缀**&#x200B;或&#x200B;**高多边形网格后缀** **低多边形网格后缀** | 使用“按名称匹配”功能时，网格名称后缀用于标识和分组几何。 可用后缀：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>低多边形网格</strong>：用于识别场景中低多边形网格的后缀</li><li data-preserve-html="true"><strong>高多边形网格</strong>：用于识别场景中高多边形网格的后缀</li><li data-preserve-html="true"><strong>忽略背面</strong>：后缀用于标识应被特定烘焙器忽略的网格（如[来自网格的环境遮蔽](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)）</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md) 。 |
|  |  |
| **使用倾斜校正** | 如果启用，将根据输入纹理从&#x200B;**平均法线**&#x200B;或原始几何法线计算光线方向。 纹理中的黑色值使用计算出的平均法向，而白色值使用原始网格法向。*在Substance Painter中不可用。* |
| **倾斜映射** | 用于倾斜光线投影的纹理文件的路径。 |
| **反转倾斜校正** | 反转输入纹理的读数（黑色变成白色，白色变成黑色）。 |
