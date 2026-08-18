---
title: OpenPBR
description: 了解材质模型以及如何将其用于跨3D应用程序基于物理的渲染。
source-git-commit: 17ce332abf45d97c495c30b89df031ad2f2bbdf0
workflow-type: tm+mt
source-wordcount: '9657'
ht-degree: 0%

---


# OpenPBR

[**下载此页面的脱机版本。**](../assets/openpbrf/openpbr.pdf)

**OpenPBR**&#x200B;是一种开放的、基于物理的表面着色模型，旨在提供一致且可预测的方式以描述跨不同3D工具、渲染器和管道的材料。 它定义了一个单一、全面的材质模型，能够呈现广泛的真实世界表面，同时保持足够的灵活性，以使用物理上有意义的参数支持更具风格化或艺术家驱动的外观。

该模型解决了“标准”着色器之间长期存在的不一致问题，这些着色器名义上行为类似，但在应用程序间的参数定义和物理假设方面不同。 基于物理渲染原理，OpenPBR从真实世界的光线行为角度描述材料，强调能量守恒、直观的参数范围和稳定的光照响应。 OpenPBR不再规定特定的用户界面，而是定义素材在基本层上的行为，从而允许工具以自己的方式实现模型，同时当资源在应用程序和管道之间移动时保持一致的视觉结果。

本文档旨在为艺术家提供理解和使用OpenPBR的指南。 它解释了模型的基本原则，它的组成部分如何描述真实的光行为，以及这些想法如何转化为实际的物质创造。 该指南针对从事外观开发、纹理化和渲染等领域的3D艺术家，他们不想专注于某个特定应用程序，而是希望构建稳定、物理上可信的材料，这些材料在不同的软件环境中保持一致并且可传输。

>[!NOTE]
>
> 如果您已在使用OpenPBR版并且正在寻求技术帮助，[OpenPBR常见问题解答](openpbr-faq.md)可能已经有您问题的答案。

![](../assets/OpenPBR_desk.jpg)

*上面的OpenPBR演示场景由Nikie Monteleone创建。 此文档中的示例素材和通道渲染由Celine Dameron创建。*

## 互操作性和文件标准

### 与OpenPBR共享素材语言

OpenPBR的核心目标之一是改善工具之间材料的移动方式。 OpenPBR定义&#x200B;**共享着色模型**，而不是与单个渲染器或应用程序关联的着色器，这是描述素材如何响应光线的常见方式。

对于艺术家来说，这意味着一种OpenPBR材料不仅仅是，例如，“Adobe材料”或“Autodesk材料”，而是对表面和体积行为的描述，原则上可通过多种工具理解。 其目的是为了在一个应用程序中创作的材料可以在其他地方得到一致的解释，只要这些工具支持OpenPBR模型。

### 资源交换问题

该OpenPBR规范明确承认生产中存在一个长期挑战：**材料无法在应用程序之间正常传递**。 不同的渲染器通常使用不同的参数名称、着色假设和基础模型，这使得外观匹配变得困难且耗时。

OpenPBR旨在解决此问题。 通过定义单一、物理上接地的材质模型，涵盖常见的生产需求（金属、电介质、分层材料、传输、散射），它可以提供稳定的交换目标。 虽然这不能保证在所有情况下都实现完美的视觉匹配，但是与专有着色器模型相比，它显着减少了歧义。

对于艺术家来说，实际收获是OpenPBR旨在保持&#x200B;*意图*。 即使无法实现精确的视觉平衡，材料的结构 — 即金属、可传输、表面有多粗糙或各向异性 — 仍然清晰且可传输。

![](../assets/OpenPBR_meetmat.jpg)

### 与MaterialX的关系

OpenPBR与&#x200B;**MaterialX**&#x200B;密切相关，后者是一种行业标准框架，用于以渲染器不可知的方式描述材料和外观。 OpenPBR的参考实现寿命在MaterialX内，这意味着可以使用在许多管道上受支持的既定交换格式表示OpenPBR材料。

此关系很重要，因为OpenPBR本身&#x200B;**不是文件格式**。 相反，它定义了&#x200B;*什么*&#x200B;素材，而MaterialX提供了一种标准化方式来&#x200B;*存储和交换*&#x200B;工具之间的素材。 实际上，这允许将OpenPBR素材嵌入到更广泛的场景描述中，并在支持MaterialX的DCC和渲染器之间共享。

对于艺术家来说，这通常发生在引擎盖下面，但它解释了为什么现代管道中越来越多的OpenPBR材料被描述为“可移植”或“可互操作”。

### 互操作性到底是什么意思，什么不意味着什么

在互操作性方面设定切合实际的期望非常重要。 OpenPBR不保证材料在每个应用程序中的外观都相同。 光照、渲染算法、色彩管理和功能支持方面的差异仍然可能会影响最终图像。

OpenPBR提供了共同的基线：一组一致的参数和行为，对材料构造方式的共同理解，以及更清晰的在工具之间转移材料而无需从头重建它们的途径。

对于艺术家来说，这意味着在部门或应用程序之间移动资源时意外事件更少，而且工作流程强调耐用的材料逻辑而不是特定于工具的技巧。

### 对艺术家的实践启示

从日常的角度来看，与OpenPBR合作会鼓励那些自然支持互操作性的习惯：

* 从光线行为而不是特定于应用程序的材质类型进行思考
* 使用物理上有意义的参数（金属度、粗糙度、透射率、散射）
* 避免依赖无文档解决方案或特定于渲染器的解决方案

即使素材永远不会离开单个应用程序，这些实践也符合现代的管道标准，使资源随着工具和渲染器的发展更加适应未来。

## 材料类型

### 通过光线相互作用定义的材质

OpenPBR是一种整体模型(“uber-shader”)，旨在表示广泛的材料类型；这些类型根据光线与它们的相互作用方式描述。 每个OpenPBR素材不是根据固定预设定义素材，例如“玻璃”或“皮肤”，而是基于水平和垂直分层模型构建，这使艺术家能够将完全定义且物理上有意义的特征（如漫反射、Specular反射、透射、次表面散射和分层）混合在一起。 这些行为的不同组合自然地产生熟悉的现实世界材料。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingInteriorAtelier.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingStudio.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingTerraceNearGranaries.png" alt=""/></td>
  </tr>
</table>

该方法使用事先定义分层和混合框架的固定模型，从而规避了艺术家在个案基础上创建着色网络的任何要求，并允许OpenPBR以一致、物理上稳定的方式表示简单和复杂的材料。

![](../assets/openpbrf/model_schematic2.png)单击可缩放。 *该图改编自Academy Software FoundationOpenPBR表面规范，在Apache许可证2.0下使用*

### 核心材料行为

虽然OpenPBR没有规定严格的材料类型，但大多数真实材料都属于一些广泛的行为类别。 了解这些类别有助于为建筑材料建立一个坚实的心理模型。

### 电介质（非金属）材料

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorViolet.png" alt=""/><br><em>介电材料的一个示例。</em></td>
    <td style="border: 0;" valign="top">电介质是非金属材料，如塑料、木材、石材、织物、橡胶和表皮。 它们的定义特点是：<br><br><ul><li>可见的漫射分量</li><li>大多是无色（白）Specular反射</li><li>主要由折射率(IOR)控制的反射率</li><li>无金属反射行为</li></ul><br><br><strong>介电材料的主要参数：</strong><br><br><ul><li>基色定义素材的整体颜色</li><li>Specular影响Specular高光的色调（在掠过角度时最明显）</li><li>“Specular粗糙度”可控制Specular高光显示的锐化或模糊程度</li><li>“Specular粗细”可调整Specular高光的整体强度 </li><li>对于介电材料，漫反射主导表面的外观，并由基色控制。 正常入射时Specular反射有限，朝掠入射角增加，但保持不着色。</li></ul></td>
  </tr>
