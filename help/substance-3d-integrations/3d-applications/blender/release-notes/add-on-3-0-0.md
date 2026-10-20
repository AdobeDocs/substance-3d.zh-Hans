---
title: Blender插件3.0.0+
description: 适用于Blender的Substance 3D插件的发行说明列表。
source-git-commit: 1488c476be7921c113d2a54f870fee090e6295e9
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%
---

# 加载项3.0.0+

**加载项3.1.0**.*发布日期：2026年10月20日*

**混合器加载项：**

* &amp;lbrack；错误&amp;rbrack；修复的库路径不起作用
* &amp;lbrack；错误&amp;rbrack；修复了多线程中的上下文问题，导致SBSAR无法加载/更新
* &amp;lbrack；Bug&amp;rbrack；固定纹理导出格式被忽略
* &amp;lbrack；性能改进&amp;rbrack；多项性能改进

**Substance集成工具（Substance远程引擎）：**

* &amp;lbrack；Feature&amp;rbrack；更新为Substance 引擎9.6.1
* &amp;lbrack；Performance&amp;rbrack；更新了相关性和多项性能改进

**加载项3.0.1**.*发布日期：2026年2月*

**混合器附加：**

* &amp;lbrack；固定&amp;rbrack；参数最小/最大值不起作用
* &amp;lbrack；固定&amp;rbrack；物理尺寸不适用于自定义场景缩放
* &amp;lbrack；固定&amp;rbrack；物理尺寸不适用于非公制系统单位
* &amp;lbrack；Fixed&amp;rbrack；透明图不适用于混合器4+
* 着色器上缺少&amp;lbrack；Fixed&amp;rbrack；透明色图
* &amp;lbrack；修复&amp;rbrack；加载项定义中的标签错误
* &amp;lbrack；固定&amp;rbrack；Substance随机崩溃SRE（使用color float4值）
* &amp;lbrack；固定&amp;rbrack；图像输入未显示在参数列表中
* &amp;lbrack；固定&amp;lbrack；关闭并重新打开混合器后，图像输入不起作用

**Substance集成工具（Substance远程引擎）：**

* 升级到版本3.0.1
* 删除了用于新Linux编译的C++11 ABI
