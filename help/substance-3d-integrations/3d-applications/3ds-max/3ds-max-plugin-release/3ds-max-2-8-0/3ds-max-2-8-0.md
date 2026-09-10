---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-8-0.html"
breadcrumb-title: ''
description: 查看3ds Max增效工具版本2.8.0的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.8.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# 3ds Max 2.8.0

<b>已添加/已更新：
</b>

* 支持参数的条件可见性(“visible if”)；现在，当条件不满足时，将隐藏参数，同时保持其相应的组可见。
* 已将Corona渲染器升级到3ds Max增效工具中的版本10，提升了渲染功能并
* 在使用Substance时，此最新更新显着提高了3ds Max 2024中的渲染速度和CPU利用率，使其性能与3ds Max 2022中观察到的效率更加接近。

<b>已修复：</b>

* 增强了Substance增效工具，将键盘输入值限制在每个参数的实际范围内，从而防止出现滑块控制和手动值调整的问题。
* 解决了在Slate纹理编辑器中复制Substance2材料转换(.sbsar)会导致所复制节点意外实例化，从而可能导致与d3d11.dll相关的崩溃的问题
* 解决了使用Corona Interactive渲染自定义/编辑的复制材料物质(.sbsar)时3ds Max中的崩溃问题
* 修复了3ds Max的Substance2整数中的一个问题：节点3和节点4的滑块无响应，且仅手动数字输入更新了值。 此外，这些值错误地以浮点格式显示。 滑块现在起作用并准确反映预期值类型。
* 解决了使用Corona渲染的3ds Max 2021中的一个问题：材料在视口中正确显示，但在文件传输到另一台电脑时呈现灰色。 用户不再需要从头开始设置材料或加载预设以进行正确渲染。
* 解决了尝试在Slate材料编辑器中复制Substance崩溃时3ds Max增效工具中的节点问题。
* 解决了重新启动3ds Max后未保存Substance增效工具中的“CPU内核限制”设置的问题，从而确保用户配置的值现在跨会话保留。

此版本针对3ds Max 2021、2022和2023发行
