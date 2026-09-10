---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/common-parameters.html"
breadcrumb-title: ''
description: 了解适用于所有Baker的常见参数，以及如何配置这些参数以生成最佳纹理。
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

通用参数适用于所有Baker。 这些参数通常定义Baker的行为以及与高多边形网格配合使用的方式，但如何生成最终纹理。 这些参数中的某些参数可以由特定Baker覆盖。

虽然这些参数中的大部分在所有软件（包括Substance自动化工具包）中均可使用，但它们的行为可能略有不同；或者根据软件工作流程和实施情况，有些参数可能不可用。

## 常规参数

这些参数会影响Baker生成纹理的方式。

| *名称* | *描述* |
| --- | --- |
| **大小**（默认大小或输出大小） | 控制烘焙输出纹理分辨率（以像素为单位）。可用值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>32</strong></li><li data-preserve-html="true"><strong>64</strong></li><li data-preserve-html="true"><strong>128</strong></li><li data-preserve-html="true"><strong>256</strong></li><li data-preserve-html="true"><strong>512</strong></li><li data-preserve-html="true"><strong>1024</strong></li><li data-preserve-html="true"><strong>2048</strong>（默认）</li><li data-preserve-html="true"><strong>4096</strong></li><li data-preserve-html="true"><strong>8192</strong></li></ul>还支持非方形分辨率，例如：2048x1024（2:1比率）。 在Substance Designer中，此参数可以由Baker本身覆盖。 |
| **格式** | 纹理的文件格式。*在Substance Painter中不可用。* 请参阅： [如何导出已烘焙贴图](../../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md)。 |
| **消除锯齿** | 控制消除锯齿，这可以提高纹理的质量，并减少不同几何连接处的锯齿。要了解有关锯齿的更多信息，请参阅[接缝上的锯齿](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)和[维基百科上的锯齿](https://en.wikipedia.org/wiki/Aliasing)。可用值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>（默认）</li><li data-preserve-html="true"><strong>次取样2x2</strong></li><li data-preserve-html="true"><strong>次取样4x4</strong></li><li data-preserve-html="true"><strong>次取样8x8</strong></li></ul>  **注意：**&#x200B;启用消除锯齿功能可以显着增加烘焙时间，因为消除锯齿功能是通过以更高的分辨率计算纹理然后再将其缩小到最初选择的大小来起作用的。 这意味着具有2x2次取样的2K纹理将实际计算4K纹理。有时，最好增加Baker中的光线数量，而不是增加次取样。 它可以在无需等待太长时间的情况下取得更好的结果。 |
| **UV 集** | 控制将使用来自低多边形网格的哪些UV来计算烘焙纹理。*在Substance Painter中不可用。* |
|  |  |
| **膨胀（像素）** | 按给定的像素量扩展UV外部或其边框的像素。 当这些边框未与UV像素完全对齐或当纹理分辨率降低（例如：中间映射）时，此操作可以避免在纹理边框接缝。 这是在烘焙过程之后应用的后过程。 有时也可以称为“填充”。要了解有关膨胀的更多信息，请参阅[UV接缝上的别名](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)和[填充](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/padding-134643719.html)。 |
| **应用漫射** | 如果启用，UV外部将填充基于UV边框的平滑渐变色。 此过程可确保纹理大小在减小后保持稳定，不会创建过度可见的接缝（例如：mipmap）。 这是在烘焙过程之后应用的后过程。 |
| **平均法线** | 如果启用此选项，则会计算顶点的平均法线，以了解烘焙的网格匹配过程中将光线发送到哪个方向。 如果禁用，光线将遵循网格的原始顶点法线。 |

## 高多边形参数

以下参数用于控制高多边形到低多边形烘焙（“从网格”Baker）。

| *名称* | *描述* |
| --- | --- |
| **高清晰度网格** | 包含高多边形网格的文件（或Substance包资源）列表。 当烘焙进程开始计算不同的信息并将该网格信息保存到纹理时，Baker会将它们加载到内存中。 如果启用“**使用低作为高清**”，则会忽略此列表。 |
| **使用低作为高清**&#x200B;或&#x200B;**使用低模网格作为高模网格** | 如果启用，则提供给Baker的高多边形网格列表将被忽略，而低多边形网格将在其自身上烘焙。直接处理高多边形网格时，此参数非常有用。 例如，在启用此设置的情况下，烘焙高多边形轿车的ambient occlusion纹理时，将忽略光线距离，并且Baker将生成完美的烘焙（没有光线缺失或几何不匹配）。 |
|  |  |
| **使用笼子设置距离**&#x200B;或&#x200B;**使用笼子** | 指示在烘焙过程中是否使用笼子网格文件而不是使用光线距离值。 笼子控制光线的最大距离和方向。 |
| **笼子的文件** | 包含笼子的网格文件的路径。 |
| **正面值**&#x200B;或&#x200B;**最大正面距离** | 控制光线应从距离低多边形表面多远处开始，沿其路径查找任何高多边形几何形状。*使用笼子时，此设置无效。* |
| **后置值**&#x200B;或&#x200B;**最大后距** | 控制光线应停留在低多边形表面下方的距离，以便沿其路径查找任何高多边形几何形状。*使用笼子时，此设置无效。* |
| **相对于定界框** | 如果启用，则光线距离和其他基于大小的计算将基于低多边形网格的归一化空间。 如果禁用，则光线距离计算基于导出时在低多边形网格中指定的单位（米、厘米等）。禁用此设置并在对象具有精确测量时手动输入光线距离有时可能非常有用。 |
|  |  |
| **匹配** | 指示Baker应如何匹配低多边形和高多边形几何。 它可用于过滤烘焙过程，而无需手动分离（分解）网格。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>始终</strong>（默认）：低多边形网格与每个高多边形网格匹配。</li><li data-preserve-html="true"><strong>按网格名称</strong>：按名称筛选网格，以避免与不需要的几何相匹配。</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md)。 |
| **匹配后缀**&#x200B;或&#x200B;**高模网格后缀** **低模网格后缀** | 使用“按名称匹配”功能时，网格名称后缀用于标识和分组几何。 可用后缀：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>低模网格</strong>：标识场景中低多边形网格的后缀</li><li data-preserve-html="true"><strong>高模网格</strong>：标识场景中高多边形网格的后缀</li><li data-preserve-html="true"><strong>忽略背面</strong>：后缀用于标识应被特定Baker忽略的网格（如[来自网格的Ambient occlusion](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)）</li></ul>要了解有关匹配几何的更多信息，请参阅： [按名称匹配](../../features/matching-by-name/matching-by-name.md) 。 |
|  |  |
| **使用倾斜校正** | 如果启用，将根据输入纹理从&#x200B;**平均法线**&#x200B;或原始几何法线计算光线方向。 纹理中的黑场值使用计算的平均normal，而白场值使用原始网格normal。*在Substance Painter中不可用。* |
| **倾斜映射** | 用于倾斜光线投影的纹理文件的路径。 |
| **反转倾斜校正** | 反转输入纹理的读数（黑变白、白变黑）。 |
