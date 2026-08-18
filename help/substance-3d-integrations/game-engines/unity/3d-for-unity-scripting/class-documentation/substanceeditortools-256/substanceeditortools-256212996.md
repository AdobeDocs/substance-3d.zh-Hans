---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceeditortools-256212996.html"
breadcrumb-title: ''
description: 用于Unity中Substance材料管理的SubstanceEditorTools类的参考文档。
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceEditorTools
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# SubstanceEditorTools

## Adobe.SubstanceEditor.SubstanceEditorTools类参考

供用户在编辑器脚本上使用的工具和实用程序。

Adobe.SubstanceEditor.SubstanceEditorTools的继承图：

![](../../../../../assets/image2022-10-14-17-53-23.png)

### 静态公共成员函数

```
• static void SetGraphFloatInput (SubstanceGraphSO graph, int inputId, float value)
```


设置图形浮点输入。

```
• static void SetGraphFloat2Input (SubstanceGraphSO graph, int inputId, Vector2 value)
```


设置图形float2输入。

```
• static void SetGraphFloat3Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


设置图形float3输入。

```
• static void SetGraphFloat4Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


设置图形float4输入。

```
• static void SetGraphIntInput (SubstanceGraphSO graph, int inputId, int value)
```


将图形设置为输入。

```
• static void SetGraphInt2Input (SubstanceGraphSO graph, int inputId, Vector2Int value)
```


设置图形int2输入。

```
• static void SetGraphInt3Input (SubstanceGraphSO graph, int inputId, Vector3Int value)
```


设置图形int3输入。

```
• static void SetGraphInt4Input (SubstanceGraphSO graph, int inputId, int value0, int value1, int value2, int value3)
```


设置图形int4输入。

```
• static void SetGraphInputString (SubstanceGraphSO graph, int inputId, string value)
```


设置图形字符串输入。

```
• static void SetGraphInputTexture (SubstanceGraphSO graph, int inputId, Texture2D value)
```


设置图形纹理输入。

```
• static void RenderGraph (SubstanceGraphSO graph)
```


渲染目标图表并更新其资源。

```
• static string CreatePresetFromCurrentState (SubstanceGraphSO graph)
```


根据图形对象的当前状态创建预设XML。

```
• static List< SubstanceGraphSO > GetGraphs (this SubstanceFileSO fileSO)
```


返回与SubstanceFileSO关联的SubstanceGraphSO的列表。
