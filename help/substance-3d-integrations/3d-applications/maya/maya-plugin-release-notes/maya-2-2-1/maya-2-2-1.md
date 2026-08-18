---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-2-1.html"
breadcrumb-title: ''
description: 查看Maya插件版本2.2.1的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.2.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.2.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Maya 2.2.1

Maya 2.2.1版本：

* 将Substance 引擎更新到8.3.0
* 为Arnold添加本机支持，无需缓存到磁盘
* 在设置中启用渲染扩展并重新启动Maya后，可以使用此选项
* 支持的版本包括：
* Maya 2017 - MtoA 3.1.0/Arnold 5.2.0
* Maya 2018 - MtoA 4.0.0/Arnold 6.0.0、MtoA 4.2.0/Arnold 6.2.0
* Maya 2019 - MtoA 4.0.0/Arnold 6.0.0、MtoA 4.2.0/Arnold 6.2.0、MtoA 5.0.0/Arnold 7.0.0
* Maya 2020 - MtoA 4.0.0/Arnold 6.0.0、MtoA 4.2.0/Arnold 6.2.0、MtoA 5.0.0/Arnold 7.0.0
* Maya 2022 - MtoA 4.2.1/Arnold 6.2.0、MtoA 5.0.0/Arnold 7.0.0
* 更新了Windows和MacOS上的安装目录
* 现在使用Adobe证书对MacOS/Windows上的二进制文件进行签名
* 现在，当sbsar的作者是Allegorithmic或Adobe（而不仅仅是Allegorithmic）时，将隐藏通道切换
* 添加了新的工作流UI，增加了复制、覆盖、重命名和删除工作流的功能

添加了以下新脚本命令：

substancemaya

substanceGetEnableRenderingExtensions

substanceSetEnableRenderingExtensions

substanceworkflow.py

substanceWorkflowIsReadOnly

substanceWorkflowRenameWorkflow

substanceWorkflowDuplicateWorkflow

substanceWorkflowOverwriteWorkflow

substanceWorkflowRemoveWorkflow

错误修复：

* 修复打开“设置”对话框时出现的错误
* 生成pyc后，工作流函数不再失败

此版本在Linux、MacOS和Windows上为Maya 2017、2018、2019、2020和2022发布，在MacOS和Windows上为Maya LT 2018、2019和2020发布
