---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-3/add-on-2-0-0-plus.html"
breadcrumb-title: ''
description: 查看Blender加载项2.0.0版及更高版本的发行说明，以了解新增功能和改进。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 2.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 加载项2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---


# 加载项2.0.0+

## 加载项2.2

<b>已添加：</b>

* 支持辛烷值渲染器
* 最初支持Redshift
* 对Renderman的初始支持

<b>已更新：</b>

* 已升级到最新版本的连接器
* 添加了使用连接器接收预设的功能
* 增强了导入预设功能：现在，包含该材料的所有SBSAR实例都将添加预设
* 标准化连接器功能

<b>已修复：</b>

* 输入图像在保存混合文件后不工作的持久性错误
* 更新着色器预设时着色器网络无法运行的问题
* 下载插件按钮中的URL不正确
* 辛烷值中的反转拼贴
* 使用第三方渲染器时输入值无法正常工作
* 未创建浮点输入值参数的问题
* Renderman色彩空间无法正常工作
* 无法按可用渲染器着色器预设

## 加载项2.1.1

此更新包括对Blender 4.0+的支持以及“附加项首选项”中的几项新功能。 我们还增加了对Substance连接器的支持，以便在Substance 3D Sampler与Blender之间无缝传输数据（发送到）并解决一些错误。 请在下方查找详细的发行说明。

<b>已添加/已更新：</b>

* 增加了Substance连接器功能（支持SBSAR文件和USD文件）。
* 支持Blender 4.0及更高版本。
* 支持SRE版本2.1.0。
* 在“附加项偏好设置”中：
  * 能够选择Substance集成工具安装路径。
  * 将集成工具重置为默认路径的按钮。
  * 用于打开集成工具文件夹的按钮。
  * 已添加“应用类型”以指定材料（插入：将其设置为主要材料，附加：将其添加到列表的底部）。
  * 已添加复选框以选择输入组的默认行为（折叠/展开）。
  * 已添加复选框以选择“仅更新纹理”属性的默认行为。
  * 打开“Blender”（混合器）时自动启动Substance远程引擎(使用“Connector”（连接器）时必须启用)。
* 在附加：
  * “仅添加”选项将更新纹理（允许更改参数而不重新创建节点图形）。
  * 添加了“展开所有组”和“折叠所有组”按钮。
  * 已添加输入图像组，以便根据需要在SBSAR中对所有输入图像分组。
  * 参数输入现在按与Designer相同的顺序显示。
  * 添加了每个Substance素材的缩览图预览。

<b>已修复：</b>

* 修复了常规输入组为空的错误。

<b>已知问题：</b>

* 选择对象时自动选择SBSAR的功能目前不起作用，因此被禁用。

## 加载项2.0.0

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
* [SRE]我们已经修复了多次复制材料导致错误的问题。
* [SRE]图像节点的色彩空间现在正确匹配用户首选项。

<b>已知问题：</b>

* 使用Blender v4.0+时，多次启用和禁用后，套接字顺序不正确
* 按Cltr+Z撤消更改可能会导致错误
* 加载空文件或文件夹而不是。sbsar 文件可能会损坏增效工具
* 支持Blender无头模式