</table>

### 金属材料

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/><br><em>金属材料的一个示例。</em></td>
    <td style="border: 0;" valign="top">金属材料（如钢、铝、铜或金）的行为与非金属（电介质）材料截然不同。 对于金属，外观几乎完全由Specular反射驱动：与介质不同，金属没有散射分量，光线不会在表面下方散点，而是直接反射。 它们的定义特点是：<br><br><ul><li>无漫射分量 — 颜色完全来自反射</li><li>彩色Specular反射</li><li>表面细节，尤其是粗糙度，在外观中起着主要作用</li></ul><br><br><strong>金属材料的关键参数：</strong><br><br><ul><li>基色控制反射的颜色</li><li>Specular粗糙度控制这些反射看起来是锐利还是模糊</li><li>Specular量缩放反射强度</li></ul></td>
  </tr>
</table>

### 基底金属度

基础金属度定义材料的行为是作为电介质还是金属 — 这不仅仅是一种视觉调整，还包括材料基础光响应的变化。

* **0**→完全非金属（扩散+Specular）
* **1**→完全金属化（仅限Specular）
* **0-1**→两种行为的混合。 中间值最适合用于材料混合物，例如Dirt、腐蚀或磨损表面，而不是“部分金属”材料。

#### 金属性的实用指南

* 将&#x200B;**0**&#x200B;或&#x200B;**1**&#x200B;用于大多数材质
* 仅对混合曲面使用中间值
* 依靠粗糙度和表面细节来塑造金属外观。

对于喷涂或涂层金属、透明和透射材料，使用分层（如涂层）而不是降低金属性。

### 透明和透射材料

透明和透射材料允许光线穿过它们。 常见示例包括玻璃、许多液体以及透明或有色塑料。 它们的定义特点是：

* 光线进入曲面，离开反面
* Thickness强烈影响外观
* 受折射率(IOR)控制且受表面粗糙度影响的折射率
* 最终外观的折射、吸收、散射和色散形状

透射率描述光如何穿过物体。 较粗的区域看起来较暗或较饱和，而较细的区域看起来更清晰。 “传输颜色”、“传输深度”、“散点颜色”和“色散”等参数共同控制此行为。

“透明”和“透明”这两个词的区别在于：“透明”是现实生活中的日常用语；如果我们能看穿它，就一定是透明的。 “透明”是“半透明”的同义词。 比如，磨砂玻璃让光透过（因此是透射性的），但它并不透明 — 我们看不见它。

### 次表面材料

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/subsurface-scattering/subsurfaceScattering.png" alt=""/><br><em>使用次表面散射的材料的示例。</em></td>
    <td style="border: 0;" valign="top">次表面材质允许光线进入曲面，散点在曲面下方，然后再次在入口点附近退出。 常见的例子包括皮肤、蜡、大理石和许多有机材料，例如许多类型的食物。  — 水果、蔬菜，或者圣内克泰尔奶酪。 地下材料的界定特点是：<br><br><br><ul><li>柔和的扩散着色</li><li>薄区域中的渗色</li><li>外观取决于Thickness</li><li>光线不会穿过对象</li></ul><br><br><br>次表面散射与透射不同。 透射描述穿过材料并离开对面的光，而次表面散射描述进入表面、在该表面内散射、然后离开该表面进入的点附近的光线，大多数是在同一侧。 值得注意的是，金属材料不支持透射或次表面散射。 更改完全金属材料（即，基础金属度值为1的材料）的透射率或亚表面值不会影响其外观。</td>
  </tr>
</table>

## 在素材行为之间混合

现实世界的材料很少是完美的。 许多表面最好被描述为行为的混合，而不是属于单一类别。 例如，如果表面出现Dirt、磨损或铁锈的迹象，则表面的不同部分将对光产生不同的反应。 OpenPBR通过允许从曲面的一部分平滑地混合到另一部分来支持这一点。

### 金属感混合

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/metalness/metalnessAsBlend.png" alt="" width="400"/><br><em>在该材料中，铁的金属性为1，而铁锈的金属性为0。 铁锈向铁转变时可出现中间金属度值。</em></td>
    <td style="border: 0;" valign="top">虽然金属度通常设置为0或1（即，完全非金属性或完全金属性），但中间值是有意义的。 这些值表示金属和非金属材料小规模混合在一起的表面，例如包含金属颗粒或薄片的涂料。 此外，如前所述，OpenPBR材料由表示不同物理界面的层构成。 材料的基层（它是“核心”层）完全可以是金属的，但上方可以有一个非金属涂层，该涂层不仅仅是一个附加的Specular控件，它表示光必须经过的一个单独的物理表面。 对于某些类型的汽车油漆就是这种情况，例如：金属薄片将表示在材料的“基层”中，而“涂层”层表示透明涂层。</td>
  </tr>
</table>

### 组合图层以创建复杂行为

复合材料，例如本节前面提到的磨砂玻璃或汽车油漆，是通过受控方式结合多种行为创建的。 例如：

* **磨砂玻璃**：具有高粗糙度和散射的透射率
* **喷涂金属**：金属基底上的介电表面，通常具有清晰的涂层。考虑存在的物理行为及其交互方式比从预设的角度考虑更有效。 OpenPBR材料由描述光线与表面相互作用方式的有物理意义的元件定义。 材质“类型”从行为的组合中自然出现，而不是被显式选择。 艺术家通过专注于光线交互、混合和分层，可以创建各种逼真的素材，同时保持物理上的合理性。

## 使用OpenPBR

### OpenPBR材料的概念结构

OpenPBR被设计为一个单一、统一的表面着色模型，能够代表多种现实世界的材料。 OpenPBR将多个表面特征结合到一个分层结构中，而不是针对不同的材料类型在不同的着色器之间切换。

从概念上讲，您可以将OpenPBR素材视为具有三个关键元素：

* **基础框架**：OpenPBR会考虑材料由物理积木制成，这些积木可以混合（水平混合）或相互栈叠（垂直分层）。 这些色块对光线的反应可能不同。 当两个这样的块混合时，结果将是两者的反射的混合。 但是，当它们分层时，最下面的块将只接收和反射最上面的块所允许通过的光线。 这种设置允许艺术家将素材视为简单组件的混合。 这些组件的定义及其所处位置是第二个关键因素：
* **一系列对共享框架做出贡献的图层**：每个素材都将有一个基础图层，该图层确定素材的主要颜色、素材是粗糙还是光滑等特征。 素材可能还具有其他图层 — 薄膜、涂层和朦胧 — 可重现光油或Dust等效果。
* **一组面向艺术家的控件**：允许艺术家控制反射构图规则（以及OpenPBR素材的整体外观）的界面。 取决于特定软件在用户界面中表示这些控件的方式，这些控件实质上是一组旋钮或滑块，可让艺术家控制例如，反射应有多强烈，或在特定视角下应显示哪种色调。 某些控件将应用于整个框架（因此将应用于素材中的所有图层）；某些控件将仅应用于特定图层。

### 框架中的素材层

![](../assets/openpbrf/model_schematic2.png)单击可缩放。 *该图改编自Academy Software FoundationOpenPBR表面规范，在Apache许可证2.0下使用*

