---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/modo/working-with-references.html"
breadcrumb-title: ''
description: 在MODO中管理材料引用，以便在多个对象和场景之间共享材料。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with References
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用引用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# 使用引用

## 使用引用

材料可以与引用的场景一起使用。 但是，如果需要禁用被引用场景中Substance的输出，则需要手动删除输出。 使用MODO的默认引用首选项时，仅取消选中Substance上的输出不会删除所引用属性的输出。\
要允许被引用的材料删除其自己生成的输出要手动删除输出，必须首先更改场景的“引用覆盖”。 转到“项目”>“引用”>“编辑引用覆盖”并将“删除”设置为“如果项目允许”。 这将允许您手动删除Substance输出\
从着色器树和剪辑浏览器中打开或创建此更改后的任何场景。

请参阅MODO文档，以了解有关参考优先选项的更多信息。\
<http://modo.docs.thefoundry.co.uk/modo/801/help/pages/modointerface/ImportReference.html>
