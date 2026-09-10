---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/cinema-4d/visual-feedback-of-animated-substances.html"
breadcrumb-title: ''
description: 在Cinema 4D中启用动画预览，以查看视口中动画Substance材料的视觉反馈。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Cinema 4D > Visual Feedback of Animated Substances
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 动画Substance的视觉反馈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---


# 动画Substance的视觉反馈

要在Cinema 4D视口中生成动画Substance的视觉反馈，应对这些材料启用“动画预览”选项。

此选项位于“材料编辑器”中的“编辑器”下（请参阅下文）。 如果材料是使用“创建材料”命令创建的，则默认情况下将启用此选项。

![](../../../assets/cinema-4d-13.png){width="500px"}


## 正在创建材料

使用Substance资源管理器中的“创建材料”命令，可以使用Substance轻松快速地创建Cinema 4D材料。

因此，将使用以下通道映射：

|  |  |
| --- | --- |
| **输出通道** Substance | **材料频道** Cinema 4D |
| Diffuse | Color |
| 放射 | 亮度 |
| 反射 | 反射率 |
| 环境 | 环境 |
| 凹凸 | 凹凸 |
| 不透明度 | Alpha |
| 镜面 | 反射率/默认Specular |
| 高度 | 位移 |
| 法线 | 法线 |

此关系仅用于“创建材料”命令，随后可修改创建的材料。 您可能希望使用此命令快速创建一个基础材质，然后只需微调几个声道即可对其进行微调。

在着色器中，您不仅可以使用上面列出的几个输出声道，还可以使用Substance提供的任何输出声道。

## 手动创建材料

您也可以使用着色器手动创建材料，而不是使用“创建Substance”命令。

只需选择材料通道中的Substance着色器，然后拖入要使用的Substance即可。 下一步，选择此着色器中使用的Substance输出声道。大功告成！

喜欢这样：

![](../../../assets/cinema-4d-15.png){width="800px"}

此方法提供了许多创作自由，可让您执行以下操作：

* 将Substance输出声道分配给任意Cinema 4D材料声道。 无需限制自己仅在目标渠道中使用它们。
* 将单个Substance输出声道分配给多个Cinema 4D材料声道。
* 将多个Substance的输出声道分配给单个Cinema 4D材料。

## 限制

* 输入参数上的关键帧显示在时间轴中，而不是显示在Cinema 4D的Powerslider（视口下方的“时间轴”滑块）中。
* 由于存在限制，因此不应在Substance输出声道上使用自定义颜色配置文件。
* 于若干情况下，Substance之图像输入将\
  Cinema 4D的“合并……”命令，该命令将两个场景合并为一个。 如果要合并的场景的Substance位于其项目目录中，并且图像输入引用了项目目录中的图像，则会发生这种情况。 在这种情况下，图像输入之后必须手动重新链接。
* 如果Substance位于项目文件夹中（或全局搜索路径中的其他位置），则它们在Cineware中不起作用。 在这种情况下，这些颜色将呈红色，就好像缺少Substance一样。 为了解决此问题，需要将Substance存档存储在项目目录之外，以便使用绝对路径引用它们。 将文件移出项目路径后，可以使用Filename参数更改文件位置。
