---
title: Dynamics 365 Supply Chain Management 10.0.24 中的新增功能或更改（2022 年 2 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.24 中的新增功能或更改的功能。
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 94e465616338b0c905ccf6b8244324c18c7a59e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849436"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Dynamics 365 Supply Chain Management 10.0.24 中的新增功能或更改（2022 年 2 月）

[!include [banner](../includes/banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.24 中的新增或更改的功能。 此版本的构建版本号为 10.0.1084，并以下面的形式提供：

- **版本预览：** 2021 年 12 月
- **版本的正式发布时间（自行更新）：** 2022 年 1 月
- **版本的正式发布时间（自动更新）：** 2022 年 2 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 分布式混合拓扑 | [缩放单元上的增强的仓库执行工作负荷](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [云和边缘缩放单元的仓库管理工作负载](../cloud-edge/cloud-edge-workload-warehousing.md) | 默认启用。 |
| 分布式混合拓扑 | [云和边缘缩放单元的仓库管理工作负荷上的开始生产订单](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [云和边缘缩放单元的制造执行工作负载](../cloud-edge/cloud-edge-workload-manufacturing.md) | 功能管理（*云和边缘缩放单元的仓库管理工作负荷上的开始生产订单*）  |
| 计划 | [再订购宽限期和发货宽限期的计划优化支持](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [安全宽限期](../master-planning/planning-optimization/safety-margins.md) | 默认启用。 |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 生产控制 | 针对生产订单的按需物料可用性检查 | 此功能可以更快地打开 **生产车间管理** 工作区中的 **要下达的生产订单** 页面。 如果没有此功能，系统会在您打开页面后立即自动检查所有列出的生产订单是否有可用材料，如果您有大量订单，这可能会花费大量时间。 启用此功能后，系统会提供一个工具栏按钮，您可以只在需要时使用该按钮启动仅针对选定订单的材料检查。 |
| 生产控制 | (预览版)在生产车间执行界面(非 WMS)上登记物料消耗量 | 此功能使工人能够使用生产车间执行界面来登记材料消耗、批号和序列号。 此功能仅支持未启用使用高级仓库流程 (WMS) 的物料。 计划在未来的版本中支持启用 WMS 的物料。<p>一些制造商，尤其是加工行业的制造商，需要明确登记每个批次或生产订单的材料消耗量。 例如，工作人员可能会使用秤来称量他们工作时消耗的材料量。 为确保完整的材料可追溯性，这些组织还需要登记生产每个产品时消耗材料的批号。 |
| 生产控制 | 云和边缘缩放单元的仓库管理工作负荷上的完工入库 | 当应用针对云或边缘缩放单元上的仓库管理工作负荷运行时，此功能允许工作人员使用 Warehouse Management 移动应用将生产或批次订单报告为完工入库。 有关详细信息，请参阅[在缩放单元上报告为完工入库并储存](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF)。 |
| 仓库管理 | 新装载计划工作台页面 | 启用两个新装载计划工作台页面：**入站装载计划工作台** 和 **出站装载计划工作台**。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 按照上一部分的列举，这些文章未必与此发行版中增加的新功能有关。 但是，可能可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新文章 |
|---|---|
| 成本管理 | [库存值报表](../cost-management/inventory-value-report-storage.md) |
| 成本管理 | [库存值报表示例和逻辑](../cost-management/inventory-value-report-examples.md) |
| 主计划 | [计划优化使用的日期和时间参数](../master-planning/planning-optimization/date-time-used.md) |
| 主计划 | [需求预测设置](../master-planning/demand-forecasting-setup.md) |
| 主计划 | [使用安全存货日记帐更新最小物料覆盖范围](../master-planning/safety-stock-journal.md) |
| 生产控制 | [自定义生产车间执行界面](../production-control/production-floor-execution-customize.md) |
| 生产控制 | [设计生产车间执行界面的样式](../production-control/production-floor-execution-styles.md) |
| 销售和市场营销 | [计划销售历史记录数据清理](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| 仓库管理 | [移动设备用户帐户](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.24 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.24 的平台更新（2022 年 2 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.24 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f)。

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 和行业云：2021 版本第 2 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2021 版本第 2 波计划](/dynamics365-release-plan/2021wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management 中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
