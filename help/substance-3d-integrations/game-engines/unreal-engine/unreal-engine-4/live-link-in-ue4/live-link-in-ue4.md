---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/live-link-in-ue4.html"
breadcrumb-title: ''
description: 使用Unreal Engine 4中的Live Link在Painter和UE4之间实时同步Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Live Link in UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UE4中的Live Link
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# UE4中的Live Link

>[!WARNING]
>
> 不再支持Unreal Engine中的Live Link。 使用实时链接所在增效工具旧版本的用户仍然能够使用该功能。

>[!WARNING]
>
> Live Link不适用于UE4 BSP网格。 您发送的资源需要是导入到UE4项目的模型文件

## 正在建立到Substance Painter的链接

1. 打开Substance Painter
1. 在内容浏览器中右键单击要发送到Painter的资源，然后选择“发送到Painter”。

   ![](../../../../assets/link1-22.png){width="400px"}
1. 网格将以Substance Painter显示，您可以开始添加纹理。 在您工作时，纹理将发送到UE4并应用于素材。 工具栏中UE4图标上的绿点表示链接处于活动状态，正在发送纹理。

   ![](../../../../assets/icon-12.png)

   1. 您可以在插件的配置选项中暂停数据流。 转到“插件”>“dcc-live-link”，然后选择“配置”。 禁用“启用流式传输”以暂停数据发送到UE4。

      ![](https://helpx-prod.scene7.com/is/image/HelpxProd/config-6?$png$&jpegSize=100&wid=393)
1. Painter的纹理将显示在内容浏览器中，并将应用于UE4中的素材。

   ![](../../../../assets/link3-11.png){width="500px"}
1. 将在UE4项目文件夹中标记为“.sp”的文件夹中创建一个Substance Painter项目(.spp)

   ![](../../../../assets/link4-5.png)

## 重新建立指向Substance Painter的链接

关闭Painter或Unity后，您可以从上次中断的地方继续。

1. 在位于Unity项目> assets>.sp文件夹中的Substance Painter中打开.spp项目。
1. 右键单击内容浏览器中的网格，然后选择“发送到Painter”以重新建立链接。

   ![](../../../../assets/link5-3.png){width="600px"}
