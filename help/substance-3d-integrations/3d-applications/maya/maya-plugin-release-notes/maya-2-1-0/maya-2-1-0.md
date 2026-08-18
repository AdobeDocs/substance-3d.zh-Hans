---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-1-0.html"
breadcrumb-title: ''
description: 查看Maya增效工具版本2.1.0的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.1.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.1.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Maya 2.1.0

Maya 2.1.0 changelog中的Substance

* 确保与Python 3的兼容性
* Substance 引擎已更新至版本7.2.9
* 修复了应用工作流程时出现的全局梅尔变量名称冲突的错误
* Redshift工作流程现在将fresnel设置为金属性
* 添加了新的增效工具文件substancelink，它处理与其他Substance程序和Substance启动器的互操作性
* 如果加载了substancelink增效工具，现在打开Substance Source将会打开“源”选项卡的Substance启动器
* Substancelink增效工具允许启动器在添加UI时，将Substance Source素材发送到Maya集成
* 添加脚本命令以获取内部库版本以及打开substance启动器以进入源页面
* 网站链接现在已打开到[substance3d.com](http://substance3d.com)而不是[allegorithmic.com](http://allegorithmic.com)
* 现在，打开网页时，文档和源链接将打开用户设置的默认浏览器
* 在Windows上，不再打开Internet Explorer
* 在书架和菜单中添加了要Substance share的新链接
* 添加了用于查询Substance链接器版本和哈希的新命令
* 在Maya LT中，该版本已从设置菜单中删除
* “关于”菜单不再使用PySide2和Python编写，而是使用本机代码中的Qt进行编写。 它现在可以在Maya LT中使用，而它以前并不存在。
* “关于”菜单具有不同的诊断信息；它现在显示git哈希以匹配源代码管理中的更改
* “关于复制到剪贴板”菜单现在也将具有此Git哈希以及该插件所针对的Maya版本。
* “关于”窗口中的许可证现在以文本文件形式打开
* 增加了对Maya 2017的支持
* 工作流脚本生成器不再输出“ordering”成员的字符串。 任何现有工作流都将得到妥善处理

添加的脚本命令：\
substancemaya：\
\* substanceUtilityGetLinkerVersion\
\* substanceUtilityGetLinkerHash\
\* substanceUiOpenAboutWindow\
\* substanceUiOpenSourceWebsite\
\* substanceUiOpenDocumentation\
\* substanceUiOpenShareWebsite

substancelink：\
\* substanceLinkGetLinkVersion\
\* substanceLinkGetPortalCliVersion\
\* substanceLinkOpenLauncher

此版本适用于Windows上的Maya 2017、2018、2019和2020。\
Linux和Macos。 2018年、2019年和2020年Maya LT上映\
Windows和MacOS。
