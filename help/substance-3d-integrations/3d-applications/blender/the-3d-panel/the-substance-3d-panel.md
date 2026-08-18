---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/blender/the-substance-3d-panel.html"
breadcrumb-title: ''
description: 了解如何使用Blender中的Substance 3D面板管理材质、参数和输出。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > The Substance 3D Panel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D面板
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Substance 3D面板

![](../../../assets/blender-substance3dpanel.png)

## 面板控件

**创建** — 打开文件浏览器以选择Substance 3D素材。 默认情况下，这将使用从.sbsar文件生成的纹理创建混合器材质。

**应用** — 将选定的Substance 3D素材附加到新素材槽中的选定对象。 这不会覆盖对象先前的材质指定。

**Substance 3D社区资源** — 在Web浏览器中打开Substance 3D社区资源页面。

**Substance 3D Assets** — 在Web浏览器中打开Substance 3D Assets源页面。

**复制所选Substance 3D素材** — 加载所选Substance 3D素材的新实例。 同一Substance材料的不同实例的参数可以彼此独立地调整。

**刷新** — 重新加载Substance 3D素材

>[!WARNING]
>
> **警告：**
> 
> 使用刷新按钮将撤消用户对着色器图形所做的任何更改。 在刷新之前复制任何用户添加的节点，以便在刷新之后将它们粘贴到图形中。

**移除** — 从面板中移除选定的Substance 3D素材。

>[!NOTE]
>
> 从Substance材料创建的混合器材料将保留在项目中。 可以手动将其从对象中删除或移除。

**加载的3DSubstance素材** — 显示已加载到.blend文件中的Substance素材的列表。

## 图形参数

**输出分辨率** — 与和Height分辨率的下拉列表。 这些值可以单独与调整后的值取消链接。

**随机化和随机植入** — “随机化”按钮将生成新的随机植入值，以更改可以使用随机值的参数。 也可以手动设置随机植入。

## 使用预设

SBSAR文件可能会随预设一起发布，这些预设可在“预设”下拉框中找到。 要制作您自己的预设，请根据需要调整参数，然后使用&#x200B;**保存**&#x200B;按钮。 还有其他选项可将所选预设导出为.sbsprs文件，并从下拉列表中删除所选预设。 **加载**&#x200B;按钮可用于从.sbsprs文件导入预设。

## Substance参数

可以使用“Substance参数”控件调整已在Substance Designer中公开的参数。 这些参数由Substance材质的创建者设置，且会因材质而异。 调整这些参数将更新生成的纹理，如“载入的3DSubstance素材”部分中素材名称旁边的加工图标所示。

可通过下拉菜单切换和更改输出纹理的文件格式。

有关详细信息，请参阅Designer文档页面上的[公开参数](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/substance-graphs/manage-parameters/exposing-a-parameter)。

## 技术参数

Substance材料可能具有一组技术参数。 这些是用于颜色校正和其他材质调整的附加控件。
