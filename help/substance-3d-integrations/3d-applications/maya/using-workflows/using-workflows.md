---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/maya/using-workflows.html"
breadcrumb-title: ""
description: 在Maya中创建和使用用于Substance输出的渲染预设，为不同的渲染器自动生成着色器网络。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Using Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用工作流
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%
---

# 使用工作流

在“工作流程”下，您可以选择或创建用于Substance输出的渲染预设。 这些预设是用于渲染器（例如Arnold或Vray）的着色器网络。

>[!NOTE]
>
> **工作流预设位置**
>
> **Windows**：
> C:\Users\\Documents\maya\2022\substance\workflows\generated
> **macOS**：
> /用户//资源库/Preferences/Autodesk/maya//substance/workflows/generated
> **Linux**：
> /home//maya//substance/workflows/generated

![](../../../assets/maya-max-v3-1/maya-all-presets.png)

要使用工作流程，只需从列表中选择预设，然后单击“创建网络”按钮即可。

![](../../../assets/workflow.gif)

## 创建工作流

您可以创建自己的工作流，并将其添加到渲染器工作流列表中。 添加新工作流时，在该Substance节点之后创建的所有节点都将保存在工作流中。 这样，您就可以创建任意数量的着色节点，以构建可以保存为预设工作流程的完整自定义着色器网络。

![](../../../assets/saved-workflow.png)

## 管理工作流

### 保存自定义工作流

1. 手动创建Substance输出并将其连接到材料，如aiStandardSurface。
   1. 您可以使用任何Maya或渲染特定节点来构建着色器网络。
1. 单击&#x200B;**创建工作流**&#x200B;按钮，然后输入工作流预设的名称。

### 正在复制工作流

您可以通过单击&#x200B;**复制工作流**&#x200B;按钮来复制工作流。

### 重命名和覆盖工作流

您可以使用选定的&#x200B;**重命名**&#x200B;和&#x200B;**覆盖**&#x200B;按钮，重命名现有的工作流以及覆盖包含更新数据的工作流。

### 移除工作流

您可以使用删除工作流按钮来删除现有工作流。

## OpenPBR工作流

工作流程列表中提供了两个OpenPBR工作流程： **OpenPBR**&#x200B;和&#x200B;**OpenPBR-V-Ray**。 这些工作流程专为与使用Substance 3D Designer或Sampler中的OpenPBR材质模型创作的SBSAR文件结合使用而设计（自Designer V16.0+和Sampler V6.0+以来，OpenPBR一直是默认模型）。

### 什么是OpenPBR

OpenPBR是由Adobe和Autodesk开发的开放、基于物理的材料着色模型，为学院软件基金会(ASWF)做出了贡献。 它提供了统一的材料定义，可在各个渲染器之间兼容。 有关详细信息，请访问[OpenPBR文档](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/general-knowledge/openpbr/openpbr-overview)。

### 何时使用OpenPBR工作流程

当使用Substance 3D Designer或Substance 3D Sampler中的OpenPBR材质模型创作Sbsar 文件时，请使用OpenPBR工作流程。 如果您的SBSAR是使用Adobe标准材质模型(ASM)创作的，请使用与渲染器兼容的旧版工作流程（Arnold、V-Ray或V-Ray 6）。

>[!NOTE]
>
> 如果将OpenPBR工作流程应用于ASM材料，或将标准工作流程应用于OpenPBRSBSAR，则该增效工具将仅连接两个材质模型共用的输出。 结果可能不完整。

### 可用的OpenPBR工作流

**OpenPBR**

使用本机Maya openPBRSurface节点。 与Arnold和V-Ray兼容。 对于在Maya中使用材料的大多数用户，建议使用此工作流程。

**OpenPBR- V-Ray**

在OpenPBR模式下使用V-Ray材料(VRayMtl)。 建议用户将其管道专门围绕V-Ray材料设置构建。

### 如何应用OpenPBR工作流程

1. 使用“加载Sbsar 文件”按钮将Substance加载到增效工具中。
1. 在“工作流程”列表中，选择&#x200B;**OpenPBR**&#x200B;或&#x200B;**OpenPBR- V-Ray**。
1. 单击&#x200B;**创建网络**&#x200B;以在&#x200B;**Hypershade材料编辑器**&#x200B;中创建着色器网络。
1. 该插件自动将SBSAR输出连接到OpenPBR节点的相应输入。
1. 照常将材料分配给网格。

![](../../../assets/maya-max-v3-1/maya-openpbr-overview.png)
