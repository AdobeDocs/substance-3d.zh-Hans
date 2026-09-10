---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/scripting-in-unity-deprecated/scripting-api.html"
breadcrumb-title: ''
description: 有关针对旧版项目支持的已弃用SubstanceUnity脚本API的参考文档。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Scripting in Unity (Deprecated) > Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 脚本API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 1%

---


# 脚本API

## Unity API - 2.2.0中的Substance

## 材料参数

| Public方法 | 描述 | 参数 |
| --- | --- | --- |
| 公共&#x200B;**浮点** *GetInputFloat*（**字符串**&#x200B;输入名称） | 获取Substance **Float**&#x200B;输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| 公共&#x200B;**int** *SetInputFloat*（**字符串** inputName，**float**&#x200B;值） | 更新Substance **Float**&#x200B;输入 | **String** i *nputName* SBSAR中输入的名称&#x200B;**Float** *值*&#x200B;用于更新参数的值 |
| 公共&#x200B;**void** *SetInputVector2*（**string** inputName， **Vector2**&#x200B;值） | 更新Substance **矢量2**&#x200B;输入 | **字符串** *输入名称* SBSAR中输入的名称&#x200B;**矢量2** *输入*&#x200B;用于更新参数的值 |
| 公共&#x200B;**矢量2** *GetInputVector2*（**字符串**&#x200B;输入名称） | 获取Substance **矢量2**&#x200B;输入 | **字符串**“inputName”SBSAR中输入的名称 |
| 公共&#x200B;**void** *SetInputVector3*（**字符串** inputName，**Vector3**&#x200B;值） | 更新Substance **矢量3**&#x200B;输入 | **字符串** *输入名称* SBSAR中输入的名称&#x200B;**矢量3** *值*&#x200B;用于更新参数的值 |
| 公共&#x200B;**矢量3** *GetInputVector3*（**字符串**&#x200B;输入名称） | 获取Substance **矢量3**&#x200B;输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| 公共&#x200B;**void** *SetInputVector4*（**string** inputName， **Vector4**&#x200B;值） | 更新Substance **矢量4**&#x200B;输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Vector4** *值*&#x200B;用于更新参数的值 |
| 公共&#x200B;**矢量4** *GetInputVector4*（**字符串**&#x200B;输入名称） | 获取Substance **矢量4**&#x200B;输入 | **字符串** inputName SBSAR中输入的名称 |
| 公共&#x200B;**void** *SetInputColor*（**字符串** inputName，**颜色**&#x200B;值） | 更新Substance **颜色**&#x200B;输入 | **String** inputName用于更新参数的SBSAR **Color**&#x200B;值中的输入名称 |
| 公共&#x200B;**颜色** *GetInputColor*（**字符串**&#x200B;输入名称，**int**&#x200B;数据类型） | 获取Substance **颜色** | **字符串** *输入名称* SBSAR中的输入名称&#x200B;**Int** *数据类型* |
| 公共&#x200B;**void** *SetInputBool*（**string** inputName， **bool**&#x200B;值） | 更新Substance **布尔值**&#x200B;输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Bool** *值*&#x200B;用于更新参数的值 |
| 公共&#x200B;**bool** *GetInputBool*(**string** inputName) | 获取Substance **布尔值**&#x200B;输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| 公共&#x200B;**void** *SetInputInt*（**string** inputName， **int**&#x200B;值） | 更新Substance **Int**&#x200B;输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *值*&#x200B;用于更新参数的值 |
| 公共&#x200B;**int** *GetInputInt*(**string** inputName) | 获取Substance **Int**&#x200B;输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| 公共&#x200B;**void** *SetInputVector2Int*（**字符串** inputName， **int** x， **int** y） | 更新Substance **Vector2Int**&#x200B;输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y值的值 |
| **int[]Substance.Game.SubstanceGraph**.*GetInputVector2Int*( string inputName) | 获取2 int的数组（Vector2Int的x和y值） | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y值的值 |
| **voidSubstance.Game.SubstanceGraph**.*SetInputVector3Int*( string inputName， int x， int y， int z) | 更新Substance矢量3Int输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y的值用于更新参数&#x200B;**Int** z的值用于更新该参数 |
| **int[]Substance.Game.SubstanceGraph**.*GetInputVector3Int*( string inputName) | 获取3 int的数组（Vector3Int的x、y和z值） | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y的值用于更新参数&#x200B;**Int** z的值用于更新该参数 |
| **voidSubstance.Game.SubstanceGraph**.*SetInputVector4Int*( string inputName， int x， int y， int z， int w) | 更新SubstanceVector4Int输入 | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y的值用于更新参数&#x200B;**Int** z用于更新参数&#x200B;**Int** w的值用于更新参数 |
| **int[]Substance.Game.SubstanceGraph**.*GetInputVector4Int*( string inputName) | 获取4 int的数组（Vector4Int的x、y、z和w值） | **String** *inputName* SBSAR中输入的名称&#x200B;**Int** *x*&#x200B;用于更新参数&#x200B;**Int** y的值用于更新参数&#x200B;**Int** z用于更新参数&#x200B;**Int** w的值用于更新参数 |
| **voidSubstance.Game.SubstanceGraph**.*SetInputString*( string inputName， string value) | 更新Substance字符串输入 | **String** *inputName*&#x200B;用于更新参数的SBSAR中的输入名称&#x200B;**String** *值* |
| **字符串Substance.Game.SubstanceGraph**.*GetInputString*( string inputName) | 获取Substance字符串输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| **voidSubstance.Game.SubstanceGraph**.*SetInputTexture*（string inputName， Texture2D值） | 更新SubstanceTexture2D输入 | **字符串** *输入名称*&#x200B;用于更新参数的SBSAR中的输入名称&#x200B;**Texture2D** *值* |
| **Texture2DSubstance.Game.SubstanceGraph**.*GetInputTexture*(string inputName) | 获取SubstanceTexture2D输入 | **字符串** *输入名称* SBSAR中的输入名称 |
| **VectorIntSubstance.Game.SubstanceGraph**.*GetTexturesResolution*() | 获取图形的“目标设置”纹理分辨率（Vector4Int&#39;s x = width， y = Height，值为32， 64， 128， 256， 512， 1024， 2048和4096） | 无 |
| **intSubstance.Game.SubstanceGraph**.*SetTexturesResolution*（Vector2Int大小） | 设置图形的目标设置纹理分辨率（Vector2Int的x =宽度，y =Height，值可以是32、64、128、256、512、1024、2048和4096）如果成功，则返回0，否则： -1。 | **Vector2Int** *大小*&#x200B;用于更新参数**.** |
| **列出Substance.Game.SubstanceGraph**。*GetGeneratedTextures*() | 返回图形的材质着色器使用的所有SubstanceTexture2D对象。 | 无 |
| **intSubstance.Game.SubstanceGraph**.*烘焙*（ Texture2D纹理，字符串absolutePath） | 为图形的材质着色器使用的所有SubstanceTexture2D对象生成.png文件。 | 无 |
| **** Substance.游戏。** SubstanceGraph**.*重复*() | 复制Substance 图形 | 无 |
| **Substance.Game.SubstanceGraph**.*重复*(string newGraphName) | 复制Substance 图形并为其命名（相应的素材也将具有相同的名称） | **String newGraphName** |
| **** Substance.游戏。** SubstanceGraph**.*GetInputProperties*() | 查询程序性输入信息，返回“InputProperties”的数组，其中:public结构InputProperties {公共字符串名称； // inputName公共字符串标签； // GUI公共字符串组中的小部件标签； // GUI公共字符串组中的小部件组[] componentLabels； //用于滑块（最多4个标签）公共字符串[] enumOptions； //用于选项公共输入属性类型；公共向量4最大值；//用于滑块公共向量4最小值；//用于滑块公共浮点步骤；//用于滑块公共enum inputPropertiesType { Boolean = 0，// 0 Float， // 1 Vector2， // 2 Vector3， // 3 Vector4， // 4 Color， // 5 Enum， // 6 Texture， // 7 String， // 8 Invalid = -1// -1 }； | 无 |
| **bool** **Substance.Game.SubstanceGraph**.*HasInput*（**字符串**&#x200B;输入名称） | 检查图形中是否存在输入，返回true/false： | **字符串** *输入名称* SBSAR中的输入名称 |
| **bool** **Substance.Game.SubstanceGraph**.*IsInputVisible*（**字符串**&#x200B;输入名称） | 检查可见输入是否可见，返回true/false | **字符串** *输入名称* SBSAR中的输入名称 |

## 渲染

| Public方法 | 描述 | 参数 |
| --- | --- | --- |
| 公共&#x200B;**void** *QueueForRender*() | 将Substance图形添加到队列 | 无 |
| ***mySubstance.**RenderAsync()* | 异步渲染所有排队Substance图表 | 无 |
| ***mySubstance.**RenderSync()* | 同步渲染所有排队Substance图表 | 无 |

## 编辑器模式下的脚本：

为了在“编辑器”模式下永久修改图形，必须重新导入每个相应的Substance。 这可通过以下函数完成：

```
static void ReImportSubstance(Substance.Game.Substance pSubstance)

{



// Re-import Substance object:

SubstanceImporter importer = AssetImporter.GetAtPath(pSubstance.assetPath) as SubstanceImporter;

importer.CommitSubstanceToImporter(pSubstance); // plugin function

EditorUtility.SetDirty(importer);

importer.SaveAndReimport();



}
```


（使用“CommitSubstanceToImporter”，一个Substance增效工具功能：将所有修改后的图形参数和/或输入复制到Substance导入器对象，然后通过Unity的导入器机制将其序列化到磁盘）
