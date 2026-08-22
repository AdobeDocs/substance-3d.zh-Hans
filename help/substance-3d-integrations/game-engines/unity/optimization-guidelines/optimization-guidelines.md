---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/optimization-guidelines.html"
breadcrumb-title: ''
description: 遵循优化准则以在Unity中平衡Substance素材复杂性和渲染性能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Optimization Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 优化准则
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 优化准则

Substance素材越复杂，渲染它们所需的处理能力就越强。 因此，Substance素材必须&#x200B;**在复杂性和渲染速度之间达到平衡**。 如果将在实时图形应用程序（如游戏）中使用它们，则这是&#x200B;*尤其是*&#x200B;重要信息。

创建自己的自定义Substance材质时，请确保检查以下优化准则。

[Substance Designer优化准则](https://docs.substance3d.com/display/SDDOC/Performance+Optimization+Guidelines)

需要注意的主要问题是绝对分辨率为4K或更高的节点。

>[!WARNING]
>
> **请注意分辨率和相对于父项的分辨率设置！**\
> 较高的值将严重影响性能，因此请考虑可能如何使用素材以及是否可以减小涉及的数据大小。
>   
> SubstanceCPU引擎可以在4K下计算，但速度非常慢，可能导致集成挂起或崩溃。

在以下示例中，[平铺Sampler](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-designer/using/substance-graphs/nodes-reference-for-substance-graphs/node-library/texture-generators/patterns/tile-sampler)节点的输出大小设置为[绝对](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-designer/using/substance-graphs/output-size) 4096。 它使下游的几个节点先以4K计算，然后再进行缩放，以获得2048年最终输出分辨率。

![](../../../assets/absolute.png){width="1000px"}
