---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-0.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.4.0的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Unity 2.4.0

>[!WARNING]
>
> Unity将默认构建体系结构更改为x86而不是x86\_64。\
> 如果脚本引用Substance，则脚本将不会运行。 您需要改回x86\_64 ，该版本就可以了。

## 新增功能：

* 已添加HDRP项目支持（预览）
* 在“Substance”菜单中添加了偏好设置
* 增加了设置默认Substance分辨率导入设置的功能
* 增加了设置默认“正常”压缩的功能
* 增加了在导入Substance时生成所有输出的功能
* 支持自定义输出+具有相同用法的输出
* 添加了平台分辨率设置
* 添加了IL2CPP支持错误修复

### 错误修复：

* 修复了在Mac操作系统上打开Substance Source时会出现Linux错误的错误
* 缩短了切换平台所需的时间。 现在，移动平台的纹理转换在构建时完成，而不是在切换目标平台时完成。
* 导入sbsar时出现“断言失败”错误
* 使用.NET 3.5升级项目会导致Substance材质损坏
* 在OS X上显示的Linux对话框中不支持Substance源
* 在ForceText序列化模式下，图形名称更改会销毁预建文件和场景文件
* 使用相同用法的具有多个输出的Substance素材将中断。增效工具不支持sbsar中的自定义输出

### 已知问题：

* 在2017-2018/2019年度升级项目时，用户导入Substance增效工具后，必须重新启动Unity才能更新项目。\
  解决方法：创建一个资源/项目包，然后使用2.4.0增效工具将该包导入到较新的项目中。 应正确转换Substance文件。
* Unity已将默认生成体系结构更改为x86。 目前，Substance插件仅支持x86\_64。

**不再完全受支持：**

* Substance实时链接已从Asset Store包中删除。 （仍可从Substance share下载该包）
