---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/using-workflows.html"
breadcrumb-title: ''
description: 在Maya中创建和使用用于Substance输出的渲染预设，为不同的渲染器自动生成着色器网络。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Using Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用工作流
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# 使用工作流

在“工作流程”下，您可以选择或创建用于Substance输出的渲染预设。 这些预设是渲染器（例如Arnold或Vray）的着色器网络。

>[!NOTE]
>
> **工作流预设位置**
> 
> **Windows**：\
> C:\Users\\Documents\maya\2022\substance\workflows\generated\
> **MacOS**：\
> /用户//资源库/Preferences/Autodesk/maya//substance/workflows/generated\
> **Linux**：\
> /home//maya//substance/workflows/generated

![](../../../assets/workflows-4.png)

要使用工作流程，只需从下拉列表中选择预设，然后单击“创建着色器网络”按钮。

![](../../../assets/workflow.gif)

## 创建工作流

您可以创建自己的工作流，并将其添加到渲染器工作流列表中。 添加新工作流时，在该Substance节点之后创建的所有节点都将保存在工作流中。 这样，您就可以创建任意数量的着色节点，以构建可保存为预设工作流程的完整自定义着色器网络。

## ![](../../../assets/saved-workflow.png)管理工作流

### 保存自定义工作流

1. 手动创建Substance输出并将其连接到材料，例如aiStandardSurface。
   1. 您可以使用任何Maya或渲染特定节点来构建着色器网络。
1. 单击&#x200B;**创建工作流**&#x200B;按钮，然后输入工作流预设的名称。

### 正在复制工作流

您可以通过单击&#x200B;**复制工作流**&#x200B;按钮来复制工作流。

### 重命名和覆盖工作流

您可以使用选定的&#x200B;**重命名**&#x200B;和&#x200B;**覆盖**&#x200B;按钮，重命名现有的工作流以及覆盖包含更新数据的工作流。

### 移除工作流

您可以使用删除工作流按钮来删除现有工作流。
