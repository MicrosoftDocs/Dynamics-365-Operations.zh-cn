---
title: "本地部署的系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 本地部署的系统要求。"
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73fefd43c9de917dc6c98b2a6893b36a5c0ccdc5
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>本地部署的系统要求

[!include[banner](../includes/banner.md)]

此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 本地部署的系统要求。 在你安装 Finance and Operations 前，适合执行此步骤时验证你正在使用的系统是否满足或超出最低网络、硬件和软件要求。

## <a name="network-requirements"></a>网络要求
Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（本地部署）支持使用 Internet 协议版本 4 (IPv4) 或 Internet 协议版本 6 (IPv6) 的网络。 在计划系统时考虑网络环境并遵照以下指南。

### <a name="network-response-time"></a>网络响应时间
下表列出了本地系统中 Web 浏览器与应用程序对象服务器 (AOS) 之间连接以及 AOS 与数据库之间连接的最低网络要求。

| 值     | 从 Web 浏览器到 AOS                      | 从 AOS 到数据库 |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| 带宽 | 每用户每秒 50 千字节 (KBps)。 | 每秒 100 兆字节 (Mbps) |
| 延迟   | 低于 250–300 毫秒 (ms)     | 低于 1 ms（仅限局域网 (LAN)）。 AOS 和数据库必须在同一个地点。 |

- Finance and Operations（本地）适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 该延迟是从浏览器客户端到托管 Finance and Operations 的数据中心的延迟。
- Finance and Operations（本地）的带宽要求取决于你的方案。 典型方案要求浏览器与 Finance and Operations 服务器之间的带宽超过每秒 50 千字节 KBps。 但是，对于需要高负载要求的方案（如涉及工作区或大量自定义的方案），建议提供更高带宽。 具体带宽量取决于使用。

不支持将 AOS 和 Microsoft SQL Server 数据库安装在不同的数据中心的部署。 AOS 和 SQL Server 数据库必须在同一个地点。 

一般来说，Finance and Operations 经过优化以缩短浏览器到服务器的往返。 从浏览器客户端到数据中心的往返次数要么为零，要么是每次用户交互往返一次，并且整个负载经过压缩。

> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 我们建议使用真实模拟 Finance and Operations 的非生产环境作为针对你的特定案例的性能的最佳衡量。 

### <a name="lan-environments"></a>LAN 环境
在 LAN 环境中，不需要通过 Microsoft Windows Server 中的 Microsoft 远程桌面即可连接到 Finance and Operations。 但是，构成服务器部署的虚拟机 (VM) 上的服务操作可能需要远程桌面。

### <a name="wan-environments"></a>WAN 环境
在广域网 (WAN) 环境中，不需要通过 Windows Server 中的远程桌面即可连接到 Finance and Operations。

### <a name="internet-connectivity-requirements"></a>Internet 连接要求
Finance and Operations（本地）不要求来自用户工作站的 Internet 连接。 但是，如果没有 Internet 连接，一些功能将不可用。

|                    |   |
|--------------------|---|
| **浏览器客户端** | 没有 Internet 连接的内部网方案是本地部署选项的一个设计点。 要求云服务的某些功能将不可用，例如 Microsoft Dynamics Lifecycle Services (LCS) 中的帮助和任务指南库。 |
| **服务器**         | AOS 或 Microsoft Azure Service Fabric 层级必须能够与 LCS 通信。 本地的基于浏览器的客户端不需要访问 Internet。 |
| **遥测**      | 如果存在长时间的连接中断，遥测数据可能会丢失。 与 LCS 的连接中断不影响本地应用程序功能。 |
| **LCS**            | 部署、代码部署和服务操作要求连接到 LCS。 |

## <a name="telemetry-data-transfer-to-the-cloud"></a>将遥测数据转移到云
大多数遥测数据存储在本地并且可以通过 Microsoft Windows 中的事件查看器访问。 遥测事件中的一个小子集被转移到云中的 Microsoft 遥测管道进行诊断。 客户数据和用户的可识别数据不是发送到 Microsoft 的遥测数据的一部分。 VM 名称被发送到 Microsoft 以帮助执行环境管理和来自 LCS 门户的诊断。

