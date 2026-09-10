---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-3-0-0-plus.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本3.0.0及更高版本的发行说明，了解新增功能和改进。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---


# Unity 3.0.0+

## Unity 3.12.0

<b>已添加/已更新：</b>

* 支持Unity中的Substance 3D连接器，支持在Substance 3D Sampler和Unity之间发送资源的“发送到”功能。
* 支持将.sbsar图形从Designer重命名和重新发布到Unity，从而确保在将更新后的图形重新导入Unity增效工具时，保留在Designer中所做的更改。
* 用于在Unity项目之间共享.sbsar文件的文档。
* 社区稿页面收录到Unity插件文档： https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/community-contributions.html.

<b>已修复：</b>

* 在重新发布。sbsar 文件后，显示上一个材料而非当前材料时，“Unity项目资源”文件夹中的缩微图未更新的问题。

## Unity 3.11.0

<b>已添加/已更新：</b>

* 改进了具有1000多个图形的项目性能，从而显着缩短了检查Assets文件夹中的sbsar文件时的UI响应时间。
* 添加了一个重置按钮，可将sbsar文件恢复到其原始状态，从而提升了工作流程效率。
* 更新了有关“图像输入锁定为8位”问题的解决方法的文档，网址为： [Unity中的Substance 3D集成 — 升级项目和已知问题](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md)。
* 更新了文档以解决在Unity中导航面板文件夹时遇到的“表达式断言失败”错误： [Unity中的Substance 3D集成 — 升级项目和已知问题](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md)。

<b>已修复：</b>

* 修正了在Linux平台上导致插件损坏的问题。
* 修复了2023版中的Unity增效工具兼容性问题。

## Unity 3.10.1

<b>已修复：</b>

* 修复了由于Substance 3D for Unity增效工具中的sbsario.dll问题而导致无法加载Substance 引擎的问题。

## Unity 3.10.0

<b>已添加/已更新：</b>

* 更新了增效工具中RenderInstanceAsync API的注释部分

<b>已修复：</b>

* 解决了增效工具C++代码中的内存泄漏问题，从而确保在处理对象时完全恢复内存。
* 修复了Linux上导入Unity增效工具包时会导致“SubstanceException：为API提供的参数无效”错误的问题，现在可以成功导入SBSAR文件。
* 解决了SubstanceGraphSO.CurrentStatePreset在Unity中加载具有自定义编辑器窗口脚本的预设时无法正常工作的问题；我们的Substance文档(HelpX)页面上现在提供了一个更正脚本： https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/game-engines/unity/substance-3d-for-unity-scripting/substance-3d-for-unity-scripting
* 修复了在Unity编辑器中重新选择时图形属性消失的错误。
* 解决了Unity增效工具中与SubstanceGraphSO相关的“引用的未知托管类型”问题，从而改进了Android平台（特别是Unity 2022.1）上的兼容性和功能，并且可能在所有Unity版本上实现此目的。
* 修复了“技术参数”部分中的“正常格式”选项未正确显示为数字输入字段，而不是显示为包含DirectX和OpenGL选项的预期下拉列表的问题。

## Unity 3.9.0

<b>已添加/已更新：</b>

* 现在可以将Sbsar文件拖放到项目中。 .sbsar对象可以应用于Unity 2022.3中预期的网格。
* 增强的增效工具文档。

<b>已修复：</b>

* 修复了Unity增效工具在Android上不起作用的问题。
* 解决了Unity增效工具中的命名限制。 当文件名包含“。”时，插件未正确加载该文件。
* 修复了取消选中“生成所有输出”不会自动删除额外纹理的问题。
* 修复了在Unity 2021.3标准项目中错误导入SBSAR材料的问题。 现在，在标准模板项目中，可以将SBSAR材料导入到Assets文件夹，然后将其应用于3D 网格，而不会出现错误。
* 修复了在Unity 2021/2022 HDRP项目中不正确导入SBSAR材料的问题。 现在，在HDRP模板项目中，可以将SBSAR材料导入到Assets文件夹并将其应用于3D 网格，而不会出现错误。
* 修正了生成Android内部版本以生成APK时出现的编译错误：“编译失败；有关详细信息，请参阅编译器错误输出。”
* 修复了导致Windows上的生成项目进程失败并出现错误。
* 修复了导致Android上的生成项目进程失败并出现错误： UnityEditor.BuildPlayerWindow+BuildMethodException。
* 解决了在运行时更改SubstanceGraph输入时遇到的UnityException。 以前，调用SubstanceRuntimeGraph.SetTexturesResolution和SubstanceRuntimeGraph.Render()会导致SubstanceGraph渲染错误的结果。
* 更正了SubstanceEditorTools.cs中的印刷错误。

