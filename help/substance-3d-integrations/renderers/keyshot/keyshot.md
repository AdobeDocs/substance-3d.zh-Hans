---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/keyshot.html"
breadcrumb-title: ''
description: 使用关键帧渲染器中的材料可直观显示导出的纹理图。
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

1. 对于关键帧，您需要使用“Diffuse”、“反射”、“金属”、“粗糙度”和“正常（直接X）”配置导出预设。

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/key-01?$png$&jpegSize=300&wid=1794)

## 高级材料设置

您将使用2个高级材料。 一个是金属的，另一个是介电的。

1. 将材料设置为“高级”，然后图形材料。

   **金属质感：**\
   a. 将折射率设置为10\
   b. 按照下表所示设置映射

   | 纹理 | 高级材料渠道 |
   | --- | --- |
   | Diffuse | Diffuse |
   | 金属 | 不透明度 |
   | 法线 | 凹凸\*法线启用 |
   | 粗糙度 | 粗糙度 |
   | 反射 | 镜面 |

1. 创建新的高级材料

   **电介质：**\
   a. 将“折射率”设置为1.5\
   b. 按照下表所示设置映射

   | 纹理 | 高级材料渠道 |
   | --- | --- |
   | Diffuse | Diffuse |
   | 法线 | 凹凸\*法线启用 |
   | 粗糙度 | 粗糙度 |
   | 反射 | 镜面 |

1. 将金属高级材料的输出添加到“介质高级”材料的+。 这将在材料上创建一个标签字段。

   ![](../../assets/key-02.png)
