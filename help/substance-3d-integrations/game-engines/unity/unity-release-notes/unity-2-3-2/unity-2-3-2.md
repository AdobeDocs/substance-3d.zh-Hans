---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-2.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.3.2的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Unity 2.3.2

## 新增功能：

* 材质序列化
* 反射：该增效工具现在允许导入包中的旧Substance文件（导入时自动更新为新Substance数据）
* 在导入包含Substance数据的包时，材料属性会结转
  * 注意：这仅适用于使用2.3.0更新版或更高版本创建的包
* 向Substance图形菜单中添加了“烘焙纹理”按钮

### 错误修复：

* 修复了在删除Substance文件夹后库材料拼贴重置的问题
* 提升了退出播放模式的速度
* 修复了在SubstanceDLL正在使用时更新增效工具时崩溃的问题
* 现在无法在Unity中删除Allegorithmic文件夹。
  * 注意：无法修改Allegorithmic文件夹的内容。 在Unity中删除该文件夹可能导致多个问题，从而导致Allegorithmic文件夹在关闭并重新打开Unity时神奇地再次出现。 现在会出现一条警告，通知用户在Unity从项目的Assets文件夹手动关闭的情况下删除它
* 提升了退出播放模式的速度
* 修复了在删除Substance文件夹后重置库素材属性的错误

## 已知问题：

**核心Substance增效工具**

* 用户必须在Xcode的“生成设置”菜单中禁用“启用位码”，才能为iOS生成
* Substance不使用资源包
* 重新导入后，“资源浏览器”中的Substance预览图标全部更改为SubstanceS图标

**脚本**

* 如果项目在生成设置中设置为x86，则脚本在运行时不起作用
* 在某些构建平台上使用il2cpp脚本后端时出现问题

**Substance Painter实时链接**

* 在使用Substance实时链接进行绘制后构建项目，会将绘制的网格重新设置为默认材质
* 未随Painter live link发送AO频道
* 在Unity Live Link中，使用多种材质的网格不起作用
* Unity LiveLink使用SimpleJson的方式与项目中的其他SimpleJson实例发生冲突