每个图层都带来特定的物理效果，材质模型管理这些图层如何以物理上可信的方式交互。 此分层结构在OpenPBR实施中是一致的。 各个应用程序可以自由地提供一个用户界面，无论它们认为合适与否都可以控制这些图层。

>[!NOTE]
>
> 上图中未显示两个“图层”：
>
> * **Specular**：控制表面的光泽或反射程度，无论基底是否具有金属质感。 Specular存在于图层栈叠中，但它本身不是真实图层，而是出现在图层栈叠中的基底图层和涂层图层的属性。
> * **几何**：其他OpenPBR图层确定素材的成分时，几何图层定义素材应用的形状和外观，包括不透明度、法线、切线和薄壁行为。
>
> 为简单起见，我们将继续将“几何”和“Specular”称为“图层”。

从最深到最外构成一个OpenPBR表面的层是：

* **基础图层**：在OpenPBR素材的底部，基础图层定义了光与素材之间的基本交互。 基底层的参数决定材料的主要颜色，是粗糙还是光滑，以及它是金属还是非金属（也称为电介质）（根据它与光的相互作用方式）。

>[!NOTE]
>
> 对于大多数材料来说，基层是绝对必要的。 根据3D中复制的素材类型，此（薄膜、涂层和模糊）上方的图层可能存在，也可能不存在。

* **薄膜**：如果存在，薄膜图层将位于基底图层的上方。 它可以再现非常薄的表面层的视觉外观，从而产生彩虹色，如在肥皂泡、烧焦的金属或油膜中看到的彩虹色。

* **涂层**：“涂层”图层（如果存在）会重现位于除Fuzz之外所有其他图层上方的透明反射图层。 这可以模拟真实效果，如清漆、湿表面或某些类型的汽车油漆。

* **模糊**：如果存在，模糊图层会从微纤维重现反射。 例如，它可用于再现模糊织物或Dust层的外观。

这些层中的每一层与光的相互作用方式由一组参数确定。

### 材料类型

而基础金属度则决定了适用于下一层材料的特性 — 完全非金属材料与金属材料具有不同的特性。

#### 非金属材料（基础金属度= 0）

完全非金属材料（即，基础金属度值为0的材料）将分为三种基本类型： **扩散**、**次表面**&#x200B;或&#x200B;**半透明**。 请注意，材质不一定只属于上述一种基本类型。 由这些基本材料类型混合而成的更复杂的材料是可能的。

**漫射材料**&#x200B;通常是木材或石头等不透明的材料。

**次表面材质**&#x200B;内部散点光；例如，皮肤或蜡可能属于这种材质类型。

**半透明基础材质**&#x200B;允许光线穿过它们；其中包括玻璃、晶体或某些液体等材料。 需要注意的关键参数包括下面的全局Specular参数、基本层参数和具体的传输参数。 次表面散射(SSS)和透射之间的区别在于，SSS不允许您通过材料看到 — 光束在材料中散射，然后回到同一侧。 相反，透射控制至少部分透明的材料 — 光束穿过该材料。

#### 金属质感（金属度> 0）

相反，启用“基本金属度”（即，其值大于0）后，它将获得一些特定的行为特征：

* 素材的Specular颜色值控制素材在掠过角度附近的色调（当光线以接近平行的角度照射到曲面时）。
* 素材的“基色”值控制垂直入射时的反射（即，当光线从表面以90度反射时）。
* 素材的“Specular重量”值可缩放反射的整体强度，从而影响正常角度和掠夺角度。

金属材质与以下通道相结合，可创建各种效果。

**发射**

发射通过直接发射光允许表面作为光源。 虽然发射不是反射现象，但是它包含在材质模型中，从而发射材料可以和反射和透射特性一致地被定义。

**薄膜**

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR15.png" alt=""/></td>
    <td style="border: 0;" valign="top">薄膜效果（如果存在）可重现非常薄的表面层的视觉外观，从而产生彩虹色，如在肥皂气泡或油膜中看到的彩虹色。</td>
  </tr>
</table>

**涂层**

涂层（如果存在）再现位于除Fuzz以外的其他所有图层上方的透明反射图层。 这可以模拟真实效果，如清漆或某些类型的汽车涂料。 皮毛图层由0到1之间的范围定义；将此值设置为0将完全禁用皮毛图层。

**模糊**

可以添加模糊层来再现类似织物的表面，例如天鹅绒或缎面，或者它可用于在表面上产生Dust层的效果。

### 材质工作流概念

#### 以光明的行为来思考，而不是物质标签

OpenPBR围绕光的行为方式而设计，而不是围绕固定材料类别而设计。 艺术家无需选择代表“玻璃”、“皮肤”或“金属”的着色器，而是通过描述光从表面反射、穿过表面、表面中的散点或表面发出的方式构建材料。 这一方法鼓励了思维模式的转变：材料不是预先定义的类型，而是物理行为的组合。 单个真实素材可能一次涉及这些行为中的几种，OpenPBR会明确指定这些行为，而不是将它们隐藏在预设或不透明的着色模型后面。

#### 关注的分离：材料与光照无关

基于物理的工作流程的核心原则是物质描述与光照的分离。 材质用于描述固有表面和体积属性，而光照则定义显示这些属性的环境。 这种分离减少了相互依赖性，使复杂场景更易于管理。 创作良好的OpenPBR素材在各种光照条件下都应可信，而无需进行特定于场景的调整。 在较小的范围内，OpenPBR继续这一哲学，尽可能保持参数独立，使艺术家能够调整素材的一个方面，而不会无意中破坏其他方面。

#### 逐步制作建筑材料

OpenPBR鼓励以渐进方式创造材料。 大多数工作流程都从建立表面响应（光线从对象反射的方式）开始，然后再引入体积效果，如透射或次表面散射。 次要行为（包括模糊、发射或薄膜干扰）通常在稍后叠加以细化真实感或实现特定的视觉提示。 这种分层方法可帮助艺术家更轻松地诊断问题，并避免在过程中早期使素材过于复杂。 通过从主要行为构建到次要行为，材质可保持更易于理解、调试和重复使用。

#### 作为学习工具的预设和示例

OpenPBR包括常见素材的预设，但这些预设最好理解为参考示例，而不是最终解决方案。 研究预设如何平衡粗糙度、金属度或传输深度等参数来帮助艺术家了解特定视觉结果的构建方式。 OpenPBR工作流程鼓励艺术家观察真实世界的材料，识别游戏中的基本光线行为，并使用对身体有意义的控制重新创建这些行为，而不是全盘依赖预设。

## OpenPBR通道和参数

### 镜面

![](../assets/openpbrf/renders/specular/color/specColorYellowNoMetal.png){width="250"}

*具有黄色Specular的介电（非金属）灰色材料。*

+++Specular参数

**Specular粗细**

虽然“Specular颜色”确定在掠过角度进行任何反射的色调，但“Specular粗细”确定此类反射的强度（范围为0至1）。 当值为0时，在掠角处完全没有反射；当值较高时，这种反射的强度变得更显着。 请注意，在“真实世界”中，每种素材都在一定程度上具有反射性，如果在3D环境中重新创建，则其“Specular权重”值将大于0。 还要注意，在参数化素材的反射时，不应将“Specular权重”视为“主要”值；“Specular粗糙度”（请参阅下文）始终是确定素材反射率的关键考虑因素。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight0.png" alt=""/><br><em>Specular重量= 0.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight05.png" alt=""/><br><em>Specular重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight1.png" alt=""/><br><em>Specular重量= 1.0</em></td>
  </tr>
