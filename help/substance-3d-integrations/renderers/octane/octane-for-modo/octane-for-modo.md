---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/octane/octane-for-modo.html"
breadcrumb-title: ''
description: 通过Live DB素材和适当的输出配置，在MODO中使用带有辛烷值渲染器的Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Octane > Octane for MODO
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 用于MODO的辛烷值
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 用于MODO的辛烷值

## MODO增效工具中的Substance

Substance输出可原生使用辛烷值。 您可以使用以下Substance输出和纹理图层效果配置。

1. 创建Substance>纹理>创建Substance并将模式设置为“不真实素材”。 使用虚线材质将允许您在高级OGL视口中查看纹理。
1. 为基色、金属、粗糙度和法线创建输出。
1. MODO使用OGL正常映射。 在Substance属性中，需要将法线方向更改为OpenGL。

   ![](../../../assets/ogl.png)
1. 载入SubstancePBR预设。 此预设为辛烷值替代。 将其拖入着色器组。

   [Substance\_PBR.lxp](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/integrations/files/162005234/162005272/1/1502792782697/substance-pbr.lxp)
1. 选择覆盖并将Substance输出从“剪辑浏览器”拖动到“示意图”视图中。 将具有文件名输出的节点连接到适当的输入节点，即基色→基色。

   ![](../../../assets/connect-6.png)
1. 连接Substance的其余输出

   ![](../../../assets/outputs-4.png){width="640px"}
