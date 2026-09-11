---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/renderers/color-management.html"
breadcrumb-title: ''
description: 了解将材料用于不同渲染器时的色彩管理和灰度系数校正。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%

---


# 色彩管理

我们将采用简单的方法，说明线性空间渲染为光照计算提供了正确的数学基础。 它创造了一种环境，允许光线交互以可信的现实世界方式呈现。 为了讨论线性空间绘制，必须引入灰度系数校正的概念。 当出于显示和存储目的对图像进行编码时，灰度系数校正是减少带宽和位分配的优化过程。 此过程利用人眼的亮度感知，亮度感知大致遵循明亮度的立方体根。

>[!NOTE]
>
> 线性空间渲染是一个高度复杂的主题。 有关详细信息，请参阅[Substance学院](https://academy.substance3d.com/)上免费的[PBR指南卷1](https://academy.substance3d.com/courses/the-pbr-guide-part-1)。

## 色彩管理

本文旨在详细介绍在[3D软件](https://www.adobe.com/cn/products/substance3d/3d-augmented-reality.html)和渲染器中处理从&#x200B;**Substance Painter**&#x200B;和&#x200B;**Substance Designer**&#x200B;导出的纹理的过程。

将图像解释为素材通道输入的正确方式取决于图像在场景中的使用方式。 色彩空间、编码以及颜色值是否与&#x200B;**场景引用的明亮度**&#x200B;或&#x200B;**显示引用的明亮度**&#x200B;成比例也起着重要的作用。

* 不应转换用于表示&#x200B;**非颜色数据**&#x200B;的图像。 这些映射通常是&#x200B;**正常**、**粗糙度**、**金属**、**位移**&#x200B;和&#x200B;**氛围**&#x200B;**遮蔽**&#x200B;映射。
* 代表我们所看到的颜色的图像可能具有多种场景。 例如，已经是&#x200B;**场景线性**&#x200B;的图像通常不需要转换，如&#x200B;**高动态范围**&#x200B;图像，这些图像以&#x200B;**OpenEXR**&#x200B;和&#x200B;**HDR**&#x200B;等格式存储。
* 为显示而创建的图像(**display-referred**)需要移除其灰度系数。 这包括&#x200B;**PNG**、**JPEG**&#x200B;和&#x200B;**BMP**&#x200B;等大多数格式。 这些图像是&#x200B;**基本**&#x200B;**颜色**、**扩散**、**Specular**&#x200B;和&#x200B;**emissive**。

虽然这过于简单化，但考虑以下过程可能会有所帮助：

* “场景引用(例如， 线性)” ：不应用转换
* &quot;display-referred(例如， sRGB)” ：应用反向变换将图像“线性化”，以进行适当计算

>[!NOTE]
>
> 将灰度系数空间转换为线性空间的sRGB解码函数(EOTF)用于Substance Painter和Substance Designer，并由IEC 61966-2-1:1999标准定义

可以将Substance Designer配置为使用[OpenColorIO](https://opencolorio.org/)进行色彩管理。 这允许您在多个应用程序间拥有&#x200B;*一致的*&#x200B;色彩变换和图像显示。 在此模式下，Substance Designer将在内部使用&#x200B;**线性RGB**&#x200B;颜色。 由于8位深度通常不足以表示线性颜色，因此建议对[图形](https://docs.substance3d.com/display/SDDOC/Graph+View)中的颜色纹理使用&#x200B;*至少* **16位**&#x200B;深度。

![](https://helpx-prod.scene7.com/is/image/HelpxProd/sd-cm?$png$&jpegSize=200&wid=686)

在引入[ACE](https://www.oscars.org/science-technology/sci-tech-projects/aces)时，我们现在具有两种不同的色彩空间：线性sRGB（无灰度系数版本的sRGB）和[ACEScg](https://acescolorspace.com/)，后者是一个宽色域（“场景引用”或线性）色彩空间，更适合CG渲染。

*色域绘图图形 —<https://acescolorspace.com/>*

Substance Designer还支持&#x200B;**Adobe 颜色引擎(ACE)**。 使用&#x200B;**ACE**，您可以在&#x200B;**sRGB**、**线性sRGB**&#x200B;和&#x200B;**ACEScg**&#x200B;之间选择工作色彩空间。 使用&#x200B;**sRGB**&#x200B;时，**ACE**&#x200B;与旧版模式几乎相同。 使用线性色彩空间时，**ACE**&#x200B;大致类似[OpenColorIO](https://opencolorio.org/index.html)。

## Substance 插件

通过Substance集成增效工具使用Substance材料时，输出通过集成和主机应用程序的色彩管理自动标记为线性/灰度系数。 但是，了解该过程很重要：将Substance映射用作导出的位图而不是Substance材料时，您可能需要手动将纹理标记为&#x200B;**灰度系数编码**&#x200B;或&#x200B;**原始**，具体取决于您使用的渲染器。 通常，8或16位.png、.jpg、.tga或.tif文件采用灰度系数编码，而&#x200B;**sRGB OETF**&#x200B;和.exr文件是线性的。

## 3D

### 使用纹理

* [Maya中的Substance纹理](../../renderers/color-management/textures-in-maya/substance-textures-in-maya.md)
* [3ds Max中的Substance纹理](../../renderers/color-management/textures-in-3ds-max/substance-textures-in-3ds-max.md)
