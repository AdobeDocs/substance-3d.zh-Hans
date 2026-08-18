---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/keyshot.html"
breadcrumb-title: ''
description: 在关键帧渲染器中使用Substance素材，通过导出的纹理图实现产品可视化。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Keyshot
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Keyshot
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 8%

---


# Keyshot

*Keyshot 6.1.72*[&#x200B;下载示例场景](https://www.dropbox.com/s/rvjsbbcx7c74aah/keyshot.zip?dl=0)

## Substance Painter导出

1. 对于“关键帧”，您将需要使用“扩散”、“反射”、“金属”、“粗糙度”和“法线（直接X）”配置导出预设。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/key-01?$png$&jpegSize=300&wid=1794)

## 高级物料设置

您将使用2种高级材质。 一种是金属材料，另一种是介电材料。

1. 将素材设置为“高级”，并用图形表示素材。

   **金属质感：**\
   a. 将折射率设置为10\
   b. 按照下表所示设置映射

   | Substance Painter纹理 | 高级材质通道 |
   | --- | --- |
   | Diffuse | Diffuse |
   | 金属 | 不透明度 |
   | 法线 | 凹凸\*法线启用 |
   | 粗糙度 | 粗糙度 |
   | 反射 | 镜面 |

1. 创建新的高级材质

   **电介质：**\
   a. 将“折射率”设置为1.5\
   b. 按照下表所示设置映射

   | Substance Painter纹理 | 高级材质通道 |
   | --- | --- |
   | Diffuse | Diffuse |
   | 法线 | 凹凸\*法线启用 |
   | 粗糙度 | 粗糙度 |
   | 反射 | 镜面 |

1. 将金属高级材料的输出添加到介电高级材料的+。 这将在素材上创建标签字段。

   ![](../../assets/key-02.png)