</table>

**Specular颜色**

这确定了当光线以掠入射角（与材料表面几乎平行的角度）反射时，与反射有关的任何色调。 对于金属材质（请参阅下面的金属色度），可能会应用色调；对于非金属材质，Specular颜色通常应该是白色。 下图显示了金属和非金属材料上的各种Specular。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorGreen.png" alt=""/><br></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorViolet.png" alt=""/><br></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorYellow.png" alt=""/><br></td>
  </tr>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorGreenNoMetal.png" alt=""/><br><em>绿Specular</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorPurpleNoMetal.png" alt=""/><br><em>紫色Specular</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorYellowNoMetal.png" alt=""/><br><em>黄色Specular</em></td>
  </tr>
</table>

**Specular粗糙度**

与PBR材料中的“粗糙度”参数一样，OpenPBR材料中的“Specular粗糙度”代表微观表面变化：即使是肉眼可见的光滑表面也具有散点反射光的微小瑕疵。 此值可重现该效果，通过定义光的反射清晰度或广度，控制曲面在其反射中出现的平滑度或粗糙度。 粗糙度较低的材质会产生锐利的镜面反射。 相反，具有较高粗糙度的材质会产生柔和且模糊的反射。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness01.png" alt=""/><br><em>Specular粗糙度= 0.1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness05.png" alt=""/><br><em>Specular粗糙度= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness08.png" alt=""/><br><em>Specular粗糙度= 0.8</em></td>
  </tr>
</table>

请注意，这与总的光反射量无关 — 它只是衡量光是以非常聚焦的方式还是以漫射的方式反射。

**IOR（折射率）**

IOR描述材料与光的相互作用程度，既控制光线进入材料时如何弯曲（折射），又控制光线如何反射，特别是在浅视角（掠射）下如何反射。 反光度较低的表面（如水或某些塑料）具有低的IOR。 反射性更强的表面 — 如玻璃或某些宝石 — 将具有更高的IOR和更强的折射效果。 材料的IOR是一个物理值，因此它是一个客观的数字，而不是一个艺术解释的问题。 在创建给定素材时，您只需查找素材的IOR，并确保其设置正确，以确保素材与光线正确反应。 有一系列信息源可以在线列出各种材料的IOR。 例如，花岗岩的IOR是1.43；如果您正在创建花岗岩材料，则应输入此值作为其IOR，这将确保光线以真实的方式反射您的材料。 请注意，印度洋地区与金属材料无关（见下面的“金属性”）。 更改金属材料的IOR值不会影响其外观。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR1.png" alt=""/><br><em>IOR = 1.1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR15.png" alt=""/><br><em>IOR = 1.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR2.png" alt=""/><br><em>IOR = 2.0</em></td>
  </tr>
</table>

**各向异性**

当微观表面变化沿同一方向排列时，如沟槽一样，材料的反射将趋向于依赖于观察方向并垂直于沟槽伸展。 这些沟槽越对齐，效果越明显。 材料的各向异性值定义曲面的反射在所有方向上是否显示相同，或者它们是否以特定方式伸展。 这可能会重现金属笔刷等材料的效果，例如，沿着“画笔效果”的反射要长得多。 当用指纹涂抹抛光表面或者当拉伸诸如干燥皮肤的可变形表面时，也可以以更细微的方式发生各向异性反射。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy0.png" alt=""/><br><em>各向异性= 0.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy05.png" alt=""/><br><em>各向异性重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy1.png" alt=""/><br><em>各向异性重量= 1.0</em></td>
  </tr>
</table>

**切线各向异性**

当存在一定程度的各向异性（即材料的各向异性值大于0）时，各向异性切线指示沟槽的主方向。 反射将垂直于该方向延伸。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentGreen.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentOrange.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentRed.png" alt=""/></td>
  </tr>
</table>

*各向异性切线的不同方向。*

+++

### 几何体

OpenPBR还包括影响材料与几何形状相互作用方式的参数，如不透明度和薄壁行为。 这些控制决定一个表面应被视为具有物理Thickness还是薄壳，这对于纸张、树叶、窗户或织物等材料尤其重要

+++几何参数

* **薄壁**：启用薄壁后，从微观上看，材料很薄。 光线被认为是在没有可见折射的情况下穿过材料的。
* **不透明度**：确定是否可以透过素材部分或完全查看内容。 请注意，虽然“传输”参数定义了材料的透明度，但“不透明度”参数可用于定义网格划分 — 本质上，是用来创建孔的“移除”材料信息。

+++

### 基底图层

在OpenPBR模型的底部，基底层代表光与表面材料本身之间的基本相互作用。 基底层由四个特性定义：基底重量、基底颜色、金属度和扩散粗糙度。

<table>
  <tr style="border: 0;">
    <th style="border: 0;"><img src="../assets/openpbrf/renders/base/basecolor/baseColorYellow.png" alt=""/></th>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/></td>
  </tr>
</table>

*黄色介电和金属材料并排。*

+++基本图层特性

* **基色**：基本定义基色的强度（如下所示），范围从0到1，值为0时主要使用黑色素材（无颜色），值为1（尽可能使用最强的红色、绿色和蓝色光线的组合）。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight0.png" alt=""/><br><em>基准重量= 0.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight05.png" alt=""/><br><em>基准重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight1.png" alt=""/><br><em>基准重量= 1.0</em></td>
  </tr>
</table>

* **基色**：用于确定材质的“主色”，并设置金属基色和漫射（非金属）基色的反照率，即红色、绿色和蓝色的反射量。 如上所述，虽然基色决定反射的颜色，但基色权重设置决定此反射的强度。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorGreen.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorViolet.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorYellow.png" alt=""/></td>
  </tr>
</table>

* **金属度**：定义在0-1标度（0 =电介质，1 =完全金属和不透明）上材料的行为是非金属（电介质）还是金属。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness05.png" alt=""/><br><em>金属度= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1.png" alt=""/><br><em>金属度= 1.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/><br><em>金属度= 1.0，基色为黄色</em></td>
  </tr>
</table>

* **漫射粗糙度**：定义材料的微观表面粗糙度，范围从0（具有非常光滑、均匀的反射）到1（具有非常粗糙的漫射反射），适用于岩石或树皮等材料。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughness0.png" alt=""/><br><em>扩散粗糙度= 0.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughness1.png" alt=""/><br><em>扩散粗糙度= 1.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughnessSplit.png" alt=""/><br><em>0.0与1.0的并排</em></td>
  </tr>
</table>

+++

### 次表面

![](../assets/openpbrf/renders/sss/radius/SSSRadius10_vers2.png){width="250"}

*使用地下通道的材质。 请注意手部和其他细网区域中的半透明。*

+++次曲面参数

* **次表面重量**：这定义了使用多少次表面散射 — 本质上，是多少光进入材料。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/TransmissionWeight0.png" alt=""/><br><em>重量= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/SSSWeight05.png" alt=""/><br><em>重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/SSSWeight1.png" alt=""/><br><em>重量= 1.0</em></td>
  </tr>
</table>

* **子表面颜色**：定义从素材表面下方重新出现的任何光线的整体颜色。 较亮的颜色通常会产生更明亮、更明显的散射；此处的黑色值将导致完全没有次表面散射效果。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorYellow.png" alt=""/></td>
  </tr>
</table>

