---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-bake/features/geometry-cache.html"
breadcrumb-title: ''
description: 使用几何缓存可保留预处理的网格数据并显着加快后续的烘焙操作。
helpx_creative_field: ""
helpx_description: bakers > Features > Geometry Cache
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 几何缓存
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# 几何缓存

烘焙时，会对网格进行预处理，以清理这些文档并以与烘焙过程兼容的格式进行转换。 几何高速缓存是以一种快速重新加载的方式保留此预处理几何的方法，以避免以后重做此操作（除非源网格发生变化）。

* 在&#x200B;**Substance Designer**&#x200B;中，在执行第一个烘焙后创建几何缓存。 然后，将高速缓存保存在内存中，直到Baker窗口关闭为止。
* 在&#x200B;**Substance Painter**&#x200B;中，几何缓存会在首次烘焙后保存为扩展名为&#x200B;**assbin**&#x200B;且位于源文件旁的文件。

重复使用几何缓存可以大大加快烘焙过程，尤其是在调整Baker设置以达到理想效果时。
