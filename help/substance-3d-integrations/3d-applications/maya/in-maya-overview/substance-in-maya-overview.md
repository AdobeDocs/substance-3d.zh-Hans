---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/substance-in-maya-overview.html"
breadcrumb-title: ""
description: 了解适用于Maya的Substance增效工具，以及如何导入和使用Substance材料。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance in Maya Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya中的Substance概述
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%
---

# Maya中的Substance概述

## 增效工具概述

利用Maya增效工具的Substance，您可以直接在Maya中加载任何现有的Substance 3D材料(.Sbsar 文件)。 可以从Substance 3D Designer或Substance 3D Sampler中创作Substance 3D材料并将其导出为SBSAR文件，也可以从现有库（如Substance 3D Assets库）中下载。 Maya增效工具的Substance可创建Maya材料并将输出纹理输入到正确的材料声道输入

>[!NOTE]
>
> 确保在“设置/首选项” — >“Maya增效工具管理器”中加载了增效工具

## 在HypershadeSbsar 文件编辑器中打开节点

1. 打开&#x200B;**Hypershade**，在&#x200B;**节点编辑器**&#x200B;中，右键单击并在标记菜单中向上滑动以选择&#x200B;**创建节点**。 在&#x200B;**创建节点窗口**&#x200B;中，搜索并选择&#x200B;**Substance节点**。

   ![](../../../assets/createnode.png)

   单击Hypershade中的&#x200B;**Substance节点**&#x200B;以将其选中。 这将打开&#x200B;**材料编辑器**，您可以在其中通过单击文件夹图标加载Substance 3D材料(Sbsar 文件)。

1. 或者，您可以将一个Sbsar 文件拖放到Maya的&#x200B;**Hypershade编辑器**&#x200B;中，然后单击自动创建的Substance节点，以便直接在&#x200B;**材料编辑器**&#x200B;中查看和编辑选项。

### 在属性编辑器中播放SBSAR参数

![](../../../assets/1.png)

1. 如果Substance包含多个图形，则会填充&#x200B;**所选图形下拉列表**。 选择要用于创建材料的图形。

1. **“图形信息”按钮**&#x200B;显示在Substance Designer中设置的图形属性。

1. 通过设置&#x200B;**宽度**&#x200B;和&#x200B;**Height**&#x200B;值来设置分辨率。 禁用&#x200B;**锁定比例**&#x200B;以选择非方形比例。

1. 启用&#x200B;**将输出缓存到磁盘**，将Substance输出烘焙到磁盘，以便可以与Arnold等渲染器一起使用。 增效工具将使用Maya文件节点读回缓存的文件。

   ![](../../../assets/outputsettings.png)

1. 为您使用的渲染器选择一个工作流程，然后单击&#x200B;**“创建着色器网络”按钮**。 为渲染器工作流程创建了一个着色器网络。 对于版本3.1.1.，工作流程列表还提供了创建着色器网络的选项。 创建着色器网络后，即可应用场景中的材料。

   ![](../../../assets/createnetwork.gif){width="1000px"}

## 故障排除

要报告错误，请加入[SubstanceDiscord服务器](https://discord.com/invite/substance3d)上的#maya-plugin频道或访问[Adobe群](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-autodesk3dsmax)。 从控制台日志和任何复制步骤中包含相关信息将有助于我们更高效地诊断问题。