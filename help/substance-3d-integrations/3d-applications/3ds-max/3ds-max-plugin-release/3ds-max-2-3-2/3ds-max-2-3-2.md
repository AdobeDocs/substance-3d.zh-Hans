---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-2.html"
breadcrumb-title: ''
description: 查看3ds Max增效工具版本2.3.2的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# 3ds Max 2.3.2

2020年4月8日发布

今天我们发布了增效工具的2.3.2版本，它主要是2.3.1之上的错误修复版本。

2.3.2版：

* 将Substance 引擎更新至7.2.9
* 修复了Redshift/VRay在3ds Max 2018、2019和2020中渲染时崩溃的问题
* 不再出现调试断言错误
* Substance2节点现在可正确使用iMultipleOutputChannelsWithValues的脚本接口
* 现在，菜单上的Substance源条目将会打开Substance启动器，如果源选项卡已安装，则会打开该启动器
* 现在，在使用Corona渲染器时，应正确更新材料
* 与VRay Next一起使用时，Substance输出不再临时替换为图像
* 渲染兼容性对话框已从自动显示中删除。 如果需要，它仍然可以在“设置”对话框中使用
* 修复了在3ds Max 2021中应用Substance材料时导出fbx时可能出现的问题

已知问题：

* 在3ds Max 2018中，导出带有材料的fbx将崩溃在fbxmax.dlu插件中。 我们目前正在与Autodesk联系，以确定我们这一端是否有可执行的操作，或者这是否是旧版fbx集成的限制。 以前的解决方法不可靠，已被删除。 在3ds Max 2019或更高版本中不会发生这种情况。

此版本针对3ds Max 2018、2019、2020和2021发行。
