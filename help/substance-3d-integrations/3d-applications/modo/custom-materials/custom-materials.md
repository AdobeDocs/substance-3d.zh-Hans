---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/modo/custom-materials.html"
breadcrumb-title: ''
description: 在MODO中将Unreal、Unity和glTF自定义素材与Substance增效工具一起用于专门的工作流程。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Custom Materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自定义材质
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 12%

---


# 自定义材质

Substance增效工具支持Unreal、Unity和glTF自定义素材。 在加载sbsar文件之前，可以选择要使用的着色模式。

## 目录

## Unity材质

使用Unity素材时，将自动设置素材图层效果。 Substance增效工具会将Unity素材直接放在Substance项素材的上方。

| Substance输出 | 色彩空间 | 材质图层效果 |
| --- | --- | --- |
| 底色 | sRGB | Unity反照率 |
| Glossiness | 线性 | UnitySmoothness |
| 金属 | 线性 | 统一金属质感 |
| 法线 | 线性 | 统一标准 |
| 放射 | sRGB | 在图像静止图像&#x200B;**上，Unity发射**\*设置为sRGB |
| 高度 | 线性 | Unity Bump |
| 环境光遮蔽 | 线性 | Unity环境遮蔽 |

![](../../../assets/unity-1.png){width="600px"}

## 不真实素材

使用非真实材质时，将自动设置材质图层效果。 Substance增效工具会将非真实素材直接放在Substance项素材的上方。

| Substance输出 | 色彩空间 | 材质图层效果 |
| --- | --- | --- |
| 底色 | sRGB | 非实基色 |
| 粗糙度 | 线性 | 不真实粗糙度 |
| 金属 | 线性 | 不实金属质感 |
| 法线 | 线性 | 非实常值 |
| 高度 | 线性 | 不真实的凹凸 |
| 放射 | sRGB | 在图像静态&#x200B;**上，将非真实发射率**\*设置为sRGB |
| 环境光遮蔽 | 线性 | 非真实环境遮蔽 |
| 不透明度 | 线性 | 需要取消选中“纹理”图层&#x200B;**上反相的不透明度**\*虚值 |

![](https://helpx-prod.scene7.com/is/image/HelpxProd/unreal?$png$&jpegSize=200&wid=1343){width="600px"}

您可能需要反转正常值。 如果Substance具有法向方向控件，则可以从“调整”菜单执行此操作。 如果没有，可以对纹理本身执行此操作。 有关详细信息，请参阅“**[使用法线](../../../3d-applications/modo/working-with-normals/working-with-normals.md)**”页面。

## glTF材质

使用glTF材质时，将自动设置材质图层效果。 Substance增效工具会将glTF素材直接放在Substance项素材的上方。

| Substance输出 | 色彩空间 | 材质图层效果 |
| --- | --- | --- |
| 底色 | sRGB | glTF基色 |
| 粗糙度 | 线性 | glTF粗糙度 |
| 金属 | 线性 | glTF金属质感 |
| 法线 | 线性 | glTF普通 |
| 放射 | sRGB | 在图像静态&#x200B;**上，glTF发射率**\*设置为sRGB |
| 环境光遮蔽 | 线性 | glTF环境遮蔽 |

![](../../../assets/gltf.png){width="600px"}

您可能需要反转正常值。 如果Substance具有法向方向控件，则可以从“调整”菜单执行此操作。 如果不是，则可以对纹理本身执行此操作。 有关详细信息，请参阅“**[使用法线](../../../3d-applications/modo/working-with-normals/working-with-normals.md)**”页面。
