---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/maxwell/maxwell-substance-painter.html"
breadcrumb-title: ''
description: 使用适当的Substance Painter和材质设置导出Maxwell渲染器的输出模板纹理。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Maxwell > Maxwell - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maxwell -Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Maxwell -Substance Painter

Substance Painter2020.1 (6.1.0)支持Maxwell [输出模板](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/getting-started/export/export)的金属质感/粗糙度和Specular/光泽度。 只需使用Maxwell**即可导出。\
Maxwell 5.1.0**与Substance Painter集成，可轻松导入纹理并自动设置Maxwell素材。

## 导出纹理

您可以选择“Maxwell”（金属粗糙度）或“Maxwell”（Specular光泽度）输出模板来导出纹理，以便在Maxwell中渲染。

![](../../../assets/maxwell-output.png){width="500px"}

## 在Maxwell中应用纹理

您可以使用Maxwell中的Substance Painter集成自动创建应用了从Substance Painter导出的映射的材质。\
首先，右键单击“素材列表”，然后选择&#x200B;**新建>Substance Painter**。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maxwell-painter?$png$&jpegSize=100&wid=413)

浏览到导出Substance Painter纹理的位置，然后选择其中一个映射，如基色。 单击“打开”后，集成将创建一个分配有映射的新Maxwell材质。\
如果您从Substance Painter中导出多个纹理集，则集成将使用纹理的命名惯例来分配匹配的纹理映射。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/image-material?$png$&jpegSize=100&wid=620){width="600px"}

然后，可将素材分配给场景中的资源。

![](../../../assets/assigned.png){width="500px"}

使用Substance Painter集成应用的所有材质。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/materials-assigned?$pjpeg$&jpegSize=300&wid=1511){width="800px"}
