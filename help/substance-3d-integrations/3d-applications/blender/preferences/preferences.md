---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/blender/preferences.html"
breadcrumb-title: ''
description: 在Blender中配置Substance 3D加载项偏好设置，以自定义增效工具行为和设置。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 首选项
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---


# 首选项

可以在Blender的首选项窗口中找到加载项首选项。 导航到编辑>首选项>加载项，然后搜索Node：Adobe适用于Blender的Substance 3D加载项。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![加载项首选项菜单的前半部分。](../../../assets/blender-prefs-1.png)

</td>
<td style="border: 0;" valign="top">

![加载项首选项菜单的后半部分。](../../../assets/blender-prefs-2-b.png)

</td>
</tr>
</table>

<b>卸载</b> — 从系统中删除加载项并将其从Blender中的加载项列表中删除。

<b>报告错误</b> — 打开Substance 3D for Blender Discord。

<b>接受工具文件夹</b> — 打开Blender文件浏览器，以选择Substance集成工具安装路径。

<b>打开工具</b> — 在“集成工具”文件夹位置打开系统文件浏览器。

<b>重置路径</b> — 将“集成工具”文件夹路径重置为默认位置。

<b>卸载工具</b> — 删除已安装的Substance 3D集成工具版本。

<b>更新工具</b> — 打开文件浏览器以选择工具zip文件并更新工具。

<b>文档</b> — 在浏览器中打开生态系统和插件文档页面。

<b>论坛</b> — 在浏览器中打开Adobe社区论坛。

<b>Discord服务器</b> — 在浏览器中打开生态系统和插件Discord服务器。

<b>拼贴</b> — 调整素材的X、Y和Z拼贴。 锁定可用于取消链接各个值并单独对其进行调整。

<b>分辨率</b> — 所生成纹理的默认分辨率。 锁可用于取消链接以单独设置其分辨率。

<b>应用类型</b> — 设置“应用”按钮的行为： <b>插入</b>将使用选定的Substance素材覆盖当前素材，<b>追加</b>将素材添加到新素材槽中的对象。

<b>导出图像格式</b> — 如果在Blender中生成的图像用作Substance素材的图像输入，可使用此格式将该图像保存到临时文件夹。

<b>默认折叠输入组</b> — 切换默认情况下Substance素材的输入组是展开还是折叠状态。

<b>默认情况下仅更新纹理</b> — 切换天气更新Substance参数只会影响Blender着色网络中的输出纹理。 禁用此选项将在调整参数后重置节点连接。 建议在向材料中添加其他节点时启用，否则在调整参数后会断开这些节点。

<b>Substance远程引擎</b> — 设置Substance远程引擎使用的硬件。

<b>自动应用素材</b> — 创建Substance素材时，自动将素材附加到新素材槽中的选定对象。

<b>自动突出显示所选对象的材质</b> — 如果选中具有该材质的对象，请在Substance 3D面板中更改突出显示的材质。

<b>循环自动更新纹理</b> — 在使用“循环”渲染视图时，强制在3D视口中更新纹理。

<b>移除预设删除确认</b> — 移除在删除素材预设时出现的确认窗口。

<b>启用伪用户创建素材</b> — 设置创建素材时启用或禁用“伪用户”。 即使没有使用数据，在关闭之后也不会清除标记为假用户的混合器数据。

<b>自动启动Substance远程引擎</b> — 在混合器启动时切换Substance远程引擎是否已初始化。 如果禁用此复选框，则远程引擎将仅在用户加载按钮或使用加载快捷键时启动。

>[!NOTE]
>
> 注意：如果使用Substance连接器，则SRE必须处于活动状态，发送应用程序才能将Blender检测为端点。

<b>SBSAR库路径</b> — 在加载按钮搜索Substance文件时默认打开的文件夹。

<b>临时文件夹</b> — 此文件夹将是首次保存文件之前存储纹理的默认位置。

<b>保存时将.sbsar文件复制到</b> — 启用此选项后，在保存文件时，会将.sbsar文件复制到指定的相对路径。 这有助于在设备之间共享项目。

<b>保存后，将纹理复制到</b> — 首次保存文件时，会将临时文件夹中的纹理复制到此位置。 $matname变量用于为每个素材创建子文件夹。

<b>着色器预设</b> — 设置从物质文件创建混合器材质时使用的默认着色器预设。 对于基于UV的映射，可将它们设置为标准；对于基于“框”、“球”和“圆柱”投影的映射，可将它们设置为标准。

<b>位移中级</b> — 默认值是位移节点中位移的基数。 值高于缺省值会将曲面向外推，而值低于缺省值会将曲面向内拉。

<b>位移比例</b> -位移节点中的默认比例值。

<b>发射强度</b> — 原则性BSDF节点中发射强度的默认值。

<b>投影混合</b> — 为投影方法着色器设置角度之间的混合量。

<b>AO混合</b> — 当环境遮蔽作为输出启用时，此值确定用于组合基色和环境色遮蔽的MixRGB节点的默认因子值。

<b>输出</b> — 可以启用或禁用素材的单个输出。 也可以调整各个输出的默认色彩空间、文件深度和颜色格式。

<b>快捷键</b> — 自定义用于显示浮动菜单、加载Substance素材和应用当前素材的快捷键。 快捷方式更新需要重新启动才能生效。
