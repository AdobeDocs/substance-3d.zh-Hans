---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting.html"
breadcrumb-title: ''
description: 在Unity中使用Substance 3D API编写脚本，以便在运行时更新和更改Substance参数。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 用于Unity脚本的Substance 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# 用于Unity脚本的Substance 3D

本文档的此部分包含有关我们通过Substance 3D for Unity插件提供的Substance 3D API的详细信息。 使用SubstanceAPI，您可以编写脚本以在运行时更新和更改Substance参数。

## API概述

该插件分为3个不同的程序集。

* Adobe.Substance
* Adobe.Substance.编辑器
* Adobe.Substance.运行时

### Adobe.Substance

包含与SubstanceSDK交互并生成匹配的Unity对象的共享组件。 它还具有用于在C#与SubstanceSDK C++ API之间进行通信的封送数据结构。

#### Adobe.Substance.编辑器

包含编辑器特定的类，用于处理有关UnitySubstance对象的信息显示，以及在将sbsar文件添加到项目时处理导入管道。 SubstanceEditorEngine类是一个单独的类，用于处理Substance引擎及其所有受管理实例的生命周期。

#### Adobe.Substance.运行时

此类具有一些组件，这些组件将在运行时执行期间处理Substance对象的创建和管理。 SubstanceRuntime与运行时的SubstanceEditorEngine类等效。 它将处理Substance引擎的初始化，以及用户脚本将与之交互的任何Substance实例的实例化。

## 运行时使用

为了在运行时修改Substance实例输入，需要向场景中添加一个SubstanceRuntime← — 素材（最好与Substance素材添加到同一个GameObject）。 此类充当帮助程序，以使用Adobe.Substance.Runtime.SubstanceRuntime单一实例设置材料，该实例在运行时管理SubstanceSDK对象的实例化。Substance

## 代码示例

以下示例说明如何在运行时使用SubstanceRuntimeGraph更改输入参数。

### 更改参数

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    // panel color 

    mySubstance.SetInputColor("paint_color", new Color(0.237 f, 0.834 f, 0.045 f, 1.0 f)); 

    // panel size 

    mySubstance.SetInputVector2("square_open", new Vector2(0.101 f, 0.209 f)); 

    // wear level 

    mySubstance.SetInputFloat("wear_level", 0.977 f); 

    // Submit async render. 

    mySubstance.RenderAsync(); 

  } 

}
```


您还可以使用SubstanceRuntimeGraph来访问有关Substance素材的输入和输出信息。

#### 获取输入信息

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```


以下示例说明如何使用SubstanceEditorTools在编辑器中创建自定义预设菜单。

##### 创建预设控件。

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```
