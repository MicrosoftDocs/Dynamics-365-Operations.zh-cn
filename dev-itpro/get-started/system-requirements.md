---
title: "系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本云和本地部署的系统要求。"
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: zh-cn
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>系统要求

[!include[banner](../includes/banner.md)]


此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本云和本地部署的系统要求。 在你安装 Finance and Operations 前，适当时验证你正在使用的系统是否满足或超出最低网络、硬件和软件要求。


## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序
以下 Office 应用程序在 Finance and Operations 的云和本地部署中受支持。
-   若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting)。
-   若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。

# <a name="system-requirements-specific-to-cloud-deployments"></a>特定于云部署的系统要求
## <a name="network-requirements"></a>网络要求
-   Finance and Operations 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 这是从浏览器客户端到托管 Finance and Operations 的 Microsoft Azure 数据中心的延迟。 建议在 <http://www.azurespeed.com> 测试网络延迟。
-   Finance and Operations 的带宽要求取决于你的方案。 大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。 但是，对于需要高负载要求的方案（如涉及大量自定义的工作区或方案），建议提供更多带宽。

Finance and Operations 通常已针对 Internet 进行了优化。 从浏览器客户端到 Azure 数据中心的往返次数很小，并且整个负载经过压缩。 

> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 对于注重带宽要求的客户，请使用 Finance and Operations 预览版本。

## <a name="net-framework-requirements"></a>.NET Framework 要求
Finance and Operations 需要 .NET Framework 版本 4.6.2 以满足所有一键式应用程序的要求，如文档路由代理程序。 有关安装说明，请参阅[安装 .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)。

## <a name="supported-web-browsers"></a>支持的 Web 浏览器
Web 应用程序可在指定操作系统上运行的以下任一 Web 浏览器中运行：


-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）
-   Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）

要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。 

> [!NOTE]
> -   必须安装预发布 Chrome 扩展以允许由任务录制器捕获屏幕截图图像并包括在生成的 Microsoft Word 文档。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Workflow Editor 作为 ClickOnce 应用程序启动。 只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。 Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。
> -   适用于财务申报的报表设计器作为 ClickOnce 应用程序启动。 它需要 64 位兼容操作系统。 如果使用的是 Chrome，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。 如果以匿名模式使用 Chrome，请确保也为匿名模式启用 ClickOnce 扩展。
> -   若要预览 PDF 文件，我们建议您使用 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）等浏览器。


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS 支持的 Web 浏览器

Retail Cloud POS 可在指定操作系统上运行的以下任一 Web 浏览器中运行：

-   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   Windows 10、Windows 8.1 或 Windows 7 上的 Chrome（最新公开提供的版本）

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

-   Connector for Microsoft Dynamics AX 具有两个单独的安装程序，**Async Server Connector service** 和 **Real-time service for Dynamics AX 2012 R3**。
-   两个组件都是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。
-   两个组件都支持以下操作系统：
    -   Windows 7 Professional、Enterprise 和 Ultimate 版本
    -   Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本
    -   Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本
    -   Windows Server 2012 R2、Windows Server 2016

### <a name="minimum-system-requirements"></a>最低系统要求

-   2 GB RAM，建议 4 GB RAM
-   每个核心 1.6 GHz 的峰值 CPU 速度（至少两个核心。）
-   至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）

## <a name="requirements-for-development-on-local-vms"></a>本地虚拟机上的部署要求
有关本地虚拟机 (VM) 上的部署要求的信息，请参阅[本地运行虚拟机](../dev-tools/access-instances.md)。

# <a name="system-requirements-for-on-premises-deployments"></a>本地部署的系统要求

## <a name="network-requirements"></a>网络要求
Finance and Operations（本地）可以在使用 Internet 协议版本 4 (IPv4) 或 Internet 协议版本 6 (IPv6) 的网络上使用。 在计划系统时考虑网络环境并遵照以下指南。

### <a name="network-response-time"></a>网络响应时间
下表列出了本地系统中 Web 浏览器与应用程序对象服务器 (AOS) 之间连接以及 AOS 与数据库之间连接的最低网络要求。

| 值     | 从 Web 浏览器到 AOS | 从 AOS 到数据库                                            |
|-----------|--------------------|------------------------------------------------------------|
| 带宽 | 每用户 50 KBps   | 100 Mbps                                                   |
| 延迟   | < 250-300 ms       | < 1 ms（仅 LAN）。 AOS 和数据库需要在同一个地点。 |

