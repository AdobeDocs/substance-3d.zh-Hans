---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/modo/modo-switch-engine.html"
breadcrumb-title: ''
description: 在MODO中切换CPU和GPUSubstance引擎，以根据硬件优化性能。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Switch Engine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modo切换引擎
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# Modo切换引擎

## 切换Substance 引擎

该Substance 引擎有两个版本，即CPU和GPU。 GPU引擎用于创建高于2K的纹理。 CPU引擎仅能够生成高达2K的纹理。 如需更高分辨率的纹理，需要切换到GPU引擎。

转到“Substance工具包”菜单中的“Substance设置”选项，然后选择“切换Substance 引擎”。 您需要重新启动MODO才能启用GPU引擎。 此设置用作全局首选项。 然后，每次运行MODO时都会启用GPU引擎，直到手动切换它为止。

>[!NOTE]
>
> **使用SubstanceGPU引擎需要具有1GB或更大专用视频内存的GPU。 不支持集成的GPU。**\
> Nvidia：GeForce 650M 1 GB或更高\
> AMD：6870M或更高

![](../../../assets/switch.png)
