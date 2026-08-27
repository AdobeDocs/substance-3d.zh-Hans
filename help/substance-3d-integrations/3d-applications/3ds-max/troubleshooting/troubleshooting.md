---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/3ds-max/troubleshooting.html"
breadcrumb-title: ''
description: 使用脚本侦听器诊断并解决3ds Max中的Substance增效工具问题，以获取错误消息。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 故障排除
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---


# 故障排除

脚本侦听器可用于诊断使用插件时遇到的错误。 要打开脚本侦听器，请导航到“脚本菜单”>“脚本侦听器”。 当插件使用过程中发生错误时，相应的错误消息将打印到此脚本侦听器窗口。 有关详细信息，请访问[正式脚本编辑器文档](https://help.autodesk.com/view/3DSMAX/2023/ENU/?guid=GUID-C8019A8A-207F-48A0-985E-18D47FAD8F36)。

要报告错误，请加入[SubstanceDiscord服务器](https://discord.com/invite/substance3d)上的#3dsmax-plugin频道或访问[Adobe群](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-autodesk3dsmax)。 控制台日志中的相关信息以及针对该问题的任何复制步骤都可以包含在报告中。

## 已知问题

* *将使用漫射输出的.sbsar替换为.sbsar，后者不使用漫射引线，由于丢失的漫射断开连接，因此会导致黑色渲染。*
  * 这是多输出节点的预期行为。 建议不要使用同一节点加载这些.sbsars，而是为每个节点使用不同的Substance节点。
