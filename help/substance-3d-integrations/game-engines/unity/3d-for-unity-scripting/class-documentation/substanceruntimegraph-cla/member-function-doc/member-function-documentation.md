---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class/member-function-documentation.html"
breadcrumb-title: ''
description: 有关Unity脚本中SubstanceRuntimeGraph类的所有成员函数的详细文档。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class > Member Function Documentation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 成员函数文档
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%

---


# 成员函数文档

## AttachGraph()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.AttachGraph  

( SubstanceGraphSO graph ) [inline]
```


将新的图形对象附加到此运行时处理程序。

**参数**

|  |  |
| --- | --- |
| 图形 | 目标Substance图形。 |

### CreatePresetFromCurrentState()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.CreatePresetFromCurrentState ( ) [inline]
```


将当前图形状态存储到预设XML中。

**返回**

使用图形输入的当前状态创建的预设。

### GetGeneratedTextures()

```
List< Texture2D > Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetGeneratedTextures ( ) [inline]
```


返回一个列表，其中包含Substance实例的所有输出纹理。

**返回**

输出纹理。

### GetInputBool()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputBool ( string inputName ) [inline]
```


获取Substance的布尔型输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中的输入名称。 |


**返回**

当前输入值。

### GetInputColor()

```
Color Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputColor ( string inputName ) [inline]
```


获取Substance颜色

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputDescription()

```
SubstanceInputDescription Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputDescription ( string inputName ) [inline]
```


返回目标输入名称的完整输入说明。

**参数**

|  |  |
| --- | --- |
| inputname | 目标输入名称。 |


**返回**

完成目标输入的输入说明。

### GetInputFloat()

```
float Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputFloat ( string inputName ) [inline]
```


获取Substance浮点输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputInt()

```
int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputInt ( string inputName ) [inline]
```


获取SubstanceInt输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputString()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputString ( string inputName ) [inline]
```


获取Substance的字符串输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

输入当前值。

### GetInputVector2()

```
Vector2 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2 ( string inputName ) [inline]
```


获取Substance矢量2输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputVector2Int()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2Int ( string inputName ) [inline]
```


获取2 int的数组。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputVector3()

```
Vector3 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3 ( string inputName ) [inline]
```


获取Substance矢量3输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputVector3Int()

```
Vector3Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3Int ( string inputName ) [inline]
```


获取3 int的数组（Vector3Int的x、y和z值）

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputVector4()

```
Vector4 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4 ( string inputName ) [inline]
```


获取Substance矢量4输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetInputVector4Int()

```
int[] Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4Int ( string inputName ) [inline]
```


获取4 int的数组（Vector4Int的x、y、z和w值）

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |


**返回**

当前输入值。

### GetOutputTexture()

```
Texture2D Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetOutputTexture ( string outputName ) [inline]
```


返回给定输出名称的输出纹理。

**参数**

|  |  |
| --- | --- |
| outputName | 输出名称。 |


**返回**

输出纹理。

### GetTexturesResolution()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetTexturesResolution ( ) [inline]
```


返回实例纹理输出分辨率。

**返回**

当前输出分辨率。

### HasInput()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.HasInput ( string inputName ) [inline]
```


如果此Substance实例具有给定名称的输入，则返回true。

**参数**

|  |  |
| --- | --- |
| inputname | 输入名称。 |


**返回**

如果Substance实例具有使用给定名称的输入，则为TRUE。

### LoadPreset()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.LoadPreset ( string presetXML ) [inline]
```


使用预设XML设置图形输入参数。

**参数**

|  |  |
| --- | --- |
| presetXML | 预设XML数据。 |

### RenderAsync()

```
Task Adobe.Substance.Runtime.SubstanceRuntimeGraph.RenderAsync ( ) [inline]
```


异步渲染Substance实例。

**返回**

渲染完成后完成的任务。

### SetInputBool()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputBool ( string inputName, 

bool value ) [inline]
```


更新Substance布尔输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputColor()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputColor ( string inputName, 

Color value ) [inline]
```


更新Substance颜色输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputFloat()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputFloat ( string inputName, 

float value ) [inline]
```


更新Substance浮点输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputInt()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputInt ( string inputName, 

int value ) [inline]
```


更新SubstanceInt输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputString()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputString ( string inputName, 

string value ) [inline]
```


更新Substance字符串输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputTexture()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputTexture (string inputName, 

Texture2D value ) [inline]
```


更新SubstanceTexture2D输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector2()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2 ( string inputName, 

Vector2 value ) [inline]
```


更新Substance矢量2输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector2Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2Int ( string inputName, 

Vector2Int value ) [inline]
```


更新SubstanceVector2Int输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector3()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3 ( string inputName, 

Vector3 value ) [inline]
```


更新Substance矢量3输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector3Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3Int ( string inputName, 

Vector3Int value ) [inline]
```


更新SubstanceVector3Int输入。

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector4()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4 ( string inputName, 

Vector4 value ) [inline]
```


更新Substance矢量4输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| 值 | 用于更新参数的值 |

### SetInputVector4Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4Int ( string inputName, 

int x, 

int y, 

int z, 

int w ) [inline]
```


更新SubstanceVector4Int输入

**参数**

|  |  |
| --- | --- |
| inputname | SBSAR中输入的名称 |
| x | 用于更新参数的值 |
| y | 用于更新参数的值 |
| z | 用于更新参数的值 |
| w | 用于更新参数的值 |

### SetTexturesResolution()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetTexturesResolution ( Vector2Int size ) [inline]
```


设置实例纹理输出分辨率。

**参数**

|  |  |
| --- | --- |
| 大小 |  |
