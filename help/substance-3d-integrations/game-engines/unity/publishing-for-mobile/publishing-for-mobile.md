---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-integrations/game-engines/unity/publishing-for-mobile.html"
breadcrumb-title: ''
description: 通过调整设置和纹理分辨率，在Unity中优化移动平台的Substance素材。
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Publishing for Mobile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 发布移动版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# 发布移动版

>[!NOTE]
>
> **移动设备上的纹理大小**
> 
> 在Unity编辑器中设置的纹理分辨率将为应用程序二进制文件中发布的大小。 降低Substance素材的分辨率将创建文件较小的纹理。

## 平台

## Apple iOS

1. 确保为相应的Unity版本下载iOS模块。
1. 在Unity中，将构建目标更改为iOS。
1. 打开播放器设置，将“Identification - Bundle Identifier”字段更改为更独特的字段。 （例如：com.Adobe.iosProject）
1. 构建并运行游戏。
1. 在Xcode中，单击iOS设备，然后将“Signing - Team”（签名 — 团队）下拉列表更改为开发人员团队ID。
1. 在iOS设备上，转到“设置 — 常规 — 设备管理”，然后在显示的开发人员团队ID上单击“信任”。
1. 通过单击“生成并运行当前方案”按钮（“播放”按钮）再次运行Xcode生成。
1. 游戏应在iOS设备上运行。

## Android操作系统

1. 确保为相应的Unity版本下载Android模块。
1. 在Unity中，将构建目标更改为Android。
1. 打开播放器设置，将“Identification - Bundle Identifier”字段更改为更独特的字段。 （例如：com.Adobe.androidProject）
1. 构建并运行游戏。
1. 游戏应在Android设备上运行。
