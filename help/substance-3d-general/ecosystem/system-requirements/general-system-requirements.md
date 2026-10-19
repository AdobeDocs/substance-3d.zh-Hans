---
helpx_url: 'https://helpx.adobe.com/substance-3d-general/ecosystem/general-system-requirements.html'
breadcrumb-title: ''
description: 检查Substance 3D应用程序的系统要求，以确保您的硬件满足最低、推荐或最佳规格。
helpx_creative_field: ''
helpx_description: General Knowledge > Ecosystem > General system requirements
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 一般系统要求
user-guide-description: ''
user-guide-title: ''
source-git-commit: eef3d78f33034f2c24f4c4471d9ccac805184525
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 2%
---

# 一般系统要求

## 硬件要求

+++Windows

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| **操作系统** | Windows 11（64位）23H2版 | Windows 11（64位）24H1版 | Windows 11（64位）24H2版 |
| **CPU** | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada代AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

+++

+++macOS

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| **操作系统** | macOS红杉15号 | macOS金门27 | macOS金门27 |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

>[!WARNING]
>
> 对于使用[VFX参考平台](https://vfxplatform.com/)构建的管道，Substance 3D应用程序仍可以安装在macOS 14 Sonoma上。 但是，不再为低于最低Substance要求的操作系统版本测试系统应用程序，因此不保证稳定性。 建议更新到较新的操作系统版本。

+++

+++Linux

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| **操作系统** | **企业ETLA** RHEL 8.6或更高版本或RHEL 9.2或更高版本&#x200B;**Steam** Ubuntu 22.04.1 LTS | **企业ETLA** RHEL 8.6或更高版本，或者RHEL 9.4或更高版本&#x200B;**Steam** Ubuntu 22.04.1 LTS或更高版本 | **企业ETLA** RHEL 8.6或更高版本，或者RHEL 9.4或更高版本&#x200B;**Steam** Ubuntu 22.04.1 LTS或更高版本 |

**Red Hat Enterprise Linux (RHEL) 9.x**：我们的应用程序所需的xcb-util-cursor程序包已于2024年5月10日从EPEL 9存储库中删除。 自此日期起，默认RHEL 9存储库支持该包，与RHEL 9.4的发行版一致。 在2024年5月10日之后，使用9.4之前版本的RHEL的客户将无法再从EPEL 9存储库中获取xcb-util-cursor包。

有关此包在默认RHEL 9存储库中的可用性的详细信息，请参阅： [Red Hat Enterprise Linux 9 — 包清单 — AppStream存储库](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/package_manifest/index#AppStream-repository)

有关此更改的详细信息，请参阅： [Red Hat Bugzilla - Bug 2238273](https://bugzilla.redhat.com/show_bug.cgi?id=2238273) ， [Red Hat Bugzilla - Bug 2212302](https://bugzilla.redhat.com/show_bug.cgi?id=2212302)

+++

+++VR

| 品牌 | 模型 |
| --- | --- |
| Meta | Rift、Rift S、Quest、Quest 2（带链接）、Quest Pro |

+++

有关更多详细信息，请查看每个应用程序的要求：

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/sa-appicon-noshadow-256.png" alt="Substance 3D Sampler图标" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/getting-started/system-requirements">Substance 3D Sampler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/ds-appicon-noshadow-256.png" alt="Substance 3D Designer图标" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Substance 3D</a> <a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Designer</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/pt-appicon-noshadow-256.png" alt="Substance 3D Painter图标" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/system-requirements">Substance 3D Painter</a></td>
  </tr>
</table>

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/md-appicon-noshadow-256.png" alt="Substance 3D Modeler图标" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-modeler/getting-started/system-requirements.html">Substance 3D Modeler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/sg-appicon-noshadow-256.png" alt="Substance 3D Stager图标" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-stager/getting-started/system-requirements.html">Substance 3D Stager</a></td>
    <td style="border: 0;" valign="top"></td>
  </tr>
</table>

## 其他说明

### 不支持的配置

* 不支持具有eGPU和用户安装的GPU的Apple计算机配置。
* 不支持Windows虚拟机。
* 不支持Windows Server操作系统。