- Finance and Operations（本地）适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 该延迟是从浏览器客户端到托管 Finance and Operations 的数据中心的延迟。
- Finance and Operations（本地）的带宽要求取决于你的方案。 典型方案要求浏览器与 Finance and Operations 服务器之间的带宽超过每秒 50 千字节 (KBps)。 但是，对于需要高负载要求的方案（如涉及大量自定义的工作区或方案），建议根据使用情况提供更多带宽。
AOS 和 SQL Server 数据库安装在不同的数据中心的部署不支持。 AOS 和 SQL Server 数据库需要在同一个地点。 一般来说，Finance and Operations 经过优化以缩短浏览器到服务器的往返。 从浏览器客户端到数据中心的往返次数要么为零，要么是每次用户交互往返一次，并且整个负载经过压缩。

> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 我们建议使用真实模拟 Finance and Operations 的非生产环境作为针对你的特定案例的性能的最佳衡量。 

### <a name="lan-environments"></a>LAN 环境
在局域网 (LAN) 环境，不需要通过 Microsoft Windows Server 中的 Microsoft 远程桌面连接到 Finance and Operations。 但是，它可能是构成服务器部署的 VM 上的服务操作所必需的。

### <a name="wan-environments"></a>WAN 环境
在广域网 (WAN) 环境，不需要通过 Windows Server 中的远程桌面连接到 Finance and Operations。

### <a name="internet-connectivity-requirements"></a>Internet 连接要求
Finance and Operations（本地）不要求来自最终用户工作站的 Internet 连接。 但是，没有 Internet 连接，一些功能将不可用。

| 浏览器客户端 | 没有 Internet 连接的内部网方案是本地部署选项的一个设计点。 要求云服务的某些功能将不可用，例如 LCS 中的帮助和任务指南库。 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 服务器         | AOS 或 Service Fabric 层级必须能够与 LCS 通信。 本地的基于浏览器的客户端不需要访问 Internet。                                                                                |
| 遥测      | 如果存在长时间的连接中断，遥测数据可能会丢失。 与 LCS 的连接中断不影响本地应用程序功能。                                                |
| LCS            | 部署、代码部署和服务操作要求连接到 LCS。                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>将遥测数据转移到云
大多数遥测本地存储并且可以通过 Microsoft Windows 中的事件查看器访问。 遥测事件中的一个小子集被转移到云中的 Microsoft 遥测管道进行诊断。 客户数据和最终用户的可识别数据不是发送到 Microsoft 的遥测的一部分。 VM 名称被发送到 Microsoft 以辅助环境管理和来自 LCS 门户的诊断。

## <a name="domain-requirements"></a>域需求
在安装 Finance and Operations（本地）时考虑以下域要求：

- 托管 Finance and Operations（本地）组件的虚拟机必须属于 Active Directory 域。 Active Directory 域服务 (AD DS) 必须在本机模式中配置。
- 运行 Finance and Operations（本地）组件的虚拟机必须具有互相访问在 Active Directory 域服务中配置的虚拟机的权限。 
- 域控制器必须在 Microsoft Windows Server 2016 上运行。

## <a name="hardware-requirements"></a>硬件要求
本节介绍运行 Finance and Operations（本地）所需的硬件。
基于系统配置、数据构成以及你决定要使用的应用程序和功能，实际硬件要求将不同。 以下是可能影响 Finance and Operations（本地）适当硬件选择的一些因素：

- 每小时的交易数量。
- 并发用户的数量。

## <a name="minimum-infrastructure-requirements"></a>最低基础结构需求
Finance and Operations（本地）使用 Microsoft Azure Service Fabric 托管 AOS、批处理、数据管理、Management Reporter 和环境 Orchestrator 服务。 Microsoft SQL Server Reporting Services (SSRS) 不在 Service Fabric 群集中托管。
SQL Server 必须在至少具有两个用于生产的节点的高可用性 HADRON 设置中进行设置。
下图显示了在你的 Service Fabric 群集中的最低建议节点数量。

