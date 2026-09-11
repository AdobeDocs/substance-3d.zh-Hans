---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntime-class.html"
breadcrumb-title: ''
description: 有关在Unity中用于运行时材料操作的SubstanceRuntime类的参考文档。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntime Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceRuntime类
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# SubstanceRuntime类

## Adobe.Substance.Runtime.SubstanceRuntime类引用

处理引擎初始化的单一实例类，用于获取Substance实例的本机处理程序。\
Adobe.Substance.Runtime.SubstanceRuntime的继承图：

![](../../../../../assets/image2022-6-22-14-35-28.png)

### 公共成员函数

```
• SubstanceNativeGraph InitializeInstance (SubstanceGraphSO substanceInstance)
```


为给定SubstanceGraphSO创建SubstanceSDK句柄。

### 属性

```
• static SubstanceRuntime Instance [get]
```


单个实例。

### 详细说明

处理引擎初始化的单一实例类，用于获取Substance实例的本机处理程序。

### 成员函数文档

#### InitializeInstance()

```
SubstanceNativeGraph Adobe.Substance.Runtime.SubstanceRuntime.InitializeInstance  

( SubstanceGraphSO substanceInstance ) [inline]
```


为给定SubstanceGraphSO创建SubstanceSDK句柄。

**参数**

|  |  |
| --- | --- |
| substanceInstance | 目标SubstanceGraphSO |


**返回**

与SubstanceSDK通信的句柄

### 属性文档

#### 实例

```
SubstanceRuntime Adobe.Substance.Runtime.SubstanceRuntime.Instance [static], [get]
```


单个实例。

全局单个实例。

>[!NOTE]
>
> NativeGraph.InRenderWork仅供内部使用，用于与Substance 引擎通信，不应用于自定义工作流。
