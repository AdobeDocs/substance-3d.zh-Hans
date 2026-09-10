---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/maxwell/maxwell-substance-painter.html"
breadcrumb-title: ''
description: 使用正确的输出模板和Substance Painter设置导出Maxwell渲染器的材料纹理。
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

Substance Painter2020.1 (6.1.0)支持金属/粗糙度和Specular/光泽度的Maxwell [输出模板](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/export/export)。 只需使用Maxwell**即可导出。\
Maxwell 5.1.0**与Substance Painter集成，可轻松导入纹理并自动设置Maxwell材料。

## 导出纹理

您可以选择Maxwell(金属粗糙度)或Maxwell(Specular光泽度)输出模板以导出纹理以便在Maxwell中渲染。

![](../../../assets/maxwell-output.png){width="500px"}

## 在Maxwell中使用纹理

您可以使用Maxwell中的Substance Painter集成自动创建应用了从Substance Painter导出的映射的材料。\
首先，在材料列表中单击鼠标右键，然后选择&#x200B;**新建>Substance Painter**。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maxwell-painter?$png$&jpegSize=100&wid=413)

浏览到导出纹理的位置，然后选择其中一个地图，例如base color。 单击“打开”后，集成将创建一个分配了映射的新Maxwell材料。\
如果从Substance Painter中导出多个纹理集，则集成将使用纹理的命名惯例来分配匹配的纹理映射。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/image-material?$png$&jpegSize=100&wid=620){width="600px"}

然后可将材料分配给场景中的资源。

![](../../../assets/assigned.png){width="500px"}

使用Substance Painter集成应用的所有材料。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/materials-assigned?$pjpeg$&jpegSize=300&wid=1511){width="800px"}
