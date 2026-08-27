---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-3-0-0-plus.html"
breadcrumb-title: ''
description: 查看Maya增效工具版本3.0.0及更高版本的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > Maya 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Maya 3.0.0+

## Maya 3.0.3

<b>已添加/已更新：</b>

* 增强的Maya插件的缓存系统在最初创建网络时仅缓存一次，并启用手动缓存。
* 提供了一个用于更改Maya增效工具中“substance”文件夹位置的选项。
* 更新了Maya增效工具的工作流导入系统，以确保与Autodesk更新至Python 3.12兼容。
* 使用最新图标更新了Substance增效工具图标。
* 增加了对使用增效工具中的连接器发送和接收预设的支持。

<b>已修复：</b>

* 解决了加载/卸载Maya的Substance增效工具时产生错误屏幕和崩溃的问题。
* 修复了缓存问题，特别是确保.exr文件正确引用，以及减少大型场景中与缓存相关的冻结。
* 解决了在Maya增效工具中加载材料时无法在“示例”窗口中显示Sbsar 文件预览的问题。
* 解决了至少有一个SBSAR已在Hypershade中时连接器无法接收Sbsar 文件的问题。
