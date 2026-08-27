---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/color-management/substance-textures-in-maya.html"
breadcrumb-title: ''
description: 在Maya中为纹理配置色彩空间设置，以确保准确的色彩管理和渲染。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management > Substance textures in Maya
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya中的Substance纹理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Maya中的Substance纹理

为映射设置的色彩空间取决于[Maya色彩管理设置](https://help.autodesk.com/view/MAYAUL/2020/ENU/?guid=GUID-B260195C-A0FE-4F51-9EA2-099B61B7725A)中建立的设置和规则。

Maya增效工具中的Substance在文件节点上设置为“忽略色彩空间文件规则”。 该增效工具会使用下列方式处理色彩空间设置，而不管色彩管理：

BaseColor、Diffuse、Emissive、Specular= sRGB\
正常、Height、位移、粗糙度、金属= RAW

通常，对于表示非颜色数据的图像，您需要将色彩空间设置为RAW 。 但是，此设置可能会受到您在“色彩管理”中设置的规则的影响。

![](../../../assets/raw.png)
