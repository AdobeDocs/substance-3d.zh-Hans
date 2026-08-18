---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-4.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.4.4的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# Unity 2.4.4

2020年2月发布

* 已添加：对2019.3的正确支持：修复了破坏Substance增效工具脚本对象的Unity API更改。 重工对象以使用2019.3 API更新。 修复 — 使用自定义素材会导致退出播放时素材变黑
* 修复 — 在脚本中使用Duplicate()函数，然后进入和退出播放时崩溃。
* 固定 — 2019.3版中的素材拼贴、设置和着色器重置
* 固定 — HDRP材质着色器未刷新参数更改
* 修复 — HDRP蒙版映射未更新
* 固定 — 为Duplicate函数添加字符串参数
* 已修复 — 在最新的Unity稳定版中修复Linux支持
* 修复 — 解决iOS中必须禁用位码的问题

已知问题：

* 重命名HDRP资源将导致增效工具不生成蒙版映射。
* 在HDRP项目中使用Substance增效工具时，使用Raw压缩会将灰度纹理设置为Alpha8。
* 在“播放”模式下，将取消选择GameObjects
* 在“播放”模式中单击Substance图表上的“生成Mip映射”时，更改参数会导致无限挂起。
