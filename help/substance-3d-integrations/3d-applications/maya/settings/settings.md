---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/maya/settings.html"
breadcrumb-title: ''
description: 通过工具架或菜单在Maya中配置Substance增效工具设置以自定义行为。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# 设置

可以通过工具架或Substance菜单访问Substance设置菜单。 此菜单的设置存储在可编辑的配置文件“substance.cfg”中。

>[!NOTE]
>
> **配置文件位置**
> 
> **Windows**：\
> C:\Users\\Documents\maya\\substance\\
> **MacOS**：\
> /Users//Library/Preferences/Autodesk/maya//substance/\
> **Linux**：\
> /home//maya//substance/

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 默认分辨率

设置sbsar 文件加载时的默认分辨率。

## 渲染工作流程

设置要在Substance节点上使用的默认渲染工作流。

## Substance Engine

设置特定于该Substance 引擎的首选项以及所有Substance节点的全局首选项。 引擎用于计算Substance纹理。

### 引擎类型

该Substance 引擎可用作CPU和GPU引擎。 切换引擎需要重新启动Maya。 GPU引擎的分辨率将高于CPU引擎。

>[!WARNING]
>
> CPU和GPU引擎之间可能存在计算差异，因此要获得一致的结果，最好将类型设置为Substance Designer中使用的相同引擎。

CPU核心和引擎内存是允许Substance引擎使用的资源量的设置。

### 阻止渲染

此选项允许您设置引擎计算是否阻止Maya UI进程。 启用后，将优先使用引擎并阻止Maya UI进程。 禁用后，Maya UI进程将不会被引擎计算阻止。

## 缓存输出到磁盘

为项目中所有新建的Substance节点设置默认缓存位置、文件类型和缓存文件夹。

## 渲染扩展

启用渲染扩展以直接对Arnold着色器使用Substance输出。

## 物理大小

如果在加载sbsar文件时应默认使用物理尺寸，以及在重新加载sbsar时是否应重新计算路径，则启用此选项。

</td>
<td style="border: 0;" valign="top">

![](../../../assets/settings-35.png)

</td>
</tr>
</table>
