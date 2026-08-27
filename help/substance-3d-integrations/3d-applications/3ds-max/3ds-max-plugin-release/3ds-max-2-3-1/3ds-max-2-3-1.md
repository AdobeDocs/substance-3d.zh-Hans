---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-1.html"
breadcrumb-title: ''
description: 查看3ds Max增效工具版本2.3.1的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---


# 3ds Max 2.3.1

2020年2月13日发布

该插件现在安装在3ds Max目录之外的C:\ProgramData\Autodesk\ApplicationPlugins\SubstanceIn3dsMax中。 它现在可以在任何要求3ds Max查找插件的地方工作，因此它现在应该可以安装在网络驱动器等上。\
请注意，切换到应用程序插件并更改安装目录会使从2.1.1版本及更低版本的升级无法正常工作。 对于3ds Max 2018和2019，应手动删除这些端口。 2.2.0版本应正确升级。\
对于此版本中未解决的一些问题，我们计划不久将再发布一个问题来修复这些问题和任何其他可能出现的问题。

此版本目前针对3ds Max 2018、2019、2020和2021发行。

* 现在，“加载sbsar”会首先查找项目图像文件夹
* 现在仅针对VRay RT和VUE文件渲染器显示渲染器兼容性对话框
* 拖放已禁用的Slate材料编辑器，以删除Max批处理问题
* 渲染对话框不再显示在3ds Max静默模式下
* 较小的Python脚本现在与Python 3兼容
* 增加了对Substance启动器将Substance Source资源发送到3ds Max的支持。 这将需要更改启动器，但添加该功能时，将会提供插件支持。
* 现在，Redshift渲染器脚本使用Redshift 2.6.24中设置的新节点名称
* 为Substance2 SubstanceFilePath分配空崩溃时，最大路径不再为
* 删除SubstanceOutput类型与旧插件的名称冲突
* 将SubstanceOutput类重命名为Substance2Output
* 将Substance菜单管理器类重命名为Substance2MenuManager
* 现在，打开场景时会强制清除参数块ID，从而删除场景文件之间的冲突。 这应该可以修复在场景之间切换时加载时参数块无效的问题。 导入可能仍存在问题，因为这需要进行更复杂的更改
* 现在，增效工具安装在3ds Max之外。 所有路径都已更改为相对于载荷位置。
* 该插件现在使用Autodesk应用程序插件系统。