* **次表面半径**：定义在散射或吸收之前，光线在素材中可以传播的距离。 如果使用较低的值，则光线仅会传播很短距离；因此，材质外观会比较密集。 使用较大的半径时，光线可以传播得更远；材质将具有柔软、蜡质和半透明的外观。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius1_vers2.png" alt=""/><br><em>半径= 1</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius10_vers2.png" alt=""/><br><em>半径= 10</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius20_vers2.png" alt=""/><br><em>半径= 20</em></td>
  </tr>
</table>

* **子表面半径比例**：控制平均自由路径的颜色通道依赖性。 换句话说，光在被吸收或散射之前，在每个RGB通道中独立地通过材料的距离。 这产生了在地下材料中可见的特征颜色变化：在网格的较薄区域（其中光传播较短距离）中，颜色向具有最长半径的通道偏移。

默认值(1， 0.5， 0.25)表示红光传播最深，其次是绿色，然后是蓝色，这与许多真实世界地下材质（包括皮肤）的行为非常匹配。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleDefault.png" alt=""/><br><em>半径比例=默认值</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleGrey.png" alt=""/><br><em>半径比例=灰度</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleWhite.png" alt=""/><br><em>半径缩放=白色</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleYellow.png" alt=""/><br><em>半径比例=黄色</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleBrown.png" alt=""/><br><em>半径缩放=棕色</em></td>
  </tr>
</table>

* **次表面各向异性**：定义光线在次表面材质内偏好散点的方向。 值为0时，光照将在所有方向均匀散点。 如果为正值，光线将趋向于向前散点，方向与初始光线相同；这通常会使材质外观更清晰、半透明。 在负值下，光线将趋向于向后散点到光束的来源；这通常会使材质看起来更不透明、更密。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy-1.png" alt=""/><br><em>各向异性= -1</em></td>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy0.png" alt=""/><br><em>各向异性= 0</em></td>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy1.png" alt=""/><br><em>各向异性= 1</em></td>
  </tr>
</table>

+++

### 透射

透射控制穿过材质的光量。 与次表面不同，透射控制穿过对象的光线总量，而次表面控制从对象内部反射回表面的光线的总量。

![](../assets/openpbrf/renders/transmission/color/transmission_orange.png){width="250"}

*具有橙色透射颜色的高透射性材料的示例。*

+++传输参数

* **重量**：控制穿过素材表面的光量。 通常用于液体或玻璃等透明材料。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight0.png" alt=""/><br><em>重量= 0.0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight05.png" alt=""/><br><em>重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight1.png" alt=""/><br><em>重量= 1.0</em></td>
  </tr>
</table>

* **颜色**：确定通过素材的光线的颜色。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_green.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_orange.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_purple.png" alt=""/></td>
  </tr>
</table>

* **深度**：以厘米为单位定义在透射色达到完全饱和之前，光线穿过材质所需的距离 — 本质上，是光线穿过透明（或部分透明）材质时拾取颜色的速度。 对于传输深度较低的材料，光线将很快拾色，这意味着即使材料的很薄部分看起来也是颜色强烈的。 相反，如果高的深度，较粗的部分看起来很暗或几乎不透明，并且材料具有“浓缩”外观，如彩色树脂或浓液体。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth0.png" alt=""/><br><em>深度= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth1.png" alt=""/><br><em>深度= 1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth10.png" alt=""/><br><em>深度= 10</em></td>
  </tr>
</table>

* **散点颜色**：此选项用于定义在透明或部分透明的素材中散射的光线的颜色和强度。 它实质上定义了材料的内部“混浊度”，决定了光线在材料内的扩散和软化方式。 散点可用于重现光线不能干净或沿直线传播的材料，例如某些塑料、牛奶或阴沉的苹果汁，甚至可用于重现大量的水（例如，创建海洋的蓝色调）。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterDarkGrey.png" alt=""/><br><em>深灰色散点</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterMiddleGrey.png" alt=""/><br><em>中间灰色散点</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterWhite.png" alt=""/><br><em>白散点颜色</em></td>
  </tr>
</table>

* **各向异性**：用于确定光线在素材内部的散点方向。 值为0时，光照将在所有方向均匀散点。 如果为正值，光线将趋向于向前散点，方向与初始光线相同；这通常会导致材料具有更清晰、更类似玻璃的外观。 在负值下，光线将趋向于向后散点到光束的来源；这通常会使材质呈现毛砂或粉笔质感更强的外观。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy-1.png" alt=""/><br><em>各向异性= -1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy0.png" alt=""/><br><em>各向异性= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy1.png" alt=""/><br><em>各向异性= 1</em></td>
  </tr>
</table>

>[!NOTE]
>
> 各向异性取决于光方向，因此这种散射的结果将随光源的放置位置（相对于所照明的材料）而变化。

