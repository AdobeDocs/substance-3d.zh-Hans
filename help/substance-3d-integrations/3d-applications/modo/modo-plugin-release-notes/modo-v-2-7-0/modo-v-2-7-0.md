---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/modo-plugin-release-notes/modo-v-2-7-0.html"
breadcrumb-title: ''
description: 查看MODO增效工具版本2.7.0的发行说明，以了解新功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Plugin Release Notes > Modo v. 2.7.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modo诉 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Modo诉 2.7.0

* 大量崩溃修复
* 支持32位浮点
* CPU引擎中的4k纹理和GPU引擎中的8k纹理
* 增效工具版本的新LPK格式
* Substance增效工具的新工具包菜单
* glTF/对MODO 12.0的原则性着色器支持
* 已为Substance文件添加相对路径
* Linux支持
* 用于加载和保存预设的新UI
* 从Designer加载嵌入的预设
* 已删除GPU内存警告框
* 已编辑的预设加载/存储命令

  可用的新命令包括：

  **substance.getsbsname**&#x200B;将substance对象的标识符转换为其内部名称

  所有这些文档都期望从substance.getsbsname获得正确的内部名称：

  **substance.setpreset**&#x200B;将Substance的当前预设设置为索引&#x200B;**substance.getpresetindex**&#x200B;获取当前预设索引&#x200B;**substance.getpresetat**&#x200B;以给定的&#x200B;**index substance.getpresetcount**&#x200B;返回预设的字符串名称返回Substance具有&#x200B;**substance.savepresetfile**&#x200B;将当前配置的预设保存到给定文件路径&#x200B;**substance.loadpresetfile**&#x200B;将预设文件加载到给定文件路径的Substance

  UI命令：

  **substance.loadpresetui** UI命令，用于加载预设&#x200B;**substance.savepresetui** UI命令，用于存储预设&#x200B;**substance.selectpresetui** UI命令，用于设置预设
