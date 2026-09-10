---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/unreal-engine-4-plugin-release-notes/unreal-plugin-4-24-0-3.html"
breadcrumb-title: ''
description: 查看Unreal Engine 4增效工具版本4.24.0.3的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Unreal Engine 4 plugin release notes > Unreal plugin 4.24.0.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非实际插件4.24.0.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# 非实际插件4.24.0.3

虚幻Substance经历了重大重组。 此重构的一部分提供了&#x200B;**UTexture2D**&#x200B;的完全支持，并且包括输入和输出。 借助&#x200B;**UTexture2D**&#x200B;支持，该插件现在可用于发布到任何平台，包括移动设备在内的虚实支持。 除了添加多个平台支持外，**UTexture2D**&#x200B;还允许在UE4中本地使用纹理流系统。

该增效工具还完全支持材料&#x200B;**实例化**，并引入了一个新的材料模板工作流程，该工作流程具有该Substance 引擎支持的数字输出。 通过材料模板，可以确切定义如何在UE4中配置Substance材料着色器。

![](../../../../../assets/ue4-material-templates.png)

我们随附了用于处理位移、折射和世界对齐材料的模板，这些模板内置了用于调整拼贴、纹理大小、位移和emissive参数的控件。 材料模板系统还允许您提供自己的自定义模板。

![](../../../../../assets/ue4-material-instance-params.png)
