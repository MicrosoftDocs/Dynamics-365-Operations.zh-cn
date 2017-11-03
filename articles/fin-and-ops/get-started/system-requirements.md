---
title: "云部署的系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 云部署的系统要求。"
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: 7fe11966b27eb0793a47835e05e465d809bf3407
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>云部署的系统要求

[!include[banner](../includes/banner.md)]

此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 云部署的系统要求。 在你安装 Finance and Operations 前，适合执行此步骤时验证你正在使用的系统是否满足或超出最低网络、硬件和软件要求。

## <a name="supported-web-browsers"></a>支持的 Web 浏览器
Web 应用程序可在指定操作系统上运行的以下任一 Web 浏览器中运行：

-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）
-   Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）

要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。 

> [!NOTE]
> -   必须安装预发布 Chrome 扩展以允许任务录制器捕获屏幕截图并包括在生成的 Microsoft Word 文档中。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   Workflow Editor 作为 ClickOnce 应用程序启动。 只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。 Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。
> -   适用于财务申报的报表设计器作为 ClickOnce 应用程序启动。 它需要 64 位兼容操作系统。 如果使用的是 Chrome，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。 如果以匿名模式使用 Chrome，请确保也为匿名模式启用 ClickOnce 扩展。
> -   若要预览 PDF 文件，我们建议您使用 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）等浏览器。

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS 支持的 Web 浏览器

Retail Cloud POS 可在指定操作系统上运行的以下任一 Web 浏览器中运行：

-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1 或 Windows 7 上的 Chrome（最新公开提供的版本）

## <a name="network-requirements"></a>网络要求
-   Finance and Operations 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 此延迟是从浏览器客户端到托管 Finance and Operations 的 Microsoft Azure 数据中心的延迟。 建议在 <http://www.azurespeed.com> 测试网络延迟。
-   Finance and Operations 的带宽要求取决于你的方案。 大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。 但是，对于需要高负载要求的方案（如涉及工作区或大量自定义的方案），建议提供更高带宽。

Finance and Operations 通常已针对 Internet 进行了优化。 从浏览器客户端到 Azure 数据中心的往返次数很小，并且整个负载经过压缩。 

> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 注重带宽要求的客户应使用 Finance and Operations 预览版本。

## <a name="net-framework-requirements"></a>.NET Framework 要求
Finance and Operations 需要 Microsoft .NET Framework 版本 4.6.2 以满足所有一键式应用程序的要求，如文档路由代理程序。 有关安装说明，请参阅[安装 .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序
以下 Microsoft Office 应用程序在 Finance and Operations 的云和本地部署中受支持：

-   若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的详细信息，请参阅 [Office 集成疑难解答](../../dev-itpro/office-integration/office-integration-troubleshooting.md)。
-   若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS 要求

> [!NOTE]
> 如果 Retail Modern POS 将使用脱机数据库，计算机必须满足 Microsoft SQL Server 的所有系统要求。 Retail Modern POS 脱机数据库支持带 Service Pack 3 或更高版本的 Microsoft SQL Server 2012、带 Service Pack 2 或更高版本的 Microsoft SQL Server 2014，以及 Microsoft SQL Server 2016。 建议始终使用可用的最新版本，并安装所有最新服务包。

### <a name="supported-operating-systems"></a>支持的操作系统

-   Retail Modern POS 是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   只有 Windows 10 Pro, Enterprise 和 Enterprise Long Term Servicing Branch (LTSB) 版本才支持 Retail Modern POS。

### <a name="minimum-system-requirements"></a>最低系统要求

-   支持的最低分辨率为 1280 × 1024。
-   运行 Retail Modern POS 的计算机必须满足以下要求：

    -   必须配备以最低不低于 2 千兆赫兹 (GHz) 的速度运行的双核处理器。
    -   必须配备最低 3 千兆字节 (GB) 的随机存取内存 (RAM)。
    -   必须可以访问 Internet。

## <a name="retail-hardware-station-requirements"></a>零售硬件工作站要求
### <a name="supported-operating-systems"></a>支持的操作系统

-   零售硬件工作站是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   以下操作系统支持零售硬件工作站：

    -   Windows 7 Professional、Enterprise 和 Ultimate 版本 
    
        > [!NOTE]
        > 只有当在系统上手动安装 Internet Explorer 11 时，Windows 7 才受支持。

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

## <a name="connector-requirements"></a>连接器需求
### <a name="supported-operating-systems"></a>支持的操作系统

-   Connector for Microsoft Dynamics AX 具有两个单独的安装程序，一个针对 Async Server Connector service，一个针对 Real-time service for Dynamics AX 2012 R3。
-   两个组件都是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   两个组件都支持以下操作系统：

    -   Windows 7 Professional、Enterprise 和 Ultimate 版本
    -   Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本
    -   Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本
    -   Microsoft Windows Server 2012 R2 和 Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>最低系统要求
-   2 GB RAM（建议 4 GB RAM）。
-   每个核心 1.6 GHz 的峰值 CPU 速度（至少两个核心。）
-   至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）

## <a name="requirements-for-development-on-local-vms"></a>本地虚拟机上的部署要求
有关本地虚拟机 (VM) 上的部署要求的信息，请参阅[本地运行虚拟机](../../dev-itpro/dev-tools/access-instances.md)。


## <a name="see-also"></a>请参阅

[获取 Dynamics 365 for Finance and Operations Enterprise Edition 的评估副本](../../dev-itpro/dev-tools/get-evaluation-copy.md)

