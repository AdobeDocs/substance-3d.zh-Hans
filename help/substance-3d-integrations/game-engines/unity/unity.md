---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity.html"
breadcrumb-title: ''
description: 在Unity游戏引擎中导入和使用Substance素材，并具有原生增效工具支持和运行时参数控制。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 统一
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---


# 统一

![](../../assets/unity.png)

>[!NOTE]
>
> **Unity支持的版本**
> 
> 适用于Unity的Substance 3D增效工具Adobe版本3.0.0目前支持Unity 2020.3.27x及更高版本。 可以从[Unity Asset Store](https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208)下载。

>[!WARNING]
>
> 在升级或使用插件之前，请检查[升级项目页面](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html)。

>[!WARNING]
>
> 在创作自定义Substance素材之前，请确保检查[优化准则](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md)页。

## 目录

* [Unity发行说明](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) - Unity增效工具各版本Substance的新增功能
* [在Unity中下载Substance 3D插件](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md) - Unity Asset Store中提供Substance 3D for UnityAdobehttps://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Unity插件概述](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Unity首选项](../../game-engines/unity/unity-preferences/unity-preferences.md) —Substance首选项窗口允许您为增效工具设置用户定义的选项。
* [优化准则](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) — 创建自己的自定义Substance素材时，请确保检查以下优化准则。
* [升级项目/已知问题](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html) - Unity增效工具中Substance的已知问题
* [管理Substance 图形](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html) — 您可以使用Substance 图形管理器(SGM)基于Substance素材创建新素材
* [更改参数](../../game-engines/unity/changing-parameters/changing-parameters.md) — 可在Substance 图形对象(SGO)上访问Substance素材的参数。
* [生成的纹理(打包)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md) — 生成的纹理显示Substance 引擎为创建纹理而计算的Substance输出
* [渲染色彩空间](../../game-engines/unity/rendering-color-space/rendering-color-space.md) — 为获得最佳效果，应在Unity Player设置中将色彩空间设置为线性。
* [使用图像输入](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [发布为移动设备](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) — 在移动平台上发布的准则
* [Substance 3D for Unity脚本编写](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md) — 使用SubstanceAPI，您可以编写脚本以在运行时更新和更改Substance参数。
* [在Unity中编写脚本（已弃用）](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html) — 使用SubstanceAPI，您可以编写脚本以在运行时更新和更改Substance参数。
* [Substance 3D Assets库使用情况](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [正在删除Substance增效工具](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [UnityTutorials中的Substance 3D](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [统一的物理尺寸](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
* [在项目之间共享sbsar文件](https://helpx.adobe.com/sharing-sbsar-files-between-projects.html) [&#128279;](../../game-engines/unity/sharing-sbsar-files-bet/sharing-sbsar-files-between-projects.md)

**[找到表单 — 需要规则]**

>[!WARNING]
>
> 在升级或使用插件之前，请检查[升级项目页面](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html)。

>[!WARNING]
>
> 在创作自定义Substance素材之前，请确保检查[优化准则](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md)页。

### 目录

* [Unity发行说明](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) - Unity增效工具各版本Substance的新增功能
* [在Unity中下载Substance 3D插件](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md) - Unity Asset Store中提供Substance 3D for UnityAdobehttps://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Unity插件概述](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Unity首选项](../../game-engines/unity/unity-preferences/unity-preferences.md) —Substance首选项窗口允许您为增效工具设置用户定义的选项。
* [优化准则](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) — 创建自己的自定义Substance素材时，请确保检查以下优化准则。
* [升级项目/已知问题](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html) - Unity增效工具中Substance的已知问题
* [管理Substance 图形](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html) — 您可以使用Substance 图形管理器(SGM)基于Substance素材创建新素材
* [更改参数](../../game-engines/unity/changing-parameters/changing-parameters.md) — 可在Substance 图形对象(SGO)上访问Substance素材的参数。
* [生成的纹理(打包)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md) — 生成的纹理显示Substance 引擎为创建纹理而计算的Substance输出
* [渲染色彩空间](../../game-engines/unity/rendering-color-space/rendering-color-space.md) — 为获得最佳效果，应在Unity Player设置中将色彩空间设置为线性。
* [使用图像输入](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [发布为移动设备](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) — 在移动平台上发布的准则
* [Substance 3D for Unity脚本编写](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md) — 使用SubstanceAPI，您可以编写脚本以在运行时更新和更改Substance参数。
* [在Unity中编写脚本（已弃用）](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html) — 使用SubstanceAPI，您可以编写脚本以在运行时更新和更改Substance参数。
* [Substance 3D Assets库使用情况](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [正在删除Substance增效工具](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [UnityTutorials中的Substance 3D](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [统一的物理尺寸](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
