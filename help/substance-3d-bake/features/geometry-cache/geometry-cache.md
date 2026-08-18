---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/geometry-cache.html"
breadcrumb-title: ''
description: 使用几何缓存可保留预处理的网格数据并显着加快后续烘焙操作。
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

在烘焙时，对网格进行预处理以对其进行清理并以与烘焙过程兼容的格式转换。 几何高速缓存是以一种快速重新加载的方式保留此预处理几何的方法，以避免以后重做此操作（除非源网格发生变化）。

* 在&#x200B;**Substance Designer**&#x200B;中，几何缓存是在执行第一个烘焙后创建的。 然后，将高速缓存保存在存储器中，直到烘焙窗口关闭。
* 在&#x200B;**Substance Painter**&#x200B;中，几何缓存保存为文件，扩展名为&#x200B;**assbin**，在第一次烘焙后位于源文件旁边。

重复使用几何缓存可以大大加快烘焙过程，尤其是在调整烘焙器设置以获得最佳效果时。
