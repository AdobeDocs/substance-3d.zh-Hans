---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/tangent-space.html"
breadcrumb-title: ''
description: 了解Substance Bakers如何处理切线空间计算并为您的工作流程自定义算法。
helpx_creative_field: ""
helpx_description: bakers > Features > Tangent Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 切线空间
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 2%

---


# 切线空间

Substance Bakers可以加载位于低多边形网格上的切线和二项式，也可以重新计算它们。 重新计算它们时，可以定义自定切线空间算法（默认情况下为MikkTSpace）。

## 相切空间插件列表

## Substance Painter

在Substance Painter中，无法更改Tangent Space增效工具，它始终为&#x200B;**MikkTSpace**。 但是，有一个参数可以略微改变其行为，使其与其他应用程序兼容：

| *参数* | *兼容* *应用程序* |
| --- | --- |
| **计算每个片段的正切空间：已禁用** | 与xNormal、Unity 5.3或更高版本兼容。 |
| **计算每个片段的正切空间：已启用** | 与Unreal Engine 4、Blender和Unity HDRP工作流程兼容。 |

## Substance Designer

Substance Designer支持以下算法：

| *文件名* | *描述* |
| --- | --- |
| **miktspace.dll** | Miktspace，基于Morten S. Mikkelsen的切线空间算法。与xNormal、Unity 5.3或更高版本兼容。 |
| **mikkunrealtspace.dll** | Miktspace，基于Morten S. Mikkelsen的切线空间算法。与Unreal Engine 4、Blender和Unity HDRP工作流程兼容。 |
| **unitytspace.dll** | 基于Unity 4的切线空间算法。 |

>[!NOTE]
>
> 可以编写自定义相切空间插件。 名为&#x200B;**tangentspaceplugin.h**&#x200B;的标头文件位于&#x200B;**Substance Designer/SDK/tangentspace**&#x200B;下的安装文件夹中，可以用作接口。

## 设置自定切线空间

## Substance Painter

Substance Painter目前不支持自定义Tangent Space插件。 这意味着，如果低多边形网格上不存在Tangents和Binormals（用于创建项目），将根据MikkTSpace算法重新计算它们。

## Substance Designer

要在Substance Designer中设置切线空间算法，请执行以下步骤：

1. 选择&#x200B;**编辑** > **首选项**。

   ![](../../assets/sd-edit-pref.png)
1. 单击&#x200B;**项目**。

   ![](../../assets/sd-pref-projects.png)
1. 导航到&#x200B;**常规**&#x200B;选项卡。 滚动直到部分&#x200B;**3D场景**&#x200B;可见。

   ![](../../assets/sd-tab-general.png)
1. 单击&#x200B;**三个点** (...) 以加载自定义插件。

## Substance自动化工具包

使用自动化工具包生成文件时，可以使用特定的命令行参数指定相切空间插件：

```
sbsbaker normal-from-mesh --tangent-space-plugin "C:/Substance Designer/plugins⁄tangentspace⁄mikktspace.dll" ...
```
