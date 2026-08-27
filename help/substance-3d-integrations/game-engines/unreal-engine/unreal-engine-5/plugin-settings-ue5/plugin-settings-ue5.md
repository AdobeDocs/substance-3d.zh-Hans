---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/plugin-settings-ue5.html"
breadcrumb-title: ''
description: 通过“项目设置”在“虚构引擎5”中配置Substance增效工具设置以自定义增效工具行为。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Plugin Settings - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 增效工具设置 — UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# 增效工具设置 — UE5

要访问设置，请转到编辑>项目设置，向下滚动到增效工具类别，然后单击Substance。

![](../../../../assets/screen-shot-2022-03-31-at-5-50-29-pm.png)

## 硬件预算

内存预算是用于引擎的最大内存量。 可以增加以提高Substance处理的速度，但是会消耗更多的系统资源。 （在项目层面，这并非总能带来有益的增长）。

CPU内核决定允许引擎使用的内核数。 这包括物理内核和超线程。 (如果分配的数量大于系统上的可用内核，则默认为使用所有可用内核。

## 烹饪

烹饪期间移除的MIP级别计数将改变为包装创建纹理的方式。 此设置可以极大地缩短加载时间并减少包大小，因为将不再需要加载较大的纹理mip级别。 将加载较低的分辨率/较小的LOD，UE5将默认最高分辨率。 然后通过引擎处理Substance，并在运行时使用高分辨率LOD进行更新。

Substance 引擎可以是CPU或GPU。 GPU引擎将允许您创建4K纹理。 CPU引擎上限为2K。

## 优化：

这限制了每批可传递到物质引擎的异步物质数量。 数量越少，异步任务的完成速度就越快；数量越多，异步任务的批量渲染和一次处理多个Substance的速度就越快，异步任务更新的速度就越快。 （该数字越大，纹理更新变得越不连贯，因为更新之间的时间越长）。

## 异步/同步渲染

同步渲染是一个阻止渲染调用。 这将将Substance图形实例传递给Substance引擎进行重新计算，但它将停止执行，直到Substance引擎完成对Substance的处理，然后再继续执行任何进一步的代码执行。 该过程结束后，系统也会立即在屏幕上更新结果。

Async将在插件更新中将您的图形添加到队列，并一次将多个图形发送到Substance引擎（在Substance设置内设置）。 与同步渲染不同，一旦发送出去，程序就会像往常一样继续运行，而不是一直等待Substance引擎完成。 当Substance引擎完成该批后，它将结果发送回，然后将这些结果应用到输出中，我们启动另一个批处理。