[![Service Fabric 群集的建议节点数量](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>处理器和 RAM 要求
下表列出了运行此部署选项所需的每个角色所需的处理器的数量和随机存取内存 (RAM) 量。 有关详细信息，请参阅 Service Fabric 独立群集的最低要求建议、[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)。

> [!NOTE]
> 如果在同一台计算机上安装了其他 Microsoft 软件，系统还必须符合该软件的硬件要求。 我们建议你将与 AOS 相同的计算机上的其他服务器应用程序限制为 1 千兆字节 (GB) RAM。

**按角色和拓扑类型的规模调整**

| 拓扑   | 节点（节点类型）              | 建议的处理器核数量 | 建议的内存 (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| 生产 | AOS、数据管理、批处理   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| 沙盒    | AOS、数据管理、批处理   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**生产和沙盒部署的最低规模调整估计**\*

| 拓扑                                  | 角色                          | 实例数 |
|-------------------------------------------|-------------------------------|---------------------|
| 生产                                | AOS（数据管理、批处理）  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| 沙盒                                   | AOS、数据管理、批处理   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *汇总生产和沙盒拓扑* |                               | 16                  |

\*这些数字正由我们的预览客户进行验证，并可能根据他们的反馈进行必要的调整。

\*\*Orchestrator 被指定为主节点类型，并用于运行 Service Fabric 服务。

**后端 SQL Server 和 AD 初始估计**

[![后端 SQL Server 和 AD 初始估计](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server 大小高度依赖于工作负荷。 有关详细信息，请参阅[针对本地环境的硬件规模调整](#Hardware-sizing-for-on-premises-environments) 部分。

## <a name="storage"></a>存储

- **AOS** - Finance and Operations（本地）将使用服务器消息块 (SMB) 3.0 共享以存储非结构化数据。 有关详细信息，请参阅 [Windows Server 2016 中的 Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)。
- **SQL** - 可行选择：
    - 高可用性的固态驱动器 (SSD) 设置。
    - 针对 OLTP 吞吐量进行优化的存储区域网络 (SAN)。
    - 高性能直接连接的存储 (DAS) 
- **SQL 和数据管理 IOPS** - 用于数据管理和 SQL Server 的存储每秒钟至少应具有 2,000 次输入/输出操作 (IOPS)。 生产 IOPS 取决于许多因素。 有关详细信息，请参阅“针对本地环境的硬件规模调整”部分。 
- **虚拟机 IOPS** - 每个虚拟机应至少具有 100 个写入的 IOPS。

## <a name="virtual-host-requirements"></a>虚拟主机要求
当你设置 Finance and Operations（本地）环境的虚拟主机时，参考以下指南：[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) 和[描述 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description)。 每个虚拟主机都应具有足够的核心用于正在进行规模调整的基础结构。 当 SQL Server 位于物理硬件但其他所有内容均虚拟化时，可以进行多种高级配置。 如果 SQL Server 虚拟化，磁盘子系统应为快速 SAN 或等效物。 在任何情况下，确保虚拟主机的基本设置可用性高且冗余。 在任何情况下，在使用虚拟化时，不应拍摄 VM 快照。

## <a name="software-requirements-for-all-server-computers"></a>针对所有服务器计算机的软件要求
在安装任何 Finance and Operations（本地）组件前，计算机上必须存在以下软件：

- Microsoft .NET Framework 4.5.1 或更高版本
- Service Fabric 有关详细信息，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)。

## <a name="supported-server-operating-systems"></a>支持的服务器操作系统
下表列出了支持 Finance and Operations 组件的服务器操作系统。

| 操作系统                                     | 注释                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 数据中心或标准 | 以下是针对托管 AOS 的数据库和 Service Fabric 群集的要求。 |

## <a name="software-requirements-for-database-servers"></a>针对数据库服务器的软件要求

- 仅 SQL Server 2016 的 64 位版本受支持。
- 在生产环境中，我们建议你针对你使用的 SQL Server 版本安装最新累积更新 (CU)。
- Finance and Operations（本地）支持区分大小写、区分重音、区分假名、不区分全半角的 Unicode 排序规则。 排序规则必须与运行 AOS 实例的计算机的 Windows 区域设置相匹配。 如果你正在设置新的安装，建议你选择 Windows 排序规则而不是 SQL Server 排序规则。 有关如何选择 SQL Server 数据库排序规则的详细信息，请参阅 [SQL Server 文档](/sql/sql-server/sql-server-technical-documentation)。
下表列出了支持 Finance and Operations 数据库的 SQL Server 版本。 有关详细信息，请参阅 [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) 的最低硬件要求。

| 需求                                                      | 注释                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard 版本 或 Enterprise 版本 | 有关 SQL Server 2016 的硬件要求，请参阅[安装 SQL Server 2016 的硬件和软件要求](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)。 |

## <a name="software-requirements-for-client-computers"></a>针对客户端计算机的软件要求
Finance and Operations Web 应用程序可以使用兼容 HTML5.0 的 Web 浏览器在任何设备上运行。 Microsoft 已确认的特定设备/浏览器组合包括：

- Windows 10 上的 Microsoft Edge（最新公开提供的版本）
- Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
- Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）
- Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory 联合身份验证服务的软件要求 
Windows Server 2016 上的 Active Directory 联合身份验证服务 (AD FS)

域控制器必须是具有 2012 R2 域功能级别或更高级别的 Windows Server 2012 R2 或更高版本

有关域功能级别的详细信息，请参阅： 
- [什么是 Active Directory 功能级别](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [了解 Active Directory 域服务功能级别](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>针对 Retail 组件的硬件和软件要求
Finance and Operations（本地）暂时不包括 Retail 组件。

<a name="see-also"></a>请参阅
--------

[获取 Dynamics 365 for Finance and Operations Enterprise 版本的评估副本](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

