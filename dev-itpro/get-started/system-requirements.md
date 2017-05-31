---
title: "系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Operations 的系统要求。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: de2f71a21c5aac953349559c84283d0f76082d42
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="system-requirements"></a>系统要求

[!include[banner](../includes/banner.md)]


此主题列出了当前版本的 Microsoft Dynamics 365 for Operations 的系统要求。

<a name="supported-web-browsers"></a>支持的 Web 浏览器
----------------------

Microsoft Dynamics 365 for Operations Web 应用程序可在指定操作系统上运行的以下任一 Web 浏览器中运行：

-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）
-   Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）

要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。 

**注意：**

-   若要捕获从任务录制器生成的图像并插入到 Microsoft Word 文档中，必须安装 Chrome 扩展。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Workflow Editor 作为 ClickOnce 应用程序启动。 只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。 Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。
-   适用于财务申报的报表设计器作为 ClickOnce 应用程序启动。 它需要 64 位兼容操作系统。 如果使用的是 Chrome，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。 如果以匿名模式使用 Chrome，请确保也为匿名模式启用 ClickOnce 扩展。
-   若要预览 PDF 文件，我们建议您使用现代浏览器，如 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）。


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS 支持的 Web 浏览器

适用于 Dynamics 365 for Operations 的 Retail Cloud POS 可在指定操作系统上运行的以下任一 Web 浏览器中运行：

-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1 或 Windows 7 上的 Chrome（最新公开提供的版本）

## <a name="network-requirements"></a>网络要求
-   Dynamics 365 for Operations 适用于延迟在 250-300 毫秒 (ms) 或更低的网络。 这是从浏览器客户端到主管 Dynamics 365 for Operations 的 Microsoft Azure 数据中心的延迟。 建议在 <http://www.azurespeed.com> 测试网络延迟。
-   Dynamics 365 for Operations 的带宽要求取决于您的方案。 大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。 但是，对于需要高负载要求的方案（如涉及大量自定义的工作区或方案），建议提供更多带宽。

Dynamics 365 for Operations 通常已针对 Internet 进行了优化。 从浏览器客户端到 Azure 数据中心的往返次数很小，并且整个负载经过压缩。 

**警告：**请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 对于注重带宽要求的客户，请使用 Dynamics 365 for Operations 预览版本。

## <a name="net-framework-requirements"></a>.NET Framework 要求
Dynamics 365 for Operations 需要 .NET Framework 版本 4.6.2 以满足一键式应用程序的要求，如文档路由代理程序。 有关安装说明，请参阅[安装 .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序
-   若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting)。
-   若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS 要求
### <a name="supported-operating-systems"></a>支持的操作系统

-   Retail Modern POS 是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   只有 Windows 10 Pro, Enterprise 和 Enterprise Long Term Servicing Branch (LTSB) 版本才支持 Retail Modern POS。

### <a name="minimum-system-requirements"></a>最低系统要求

-   支持的最低分辨率为 1280 × 1024。
-   运行 Retail Modern POS 的计算机必须满足以下要求：
    -   必须配备以最低不低于 2 千兆赫兹 (GHz) 的速度运行的双核处理器。
    -   必须配备最低 3 千兆字节 (GB) 的 RAM。
    -   必须可以访问 Internet。

## <a name="retail-hardware-station-requirements"></a>零售硬件工作站要求
### <a name="supported-operating-systems"></a>支持的操作系统

-   零售硬件工作站是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   以下操作系统支持零售硬件工作站：
    -   Windows 7 Professional、Enterprise 和 Ultimate 版本 **注释：**仅当系统上手动安装了 Internet Explorer 11，才支持 Windows 7。
    -   Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本
    -   Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本

### <a name="minimum-system-requirements"></a>最低系统要求

计算机必须满足安装和使用以下项的所有系统要求：

-   Internet 信息服务 (IIS)
-   第三方硬件

## <a name="retail-store-scale-unit-requirements"></a>零售商店扩展单位要求
### <a name="supported-operating-systems"></a>支持的操作系统

-   零售商店扩展单位是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   以下操作系统支持零售商店扩展单位：
    -   Windows 7 Professional、Enterprise 和 Ultimate 版本
    -   Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本
    -   Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本

### <a name="minimum-system-requirements"></a>最低系统要求

-   4 GB 的 RAM
-   每个核心 1.6 GHz 的峰值 CPU 速度（至少两个核心。）
-   至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）

### <a name="recommended-system-requirements"></a>建议的系统要求

-   6 GB 的 RAM
-   每个核心 2.4 GHz i7（或等效）峰值 CPU 速度（建议四个核心。）
-   至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）

## <a name="requirements-for-development-on-local-vms"></a>本地虚拟机上的部署要求
有关本地虚拟机 (VM) 上的部署要求的信息，请参阅[本地运行虚拟机](../dev-tools/access-instances.md)。

<a name="see-also"></a>请参阅
--------

[获取 Dynamics 365 for Operations 评估副本](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




