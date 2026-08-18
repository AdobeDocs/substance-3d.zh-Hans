---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-6-0.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.6.0的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.6.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.6.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# Unity 2.6.0

2021年6月7日发布

更新/添加：

* 访问Substance Source的全新工作流程！ 现在，Substance Source操作可访问Substance启动器中的“源”选项卡，从而允许将资源直接发送到Unity
* 可以将插件版本信息复制到剪贴板
* 已从目标设置中删除“加载时生成”

修复：

* 在HDRP项目中，当对材质设置进行更改时，位移模式将恢复为默认值（镶嵌）
* “检查器”窗口中不显示分辨率大小
* 无法将插件安装到Unity版本2020.2及更高版本

已知问题：

* 从早期版本2.5.4及更低版本更新插件时，出现“拒绝访问”错误和/或崩溃
  * 解决方法：在安装增效工具版本2.6.0之前，需要从Unity Project版本2020.2及更高版本中卸载以前的增效工具版本2.5.4及更低版本
* 安装Substance增效工具后，检查器中不会显示图像文件的纹理预览
  * 此问题的根源在于Unity，计划由Unity在其2021.2版（目前为Beta版）中修复