## Unity 3.8.0

<b>已添加/已更新：</b>

* 引入了对于具有条件可见性的参数的支持（可视性特征）。
* 已将引擎升级到版本9。
* 更新了文档以解决在自定义编辑器窗口脚本中无法运行NativeGraph.InRenderWork的问题。 有关更多详细信息，请参阅： [Substance 3D for Unity脚本 — 类文档](../../../../game-engines/unity/3d-for-unity-scripting/class-documentation/substanceruntime-class/substanceruntime-class.md)

<b>已修复：</b>

* 解决了影响Android项目中法线图的问题。
* 修复了将sbsar对象拖入场景视图时会无意中导致所有鼠标悬停对象的材料被sbsar对象材料覆盖的错误。
* 修复了在运行时模式下检查标记为“仅运行时”的材料并打开输出纹理映射时，导致出错的错误。

## Unity 3.7.0

<b>已添加/已更新：</b>

* 支持嵌入预设和外部预设
* 与Unity 2022.2的兼容性

<b>已修复：</b>

* 使用“复制图形”按钮为sbsar 文件创建新图形时出错：“脚本类的意外递归传输”
* 重新打开项目后，在Mac上创建额外的材料文件夹
* 创建/删除图形实例时SubstanceFileSO数组未更新
* 复制Substance时显示错误的输入选项
* .sbsprs文件导出中的空标签字段
* 在编辑器中导出/导入预设时出错：必须先调用EndLayoutGroup： BeginLayoutGroup。

<b>已删除：</b>

* 由于缺少用户价值，Unity插件的Channels部分

## Unity 3.6.0

<b>已添加/已更新：</b>

* 使单个Int 4值可独立编辑的能力。

<b>已修复：</b>

* 重新打开项目时材料恢复到以前状态的问题
* 尝试修改图形时显示消息“未找到图形”的错误
* 物理尺寸特征中“旋转偏移”参数的输入值未更改的问题
* 重复的图形实例的输入的GraphID值不正确的问题
* 使用编辑器脚本（自定义编辑器窗口）更改图形时，Substance生成器未能在编辑器中正确初始化
* 从自定义编辑器窗口脚本导出SubstanceGraphSO.CurrentStatePreset时导出缓存版本的图形的问题
* 在检查器窗口被锁定时未保存参数更改的问题
* 在“编辑器”模式下，在物理尺寸选项的“位置偏移”部分手动输入键盘对材料没有影响的问题
* 在SBSAR对象中手动键入参数值时出错

## Unity 3.5.0

<b>已添加/已更新：</b>

* 支持用户更改将输出纹理分配给Unity材料的方式
* 插件与最新Unity 2022.2版本的兼容性

<b>已修复：</b>

* 材料具有Int4输入时出现Null引用错误
* Int4输入有错误，W值被分配给Data2而不是Data3
* 函数名称“\_OcclusionStrength”中的拼写错误

## Unity 3.4.0

<b>已添加/已更新：</b>

* “位置平移”控件用于在“纹理”面板中使物理尺寸在曲面上偏移
* 用于下载项目设置中的Substance 3D Assets和Substance社区资源的链接

## 统一3.3.0

<b>已添加/已更新：</b>

* HDRP的物理尺寸功能，允许材料根据现实世界的大小进行应用和缩放
* 在项目设置中启用GPU的UI

<b>已删除：</b>

* 来自大多数API调用的图形ID

## Unity 3.2.1

<b>已修复：</b>

* 将插件从3.0.0和3.1.0升级到最新版本时出现的问题。

## Unity 3.2.0

<b>已添加/已更新：</b>

* 脚本重新编译的性能改进

<b>已修复：</b>

* 导入自定义Sbsar材料时，在Unity增效工具中导入资源失败
* “ArgumentException：值不在预期范围内”错误
* “ArgumentOutOfRangeException：索引超出范围”错误

## Unity 3.1.0

<b>已添加/已更新：</b>

* Mac的性能提高了1.38倍
* Mac上的GPU引擎使用Metal而不是OpenGL

<b>已修复：</b>

* 输出纹理的R和B声道将被翻转的Mac问题

## Unity 3.0.0

<b>已添加/已更新：</b>

* 支持Apple Silicon
* 有关如何使用增效工具的新YouTube教程
* 新的脚本文档

<b>已修复：</b>

* 反复点击“随机化”按钮时，检查器会显示错误
* 空纹理输入会中断Substance更新
* “生成所有输出”、“生成Mip映射”和“仅运行时”切换开关不起作用
* 命名空间的问题
* 在选择图形资源的情况下进入播放模式时出现“空参考”错误
* 使用仅运行时材料时，最新的2021.3 LTS版本Unity的HDRP和URP出现问题
