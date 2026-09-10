---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/error-and-warning-messages.html"
breadcrumb-title: ''
description: 有关使用Substance软件烘焙时可能出现的所有错误和警告消息的参考指南。
helpx_creative_field: ""
helpx_description: bakers > Guides > Error and Warning Messages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 错误和警告消息
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---


# 错误和警告消息

下面是使用Substance软件生成时可能出现的所有错误消息的列表。

## 任何Baker

| *消息* | *描述* |
| --- | --- |
| 面包机不可用。 | 此错误消息后面通常还会跟其他错误消息，这些错误消息通常与GPU问题相关。 如果GPU太旧且不符合软件的[技术要求](https://www.allegorithmic.com/products/tech-specs)，则可能会发生这种情况。 |
| UV 集[X]不存在。 | Baker尝试使用低多边形网格中不存在的给定UV 集。 |
| 无法从URL加载场景。 | 此消息表示Baker无法加载网格文件，通常是高模网格。 此消息可能源于以下几个原因：<ul data-preserve-html="true"><li data-preserve-html="true">引用的网格文件不再存在。</li><li data-preserve-html="true">网格文件已损坏或损坏，无法读取。</li><li data-preserve-html="true">该网格当前正由其他应用程序编辑，无法读取。</li></ul> |

## UV到SVG烘焙器

| *消息* | *描述* |
| --- | --- |
| 找不到网格[网格名称]的UV。 | 未找到与特定网格相关的UV。 如果导入多个网格但其中只有少数具有UV，则可能会发生这种情况。 |
| 场景没有UV。 正在取消烘焙。 | 如果场景中没有网格具有UV，则烘焙过程将被取消。 |

## 位置Baker

| *消息* | *描述* |
| --- | --- |
| 网格[网格名]没有位置。 | 低模网格没有顶点位置。 |
| 网格[网格名]没有uv集[X]的UV。 | Baker尝试使用低多边形网格中不存在的给定UV 集。 |

## 任何“来自网格”Baker

| *消息* | *描述* |
| --- | --- |
| 在网格[顶点名称]中找不到网格法线。 | 在给定网格中找不到顶点法线。 通常不会发生，因为顶点法线在网格没有时重新计算。 这可能是由错误的定制切线空间插件造成的。 |
| 在网格[顶点名称]中找不到网格正切。 | 同上文。 |
| 在网格[网格名]中找不到顶点二项式。 | 同上文。 |
| 在网格[顶点名称]中找不到网格。 | 在给定的网格中找不到顶点颜色。 如果高多边形网格中的至少一个子网格未定义任何顶点，则可能会发生这种情况。 |
| 高多边形中的数据不足，无法使用所选Baker。 正在中止烘焙。 | 前面至少有一个上述消息。 通常，如果场景中仅缺少一点数据（示例：高多边形场景中只有一个网格没有顶点色），则烘焙过程会用零填充缺少的数据，并保持烘焙。 如果缺少太多数据，则会输出此消息并停止烘焙过程。 |

## 来自网格的转移纹理

| *消息* | *描述* |
| --- | --- |
| 详细信息纹理加载失败。 | 无法加载Baker设置中定义的纹理。 这可能是因为磁盘上确实缺少该文件，或者该文件已损坏并且不可读。 |
