---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/corona/corona-for-3ds-max.html"
breadcrumb-title: ''
description: 在3ds Max中使用Substance素材和电晕渲染器，同时使用Specular/光泽度和必要的地图。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Corona > Corona for 3ds Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 用于3ds Max的电晕显示器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# 用于3ds Max的电晕显示器

## Maya增效工具中的Substance

![](../../../assets/scene-001v03.jpg)

## 科洛纳1.6 - 6

使用[3ds Max增效工具](../../../3d-applications/3ds-max/3ds-max.md)，您可以在“Substance”菜单中选择“电晕”，以自动设置带有Substance纹理输入的电晕素材。

![](../../../assets/corona.png){width="500px"}

## 科洛纳7 - 9

对于电晕渲染7及更高版本，选择“Substance到电晕”并选定Substance2节点，将为电晕物理材料创建一个网络。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/corona-physical-material?$png$&jpegSize=200&wid=857)

* **LiftGamaGain**&#x200B;是在基色输出和基色输入之间创建的。 灰度系数值为0.455时用于校正色差。
* **CoronaNormal**&#x200B;是在正常输出和基本凹凸输入之间创建，也是在涂层正常输出和透明涂层凹凸输入之间创建。 不会更改任何设置，但可以在此处修改“正常”设置。
* 在光泽颜色输出和光泽颜色输入之间创建&#x200B;**CoronaMix**。 将“混合量”设置为0，并将“基础图层”的乘数设置为2。 用户可以调整“混合量”值来控制光泽。
