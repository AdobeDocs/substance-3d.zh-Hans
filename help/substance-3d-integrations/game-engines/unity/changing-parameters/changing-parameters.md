---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/changing-parameters.html"
breadcrumb-title: ''
description: 在Unity中修改材料参数，以便在运行时自定义材料外观和属性。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Changing parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 更改参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# 更改参数

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

材料的参数可在Substance 图形对象(SGO)上访问。

1. 在项目窗口中，选择要自定义的图形的sbsar 文件徽标。 sbsar具有绿色“SBSAR”徽标。

   ![](../../../assets/screen-shot-2022-03-29-at-2-27-56-pm.png)

## 程序化属性

1. **生成所有输出**：从sbsar 文件生成所有输出。 默认情况下，仅创建标准着色器使用的输出。
1. **生成Mipmaps**：将为每个Substance输出生成mip纹理。
1. **随机植入**：此按钮将更改图形用于生成纹理的随机植入。 更改此值将基于种子值为计算纹理创建新结果。
1. Substance文件中公开的参数在Unity中可用。 编辑器控件基于为Substance创建的参数类型。
1. **预设处理：**&#x200B;您可以导出或导入Substance预设文件(sbars)。 导出预设将根据Substance的参数设置创建预设文件。 您可以从Substance Designer和Substance Player中导出预设文件，然后使用“导入预设”按钮导入这些预设文件。 这有助于在应用程序和团队之间共享Substance预设。

</td>
<td style="border: 0;" valign="top">

![](../../../assets/changing-parameters.png)

</td>
</tr>
</table>
