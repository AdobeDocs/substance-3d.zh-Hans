---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-5.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.4.5的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Unity 2.4.5

2020年4月6日发布

* 添加：使用2019.3 API进行HDRP资源检查
* 已添加：Substance 引擎7.2更新 — 修复了源中某些Substance材质不起作用的问题
* 已添加：更新目标设置以匹配CPU分辨率
* 已添加：CPU引擎最大分辨率设置（4k或2k设置）
* 已添加：在HDRP项目中转换非HDRPSubstance
* 修复：导入大量Substance时崩溃
* 修复：在更改Substance参数后单击在播放模式下重新导入时出现异常
* 修复：验证输出（纹理）分辨率（API可将CPU引擎限制为2K）用户首选项将默认值设置为4K
* 修复：在“播放”模式下单击Substance图表上的“生成Mip映射”，然后更改参数会导致无限挂起
* 修复：在HDRP项目中使用Substance增效工具时，使用Raw压缩会将灰度纹理设置为Alpha8
* 修复：在“播放”模式下取消选择GameObject
* 修复：粗糙度映射不会随参数更改而更新
* 修复：无法为HDRP中的某些Substance文件正确生成蒙版输出
* 修复：在两个选项之间切换打包Alpha映射下拉菜单时崩溃
* 修复：在离开Substance素材的情况下单击时，会还原GPU实例化复选框。
* 修复：使用Duplicate()函数时，复制的Substance图形没有将Smoothness正确填充到金属的Alpha中。
* 修复：将生成目标切换到Android会导致纹理格式错误，直到手动重新导入为止。
* 修复：删除Unity中的Substance文件将导致NullReferenceException。
* 修复：禁用以前版本的Unity 2019.3 HDRP API

已知问题：

* 默认情况下不启用发射复选框，并且导入Substance时HDR值设置为黑色。
* 带有标准Substance素材的包中的素材属性不会在导入时继续使用。
* 在HDRP中无法从2017-2019/2020进行更新
* 如果在目标设置中选中4096时单击“设置”菜单中的“2048钳位”选项（而不单击“应用”），将会在“控制台日志”中产生错误
