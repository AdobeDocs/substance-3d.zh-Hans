---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-2-0.html"
breadcrumb-title: ''
description: 查看Unity增效工具版本2.2.0的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.2.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.2.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---


# Unity 2.2.0

## 2.2.0发行说明

**发布日期： 1/10/2019**

### 核心增效工具：

* 更新的Substance 引擎
* 改进了代码稳定性
* **支持Unity 2018.3**
* **.NET 4.x支持**
* 2018.3版Substance Source支持
* Substance Source着色问题已修复
* 现在，图形和相应的材质具有相同的对象名称
* 增加了Unity Pro皮肤GUI可读性改进
* 增加了对素材输出分配的支持
* 修复了sRGB处理的一个错误
* 修复了用户可删除图形的所有实例的错误
* 修复了在运行时更改参数时尝试渲染Substance只会导致一次渲染两个参数的错误
* 现在，在导入包含旧Substance文件的包时，该增效工具会通知用户它包含旧Substance数据，并在Unity尝试导入包文件时将其删除（这样，如果文件损坏，用户就不必手动删除所有文件）
* 在“Substance”菜单中添加了一个“关于”按钮，以显示与Substance增效工具相关的生成信息
* 在SubstanceGUI中添加了鼠标悬停工具提示，以显示公开的Substance参数名称
* 在SubstanceGUI中添加了导航按钮，以链接到Substance图形和材料
* 在“Content Browser”（内容浏览器）中为Substance图形/素材/纹理添加新图标
* 已更新Substance浏览器中的内容缩略图
* 已从Substance材质名称前面删除.mat
* 增加了重命名Substance图形和材质的功能
* 更改Substance图形分辨率时，应用/恢复弹出窗口将不再显示，此时将不能强制用户提交更改
* 修复了反射进程将仅使用默认Substance分辨率而非用户定义的分辨率的错误
* 在SubstanceGUI中添加了鼠标悬停警告，告知用户色彩空间是否设置为灰度系数
* 更改了Substance图形实例的功能：用户现在可以在Substance中创建图形实例，而无需在Substance图形GUI中提示每个创建的实例

### 脚本：

* 我们隐藏了一些不适合脚本支持的功能
* 通过脚本向重复Substance图形实例添加了函数：Duplicate()
* 已通过C#向查询过程式输入信息添加函数，返回“InputProperties”元素的数组： GetInputProperties()
* 添加了用于检查图形中是否存在输入的函数，返回true/false： HasInput(string inputName)
* 添加了用于检查可见输入是否可见的函数，返回true/false： IsInputVisible(string inputName)
* 对渲染方案进行了重新设计。 因此，RenderSubstancesAsync()已弃用，此项已更改为graphName.RenderAsync()

## 已知问题：

**核心Substance增效工具**

* 用户必须在Xcode的“生成设置”菜单中禁用“启用位码”，才能为iOS生成
* 将构建Substance设置为Android/iOS时，内容浏览器中的内容对象预览显示为黑色
* 导入Substance增效工具后，非SubstanceAlphaGUI上缺少“纹理”按钮和“Mip映射”预览滑块
* 用户必须使用2的幂来通过脚本定义Substance图分辨率
* 使用Unity包导出/导入时，Substance素材不会永久保留
* Substance不使用资源包
* 重新导入后，“资源浏览器”中的Substance预览图标全部更改为SubstanceS图标
* 重命名场景中包含素材的Substance图表将从该素材所在的对象中删除该素材
* （仅限Mac）更新Mac上的增效工具会从场景中的预合成文件中删除Substance素材|

**脚本**

* 如果项目在生成设置中设置为x86，则脚本在运行时不起作用
* 在某些构建平台上使用il2cpp脚本后端时出现问题

**Substance Painter实时链接**

* 在使用Substance实时链接进行绘制后构建项目，会将绘制的网格重新设置为默认材质
* 未随Painter live link发送AO频道
* 在Unity Live Link中，使用多种材质的网格不起作用
* Unity LiveLink使用SimpleJson的方式与项目中的其他SimpleJson实例发生冲突
