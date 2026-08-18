---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/plugin-settings-ue4.html"
breadcrumb-title: ''
description: 通过“项目设置”配置Unreal Engine 4中的Substance增效工具设置，以自定义增效工具行为。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Plugin Settings - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 增效工具设置 — UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---


# 增效工具设置 — UE4

要访问设置，请转到编辑>项目设置，向下滚动到增效工具类别，然后单击Substance。

![](../../../../assets/settings-36.png){width="400px"}

## 硬件预算

内存预算是用于Substance引擎的最大内存量。 可以提高物质处理的速度，但会消耗更多的系统资源。 （在项目层面，这并非总能带来有益的增长）。

CPU核心数是允许Substance引擎使用的核心数。 这包括物理内核和超线程。 (如果分配的数量大于系统上的可用内核，则默认为使用所有可用内核。

## 烹饪

烹饪期间移除的MIP级别计数将改变为包装创建纹理的方式。 此设置可以极大地缩短加载时间并减少包大小，因为将不再需要加载较大的纹理mip级别。 将加载较低的分辨率/较小的LOD，UE4将默认最高分辨率。 然后这些物质通过物质引擎进行处理，并在运行时使用高分辨率LOD进行更新。

Substance 引擎可以是CPU或GPU。 GPU引擎将允许您创建4K纹理。 CPU引擎上限为2K。

## 默认层代：

Substance生成模式(SGM)控制如何生成纹理。 这是Substance的全局设置。 股东特别大会可由Substance工厂按每位Substance进行变更。

**SGM烘焙**：烘焙物质纹理。 您可以在运行时更改参数。

**加载同步上的SGM**：在Substance加载时阻止应用程序。

加载同步和缓存上的&#x200B;**SGM**：缓存磁盘上的纹理的中间结果。

**加载异步**&#x200B;上的SGM：非阻止。 Substance在后台生成。

**加载异步和缓存上的SGM**：缓存磁盘上的纹理的中间结果。

***平台默认值为加载异步和缓存***

## Substance工厂

要更改Substance的SGM，请右键单击“Substance工厂”>“资源操作”>“通过属性矩阵批量编辑”。 然后可以更改SGM。

![](../../../../assets/sgm.png){width="800px"}

## 优化：

这限制了每批可传递到物质引擎的异步物质数量。 数量越少，异步任务的完成速度就越快；数量越多，异步任务的更新速度就越快，越能批量渲染和一次处理多种材质。 （该数字越大，纹理更新就越不连续，因为更新之间的时间越长）。

## 异步/同步渲染

同步渲染是一个阻止渲染调用。 这将将Substance Graph实例传递给Substance引擎进行重新计算，但将停止执行，直到Substance引擎处理完该Substance后，才能继续任何进一步的代码执行。 该过程结束后，系统也会立即在屏幕上更新结果。

Async将在插件更新中将您的图形添加到队列，并一次将多个图形发送到Substance引擎（在Substance设置中设置）。 与同步渲染不同，一旦发送出去，该程序就会像往常一样继续运行，而不是一直等待Substance引擎完成。 当Substance引擎完成该批后，它将结果发送回，我们将其应用于输出，然后我们启动另一个批次。
