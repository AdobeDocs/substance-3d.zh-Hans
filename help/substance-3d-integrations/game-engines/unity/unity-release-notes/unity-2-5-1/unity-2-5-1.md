---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-1.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.5.1的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Unity 2.5.1

2020年5月21日发布

已添加

* 通用渲染管道支持：纹理将自动使用URP着色器和材料

固定

* SubstanceCPU引擎最大分辨率设置：
  * 已将“Substance设置”菜单中的字段名称从“纹理钳制\*\*”更新为“SubstanceCPU引擎最大分辨率”
  * 修改设置时，将显示警告通知，指示将重新导入所有Substance材料
* 删除了安装时显示的不必要的调试消息(“TextureClamp = 4096 Unity.引擎.Debug:Log（对象）”)
* HDRP项目：在导入包含材料的包时，同时处于标准和HDRP材料的Substance属性将结转
* 从早期Unity版本的Substance包导入Substance材料时，反射和HDRP蒙版将按预期创建和工作
* 重复的材料将是预期颜色，在使用重复功能时不再为黄色
* 关闭并重新打开Unity后，Substance源将按预期加载
* 将包导入HDRP项目时崩溃（间歇性）
* 对于编辑器设置为“彩色（灰度）”的公开参数的Substance材料，滑块将按预期工作
* 当使用没有默认分辨率的图形单击“将预设重置为默认值”时崩溃
* 在未公开输出大小参数的情况下更改Substance材料的输出大小时崩溃
* 为iOS构建不会失败
* 为Windows独立版构建时，将执行使用材料的脚本
