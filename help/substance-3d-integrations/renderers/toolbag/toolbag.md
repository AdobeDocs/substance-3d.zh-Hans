---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/toolbag.html"
breadcrumb-title: ''
description: 使用“工具包2”中的Substance粗糙度和金属质感输出进行实时素材预览和渲染。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Toolbag
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 工具袋
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 5%

---


# 工具袋

本页介绍如何对“工具箱2”使用粗糙度/金属质感输出。

工具包支持Specular/光泽度和金属/粗糙度工作流程。

Substance 3D Painter使用金属PBR着色器作为默认值，但您也可以与Specular/光泽度着色器一起使用。 此工作流程将显示如何使用工具包2的金属输出。 工具包支持金属质感的工作流程。

[下载示例场景](https://www.dropbox.com/s/qyed3un2zhtuibj/toolbag.zip?dl=0)

## 从Painter导出

1. 使用默认金属PBR着色器时，可使用默认文档通道+正常+ AO导出预设进行导出。 ***\*文档通道会根据项目配置导出法线图。 工具包需要OGL正常映射。 您可以在项目配置中切换普通格式。***
1. 或者，您可以创建使用光泽度的自定义导出配置

   ![](../../assets/settings-export.png){width="600px"}
1. 在导出之前，可以将“正常格式”更改为OpenGL。  **编辑>项目配置**

   ![](../../assets/settings-normal-format.png)

## 材质设置

1. 将反射率设置为“金属度”
1. 将反射设置为GGX
1. 将纹理添加到相应的通道中，如下图所示：

   | Substance 3D Painter纹理 | 色彩空间 | 工具包材料 |
   | --- | --- | --- |
   | 底色 | sRGB | 反射率 |
   | 粗糙度 | 关闭sRGB | 微表面 — 光泽 — 单击反转 |
   | 金属 | 关闭sRGB | 反射率 — 金属度图 |
   | 法线 | 关闭sRGB | 法线 |
   | 环境光遮蔽 | 关闭sRGB | 遮挡 |

![](../../assets/settings-toolbag.jpg){width="600px"}
