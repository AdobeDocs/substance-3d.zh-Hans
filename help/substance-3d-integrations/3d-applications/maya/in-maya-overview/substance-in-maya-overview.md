---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/maya/substance-in-maya-overview.html"
breadcrumb-title: ''
description: 了解适用于Maya的Substance增效工具，以及如何在您的工作流程中导入和使用Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance in Maya Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya中的Substance概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Maya中的Substance概述

## 增效工具概述

Substance增效工具允许您直接在Maya中加载在Substance Designer中创建的Substance素材。 该增效工具将创建Maya素材，并将素材纹理添加到素材通道输入中。 然后，您可以更改Substance参数，纹理将自动更新。

>[!NOTE]
>
> 确保在“设置/首选项” — >“Maya增效工具管理器”中加载了增效工具

![](https://helpx-prod.scene7.com/is/image/HelpxProd/plugin-4?$png$&jpegSize=100&wid=618)

## 打开Substance

1. 打开Hypershade，然后在节点编辑器中，右键单击标记菜单并向上滑动以选择创建节点。 此时将打开“创建节点”窗口。 在此处，您可以搜索Substance节点。

   ![](../../../assets/createnode.png)

   还可以在节点编辑器中按Tab键，然后在文本字段中键入substance，这样即可筛选到substance选项。 从选项中选择“Substance纹理”。
1. 在“属性编辑器”中选择Substance节点并浏览以加载Substance(.sbsar)文件。

   ![](../../../assets/1.png)
1. 如果Substance包含多个图形，则会填充“选定图形”下拉列表。 选择的图形将用于创建材料。
1. “图形信息”按钮将以Substance Designer显示图形属性集。
1. 通过从“宽度和Height”下拉框中选择一个值来设置分辨率。 锁定比例默认处于启用状态。
1. 启用“缓存输出到磁盘”，以便将Substance输出烘焙到磁盘，以便可以将其与渲染器（如Arnold）一起使用。 增效工具将使用Maya文件节点读回缓存的文件。

   ![](../../../assets/outputsettings.png)
1. 为您使用的渲染器选择一个工作流程，然后单击“创建着色器网络”按钮。 将为渲染器工作流程创建着色器网络。 您现在可以在场景中应用素材。

   ![](../../../assets/createnetwork.gif){width="1000px"}
