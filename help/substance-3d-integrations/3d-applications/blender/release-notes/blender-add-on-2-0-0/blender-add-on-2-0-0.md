---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/blender-add-on-2-0-0.html"
breadcrumb-title: ''
description: 查看Blender加载项2.0.0版的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 加载项2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# 加载项2.0.0

Substance 3D附加2.0标志着Blender用户的一次革命性更新，其特点是插件体系结构完全重构。 此重新设计的重点是无缝集成、增强的性能以及为未来的扩展提供灵活的基础。 它不仅仅是一种升级，也是对Substance素材在Blender中的处理方式的重新设想，从而满足3D专业人士不断变化的需求。

<b>版本2.0的亮点：</b>

* 重构的体系结构 — 改进的插件结构增强了性能和集成
* 未来扩展支持 — 此更新为将来轻松添加新功能奠定了基础
* 更广泛的兼容性 — 与Blender 3.0及更高版本完全兼容，包括支持Mac用户

<b>已添加/已更新：</b>

* [SRE]支持Substance 引擎选择（默认使用GPU）
* [SRE]导出纹理的新图像格式
* [SRE]每种映射类型的位深度选择
* [BLD]值输出支持
* [BLD]字符串输入支持
* [SRE]添加了选择图像导出目标的默认临时文件夹的选项

<b>已修复：</b>

* [SRE]整体性能提升
* [BLD]修复了集成工具与混合器之间的通信问题
* [BLD]集成工具安装/启动失败
* [BLD]关闭Blender时集成工具无法结束
* [BLD]更改映射的文件类型时材料未更新
* [SRE]所有材料的地图都随时导出
* [SRE]集成工具使用阶梯导出正常映射
* [SRE]Substance加载永不完成
* [SRE]物理尺寸单位未根据场景进行调整
* [BLD]在Blender中生成的预设不适用于其他集成
* [BLD]物料未在循环中更新
* [BLD]忽略输入的软限制和硬限制
* [BLD]调整参数时颜色强度未正确更新
* [SRE]集成工具卸载失败
* [SRE]我们已修复多次复制素材导致错误的问题。
* [SRE]图像节点的色彩空间现在正确匹配用户首选项。

<b>已知问题：</b>

* 使用Blender v4.0+时，多次启用和禁用后，套接字顺序不正确
* 按Cltr+Z撤消更改可能会导致错误
* 加载空文件或文件夹而不是.sbsar文件可能会损坏插件
* 支持Blender无头模式