## <a name="domain-requirements"></a>域需求
在安装 Finance and Operations（本地）时考虑以下域要求：

- 托管 Finance and Operations（本地）组件的 VM 必须属于 Active Directory 域。 Active Directory 域服务 (AD DS) 必须在本机模式中配置。
- 运行 Finance and Operations（本地）组件的 VM 必须可以彼此访问。 此访问在 AD DS 中配置。 
- 域控制器必须是 Microsoft Windows Server 2012 R2 或更高版本，域功能级别必须是 2012 R2 或更高版本。

## <a name="hardware-requirements"></a>硬件要求
本节介绍运行 Finance and Operations（本地）所需的硬件。

基于系统配置、数据构成以及你决定要使用的应用程序和功能，实际硬件要求将不同。 以下是可能影响 Finance and Operations（本地）适当硬件选择的一些因素：

- 每小时的交易数量
- 并发用户的数量

## <a name="minimum-infrastructure-requirements"></a>最低基础结构需求
Finance and Operations（本地）使用 Service Fabric 托管 AOS、批处理、数据管理、Management Reporter 和环境 Orchestrator 服务。 

必须为 SQL Server 设置至少具有两个用于生产的节点的高可用性 HADRON。

下图显示了为 Service Fabric 群集建议的最低节点数量。

[![为 Service Fabric 群集建议的节点数量](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>处理器和 RAM 要求
下表列出了运行此部署选项所需的每个角色所需的处理器的数量和随机存取内存 (RAM) 量。 有关详细信息，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)中的 Service Fabric 独立群集建议最低要求。

> [!NOTE]
> 如果在同一台计算机上安装了其他 Microsoft 软件，系统还必须符合该软件的硬件要求。 如果其他服务器应用程序与 AOS 安装在同一台计算机上，我们建议你将这些服务器应用程序限制为 1 千兆字节 (GB) RAM。

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

**生产和沙盒部署的最低规模调整估计\***

| 拓扑                                        | 角色                          | 实例数 |
|-------------------------------------------------|-------------------------------|---------------------|
| 生产                                      | AOS（数据管理、批处理）  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| 沙盒                                         | AOS、数据管理、批处理   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *生产和沙盒拓扑摘要* |                               | *16*                |

\* 此表中的数字正在由预览客户验证，可能根据这些客户的反馈进行调整。

\*\*Orchestrator 被指定为主节点类型，也用于运行 Service Fabric 服务。

**后端 SQL Server 和 AD DS 的初始估计**

<table>
<thead>
<tr>
<th></th>
<th>角色</th>
<th>VM/实例</th>
<th>内核</th>
<th>内核总数</th>
<th>每个实例的内存 (GB)</th>
<th>内存总量 (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>共享基础结构</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>文件服务器/存储是网络/高可用性存储</td>
<td colspan="5"><p>后端存储必须基于运行时存储区域网络 (SAN) 中的固态硬盘 (SSD)。</p>
<p>大小和每秒输入/输出操作 (IOPS) 吞吐量基于工作负载的大小。</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>共享基础结构摘要</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server 大小高度依赖于工作负荷。 有关详细信息，请参阅[针对本地环境的硬件规模调整](hardware-sizing-on-premises-environments.md)。

## <a name="storage"></a>存储

- **AOS** - Finance and Operations（本地）使用服务器消息块 (SMB) 3.0 共享以存储非结构化数据。 有关详细信息，请参阅 [Windows Server 2016 中的 Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)。
- **SQL** - 支持以下选项：

    - 高可用 SSD 设置
    - 专门针对在线交易处理 (OLTP) 吞吐量进行过优化的 SAN
    - 高性能直接连接的存储 (DAS) 

- **SQL Server 和数据管理 IOPS** - 用于数据管理和 SQL Server 的存储每秒钟至少应具有 2,000 次 IOPS。 生产 IOPS 取决于许多因素。 有关详细信息，请参阅[针对本地环境的硬件规模调整](hardware-sizing-on-premises-environments.md)。
- **VM IOPS** - 每个 VM 应具有至少 100 次的写入 IOPS。

## <a name="virtual-host-requirements"></a>虚拟主机要求
当你设置 Finance and Operations（本地）环境的虚拟主机时，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) 和[描述 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description)中的指南。 每个虚拟主机都应具有足够的核心用于正在进行规模调整的基础结构。 当 SQL Server 位于物理硬件但其他所有内容均虚拟化时，可以进行多种高级配置。 如果 SQL Server 虚拟化，磁盘子系统应为快速 SAN 或等效物。 在任何情况下，确保虚拟主机的基本设置可用性高且冗余。 在任何情况下，在使用虚拟化时，不应拍摄 VM 快照。

## <a name="software-requirements-for-all-server-computers"></a>针对所有服务器计算机的软件要求
在安装任何 Finance and Operations（本地）组件前，计算机上必须存在以下软件：

- Microsoft .NET Framework 版本 4.5.1 或更高版本
- Service Fabric

有关详细信息，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)。

