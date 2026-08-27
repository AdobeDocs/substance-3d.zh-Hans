---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-general/ecosystem/substance-for-linux.html"
breadcrumb-title: ''
description: 了解如何使用Adobe下载访问门户在Linux上下载、安装和激活Substance 3D应用程序。
helpx_creative_field: ""
helpx_description: Substance 3D General
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D for Linux (ADA)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 081136918fdf7f431ecee47e5ce64d8b5235bb1b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# 部署指南

通过企业合同购买Substance 3D for Linux®后，将在[Adobe下载访问(ADA)](https://download-access.adobe.com/lws/downloads)门户上配置相应的产品和许可证。 要成功部署软件，您需要从ADA下载软件内部版本和许可证密钥文件。

## 下载软件内部版本和许可证密钥文件：

登录到[Adobe下载访问权限](https://download-access.adobe.com/lws/downloads)。 查找软件内部版本和许可证密钥文件：

1. 使用帐户下拉列表选择您购买Substance 3D Linux时所使用的帐户。

   ![](../../assets/ADA1.png)
1. 使用页面标题中的链接导航至“下载” 。

   ![](../../assets/ADA2.png)
1. 在相应的产品上单击“查看下载” 。

   ![](../../assets/ADA3.png)
1. ADA将加载与此ID相关的许可证信息并在下表中显示它。
1. 单击“数字证书”行上的“下载”以下载包含许可证密钥文件的zip文件。

   * zip文件对每个产品包含一个许可证密钥。
   * 许可证密钥将在您的每台许可计算机上激活该产品。

   ![](../../assets/ADA4.png)
1. 单击“Substance 3D” Sampler、Painter或Designer以显示Substance 3D Painter、Substance 3D Designer和Substance 3D Sampler的软件内部版本。
1. 单击“下载”下载要安装的产品的安装文件。

   ![](../../assets/ADA5.png)
1. 屏幕上会弹出“下载软件”通知。 单击“接受”

   ![](../../assets/ADA6.png)

## 安装和激活

要安装软件，请执行以下操作：

1. 双击产品的EXE文件以启动安装向导。
1. 按照安装步骤完成安装。

软件激活有两个选项：本地激活或网络激活。

### 本地激活

1. 解压缩从ADA下载的zip文件夹。
1. 启动要激活的软件。
1. 在激活向导中，选择“使用许可证密钥文件激活”。

   ![](../../assets/LinuxActivation3.png)
1. 单击“Browse”（浏览），并指向相应许可证密钥文件的位置。
1. 单击“下一步”以激活软件。

### 网络激活

1. 解压缩从ADA下载的zip文件夹。
1. 将解压缩的许可证密钥文件放在共享挂载的网络上。
1. 在用户计算机上，设置指向许可证密钥文件的环境变量，如以下页面所述：

   * Substance 3D Painter - <https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/pipeline-and-integration/configuration/environment-variables>
   * Substance 3D Designer - <https://experienceleague.adobe.com/zh-hans/docs/substance-3d-designer/using/pipeline-and-project-configuration/environment-variables>
   * Substance 3D Sampler - <https://experienceleague.adobe.com/zh-hans/docs/substance-3d-sampler/using/pipeline-and-integrations/environment-variables>
