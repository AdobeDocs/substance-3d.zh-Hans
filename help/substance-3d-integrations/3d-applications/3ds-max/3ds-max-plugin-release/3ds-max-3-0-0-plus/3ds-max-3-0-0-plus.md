---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-3-0-0-plus.html"
breadcrumb-title: ''
description: 查看3ds Max增效工具版本3.0.0及更高版本的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Ds Max 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# 3ds Max 3.0.0+

## 3ds Max 3.0.4

<b>已添加/已更新：</b>

* 使用最新图标更新了Substance增效工具图标。
* 增加了对使用插件中的连接器发送和接收预设的支持。
* 集成了Menu Manager中的通知参数，以替换核心界面的使用。

<b>已修复：</b>

* 解决了石板材质编辑器打开并选择Substance2纹理映射时，Substance2材质可能无法在IR/Production with Corona中渲染的问题。
* 解决了Sampler连接器更新创建新的Substance2节点而不是更新现有节点的问题。
* 解决了添加Substance2节点时3ds Max增效工具中的崩溃问题，并确保使用批量导入加载.sbsar文件不再打开脚本编辑器。
* 解决了使用.msi安装程序时，由于.dll文件不兼容，导致3DSMax 2025插件加载失败的问题。

## 3ds Max 3.0.2

<b>已添加/已更新：</b>

* 通过将所有现有图标合并到qrc和rcc文件中，实现Substance增效工具中图标管理的标准化，与Autodesk的首选方法一致，并确保在SBSAR图形面板中加载的一致性。
* 提高了增效工具中“Substance设置”窗口的响应能力，以确保在调整窗口大小时输入字段及其描述能够正确匹配。
* Substance增效工具现在与Corona 11兼容。

<b>已修复：</b>

* 解决了在V射线素材中光泽颜色和光泽粗糙度未自动连接的问题。 现在，在V-Ray和Arnold中创建工作流程时，这两个属性都将自动链接。
* 修复了增效工具中的UI问题，即如果保存的值为一位数，则调整CPU核心限制设置可能会错误地显示两位值。
* 修正了控制台中与Substance兼容性功能相关的3ds Max增效工具v3.0.0渲染错误。 现在，使用“Substance批量导入”菜单创建的Substance节点会按预期渲染。
