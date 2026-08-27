---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/blender/workflows.html"
breadcrumb-title: ''
description: 了解如何针对不同的工作流程将Substance素材与混合器的循环和Eevee渲染器配合使用。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 工作流
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---


# 工作流

## 使用循环

默认情况下，在“循环”渲染视图中查看时，参数更改不会在3D视口中自动更新。 要在“循环”渲染视图中查看更新，请在首选项中启用&#x200B;**循环自动更新纹理**&#x200B;以强制更新。

## 多图.sbsar文件

该插件支持包含多个Substance图形的.sbrar文件。 加载包含多个图形的文件时，Substance 3D面板上将出现一个新的图形下拉列表。 与其它参数更改不同，切换图形不会自动更新材料。 因此，必须使用&#x200B;**应用**&#x200B;按钮在更改图表后再次分配材质。

>[!NOTE]
>
> 缺省情况下，“应用”按钮将材料添加到新槽中，而不会覆盖先前的材料指定。 删除以前的素材，或使用素材下拉列表重新分配新应用的素材。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/blender-workflows-multigraphs?$png$&jpegSize=100&wid=168)

## 使用图像输入

使用允许自定义图像输入的Substance素材时，图像选择参数Substance 3D Panel将允许您打开图像的文件浏览器（文件夹图标）或从项目中存在的图像中进行选择（图像图标下拉菜单）。

“导出图像格式”首选项可用于将Blender中生成的图像输入保存到临时文件夹。 有关更多详细信息，请参阅[首选项](../../../3d-applications/blender/preferences/preferences.md)页面。

![](../../../assets/blender-workflows-image-inputs-steps.png)

## 着色器网络预设。

可以通过Substance 3D面板输出部分中的下拉菜单快速调整着色器预设。 这些着色器预设可调整图像纹理的应用方式。循环/Eeve标准使用常规的UV纹理坐标映射。 其他三个“循环/边缘投影”预设使用为“方框”、“球面”或“圆柱”投影方法生成的纹理坐标映射。

可以在加载项[首选项](../../../3d-applications/blender/preferences/preferences.md)中选择素材使用的默认着色器预设。

![](../../../assets/2022-08-12-12-12-33-adobeexpress-1.gif)

## 过滤和调整输出

Substance 3D面板的“输出”部分还提供了用于筛选输出的选项。 着色器预设下拉列表旁的三个按钮可用于按启用的输出（复选标记）、着色器输出（球形）和所有可用的输出（线）进行过滤。

可使用复选框单独启用输出。 启用输出后，将创建纹理节点组中的相应输出。 如果Principled BSDF材料节点支持该输出，则它将自动连接到该节点。 Height将连接到位移节点，Ambient occlusion将与MixRGB节点中的base color合并。\
复选标记旁边的文件格式下拉菜单可用于设置输出纹理保存的文件类型。

此外，可以在加载项[首选项](../../../3d-applications/blender/preferences/preferences.md)中更改默认文件输出首选项。

## 交换对象上的材料

单击Blender的材料属性面板中的球面图标，以打开Blende项目中的材料列表。 已在面板中创建的材料也将显示在列表中。 从此列表中选择材料将替换该材料插槽中的活动材料。

## 位移

从循环渲染器支持的位移网格，但不在Eevee中。 要查看位移，请确保已启用Height输出。 该加载项将自动将材料的位移设置设为&#x200B;**位移和凹凸**。 现在，查看对象上的材料将在渲染视图中显示位移。 可以在“位移”面板或材料位移中调整节点比例。

为获得最佳效果，请针对具有复杂位移细节的材料，使用较高的细分级别或高多边形网格。
