---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/generated-textures-packing.html"
breadcrumb-title: ''
description: 了解Substance如何在Unity中生成纹理，并配置纹理打包以获得最佳着色器输入。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Generated Textures (Packing)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 生成的纹理(打包)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 6%

---


# 生成的纹理(打包)

“生成的纹理”显示Substance的输出，Substance 引擎计算这些输出以创建纹理。 这些纹理被输入到着色器输入中。 默认情况下，仅创建着色器使用的基本输入。 如果启用“生成所有输出”，则所有纹理都将显示在此处。

![](../../../assets/screen-shot-2022-03-29-at-1-24-16-pm-copy.png)

启用“生成所有输出”时

![](../../../assets/screen-shot-2022-03-29-at-1-29-35-pm-copy.png)

## 使用情况

1. 选择纹理图标将在“项目”窗口中选择纹理。 这对运行时材质不起作用，因为未在项目文件夹中生成纹理。
1. sRGB按钮的工作方式类似于纹理导入设置中的sRGB（颜色纹理）选项。 它允许您设置是采用灰度系数空间(sRGB)还是线性来解释纹理。 Substance增效工具会自动处理此解释，但可视需要覆盖它。

   | Substance输出 | sRGB |
   | --- | --- |
   | 底色 | 启用 |
   | Diffuse | 启用 |
   | 镜面 | 启用 |
   | 法线 | 禁用 |
   | 金属 | 禁用 |
   | 粗糙度 | 禁用 |
   | Glossiness | 禁用 |
   | 高度 | 禁用 |
   | 环境光遮蔽 | 禁用 |

## 打包通道

您可以使用下拉菜单将纹理打包到另一个纹理的Alpha通道中。 每个生成的纹理都有一个下拉菜单，其中包含由Substance材质生成的所有纹理输出的列表。 只需从列表中选择一个映射，将其打包到纹理的Alpha通道中即可。 “源”选项是纹理的Alpha通道。

在此图像中，我选择了Height映射：

![](../../../assets/screen-shot-2022-03-29-at-2-48-33-pm.png)

在下面的图像中，您可以看到Height输出正在打包到基本颜色映射的Alpha通道中。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-29-at-2-53-20-pm-copy?$png$&jpegSize=200&wid=1248)

## 输出纹理映射

此外，可以通过“输出纹理映射”部分将输出纹理分别指定给统一素材的“曲面输入”。 .sbsar生成的输出纹理将显示在左列，可用的Unity表面输入将显示在右列。 稍后可通过下拉菜单进行更改。

![](../../../assets/image2023-3-27-14-30-24.png)