## <a name="supported-server-operating-systems"></a>支持的服务器操作系统
下表列出了支持 Finance and Operations 组件的服务器操作系统。

| 操作系统                                     | 注释 |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 数据中心或标准 | 以下是针对托管 AOS 的数据库和 Service Fabric 群集的要求。 |

## <a name="software-requirements-for-database-servers"></a>针对数据库服务器的软件要求

- 仅 SQL Server 2016 的 64 位版本受支持。
- 在生产环境中，我们建议你针对你使用的 SQL Server 版本安装最新累积更新 (CU)。
- Finance and Operations（本地）支持区分大小写、区分重音、区分假名、不区分全半角的 Unicode 排序规则。 排序规则必须与运行 AOS 实例的计算机的 Windows 区域设置相匹配。 如果你正在设置新的安装，建议你选择 Windows 排序规则而不是 SQL Server 排序规则。 有关如何选择 SQL Server 数据库排序规则的详细信息，请参阅 [SQL Server 文档](/sql/sql-server/sql-server-technical-documentation)。

下表列出了支持 Finance and Operations 数据库的 SQL Server 版本。 有关详细信息，请参阅 [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) 的最低硬件要求。

| 需求                                                      | 注释 |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard 版本 或 Enterprise 版本 | 有关 SQL Server 2016 的硬件要求，请参阅[安装 SQL Server 2016 的硬件和软件要求](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)。 |

## <a name="software-requirements-for-application-object-server-aos"></a>应用程序对象服务器 (AOS) 的软件要求 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>报表服务器 (BI) 的软件要求
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>针对客户端计算机的软件要求
Finance and Operations Web 应用程序可以使用兼容 HTML 5.0 的 Web 浏览器在任何设备上运行。 下面是 Microsoft 已确认的一些特定设备/浏览器组合：

- Windows 10 上的 Microsoft Edge（最新公开提供的版本）
- Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
- Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）
- Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory 联合身份验证服务的软件要求 
需要 Windows Server 2016 上的 Active Directory 联合身份验证服务 (AD FS)

域控制器必须是 Windows Server 2012 R2 或更高版本，域功能级别必须是 2012 R2 或更高版本。 有关域功能级别的详细信息，请参阅以下页面：

- [什么是 Active Directory 功能级别](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [了解 Active Directory 域服务功能级别](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序
以下 Microsoft Office 应用程序在 Finance and Operations 的云和本地部署中受支持：

-   若要运行 Microsoft Excel 和 Microsoft Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的详细信息，请参阅 [Office 集成疑难解答](../../dev-itpro/office-integration/office-integration-troubleshooting.md)。
-   若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>针对 Retail 组件的硬件和软件要求
Finance and Operations（本地）目前不包括 Retail 组件。

