---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/cinema-4d/attribute-manager.html"
breadcrumb-title: ''
description: 使用Cinema 4D的属性管理器来配置Substance资源属性和材质设置。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Cinema 4D > Attribute Manager
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 属性管理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# 属性管理器

Cinema 4D的“属性管理器”中为Substance资源提供了一个新模式。

在Substance资源管理器中选择Substance后，属性管理器将自动切换到Substance资源模式。 也可以在属性管理器的模式菜单中手动切换到此模式。

在Substance资源模式下，您可以访问Substance的所有输入，并可以概览所有输出声道。

![](../../../assets/cinema-4d-9.png){width="500px"}

## Substance输入分组

如果对Substance的输入进行了分组，则这些组将在属性管理器中按此方式显示。 有两个预定义组： **基本属性**&#x200B;和&#x200B;**图像输入**。

* 于基本物业组别中，所有未分配至Substance Designer组别的输入值将会显示。
* 顾名思义，链接到外部图像的所有Substance输入都收集在“图像输入”组中。

## Filename参数

通过使用“属性管理器”中的Filename参数，可以在将Substance资源加载到场景中后更改其文件位置。

![](../../../assets/cinema-4d-10.png){width="500px"}

这不仅对于重新定位Substance文件有用，而且对于与完全不同的Substance交换文档也很有用。

在这种情况下，将询问用户是否将对先前Substance输出通道的任何现有引用重新映射到新Substance。

![](../../../assets/cinema-4d-11.png){width="500px"}

如果问题的答案为“否”，则将从所有Substance着色器中删除指向上一个Substance的链接。 为了重新映射输出通道，增效工具将首先搜索具有相同类型的输出通道，然后搜索具有相同名称的输出通道。

## 参数三状态

如果同时选择多个Substance，则这些Substance之间共享的输入将显示为三状态，并且可以同时为所有选定的Substance进行编辑（就像Cinema 4D中的所有其他参数一样）。

在这些实例中，输出通道将显示如下。

![](../../../assets/cinema-4d-12.png){width="300px"}
