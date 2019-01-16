---
title: "针对本地环境的硬件规模调整要求"
description: "本主题列出了针对本地环境的硬件规模调整要求。"
author: kfend
manager: AnnBe
ms.date: 06/23/2017
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
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: d277bc4c4c815317bade8a04b9111232fb707086
ms.contentlocale: zh-cn
ms.lasthandoff: 12/18/2018

---

# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>针对本地环境的硬件规模调整要求

[!include [banner](../includes/banner.md)]

在你开始对本地环境执行硬件和基础结构规模调整流程前，请熟悉[系统要求](system-requirements.md) 和[设置和部署说明](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) 以充分了解基础结构。

> [!NOTE]
> 密切关注可实现最优性能的系统设置最佳实践。

在查看文档后，你可以开始评估你的事务性和并发用户数量并基于平均核心吞吐量对环境调整规模的流程。

## <a name="factors-that-affect-sizing"></a>影响规模调整的系数

在下图显示的所有系数都对规模调整具有影响。 收集的详细信息越多，你就越能更加精确地确定规模调整。 不具有支持数据的硬件规模调整可能不准确。 所需数据的绝对最低需求是峰值交易记录行每小时负荷。

[![针对本地环境的硬件规模调整](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

从左到右查看，准确估计规模调整所需的第一个和最重要的系数是交易记录模板或交易记录特征。 始终查找每小时交易量峰值很重要。 如果存在多个峰值期间，则需要准确地定义这些期间。

你了解影响基础结构的负荷后，还需了解有关这些系数的更多详细信息：

- **交易记录** – 交易记录通常在一天/周中具有特定的峰值。 这主要取决于交易记录类型。 时间和支出条目通常显示每周峰值，而销售订单条目通常通过集成批量出现或在一天中缓缓出现。
- **并发用户的数量** - 并发用户的数量是第二重要的规模调整系数。 基于并发用户的数量无法可靠地获取规模调整估计，因此如果这是你唯一可用的数据，则估计一个近似数字，然后当你获得更多数据时再次访问。 准确的并发用户定义意味着：

    - 指定用户不是并发用户。
    - 并发用户始终是指定用户的子集。 
    - 峰值工作负荷定义规模调整的最大并发数。

    并发用户的条件是用户满足以下所有条件：

    - 已登录。
    - 在盘点时的工作交易记录/查询。
    - 不是空闲会话。

- **数据构成** - 这主要与你的系统将如何设置和配置有关。 例如，你有多少法人、多少物料、多少 BOM 级别以及你的安全设置将有多复杂。 这些系数中的每个系数都可能对性能有较小的影响，因此可以通过对基础结构使用明智的选项来抵消这些系数。
- **扩展** - 可以是简单或复杂的自定义。 自定义的数量以及复杂性和使用的性质对所需基础结构的规模有不同的影响。 对于复杂的自定义，建议执行性能评估以确保它们不仅通过效率测试，而且有助于了解基础结构需要。 没有根据性能和可扩展性最佳实践对扩展进行编码时，这一点甚至更加关键。
- **报告和分析** - 这些系数通常包括在 Finance and Operations 数据库系统中对不同数据库运行大量查询。 了解和减少运行昂贵报表的频率将帮助你了解它们的影响。
- **第三方解决方案** - 这些解决方案，例如 ISV，同扩展一样具有相同的影响和建议。

## <a name="sizing-your-finance-and-operations-environment"></a>对你的 Finance and Operations 环境进行规模调整

若要了解你的规模调整需求，你需要知道你需要处理的峰值交易记录量。 大多数辅助系统，例如 Management Reporter 或 SSRS，对任务没有那么关键。 因此，文档主要关注 AOS 和 SQL Server。

> [!NOTE]
> 一般来说，计算层扩大且应按 N+1 的方式设置，意味着如果你估计有三个 AOS，则添加第四个 AOS。 数据库层应在 Always On 高可用性设置中进行设置。

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>规模调整

- DB 服务器上每核心每小时 3K 到 15K 交易记录行。
- 主要 SQL Server 的典型 AOS 到 SQL 核心比率 3:1。 基于所选的高可用性配置需要额外核心。

    - 处理数据库负荷重的操作可能使其后退到 2:1。

- 以下系数影响差异：

    - 在使用中的参数设置。
    - 扩展级别。
    - 附加功能的使用，如数据库日志和预警。 极端数据库记录将进一步将每核心每小时吞吐量降低至 3K 行以下。
    - 数据构成的复杂性 - 一个简单的会计科目表与详细的会计科目表之间的对比对吞吐量具有影响（作为示例）。
    - 交易记录特征。
    - 每核心 2 GB 至 4 GB 内存。
    - DB 服务器上的辅助数据库，例如 Management Reporter 和 SSRS 数据库。
    - 临时 DB = DB 大小的 15%，其中文件的数量与物理处理器的数量相同。
    - 基于总并发交易记录数量/使用量的 SAN 大小和吞吐量。

### <a name="high-availability"></a>高可用性

我们建议始终在群集或镜像设置中使用 SQL Server。 第二个 SQL 节点应与主节点具有相同数量的核心。

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory 联合身份验证服务 (AD FS)

有关 AD FS 规模调整，请参阅 [AD FS 服务器产能文档](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)。

[规模调整电子表格](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) 可用于规划你的部署中的实例数量。

## <a name="aos-online-and-batch"></a>AOS（联机和批处理）

### <a name="sizing"></a>规模调整

- 按交易量/使用量进行规模调整

    - 每核心 2K 到 6K 行
    - 每个实例 16 GB
    - 标准框– 4 到 24 个核心
    - 每核心 10 到 15 个企业用户
    - 每核心 15 到 25 个活动用户
    - 每核心 25 到 50 个团队成员

- 批处理

    - 每核心 1 到 4 个批处理线程数。
    - 基于批处理窗口特征进行规模调整

- 注意，AOS、数据管理和批处理在 Service Fabric 中具有相同的角色。 你需要为合并的这三种工作负荷进行规模调整，而不像在 Microsoft Dynamics AX 2012 中一样将它们分开。
- 用于 SQL Server 的相同可变性系数在此处适用。

### <a name="high-availability"></a>高可用性

- 确保可用的 AOS 比你估计的数量多 1 到 2 个。
- 确保你具有至少 3 到 4 个虚拟主机可用。

## <a name="management-reporter"></a>Management Reporter

在大多数情况下，除非使用广泛，否则建议的最低需求使用两个节点应可以正常工作。 只有在使用量大的情况下，你才需要两个以上节点。 请根据需要扩展。

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services

对于一般可用性版本，只可以部署一个 SSRS 节点。 在测试时监控你的 SSRS 节点，并根据需要增加可用于 SSRS 的核心数量。 确保你在不同于 SSRS VM 的虚拟机上有预先配置的次节点可用。 如果托管 SSRS 的虚拟机或虚拟主机出现问题，则这一点很重要。 如果出现这种情况，将需要更换它们。

## <a name="environment-orchestrator"></a>环境 Orchestrator

Orchestrator 服务是用于管理你的部署和与 LCS 的相关通信的服务。 此服务部署为主 Service Fabric 服务并需要至少三个 VM。 此服务与 Service Fabric Orchestration 服务位于同一位置。 这应该调整到群集的峰值负荷。 有关详细信息，请参阅 [Service Fabric 群集产能规划注意事项](/azure/service-fabric/service-fabric-cluster-capacity)。

## <a name="virtualization-and-oversubscription"></a>虚拟化和过度订阅

关键任务服务（如 AOS）应在具有专用资源（核心、内存和磁盘）的虚拟机上托管。

