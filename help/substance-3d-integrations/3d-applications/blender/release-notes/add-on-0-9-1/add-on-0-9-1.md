---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-1.html"
breadcrumb-title: ''
description: 查看Blender加载项0.9.1版的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 0.9.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 加载项0.9.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# 加载项0.9.1

**加载项版本0.91+**&#x200B;的发行说明

* 注意： *增效工具版本0.91+与以前版本的增效工具没有向后兼容性！*
* 重新构建内部代码库以提高插件的性能和稳定性
* 改进了UI以改进整体用户体验
* 添加了UI，可修改默认拼贴
* 增加了对在循环渲染视图中更新纹理的支持
* 在控制台中添加了错误处理，以在Substance加载失败时发出通知
* 已使用快速操作更新浮动菜单

**首选项部分：已添加/已更新：**

* “导出图像格式”参数；将在Blender中生成的图像用作Substance素材的图像输入时，可使用此格式将该图像保存到“时间”文件夹。
* Sbsar库路径；指定在使用“加载”按钮搜索Substance文件时默认打开的文件夹。
* 默认纹理导出路径（“时间”文件夹），它模拟Substance3d Painter用于处理未保存文件导出的路径
* 纹理相对路径与上述路径相同，可选择使用$matName等项创建子文件夹
* Sbsar文件创建子文件夹的相对路径，该子文件夹打包在保存项目时混合文件中使用的sbsar文件
* 能够在首选项中动态设置不同的着色器网络 — 在着色器网络中，可以根据着色器的需要为每个着色器设置不同的变量
* 在着色器网络的输出部分中，可以设置默认情况下是否启用输出
* 能够设置色彩空间（这将支持aces、线性exr和blender影片工作流程，而不仅仅是srgb）
* 图像格式和位深度的默认选择
* 一种通用输出，用于设置着色器中未定义的输出用法的值，例如，如果您有另一个默认情况下着色器未使用的输出，例如蒙版。
* 用于更改输出类型的过滤器（1仅启用的输出，2着色器和Substance中的所有输出，3Substance中的所有可用输出）
* 支持自定义快捷键（已编辑）

**Substance 3D面板部分：已添加/已更新：**

* 能够调整和锁定拼贴和分辨率参数值
* 更新的预设UI — 着色器类型下拉菜单，用于更改用户想要的图表类型
* 已将图像输入参数更改为混合器中使用的标准图像输入。 您现在可以使用混合器图像，而不仅仅是文件
* 能够随时在多个Blender实例中工作
* 在视区中选择素材后，支持在Substance 3D面板中自动突出显示素材
