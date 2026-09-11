---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/installing-to-source-builds-ue5.html"
breadcrumb-title: ''
description: 将Substance 3D插件安装到Unreal引擎5源内部版本以进行自定义引擎修改。
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 安装到源版本 — UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# 安装到源版本 — UE5

Substance增效工具可以与从源构建的Unreal引擎版本一起使用。 为此，可以将增效工具安装到C++project文件夹或源内部版本的引擎文件夹中。

>[!NOTE]
>
> 这些方法要求您拥有从Marketplace下载的插件版本。 可以在计算机和UE内部版本之间传输Substance增效工具文件夹。

## 安装到C++项目文件夹

1. 在项目文件夹中，创建一个“插件”文件夹（如果尚不存在）。
1. 在“插件”文件夹中，创建一个“运行时”文件夹。
1. 将Substance文件夹放在Runtime文件夹中。 LINUX用户：在步骤3之后，在Substance文件夹中找到“include”文件夹，然后将其重命名为大写“i”(include > Include)。
1. 启动虚构引擎。
1. 通过启动器打开C++项目。
1. 启动项目后，虚构引擎会提示询问您是否要在启动前重建增效工具组件，请选择是。 此操作将通过Microsoft Visual Studio (Windows、Linux)或Xcode (Mac)来完成。
1. 虚构引擎将关闭，但组件将在后台生成。 这个过程大约需要5分钟。 完成后，项目将打开。 如果失败，您将看到一个错误窗口。

## 安装到引擎文件夹

>[!NOTE]
>
> 必须先按照上述步骤重建Plugin Binaries文件夹，然后才能将Plugin安装到引擎文件夹中。

1. 从“项目文件夹”>“Substance”>“运行时”内复制插件文件夹。
1. 打开“虚构引擎版本”文件夹，然后导航到“引擎” > “增效工具” > “Marketplace” 。
1. 粘贴Substance文件夹。
1. 打开虚构引擎编辑器。 根据需要创建新项目。
1. 打开“增效工具”菜单并验证是否已启用Substance增效工具。
