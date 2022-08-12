---
title: Dynamics 365 Supply Chain Management 10.0.20 的新增功能或更改（2021 年 8 月）
description: 本文介绍 Dynamics 365 Supply Chain Management 10.0.20 中的新增功能或更改的功能。
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3465866df0d766b2300eb4fd1989c034cedbbb22
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123799"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Dynamics 365 Supply Chain Management 10.0.20 的新增功能或更改（2021 年 8 月）

[!include [banner](../includes/banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.20 中的新增或更改的功能。 此版本的构建版本号为 10.0.886，并以下面的形式提供：

- **版本预览：** 2021 年 5 月
- **版本正式发布（自行更新）：** 2021 年 7 月
- **版本的正式发布时间（自动更新）：** 2021 年 8 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 *功能* 列提供了指向[发布计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)的链接，您可以在那里查看每项功能的官方发布日期。 *更多信息* 列提供了更多详细信息和/或相关文档的链接。

这些功能中的大多数必须先使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用，然后才能使用。

| 特征区域 | 功能 | 更多信息 |
|---|---|---|
| 库存和物流&nbsp;&nbsp; | [销售订单详细信息性能增强](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | 此功能使用户界面在打开销售订单（尤其是包含多行的订单）时更具响应性。 |
| 制造 | [调用流程自动化流来创建质检订单](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [调用流程自动化流来创建质检订单](../production-control/process-automation-quality-orders.md ) |
| 制造 | [用于制造的增强生产车间执行界面](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [配置生产车间执行界面](../production-control/production-floor-execution-configure.md) |
| 计划 | [计划优化的无限容量计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [具有无限容量的计划](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| 产品信息管理 | [管理公式及其成分的更改](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [管理配方及其成分的更改](../engineering-change-management/manage-formula-changes.md) |
| 产品信息管理 | [产品准备情况检查](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [产品准备情况](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 每一项增强都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。 如果要使用这些功能中的任何一个，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中明确启用。

| 模块 | 功能管理中的功能名称&nbsp;&nbsp;&nbsp; | 更多信息 |
|---|---|---|
| 主计划 | 针对调整后需求预测的并行授权 | 此功能允许从 **调整后的需求预测** 页并行授权调整后的需求预测。 此功能的目的是在授权大量预测时提高性能。 授权时，用户可以在授权对话中指定 **线程数**。 |
| 主计划 | (预览)计划散装批次订单和包装批次订单的可批处理确认和合并 | 此功能允许您使用批处理作业来确认和合并计划散装订单和包装订单。 |
| 生产控制 | 复制通用工艺路线 | 此功能增强了复制工艺路线功能，允许用户复制不特定于物料的工艺路线。 利用此功能，系统可在复制工艺路线功能用于覆盖尚未分配给物料的工艺路线之后更新所有相关信息（如站点、工艺路线组、资源要求以及不同时间）。 |
| 生产控制 | 在更改工艺路线工序时更新相关的资源要求 | 利用此功能，系统可在用户更改现有工艺路线步骤的工序后更新相关的资源要求。 |
| 产品信息管理 | 预处理物料清单报表以防止超时 | 此功能使物料清单报表被预处理。 当报表具有大量数据负载时，这将避免超时问题。 |
| 采购 | 启用重置与采购相关的工作流 | 此预览功能让您可以将以下工作流重置为草稿状态：采购订单、供应商更改和采购申请。 |
| 运输管理 | 放弃货运帐单时启用创建供应商发票日记帐 | 启用此功能后，仅当您使用支付供应商选项时，才会出于对帐原因创建相应的供应商发票日记帐。 否则，将始终创建发票日记帐。 |
| 仓库管理 | 验证为补货作业选择的模板 | 此功能帮助确保用户在设置补货作业时选择有效的补货模板。 它可以防止用户在没有模板的情况下创建补货作业以及选择 *波次需求* 类型的模板，这不会创建任何补货工作，而且可能需要很长时间来处理。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 它们不一定与上一节中列出的为此版本添加的新功能相关，但是它们可以帮助您从现有功能中获得更多益处。

| 特征区域 | 新增或更新文章 |
|---|---|
| 工程更改管理 | [产品生命周期状态和交易](../engineering-change-management/product-lifecycle-state-transactions.md) |
| 库存管理 | [库存可见性加载项](../inventory/inventory-visibility.md)<br><br>[质量和不符合项管理概览](../inventory/quality-management-processes.md)（以及所有相关的质量管理文章） |
| 采购 | [维护供应商认证](../../finance/public-sector/manage-vendor-certification.md) |
| 生产控制 | [设计生产车间执行界面的样式](../production-control/production-floor-execution-styles.md) |
| 仓库管理 | [为 Warehouse Management 移动应用分配步骤图标和标题](../warehousing/step-icons-titles.md)<br><br>[延期处理手动库存变动](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>财务和运营应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.20 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.20 的平台更新（2021 年 7 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.20 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8)。 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365：2021 发布波次 1 计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365：2021 发布波次 1 计划](/dynamics365-release-plan/2021wave1/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management 中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

