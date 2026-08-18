---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/parameters.html"
breadcrumb-title: ''
description: 通过“Substance属性”面板在MODO中修改Substance材质参数以自定义材质。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---


# 参数

Substance具有一组核心参数。 这些参数分为Substance、输出和微调。 可在“Substance属性”面板中找到它们。\
从Substance中将包含技术参数和渠道。 在MODO中，“通道”选项无效。 使用“输出”部分启用/禁用输出。

![](../../../assets/parameters-4.png){width="300px"}

## Substance

Substance具有一组核心参数，可以在“Substance属性”面板的“Substance”类别中找到这些参数。

* **重新加载Substance：**&#x200B;此参数允许您重新加载Substance。 它旨在与Substance Designer配合使用。 如果您正在处理自定义Substance并添加了新的调整或输出，则可以将新发布的Substance重新加载回MODO。 将添加新的微调和输出，并保留以前的微调设置。
* **着色模式：**&#x200B;此参数允许您设置用于Substance的着色模式。 Principled（默认）、Unreal、Unity或glTF。
* **重置Substance：**&#x200B;此参数会将微调重置为默认设置。
* **选择图形：**&#x200B;允许您选择Substance文件中的哪个图形来创建材质。
* **加载预设：**&#x200B;您可以加载一个预设，这将配置Substance微调参数。 可以使用Substance Player创建预设。 预设文件是.sbsprs文件类型。 加载预设后，您需要单击“预设”下拉菜单并选择预设，因为.sbspr可以包含多个预设。
* **保存预设：**&#x200B;允许您保存预设
* **选择预设：**&#x200B;允许您选择Substance文件中的嵌入预设或从MODO中存储的预设中进行选择。
* **烘焙到磁盘：**&#x200B;此参数会将由Substance生成的纹理烘焙到位图文件。
* **输出大小：**&#x200B;此参数会将纹理动态调整为所设置的大小。 Substance 引擎会将纹理重新生成到所需大小。
* **随机植入：**&#x200B;此参数将改变Substance的程序生成。 此参数非常适合创建同一Substance的随机版本。 它允许您快速改变Substance参数以生成新版本的纹理

## 输出

“输出”选项允许您启用或禁用Substance输出。 输出是由Substance 引擎生成并在着色器树中渲染为纹理。

![](../../../assets/outputs-02.png){width="300px"}

## 调整

微调是在Substance文件中编写并可在MODO中编辑的参数。 您可以选择通道，在“项”模式中，使用“通道拖动”在弹出控制器中一起获取控件。

![](../../../assets/haul.png){width="300px"}
