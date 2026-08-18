---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class.html"
breadcrumb-title: ''
description: 用于Unity中运行时图操作的SubstanceRuntimeGraph类的参考文档。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceRuntimeGraph类
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# SubstanceRuntimeGraph类

## Adobe.Substance.Runtime.SubstanceRuntimeGraph类引用

此类提供运行时功能以修改输入并渲染Substance图表，从而允许←GraphSO在运行时生成其资源。

Adobe.Substance.运行时.SubstanceRuntimeGraph的继承图：

![](../../../../../assets/image2022-10-14-17-53-23-1.png)

### 公共成员函数

```
• void AttachGraph (SubstanceGraphSO graph)
```


将新的图形对象附加到此运行时处理程序。

```
• void SetInputFloat (string inputName, float value)
```


更新Substance浮点输入

```
• float GetInputFloat (string inputName)
```


获取Substance浮点输入

```
• void SetInputVector2 (string inputName, Vector2 value)
```


更新Substance矢量2输入

```
• Vector2 GetInputVector2 (string inputName)
```


获取Substance矢量2输入

```
• void SetInputVector3 (string inputName, Vector3 value)
```


更新Substance矢量3输入

```
• Vector3 GetInputVector3 (string inputName)
```


获取Substance矢量3输入。

```
• void SetInputVector4 (string inputName, Vector4 value)
```


更新Substance矢量4输入

```
• Vector4 GetInputVector4 (string inputName)
```


获取Substance矢量4输入

```
• void SetInputColor (string inputName, Color value)
```


更新Substance颜色输入

```
• Color GetInputColor (string inputName)
```


获取Substance颜色

```
• void SetInputBool (string inputName, bool value)
```


更新Substance布尔输入

```
• bool GetInputBool (string inputName)
```


获取Substance的布尔型输入。

```
• void SetInputInt (string inputName, int value)
```


更新SubstanceInt输入

```
• int GetInputInt (string inputName)
```


获取SubstanceInt输入

```
• void SetInputVector2Int (string inputName, Vector2Int value)
```


更新SubstanceVector2Int输入。

```
• Vector2Int GetInputVector2Int (string inputName)
```


获取2 int的数组。

```
• void SetInputVector3Int (string inputName, Vector3Int value)
```


更新SubstanceVector3Int输入。

```
• Vector3Int GetInputVector3Int (string inputName)
```


获取3 int的数组（Vector3Int的x、y和z值）

```
• void SetInputVector4Int (string inputName, int x, int y, int z, int w)
```


更新SubstanceVector4Int输入

```
• int[ ] GetInputVector4Int (string inputName)
```


获取4 int的数组（Vector4Int的x、y、z和w值）

```
• void SetInputString (string inputName, string value)
```


更新Substance字符串输入。

```
• string GetInputString (string inputName)
```


获取Substance的字符串输入。

```
• SubstanceInputDescription GetInputDescription (string inputName)
```


返回目标输入名称的完整输入说明。

```
• void SetInputTexture (string inputName, Texture2D value)
```


更新SubstanceTexture2D输入。

```
• Vector2Int GetTexturesResolution ()
```


返回实例纹理输出分辨率。

```
• void SetTexturesResolution (Vector2Int size)
```


设置实例纹理输出分辨率。

```
• bool HasInput (string inputName)
```


如果此Substance实例具有给定名称的输入，则返回true。

```
• List< Texture2D > GetGeneratedTextures ()
```


返回一个列表，其中包含Substance实例的所有输出纹理。

```
•  Texture2D GetOutputTexture (string outputName)
```


返回给定输出名称的输出纹理。

```
• void Render ()
```


同步渲染Substance实例。

```
• Task RenderAsync ()
```


异步渲染Substance实例。

```
• void LoadPreset (string presetXML)
```


使用预设XML设置图形输入参数。

```
• string CreatePresetFromCurrentState ()
```


将当前图形状态存储到预设XML中。

## 公共属性

```
• SubstanceGraphSO GraphSO
```


目标Substance实例。

## 受保护成员函数

```
• void Awake ()
```


在唤醒时，SubstanceRuntime将用于为Substance中的附加SubstanceGraphSO创建实例

SDK。

```
• void Update ()
```


检查渲染ConcurrentQueue以获得渲染结果。

```
• void OnDestroy ()
```


处理Substance SDK处理程序。

## 属性

```
• Material DefaulMaterial [get]
```


Substance实例生成的主要素材。