* **色散(Abbe)**：此选项用于定义当光线通过透明材料时，光的不同颜色会弯曲多少，从而导致了分色、彩虹状条纹或折射光中的彩色边缘。 色散(Abbe)值为0时，将完全禁用此效果。 低色散(Abbe)值将导致非常可见的颜色分离（就像您在棱镜中看到的那样），而高色散(Abbe)值将导致较弱或可忽略的颜色分离，以及整体上更清晰、更清晰的折射。 (色散(Abbe)参数以19世纪物理学家兼光学工程师Ernst Abbe命名。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/abbe/transmissionAbbe20.png" alt=""/><br><em>阿贝= 20</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/abbe/transmissionAbbe45.png" alt=""/><br><em>阿贝= 45</em></td>
  </tr>
</table>

* **传输色散**：与其他地方的粗细参数一样，此值定义了材料中光色散的强度。 这种情况在高对比度折射的边缘最为明显。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale0.png" alt=""/><br><em>传输色散= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale05.png" alt=""/><br><em>传输色散= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale1.png" alt=""/><br><em>传输色散= 1.0</em></td>
  </tr>
</table>

+++

### 发光

发射控制材料是否发射自己的光（与反射光无关），并允许您设置发射光的颜色和强度。

![](../assets/openpbrf/renders/emission/color/emissionColorGreen.png){width="250"}

*亮绿色发射材料。*

+++排放参数

* **明亮度**：定义从素材发射的光线的亮度，以cd/m²为单位，也称为nit。 此测量假定为白光；更改光线的颜色（请参阅下文）可能会影响整体亮度。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance100.png" alt=""/><br><em>明亮度= 100</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance400.png" alt=""/><br><em>明亮度= 400</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance1000.png" alt=""/><br><em>明亮度= 1000</em></td>
  </tr>
</table>

* **颜色**：确定素材发射的光颜色。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorYellow.png" alt=""/></td>
  </tr>
</table>

+++

### 薄膜

![](../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness05.png){width="250"}

*具有薄膜图层的深色基础材质。*

+++薄膜参数

* **粗细**：与其他位置的Weight参数一样，此选项可控制薄膜效果的强度，其值介于0和1之间。 越接近0，任何薄膜效果几乎看不见；在该范围的上端，效果越明显。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight0.png" alt=""/><br><em>重量= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight05.png" alt=""/><br><em>重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight1.png" alt=""/><br><em>重量= 1.0</em></td>
  </tr>
</table>

* **Thickness**：定义胶片图层的Thickness（以微米为单位）。 在物理上精确的材料中，大多数薄膜效果发生在0到1微米之间的Thickness。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness0.png" alt=""/><br><em>Thickness= 0</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness05.png" alt=""/><br><em>Thickness= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness1.png" alt=""/><br><em>Thickness= 1.0</em></td>
  </tr>
</table>

* **折射率(IOR)**：如上所述，素材的IOR决定了素材与光的反应程度。 OpenPBR材料的薄膜层具有其自身的IOR。 例如，菱形的IOR为2.417。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR1.png" alt=""/><br><em>IOR = 1</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR15.png" alt=""/><br><em>IOR = 1.5</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR2.png" alt=""/><br><em>IOR = 2</em></td>
  </tr>
</table>

+++

### 涂层

![](../assets/openpbrf/renders/coat/color/coatColorPurple.png){width="250"}

*低粗糙度的紫色外套图层。*

+++涂层参数

* 粗细：基本上决定皮层的强度。 将此值设置为最小值0会完全禁用涂层；值越高，图层的强度越大。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight0.png" alt=""/><br><em>重量= 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight05.png" alt=""/><br><em>重量= 0.5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight1.png" alt=""/><br><em>重量= 1.0</em></td>
  </tr>
</table>

* 颜色：确定“涂层”图层的整体颜色，这可以对下方基底图层的反射进行着色。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorYellow.png" alt=""/></td>
  </tr>
</table>

* 变暗：确定基底层的反射被变暗和饱和的程度。 例如，如果进行清漆，经过清漆的木材通常比相同的木材显得更暗；变暗特性可以重现这种效果。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening0.png" alt=""/><br><em>调暗= 0</em></td>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening05.png" alt=""/><br><em>变暗= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening1.png" alt=""/><br><em>调暗= 1.0</em></td>
  </tr>
</table>

* 折射率(IOR)：实质上是根据光线在涂层内的行为方式，非金属表面如何呈现反射效果的数值定义。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR14.png" alt=""/><br><em>IOR = 1.4</em></td>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR2.png" alt=""/><br><em>IOR = 2</em></td>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR3.png" alt=""/><br><em>IOR = 3</em></td>
  </tr>
</table>

* 粗糙度：如讨论基底层时提到的，表面粗糙度定义了表面的反射方式 — 光滑表面非常均匀地反射光，而粗糙表面在随机方向散点光。 “涂层”图层将具有其自己的粗糙度。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness01.png" alt=""/><br><em>粗糙度= 0.1</em></td>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness05.png" alt=""/><br><em>粗糙度= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness08.png" alt=""/><br><em>粗糙度= 0.8</em></td>
  </tr>
</table>

>[!NOTE]
>
> 请注意，即使Base层很光滑（即，其Roughness值接近0），Coat层的粗糙度也可能会使整体材料显得更粗糙。

* 各向异性：各向异性描述涂层反射如何随方向变化，从而使高光沿表面拉伸或对齐，而不是显示为圆形。 此效果用于表示涂层中的定向表面结构，如刷涂、划痕或流型。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy01.png" alt=""/><br><em>各向异性= 0.1</em></td>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy05.png" alt=""/><br><em>各向异性= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy1.png" alt=""/><br><em>各向异性= 1.0</em></td>
  </tr>
</table>

* 相切各向异性：由于上述各向异性值而出现的任何拉伸或条纹的方向。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent0-orange.png" alt=""/><br></td>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent03-darkRed.png" alt=""/><br></td>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent06-green.png" alt=""/><br></td>
  </tr>
</table>

*各向异性切线的不同方向。*

* 正常涂层：涂层可以发生不同程度的变形，从而产生细微的几何形状。 例如，该功能可用于重现材质上的划痕或雨滴外观。

+++

### 绒毛

![](../assets/openpbrf/renders/fuzz/color/fuzzColorYellow.png){width="250"}

*此示例说明颜色为黄色的模糊在倾斜角度时最明显。*

+++模糊参数

* **粗细**：与其他地方的粗细参数一样，此选项可控制模糊效果的强度，使用介于0和1之间的值。 设置为0时，模糊图层将完全禁用。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight0.png" alt=""/><br><em>重量= 0.0</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight05.png" alt=""/><br><em>重量= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight1.png" alt=""/><br><em>重量= 1.0</em></td>
  </tr>
</table>

* **颜色**：确定模糊效果的颜色。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorYellow.png" alt=""/></td>
  </tr>
</table>

* **粗糙度**：基本上决定此图层内“模糊粒子”的形状。 当该值接近0时，粒子高而细；当从浅（掠过）角度查看曲面时，它们更明显。 在较高的值下，颗粒会变得更接近球形；它们从更宽的角度范围内更容易看见，并且表面整体会变得更粗糙。

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness01.png" alt=""/><br><em>粗糙度= 0.1</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness05.png" alt=""/><br><em>粗糙度= 0.5</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness1.png" alt=""/><br><em>粗糙度= 1.0</em></td>
  </tr>
</table>

+++

## 创建素材的最佳做法

本节重点介绍使用现代统一的PBR模型（如OpenPBR）创建性能稳定、可预测的材质，这些材质可在光照条件、场景和工具之间表现出色。 也就是说，以下许多建议一般适用于制作溴化阻燃材料；但少数建议仍取决于OpenPBR材料的特定特征集。

### 从真实参考资料开始

基于物理的材质基于真实世界的观察时最可靠。 尽可能地基础材质对摄影参考、测量值或类似表面的直接观察做出决定。 这不仅适用于颜色，也适用于粗糙度、反射率和表面变化。 根据参考操作有助于将材质锚定在合理的范围内，从而使其更易于重复使用且对光照或环境变化不那么敏感。 这样还可以降低对素材本身内部的照明问题进行补偿的诱惑。

### 对材料的物理结构有一个心理模型供作者参考

OpenPBR不仅仅是一个参数列表，艺术家可以对这些参数列表进行微调，直到获得想要的外观。 其核心依赖于“OpenPBR材料层概述”中描述的基础结构，该结构假定材料由类似的物理分层结构组成。 因此，在考虑到这种模型的同时，编写材料是明智的，并以OpenPBR参数来描述这些材料的物理元素。 考虑一下材料的构成吧 — 垂直切片在显微镜下会是什么样子，颜色和亮部来自哪里，等等。 尽可能多地尝试预期需要哪些OpenPBR组件才能实现这种期望的外观。 同样，也可以尝试另一种方法 — 即从一组图层构建一种材质，并发现其最终外观。

### 独立于光照创作材质

PBR工作流程的一个关键优势是区分材质和光照之间的顾虑。 素材应描述表面属性，而不是补偿场景光照、曝光或氛围。 旨在创造在多种光照条件（甚至恶劣的光照）下都保持稳定且可信的材质。 这种分离使场景更易于管理、调试和迭代，特别是在可能需要不同艺术家处理材质和光照的较大管道中。 通过一系列上下文验证材质可能非常有用。 在不同光照环境、天平和相机角度下，精心创作的素材应可以撑住。 如有可能，在多个上下文中预览素材 — 例如，在中性摄影棚照明下和较戏剧化的场景中。 这有助于揭示素材的外观是否真正基于其参数，或者它是否依赖于特定设置来看起来正确。 在上下文中经过良好验证的材质更易于重复使用，并且在生产中更可靠。

### 尽可能保持参数解耦

现代的PBR工作流程旨在最小化参数之间的隐藏相关性。 调整粗糙度、金属量或透射率等值时，目标应仅影响材料外观的特定方面。 在实践中，这意味着：

* 除非有明确的物理对齐，否则避免从单个纹理驱动多个视觉效果。
* 与紧密互连的网络相比，更偏爱简单、可读的参数设置。
* 以增量方式作出更改，尽可能单独评估其影响。 此方法使材质更易于理解、更易于调试，并且当在其他环境中重复使用时更可预测。

### 有意使用图层

分层材料功能强大，但也会增加复杂性。 每增加一个图层都会增加视觉和计算成本，并使得材质更难讲理。 分层时：

* 使用层来表示实际的表面结构（例如，Dust或材料顶部的Dirt）。
* 避免栈叠可产生类似视觉效果的图层。
* 定期评估图层是否对最终外观做出有意义的贡献。 捕捉表面基本特征的简单材料通常比难以控制的高层材料更稳健。

### 注意性能、噪音和稳定性

某些素材特征和组合本质上更昂贵或容易产生噪点，尤其是在路径跟踪渲染器中。 材质中使用的特性越多，渲染成本可能越高。 亚表面、高粗糙度结合传输、多层效果、各向异性或色散都会增加渲染时间和方差。 虽然这些功能很有价值，但使用时应该谨慎小心 — 具体取决于艺术家的设置，它们可能会产生过多的噪点、不稳定或长时间的渲染时间。 了解使用高级功能的成本，并在这些功能提供明确视觉价值的情况下使用这些功能非常重要。

### 有意偏离物理合理性

虽然在物理上看似合理的数值提供了一个强有力的基准，但生产现实有时需要有意的偏离。 风格化、可读性、艺术方向或技术约束可能使将参数推到超出实际范围的范围是合理的。

根据具体项目、素材和艺术意图，具体情形会大相径庭，而承认这些时刻本身就是一个判断问题，而不是遵守规则的问题。 重要的是偏离是有意和有目的的：你明白自己背离了什么物理原理，以及为什么这样做对工作有益。

其目的不是破坏物理原理，而是为了达到一个明确的艺术或技术目标，有意识地扭曲物理原理。

## 常见问题以及如何避免它们

### 思考预设而不是光线行为

在基于物理的工作流程中一个常见的缺陷是将材料视为预定义的“外观”，而不是作为光线行为的描述。 这通常显示为严重依赖预设或复制参数值，而不理解它们所代表的含义。

OpenPBR围绕显式的光相互作用 — 反射、透射、散射、吸收和发射。 当素材看起来不正确时，最有效的故障排除方法是确定这些行为中的哪些，并直接进行调整。 与循环切换预设或栈叠效果相比，这样可以做出更清晰的决策，获得更可预测的结果。

### 使用Specular粗细而非Specular粗糙度

要控制材料的反射率，可以先调整“Specular粗细”来进行控制，但更建议的是调整“Specular粗糙度”参数。

所有材料都有Specular反射，在掠入射角时Specular反射总是趋向于100%。 此外，大多数介电（非金属）材料具有非常相似的Specular反射，在垂直入射时在2%到8%之间。 视觉反射率差异的主要原因在于材料的微观几何结构；这由Specular粗糙度参数定义。

但是，“Specular粗细”仍然很有用，可以用作局部调整折射率、模拟微遮蔽导致的反射率变化或后期艺术调整的速记。

### 混淆传输、透明度和次表面散射

光通过效果通常松散地分组在“透明”或“半透明”下，但OpenPBR可以清楚地区分它们。 透射是指穿过材料并出射到另一侧的光线，如玻璃、水或透明塑料中看到的光线。 次表面散射描述进入材料、内部散射和在不同点出射的光，从而产生柔和的阴影和内部颜色。

在物理层面上，有两个现象在起作用：散射，使牛奶呈现白色的效果，以及吸收，使咖啡呈现黑色。 当散射很小或没有散射时，体积看起来更透明，透射率是需要考虑的关键特征。 当存在大量散射时，体积趋向于更具反射性，而次表面是一个关键特征。 通过把参数推到极值，可以使地下表面变得透明，使透射看起来不透明，但效率会非常低。

在传输更合适的位置使用次表面散射（反之亦然），可能导致材料过于复杂且渲染效率低下。 OpenPBR会分离这些行为，以便艺术家可以选择最匹配其引用的行为，或者在需要时有意组合这些行为。

### 添加没有明确视觉动机的特征

由于OpenPBR暴露出广泛的材料行为 — 包括涂层、朦胧、薄膜效果、次表面散射和发射 — 所以最好一次启用多个功能。 在没有明确参考驱动原因的情况下添加时，这会使素材更难控制，并在视觉上产生噪点。

一种更可靠的方法是从与观察到的表面或体积行为匹配的最简单的材料开始，然后仅在缺少特定视觉提示时才增加复杂性。 每个附加特征应对应于参照中可见的内容，如边缘处的纤维或体积内的颜色变化。

### 适用于单个光照设置的创作材质

基于物理的工作流程旨在减少材质和光照之间的依赖关系，但仅在特定设置下将材质调整为看起来正确时，则会出现问题。 如果某种材料需要特定的光线强度或角度才能看起来可信，它通常只是补偿光照，而不是描述材料本身。

测试各种光照条件下的材质可以揭示它们是耐用的还是过度依赖场景的。 考虑到此灵活性而创作的材质往往会更顺畅地跨不同环境和项目集成。

### 使用无参照的极端参数值

尽管OpenPBR参数是按物理含义建立的，但将它们推至无明确目的的极端值会导致不稳定或混淆结果，尤其是在光照发生变化时。 当素材的行为无法预测时，将参数选择与真实参考进行对比，可以帮助确定问题是出于艺术意图还是参数滥用。 将参考线作为基准线可使材质在整个项目中更易于诊断、优化和维护。

### 误解模型的局限性

并非所有材质都可以用OpenPBR来表示。 和任何材质模型一样，OpenPBR只是一个模型。 尽管它已经拥有相当丰富的特色，但与现存或人们所能想象到的巨大而丰富的材料相比，它仍然粗糙。 模型可以开箱即用的表示材料，一些需要更多经验来构建，将模型拉伸到极限，还有一些仍然是模型无法表示的。 在某些情况下，熟练的艺术家仍然可以通过一些“作弊”获得不错的结果；这通常是在做出非身体选择的时候。 但了解模型能做什么和不能做什么，以及何时需要替代解决方案，如更简单的材质或专用着色器，是非常重要的。

### 期望材质模型解决渲染问题

并非所有视觉问题都源自素材本身。 光照、取样或渲染器设置（而不是OpenPBR素材定义）可能会导致杂色、收敛缓慢或着色伪影。

虽然OpenPBR可提供物理上一致的材质模型，但它并不取代对适当光照和渲染配置的需求。 隔离变量（例如，在简化光照下测试素材）有助于确定问题是否存在于素材或其他地方。

### 将预设用作学习工具，而不是最终答案

最好将“OpenPBR预设”理解为“参考工具”和“学习工具”。 检查预设值（如金属度、粗糙度、各向异性或传输深度）有助于明确具体视觉结果的构建方式。

依赖预设作为最终解决方案可能会掩盖素材的实际运作方式。 使用这些模板作为起点或分析示例有助于加深理解并创造更具有适应性的材料。

## 参考和附录

### 参考文档

有关权威定义、实施细节和技术重点规范，请参阅以下来源：

* [学院软件基金会 — OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/)
* [AutodeskOpenPBR文档(Arnold)](https://help.autodesk.com/view/ARNOL/ENU/?guid=arnold_user_guide_ac_surface_shaders_ac_open_pbr_html)
* [MaxonOpenPBR文档](https://help.maxon.net/r3d/3dsmax/en-us/Content/html/Material+OpenPBR.html#StandardMaterial-Base)

应将这些资源作为技术准确性和具体实施行为的主要参考资料。

## 附录一：PBR是什么？

物理渲染(PBR)是一种围绕一个简单想法构建的渲染方法：材质应以与真实世界表面行为一致的方式响应光线，而不是依赖于特定的光照设置。 PBR材料专为在多种环境中都可信任而创作，使其更可预测、可重复使用且更易于在现代生产管道中管理。

这种真实世界基础的一个直接后果是PBR工作流程允许艺术家根据实际测量值复制现实，而不是试图猜测其最佳近似值。 在光照中，这可能意味着使用物理单位和真实世界的强度，而不是任意值。 在与拍摄内容或影片内容集成的渲染工作流程中，基于物理环境的相机和着色器可帮助保留真实镜头和传感器的视觉特性。 对于材料，相同的原理支持摄影测量等技术，其中扫描的表面可以与手动创作的材料无缝混合，因为使用相同的物理假设来描述两种材料。

对于艺术家，PBR在工具、引擎和渲染器之间提供共享的视觉语言。 使用PBR原理创建的素材旨在看起来连贯一致，无论是在实时引擎、路径跟踪渲染器中查看，还是在明显不同的光照条件下查看 — 而无需持续手动调整。 这种一致性是PBR成为游戏、VFX和可视化标准的关键原因。

PBR的核心是一些关于光和表面的基本物理思想。 光被看作是反射、散点或被表面吸收的能量，而着色器被设计来节约能量，使材料不会出现不自然的明亮或反射。 表面形貌受微观粗糙度等因素的影响，这些因素对反射的尖锐或柔和程度都有影响。 PBR工作流程也清晰地区分金属和非金属，因为这些材料类型与光的相互作用方式截然不同。 PBR依赖于描述物理属性的参数，如基色、粗糙度和金属度，着色器将使用物理推导出的模型进行解释。

同样重要的是，PBR提高了渲染过程不同部分之间的低互依性。 通过将素材定义与光照分离，艺术家无需在每次光线变化时“修复”素材。 这种划分可以将复杂的问题转变为更小、更易于管理的问题：光照可以独立于材质进行调整，材质可以在不知道最终场景设置的情况下创作。 在更细微的尺度上，现代的PBR模型（包括OpenPBR）旨在保持参数尽可能独立，使艺术家能够单独调整值，而不会导致意外的副作用。

在实践中，PBR将艺术家的角色从补偿光照或渲染器古怪，转变为根据现实世界特征描述材质。 结果就是一种优先于场景特定微调的工作流程，从明确的素材输入中自然而然地呈现真实感，而不是手工制作的光照技巧。

有关PBR技术细节的详细信息，请参阅[PBR指南，作者：Wes McDermott](https://www.adobe.com/learn/substance-3d-designer/web/the-pbr-guide-part-1)。

## 附录二：什么是OpenPBR？

OpenPBR是一种开放的、基于物理的表面着色模型，旨在提供一致且可预测的方式来描述跨3D工具、渲染器和管道的材质外观。 它定义了一个单一、全面的材质模型，可以表示广泛的真实世界表面，同时仍然保持使用物理上有意义的参数描绘更奇特的或艺术上习惯的表面的灵活性。

OpenPBR的核心目标是解决3D工作流程中长期存在的问题：工具和渲染器之间的材质不一致。 历史上，艺术家使用过多个“标准”着色器，这些着色器在精神上行为类似，但在细节、参数含义和物理假设上有所不同，具体取决于使用的软件或渲染器。 即使两个着色器对“粗糙度”或“金属度”等参数共享相同的名称，结果也不总是是一致的。 这使得在工具之间移动资源、在团队和工作室之间进行协作或在复杂管道中保持视觉连续性变得困难。

这些限制在3D社区中随处可见，艺术家、工作室和开发人员开始寻找解决方案。 最初的方法各有不同，整个社区的这一持续努力逐渐趋同于共同解决方案。 这项工作，以及围绕这项工作的许多讨论和联合决定，是在一种创造材料的统一方法下正式确立的：OpenPBR，一种通用的公开文档的材质模型，可以跨应用程序一致地实施，而不是与单个软件绑定，OpenPBR建立在不同的工具可以构建的共同基础之上，同时保留相同的底层物理行为。 这一通用模型使艺术家可以在应用程序之间转移素材，使工作室可以标准化外观开发做法，并且使资源在制作过程中保持视觉上的稳定。 最重要的是，OpenPBR从根本上说是一种共识；即使在今天，讨论仍在进行，并且在决策时也寻求来自3D部门众多专家的共识。

模型本身是基于物理渲染(PBR)原则的。 这意味着材料是以光线与真实世界中的表面相互作用的方式来描述的，重点在于节能以及对光照的可预测响应，参数植根于真实世界的光学，这些参数的组织和曝光方式支持实际外观发展而不是科学模拟。 即，OpenPBR定义了素材本身的行为 — 参数的含义、不同图层交互的方式，以及素材在光照下的响应方式。 单个软件工具可以自由地以不同的方式展示这些控件，使用任何看起来最合适的UI样式，只要基础材质模型保持一致即可 — 尽管实际上，参数的命名、分组和排序背后有一个逻辑，而特定应用程序通常倾向于遵守这一点。

## 附录三：OpenPBR倡议的背景和动机

要理解OpenPBR为什么存在，不妨研究一下在过去十年中基于物理的着色是如何演变的。 随着PBR成为行业标准，大多数主要的3D工具都引入了自己的表面着色器。 这些着色器的目的大致相似：它们旨在使用节能反射模型表示真实世界的材料，并以艺术意义的方式将参数暴露给底层物理模型，如底色、粗糙度、金属度等。

这需要多次迭代，而且3D景观最初非常零散，各个利益相关者探索不同的方式来表达视觉效果，并在不同的方面取得进展。 一个解决方案将被另一个解决方案取代，直到具体的方法变得优越，各个领域的工作开始趋同，导致GGX、金属粗糙材料方法的出现，并最终导致OpenPBR。

与此同时，生产管道也变得更加互联了。 在建模、添加纹理、外观开发、照明、渲染和实时使用等应用程序之间移动所需的资产越来越多。 工作室开始更多地依赖标准化交换格式，例如美元和MaterialX，并且很明显，允许特定材料描述移动的格式也将有利。

该OpenPBR倡议是为应对这些挑战而设立的。 它代表Adobe与Autodesk之间在学院软件基金会(ASWF)支持下的合作努力，目的是定义一个单一的开放表面着色模型，作为跨工具的共享参考点。 OpenPBR整合和形式化艺术家已熟悉的基于物理的渲染概念；这些概念然后形成具有清晰定义行为的统一模型的基础。

OpenPBR背后的一个关键动机是一致性。 此处的目标是确保使用OpenPBR描述的素材在任何实施时都能以可预知的方式表现，同时不牺牲艺术控制或创意灵活性。 当艺术家调整粗糙度、金属度或Specular响应时，预期这些更改将在合规性实现中具有相同的视觉含义。

另一个重要的动机是耐用性。 通过作为行业标准公开指定和管理，OpenPBR旨在随时间不断变化，而不受单个产品或公司的生命周期或优先级限制。 这使得其成为长期资源创建的一个更稳定的基础，特别是对于工作室和艺术家，他们希望其素材在工具更改时保持可用和相关性。