---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/using-workflows-in-3ds-max.html"
breadcrumb-title: ""
description: 使用3ds Max中的渲染工作流程，可从材料为不同的渲染器自动创建着色器网络。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Using Workflows in 3ds Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在3ds Max中使用工作流
user-guide-description: ""
user-guide-title: ""
source-git-commit: 335f3107fb325bb769325bff8c150b3e8b7ff054
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---

# 在3ds Max中使用工作流

3ds Max增效工具中的Substance包含用于自动创建着色器网络以支持渲染器的工作流程。 可在“Substance”菜单中找到渲染工作流程。

![](../../../assets/maya-max-v3-1/3dsmax-all-presets.png)

要使用工作流，请在材料编辑器中选择Substance节点，然后从“Substance”菜单中选择工作流。

![](../../../assets/max-workflow.gif)

## OpenPBR工作流

**工作流程列表**&#x200B;中提供了两个OpenPBR工作流程（从&#x200B;**Substance菜单**）： **Substance到OpenPBR**&#x200B;和&#x200B;**Substance到V-RayOpenPBR**。 这些工作流程专为与使用Substance 3D Designer或Sampler中的OpenPBR材质模型创作的SBSAR文件结合使用而设计（自Designer V16.0+和Sampler V6.0+以来，OpenPBR一直是默认模型）。

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-node-preview.png)

### 什么是OpenPBR？

OpenPBR是由Adobe和Autodesk开发的开放、基于物理的材料着色模型，为学院软件基金会(ASWF)做出了贡献。 它提供了统一的材料定义，可在各个渲染器之间兼容。 有关详细信息，请访问[OpenPBR文档](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/openpbr/openpbr-overview)。

### 何时使用OpenPBR工作流程

当使用Substance 3D Designer或Substance 3D Sampler中的OpenPBR材质模型创作Sbsar 文件时，请使用OpenPBR工作流程。 如果您的SBSAR是使用Adobe标准材质模型(ASM)创作的，请使用与渲染器兼容的旧版工作流程（Arnold、V-Ray或V-Ray 6）。

>[!NOTE]
>
> 如果将OpenPBR工作流程应用于ASM材料，或将标准工作流程应用于OpenPBRSBSAR，则该增效工具将仅连接两个材质模型共用的输出。 结果可能不完整。

### 可用的OpenPBR工作流

**OpenPBR**

使用本机3ds Max openPBRSurface节点。 与Arnold和V-Ray兼容。 对于在3ds Max中使用材料的大多数用户，建议使用此工作流程。

**OpenPBR- V-Ray**

在OpenPBR模式下使用V-Ray材料(VRayMtl)。 建议用户将其管道专门围绕V-Ray材料设置构建。

### 如何应用OpenPBR工作流程

![](../../../assets/maya-max-v3-1/3dsmax-substance-to-openpbr.png)

1. 使用“加载Sbsar 文件”按钮选择您的Substance(OpenPBR)。
1. 在顶部菜单中，选择OpenPBR或OpenPBR- V-Ray。
1. 单击“创建网络”以在Slate材料编辑器中创建着色器网络。
1. 该插件自动将SBSAR输出连接到OpenPBR节点的相应输入。
1. 照常将材料分配给网格。

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-overview.png)
