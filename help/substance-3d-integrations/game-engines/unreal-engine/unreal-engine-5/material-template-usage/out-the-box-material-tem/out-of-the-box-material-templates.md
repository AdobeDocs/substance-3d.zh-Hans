---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5/out-of-the-box-material-templates.html"
breadcrumb-title: ''
description: 将SBSAR材料导入Unreal Template 5时使用预建的材料引擎，以便快速设置和工作流程。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5 > Out-of-the-Box Material Templates
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 开箱即用的材料模板
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# 开箱即用的材料模板

将SBSAR材料导入内容浏览器时，您可以在下拉菜单中选择现成的其他材料模板。

![](../../../../../assets/screen-shot-2022-05-10-at-8-58-45-pm-copy.png)

## Substance标准模板

这是用于通用UV体验的基础材料模板。 它提供了对UV量的一些基本控制，因此您可以缩放UV以拉伸纹理。 您可以通过启用拆分UV选项来拆分UV缩放，您还有U数量、V数量、UV 偏移和UV旋转角度。 这允许您执行一些拼贴和UV旋转。

![](../../../../../assets/screen-shot-2022-05-10-at-9-06-40-pm-copy.png)

## Substance三平面模板

三平面模板对网格的X、Y和Z角度或脸部进行三平面映射，以便它可以将纹理的三个不同投影混合在一起，从而无缝混合角度。 三平面模板允许材料在对象弯曲时跨不同脸部混合在一起

![Substance三平面材料的详细信息菜单](../../../../../assets/triplanar-template.png)

三平面模板具有物理尺寸支持，因此启用物理尺寸后，三平面模板将根据材料的物理尺寸缩放图像，因此，无论您缩放对象的程度如何，该纹理将始终保持不变并具有统一的外观。 在此处了解更多物理尺寸： [物理尺寸- UE5](../../../../../game-engines/unreal-engine/unreal-engine-5/physical-size-ue5/physical-size-ue5.md)

## Substance折射模板

折射模板主要用于透明物体，例如玻璃。 它允许您修改对于玻璃材料或透明材料所具有的IOR值或标准纹理。

![](../../../../../assets/screen-shot-2022-05-10-at-9-07-38-pm.png)

## Substance车绘画模板

“汽车绘画”模板增加了清晰的涂层支持，并支持可调整的UV拼贴和值、清晰的coat roughness值和菲涅尔功率值。

![Substance汽车绘画材料的详细信息菜单](../../../../../assets/car-paint-template.png)

## 设置位移模板

>[!IMPORTANT]
>
> 实验性模板
> 
> 警告：以下模板是实验性的，可能会在不同版本之间发生重大更改。 这些模板利用了Epic的Nanite特征，该特征本身是截至本文撰写时的实验性的。 它们可能不是100%稳定，在项目中使用它们时应谨慎。

使用以下步骤可完全启用项目中的Nanite位移支持，并将位移素材与网格结合使用。

1. 导航到项目文件夹>配置> DefaultEngine.ini并打开它
1. 将以下内容附加到[/Script/Engine.RendererSettings]部分：
   * r.Nanite.AllowTessellation=1
   * r.Nanite.Tessellation=1
1. 选择要应用位移模板的静态网格，然后打开其设置。
1. 切换启用Nanite支持选项。
1. 将所需的.sbsar导入内容浏览器，然后选择Substance\_Displaceent\_Template或Susbtance\_Triplanar\_Displacement\_Template
1. 要更改位移量，请定位至物料模板并选择输出节点。 然后，调整“位移”部分下的“模”。

## 位移模板

与Substance标准模板类似，此模板允许在添加纳米级位移支持的情况下调整U和V值。

![位移素材的“详细信息”菜单](../../../../../assets/displacement-template.png)

## Substance三平面位移模板

与“位移模板”类似，此模板应用三面投影，并增加了物理尺寸支持和Nanite位移支持。

![Substance三平面位移素材的详细信息菜单](../../../../../assets/triplanar-displacement-template.png)
