---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/substance-output-node.html"
breadcrumb-title: ''
description: 了解Maya中的Substance输出节点如何将计算的纹理连接到着色器网络。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance Output Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance输出节点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Substance输出节点

Substance输出Substance 引擎是对从纹理中计算出的纹理的引用。 它连接到Substance节点。 在Substance节点上创建输出时，Substance引擎会计算纹理，并且这些数据保存为RAM。 如果使用GPU引擎，则数据将在GPU上计算，并使用SubstanceGPU混合引擎发送回内存。 不会计算Substance节点上未激活的输出。

![](../../../assets/outputnode.png)

在此节点上，您可以在Substance Designer中的输出上看到输出信息，如Identifier 、 Label和Usage设置。 此节点还允许您在“输出缓存”部分中将纹理烘焙到磁盘。
