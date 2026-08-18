---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/software-interface/substance-3d-designer.html"
breadcrumb-title: ''
description: 了解如何访问和使用Substance 3D Designer中的烘焙窗口将模型信息烘焙到纹理中。
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Software Interface > Substance 3D Designer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D Designer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 2%

---


# Substance 3D Designer

![](../../../assets/sd-mesh-right-click.png)

可以通过[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)窗口中的网格文件访问烘焙窗口。 右键单击网格名称并选择“**烘焙模型信息**”以打开烘焙窗口。

## 概述

![](../../../assets/sd-window-overview.png){width="500px"}

烘烤窗分为若干面板，如下所述。

### 要烘焙的元素

![](../../../assets/sd-mesh-selection.png)

此面板控制将使用低多边形网格的哪一部分进行烘焙。

此面板将列出在低多边形网格文件中找到的几何。 缺省情况下，该列表基于在文件中找到的单个材料，但在相关时可将其切换到子网格。 您可以取消选中在烘焙过程中应忽略的元素。

### 输出

![](../../../assets/sd-output.png)

此面板控制烘焙纹理将位于何处。

| *参数* | *描述* |
| --- | --- |
| **方法** | 控制烘焙纹理将与Substance包一起存储的方式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>嵌入</strong> ：烘焙纹理存储在具有特定命名的Substance包旁边的子文件夹中。</li><li data-preserve-html="true"><strong>已链接</strong>（默认） ：烘焙纹理存储在定义的文件夹中，然后引用到Substance包中。</li></ul> |
| **文件夹** | 存储烘焙纹理时的位置。 单击三点式按钮打开一个文件对话框并选择导出文件夹。右侧将显示一个复选标记，指示文件夹是否实际存在。 |
| **名称** | 烘焙纹理的命名约定。 单击三点式按钮以打开下拉列表并插入其他占位符（品牌名称、自定义、材质、网格）。 |
| **示例** | 模拟文件名以测试命名约定。 |
| **将资源放入网格特定的文件夹** | 如果启用，烘焙纹理将保存在名为网格文件的文件夹中。 |

### High Definition Meshes

![](../../../assets/sd-high.png)

此面板控制高多边形网格列表和相关设置。 有关详细信息，请参阅[常用参数](../../../bakers-settings/common-parameters/common-parameters.md)。

### 默认值

![](../../../assets/sd-default-values.png)

有关详细信息，请参阅[常用参数](../../../bakers-settings/common-parameters/common-parameters.md)。

### 面包机列表和设置

![](../../../assets/sd-baker-list.png)

烘焙器是您选择要生成哪种烘焙纹理的位置。 默认情况下，该列表为空。

* **添加新的面包师：**&#x200B;单击“添加面包师”按钮。
* **删除面包机：**&#x200B;在列表中选择面包机，然后单击“删除面包机”按钮。
* **将面包机移动到顶部：**&#x200B;在列表中选择面包机，然后单击“拉至顶部”按钮。
* **向下移动面包机：**在列表中选择面包机，然后单击“Push down”（下移）按钮。

默认情况下，继承中的每个面包师都使用默认值（请参阅上文）。 例如，可以通过单击面包机行上的单元格来覆盖大小（分辨率）。 这适用于行中的其他设置。

单击列表中的面包机时，“面包机参数”视图将使用其特定参数更新。

要了解有关特定参数的详细信息，请参阅： [面包师设置](../../../bakers-settings/bakers-settings.md)。
