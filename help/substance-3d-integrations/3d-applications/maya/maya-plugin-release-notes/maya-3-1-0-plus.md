---
description: 查看Maya增效工具版本3.0.0及更高版本的发行说明，以了解新功能、改进和错误修复。
title: Maya 3.0.0
source-git-commit: 6453364f7dafa75c5bb2531a8707257498953e23
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%
---

# Maya 3.1.0+

## Maya 3.1.1

**发行日期：** 2026年11月18日

**兼容：** Maya 2025及更高版本

### 已添加/已更新

* Substance 引擎更新(9.6.1.) 包括安全修复
* OpenPBR支持Maya 2025、2026和2027（Arnold和V-Ray）

### 已知限制

* 排放重量： emission_weight参数不是OpenPBR1.1规范的一部分，并且未自动连接。 应用工作流程后，如果您的材料使用发射，请在OpenPBR中手动设置发射权重值。
* OpenPBR- V射线 — 子表面半径比例：使用OpenPBR- V射线工作流程时，子表面_半径_比例可能返回值0。 如果出现这种情况，请删除连接，并在V-Ray节点中手动设置该值。
* 渲染器之间的视觉差异：Substance 3D Designer中的材料预览与在Arnold或V-Ray中渲染的结果之间存在一些差异，这是由于每个渲染器对OpenPBR规范的实施情况存在差异所致，并且随着实施的收敛将会有所改善。
* SBSAR文件从Substance 3D Painter 12.2.0导出。 使用OpenPBR工作流程时，或更早版本可能无法正确连接。

## Maya 3.1.0

**发行日期：** 2026年11月18日

**兼容：** Maya 2024

### 已添加/已更新

* Substance 引擎更新(9.6.1.) 包括安全修复
