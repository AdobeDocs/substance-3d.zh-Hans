---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/3d-applications/blender/troubleshooting.html"
breadcrumb-title: ''
description: 使用系统控制台诊断并解决Blender中Substance 3D插件的常见问题。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 故障排除
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---


# 故障排除

系统控制台可用于诊断使用插件时遇到的错误。 混合器的系统控制台窗口会根据您的操作系统以不同方式打开。 有关详细说明，请按照Blender系统控制台[文档页面](https://docs.blender.org/manual/en/2.79/advanced/command_line/introduction.html#console-window-status-and-error-messages)上的步骤进行操作。 遇到意外问题（例如纹理未加载或材质在处理过程中卡住）时，控制台输出很有帮助。

要报告错误，请加入[SubstanceDiscord服务器](https://discord.com/invite/substance3d)上的#substance-blender-beta频道或访问[Adobe群](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-blender)。 控制台日志中的相关信息以及针对该问题的任何复制步骤都可以包含在报告中。

## 常见问题和解决方案

* *与WMIC相关的控制台错误。*
  * *有时，Windows安装将不包括WMIC，在这种情况下，这是必需的。 以下是手动修复此问题的方式：*
    * 转到“设置 — 系统 — 可选功能”
    * 选择“查看功能”，然后选择“添加选项功能”
    * 此时将显示一个新窗口，向下滚动列表以查找WMIC，勾选复选框，然后按“下一步”，在下一个窗口中按“添加”。
    * 您现在应该看到一个新窗口，其中显示最近操作下WMIC安装的进度。
    * *请注意，下载该文件可能需要几分钟时间。 之后，重置计算机，并重新启动Blender和附加。 在Substance 3D面板中单击加载时，现在应显示文件浏览器窗口。*
  * 如果这不能解决问题，您可能还需要在PATH变量中定义WMIC。 请参阅适用于您特定版本的Windows的文档。
* *在更新插件并加载素材后，并非所有设置都显示在Substance 3D面板中。*
  * 如果在同一会话中移除较旧版本的加载项并安装较新版本，则可能会发生这种情况，因为较旧的文件可能仍会缓存在系统中。\
    重新启动Blender应使更改生效。
* *安装加载项时出现问题。/材料停滞在会话之间的处理中。 /材质无法在会话之间生成纹理。 /加载.sbsar文件时出错。*
  * 这可能是一个与安装集成工具有关的问题，通常可以通过手动删除工具来修复该问题。 访问[卸载加载项](../../../3d-applications/blender/uninstalling-the-add-on/uninstalling-the-add-on.md)页面，获取手动删除说明。
* *材质未在循环渲染视图中更新*。
  * 默认情况下，该插件不会更新Cycles渲染视图中的纹理。 但是，通过在加载项首选项中启用<b>循环自动更新纹理</b>，可以强制更新这些纹理。
* 在“循环”渲染视图中存储后，参数显示为要恢复的状态。
  * 这是搅拌器端的已知缓存问题，仅供查看。 存储时，不会向远程引擎发送任何消息以更新生成的纹理文件。 离开Cycles渲染视图并切换回该视图后，纹理将恢复正常。
* *材质在撤消/更改参数后不再更新。*
  * 撤消操作后，素材可能无法更新。 虽然参数将恢复到以前的状态，但纹理无法撤消以进行匹配。 要再次更新纹理，请使用“刷新”按钮将参数恢复为默认状态并重新加载纹理。
* *在Blender的拾色器中，以Substance Designer设置的颜色略有不同，颜色值也不相同。*
  * 混合器仅对混合器的拾色器的颜色应用灰度系数校正。 虽然这会导致拾色器不一致，但纹理中显示的颜色与Substance应用程序中设置的值准确。
* 在Windows中加载素材时，*出现“无法识别wmic”控制台错误。*
  * 当C:\Windows\System32\wbem\未包含在PATH系统变量中时，会出现此问题。 请参阅适用于您特定版本的Windows的文档。
* Mac上出现&#x200B;*“CPU类型错误，无法执行”错误。*
  * 当ARM Mac计算机上未启用Rosetta时会出现此问题。 有关详细信息，请参阅[Apple的Rosetta页面](https://support.apple.com/en-us/102527)。 此外，请参阅此[安装指南](https://medium.com/@jithmisha/fix-for-macbook-air-m1-m2-bad-cpu-type-in-executable-error-3719a0a1cb6)以获取进一步说明。
* *使用“刷新”按钮或更新参数时，对着色器图形的修改会撤消。*
  * 该加载项在更改或刷新之后刷新了图形中的连接。 要解决此问题，请复制从.sbsar创建的混合器材质，然后为您选择的新名称。 仅将节点添加到副本中。 纹理将在节点组中更新，同时保留用户添加的节点。 刷新时，复制这些节点，并在刷新后将其粘贴回新图形。
