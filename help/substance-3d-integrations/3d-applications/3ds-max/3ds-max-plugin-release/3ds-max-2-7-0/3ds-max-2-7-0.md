---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-7-0.html"
breadcrumb-title: ''
description: 查看3ds Max增效工具版本2.7.0的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 3ds Max 2.7.0

<b>已添加/已更新：</b>

* 已在3ds Max增效工具中将引擎升级到版本9，从而提升了性能和兼容性。

<b>已修复：</b>

* 修复了3ds Max版本2019、2022、2023和2024中的崩溃问题，该问题会导致将Substance2节点拖入Slate材料编辑器导致程序崩溃。 现在可以将Substance2节点安全地拖放到Slate材料编辑器中。
* 解决了3ds Max的Substance增效工具中的一个问题：选择“Substance到Arnold”和其他工作流未在材料Slate编辑器中创建相关节点，而是错误地打开了带有编译错误的Maxscript。 现在，可正确生成并自动连接Arnold等工作流的节点。
* 解决了以下问题：从Substance 3D Sampler导出起始资源/预设（.sbsar -Substance2纹理图），然后在3ds Max中将它们转换为电晕渲染器（版本6到9hf1），导致材料损坏、渲染时出现黑色base color且凹凸法线损坏。 此外，此更新解决了材料中无法访问“Substance属性”选项卡的问题，该问题也影响到Vray的转换。
* 修复了3ds Max增效工具中从Substance2纹理插入或拔出Corona材料输入导致崩溃的问题
* 解决了3ds Max 2024中的兼容性问题，该问题默认情况下不允许在MaxScript文件中嵌入或调用Python脚本
* 修复了3Ds Max增效工具中的一个问题：将增效工具导入并运行Substance到Corona增效工具会导致材料在着色器预览和渲染中显示为黑色并闪亮的问题。 此问题现已成功解决，确保使用Corona渲染器正确显示和渲染Substance地图。

此版本针对3ds Max 2021、2022和2023发行
