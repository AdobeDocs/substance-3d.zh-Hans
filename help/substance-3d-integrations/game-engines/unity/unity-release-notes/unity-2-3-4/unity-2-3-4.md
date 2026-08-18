---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-4.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.3.4的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.3.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# Unity 2.3.4

>[!WARNING]
>
> **在Unity 2019.2中使用插件将产生以下错误：**
> 
> InspectorSubstanceImporter.OnInspectorGUI必须调用ApplyRevertGUI以避免意外行为。\
> UnityEditor.Experimental.AssetImporters.AssetImporterEditor:OnDisable()\
> Substance.Editor.InspectorSubstanceImporter:OnDisable()
> 
> 此错误可被清除，且不会影响插件的功能

>[!WARNING]
>
> **请阅读：Substance材质中断：**\
> 包含使用空白的自定义输出的Substance素材在导入时将损坏。 此外，包含重复用法的Substance材质将损坏。\
> GameTextures.com中的旧sbsar文件当前与Unity增效工具中的Substance不兼容。 这些包含不受支持的使用量输出的素材即将中断。 在使用插件之前，请确保备份您的项目。

## 新增功能：

* 增加了对Substance 引擎v7的支持
* 增加了Linux支持

### 错误修复：

* 修复了与导入没有任何纹理映射的Substance相关的问题
* 修复了Unity 2019.x中反射过程无法正常工作的问题
* 修复了导入包含带有Substance材料的预制文件的包时的预制文件处理问题
* 反射过程之后未继续执行固定材料/纹理分配
* 修复了与更改着色器导致材质损坏相关的问题
* 修复了粗糙度未打包到金属Alpha通道的问题
* 修复了安装Substance增效工具时，更改非Substance纹理的导入设置会恢复某些选项的问题。
* 修复了Substance Source无法在Mac上打开的问题

## 已知问题：

**核心Substance增效工具**

* 用户必须在Xcode的“生成设置”菜单中禁用“启用位码”，才能为iOS生成
* Substance不使用资源包
* 重新导入后，“资源浏览器”中的Substance预览图标全部更改为SubstanceS图标
* 如果“使用”设置为“空白”的输出的自定义Substance素材将破坏该素材
* 具有重复用法的自定义Substance素材将破坏素材
* 在Linux上导入插件后，必须重新启动编辑器

**脚本**

* 如果项目在生成设置中设置为x86，则脚本在运行时不起作用
* 在某些构建平台上使用il2cpp脚本后端时出现问题

**Substance Painter实时链接**

* 在使用Substance实时链接进行绘制后构建项目，会将绘制的网格重新设置为默认材质
* 未随Painter live link发送AO频道
* 在Unity Live Link中，使用多种材质的网格不起作用
* Unity LiveLink使用SimpleJson的方式与项目中的其他SimpleJson实例发生冲突
