---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/upgrading-projects-known-issues.html"
breadcrumb-title: ''
description: 了解升级具有材料的Unity项目以及迁移期间要避免的已知问题。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Upgrading ProjectsKnown Issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 升级项目已知问题
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# 升级项目/已知问题

>[!WARNING]
>
> 适用于Unity 3.0.0的Substance 3D增效工具不支持向后兼容性。 因此，请确保使用Unity 2020.3.27x及更高版本。
> 
> Unity将默认构建体系结构更改为x86而不是x86\_64。\
> 如果脚本引用Substance，则脚本将不会运行。 您需要改回x86\_64 ，该版本就可以了。

## 已知问题

* 导航面板文件夹时，出现“*表达式断言失败”错误。*
  * 这是在Unity端发生的错误，当对UI进行更改（通常为缩略图更改）时，应会显示无害的消息。
* *图像输入似乎锁定为8位*
  * 此问题已在版本3.8.0-3中修复。 正确的工作流程是用户将Unity的纹理默认格式更改为RGBA64。 该增效工具将负责正确地将该信息发送到Substance 引擎。
