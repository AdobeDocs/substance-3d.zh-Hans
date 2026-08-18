---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-2.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.5.2的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Unity 2.5.2

2020年7月23日发布

已添加：

* &quot;IsProcessing()&quot;函数，用于指示渲染器是忙碌还是空闲（非忙）

已修复：

* 设置2048夹具和4096目标设置时不再显示错误
* 材质属性将在从标准升级到HDRP和/或URP时继续使用
* 脚本更改Substance素材将在部署到移动设备时按预期工作
* 红色通道不再复制到Alpha，并将Alpha默认为白色
* 在Mac上更改目标设置时崩溃
* 删除了在创建Unity材质时出现的NullReferenceException错误
* 删除编辑拼贴属性后退出播放模式时出现的错误
* 启用GPU实例化可以启用
* 现有播放模式时，使用透明度的素材不会消失或错误地变黑
* 升级增效工具时，不会销毁HDRP项目中的Substance材料
