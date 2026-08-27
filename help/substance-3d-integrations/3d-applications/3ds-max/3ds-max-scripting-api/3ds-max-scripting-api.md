---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-scripting-api.html"
breadcrumb-title: ''
description: 有关Substance3ds Max脚本API的参考文档，用于自动化材料操作。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds MAX Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds MAX脚本API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 2%

---


# 3ds MAX脚本API

以下是Substance2节点的命令和属性列表。

## 属性：

| 属性 | 描述 | 类型 |
| --- | --- | --- |
| name | Substance2节点的名称。 默认值为“Substance2” | 字符串 |

## 命令：

| 命令 | 描述 | Return | 返回类型： | 参数 |
| --- | --- | --- | --- | --- |
| getCurrentPackageName | 获取加载的包（在图形节点中加载的sbsar 文件）的基本文件名 | 加载的包(sbsar 文件)的文件名（不带前缀目录） | 字符串 |  |
| getCurrentGraphName | 获取当前图形的名称 | 当前图形实例的标识符 | 字符串 |  |
| getOutputsNamesFromCurrentGraph | 获取启用的输出的输出使用名称列表 | 包含已启用输出的通道名称列表的表 | 列表 |  |
| getPresetIdentifiers | 从图形获取预设列表 | 包含所有预设的字符串标识符列表的表 | 列表 |  |
| setPackageAndGraphNames | 将sbsar 文件从磁盘加载到图形节点 | 成功时为True，失败时为False | 布尔型 | ***字符串参数***： **substancePackageFilePath** disk ***String参数上sbsar文件的路径***： **graphInstanceNameToSelect**&#x200B;图形的字符串标识符 |
| setInputInt | 使用新值设置整数输入 |  |  | ***整数参数***： **值**&#x200B;将输入设置为&#x200B;***String参数的整数值***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputFloat | 使用新值设置浮点输入 |  |  | ***浮点参数***： **值**&#x200B;将输入设置为&#x200B;***String参数的浮点值***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputString | 使用新值设置字符串输入 |  |  | ***字符串参数***： **值**&#x200B;将输入设置为&#x200B;***String参数的字符串值***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputBool | 使用新值设置布尔型输入 |  |  | ***布尔型参数：*&#x200B;值&#x200B;**&#x200B;用于将输入设置为&#x200B;***String参数的布尔值&#x200B;***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputVec2 | 设置具有两个元素的矢量输入 |  |  | ***Point2参数： &#x200B;**&#x200B;***值**&#x200B;设置输入到&#x200B;***String参数的Max point2值&#x200B;***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputVec3 | 设置具有三个元素的矢量输入 |  |  | ***Point3参数：*&#x200B;值&#x200B;**&#x200B;用于将输入设置为&#x200B;***String参数的Max point3值&#x200B;***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| setInputVec4 | 设置具有四个元素的矢量输入 |  |  | ***Point4参数***： **值** Max point4值，用于将输入设置为&#x200B;***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| setInputColor | 使用新值设置颜色输入 |  |  | ***颜色参数***： **值**&#x200B;设置输入的最大颜色值&#x200B;***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| setInputComboSelection | 在组合框输入中设置当前选定的值 |  |  | ***整数参数***： **值**&#x200B;组合框widget ***String参数的索引***： **inputIdentifier**&#x200B;输入的唯一字符串标识符 |
| getInputInt | 获取整数输入类型的输入值 | 输入的当前整数值 | 整数 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputFloat | 获取浮点输入类型的输入值 | 输入的当前浮点值 | 浮点 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputString | 获取字符串输入类型的输入值 | 输入的当前字符串值 | 字符串 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputBool | 获取布尔型输入类型的输入值 | 输入的当前布尔值 | 布尔型 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputVec2 | 获取point2输入类型的输入值 | 输入的当前最大点2值 | 点2 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputVec3 | 获取point3输入类型的输入值 | 输入的当前max3值 | 点3 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputVec4 | 获取point4输入类型的输入值 | 输入的当前max点4值 | 点4 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputColor | 获取颜色输入类型的输入值 | 作为颜色的输入当前值 | Color | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getInputComboSelection | 根据标识符获取组合框选择的索引 | 所选组合框项目的索引 | 整数 | ***字符串参数：* inputIdentifier &#x200B;** 输入的唯一字符串标识符 |
| getMaterialDependentCount | 获取材料依赖关系的数量 | 材料类型的从属参照的数量 | 整数 |  |
| ApplyValuesToSelectedPreset | 用当前输入值覆盖当前选定的预设 |  |  |  |
| RemoveAllPreset | 删除当前图形节点中的所有预设 |  |  |  |
| 创建预设 | 根据当前输入创建新预设 |  |  | ***字符串参数：* newPresetName &#x200B;** 新预设的显示名称 |
| RemoveOnePreset | 移除具有给定名称的预设 |  |  | ***字符串参数：*&#x200B;选定预设名称&#x200B;**&#x200B;要删除的预设的名称 |
| 导入预设 | 将sbsprs文件导入到当前预设中 |  |  | ***String参数：**&#x200B;***filePath**&#x200B;包含导入预设的文件路径的字符串 |
| ExportPreset&#x200B;**\*已弃用**&#x200B;要在2.5.0\*中移除 | 将当前选定的预设导出到sbsprs文件 |  |  | ***字符串参数***： **filePath**&#x200B;包含要将预设导出到的文件路径的字符串 |
| 导出预设列表 | 将给定预设导出为单个预设文件 |  |  | ***字符串参数***： **filePath**&#x200B;包含将预设导出到&#x200B;***List参数的文件路径的字符串***： **预设**&#x200B;包含要导出的预设名称的列表 |
| BakeOutputsOfSelectedGraph | 将选定图形实例的位图烘焙到磁盘 |  |  | ***String参数：* filePath &#x200B;** 将图像写入的根路径目录&#x200B;***String参数&#x200B;***： **imageFormatExtension**&#x200B;将图像写入的文件扩展名/格式 |
