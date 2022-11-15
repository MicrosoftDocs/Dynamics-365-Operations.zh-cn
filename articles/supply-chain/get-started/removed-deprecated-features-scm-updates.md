---
title: Dynamics 365 Supply Chain Management 中已删除或弃用的功能
description: 本文介绍 Dynamics 365 Supply Chain Management 中已经删除或计划删除的功能。
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739862"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

随着记录 Dynamics 365 Supply Chain Management 的已删除或已弃用功能，将更新本文。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。

> [!NOTE]
> [技术参考报告](/dynamics/s-e/)中提供了有关财务和运营应用中的对象的详细信息。 可比较这些报告的不同版本，以了解财务和运营应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Supply Chain Management 10.0.29 版本中已经删除或弃用的功能

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>具有转让价格税的存货转移单

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** | [具有转让价格税的存货转移单](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)功能正在被[印度的存货转移单](../../finance/localizations/apac-ind-stock-transfer.md)功能所取代。 |
| **被另一个功能取代？**   | 是，[具有转让价格税的存货转移单](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)功能正在被[印度的存货转移单](../../finance/localizations/apac-ind-stock-transfer.md)功能所取代。 |
| **影响的产品区域** | Supply Chain Management - 库存 |
| **部署选项** | 云和本地 |
| **Status** | <p>正在被弃用。 *具有转让价格税的存货转移单* 功能将不会获得错误修复和安全修复的相关支持。</p><p>2023 年 4 月之后，默认情况下，将要求客户使用改进的功能，即 *印度的存货转移单*。 2023 年 10 月之后，*具有转让价格税的存货转移单* 功能将不再可用，并且将要求客户改用改进的 *印度的存货转移单* 功能。</p><p>有关详细信息，请参阅[印度的存货转移单](../../finance/localizations/apac-ind-stock-transfer.md)。</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Supply Chain Management 10.0.19 版本中已经删除或弃用的功能

### <a name="job-card-device"></a>作业卡设备

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** | [作业卡设备](../production-control/config-job-card-device.md)将被新的[生产车间执行界面](../production-control/production-floor-execution-configure.md)替换。 |
| **被另一个功能取代？**   | 是，[作业卡设备](../production-control/config-job-card-device.md)将被新的[生产车间执行界面](../production-control/production-floor-execution-configure.md)替换。 |
| **影响的产品区域** | Supply Chain Management - 生产控制 |
| **部署选项** | 云和本地 |
| **状态** | 已弃用。 作业卡设备将获得有关错误和安全修复的支持，但将不再提供功能增强。 在 2022 年 4 月之后，将不再支持作业卡设备，并且将要求客户移至新的生产车间执行界面。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Management 10.0.18 版本中已经删除或弃用的功能

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management - 仓库（仓库应用）

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 自 2021 年 4 月起，*Supply Chain Management - 仓库*（仓库应用）将弃用，在 2022 年 4 月之后将不再受支持。 现在它将替换为 *仓库管理移动应用*，该应用随 Supply Chain Management 的版本 10.0.17 一起发布。 新应用是一个完全替代品，但使用相同的基础框架，从而使迁移变得容易。 如果需要，可以并排使用这两个应用，以帮助用户在学习使用新应用时逐渐进行调整。<br><br>有关新仓库管理移动应用的详细信息，请参阅[仓库管理移动应用程序](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)和[安装和连接仓库管理移动应用](../warehousing/install-configure-warehouse-management-app.md)。 |
| **被另一个功能取代？**   | 是，已替换为新的仓库管理移动应用。 |
| **影响的产品区域**         | Supply Chain Management - 仓库应用 |
| **部署选项**              | 云和本地 |
| **状态**                         | 已弃用。 仓库应用将获得有关错误和安全修复的支持，但将不再提供功能增强。 在 2022 年 4 月之后，将不再支持旧仓库应用，并且将要求客户移至新的仓库管理 移动应用。 然后，将从 Microsoft Store 和 Google Play 商店中删除旧仓库应用。  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 版本中已经删除或弃用的功能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 的 Internet Explorer 11 支持已弃用

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 所有|
| **状态**                         | 已弃用。 2021 年 8 月之后将不再支持 Internet Explorer 11。|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>将内置的 Supply Chain Management 主计划引擎用于制造方案

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 为了在主计划运行期间提高性能并最大限度减小 SQL 数据库负荷，Planning Optimization 已取代了内置的 Supply Chain Management 主计划引擎。 通过 Planning Optimization，即使在办公时间也可以执行快速计划运行。 这使计划人员可以立即对需求或计划参数的变化做出反应。 |
| **被另一个功能取代？**   | 是的，Planning Optimization 将取代现有的内置 Supply Chain Management 主计划引擎。 |
| **影响的产品区域**         | Supply Chain Management - 主计划 |
| **部署选项**              | 仅限云。 本地部署不支持 Planning Optimization。 |
| **状态**                         | 已弃用。 到 2022 年 4 月 1 日，内置的 Supply Chain Management 主计划引擎将不再支持制造方案。 从该日期起，Microsoft 将停止对内置计划引擎的制造方案的所有当前开发，不会发布任何新功能，并且将仅发布关键 Bug 修复。 在此日期之后，需要对制造方案提供支持的所有公司都必须使用计划优化以进行主计划计算。 计划优化应该在 2022 年 10 月之前全面支持制造方案。 有关详细信息，请参阅[已弃用的主计划概述](../master-planning/deprecated-master-planning-overview.md)。<br><br>在 2022 年 4 月之后，在本地部署 Supply Chain Management 的公司可以继续将内置主计划引擎用于制造方案。 但是，将不再提供其他功能增强。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 版本中已经删除或弃用的功能

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>将内置的 Supply Chain Management 主计划引擎用于分发方案

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 为了在主计划运行期间提高性能并最大限度减小 SQL 数据库负荷，Planning Optimization 已取代了内置的 Supply Chain Management 主计划引擎。 通过 Planning Optimization，即使在办公时间也可以执行快速计划运行。 这使计划人员可以立即对需求或计划参数的变化做出反应。 |
| **被另一个功能取代？**   | 是的，Planning Optimization 将取代现有的内置 Supply Chain Management 主计划引擎。 |
| **影响的产品区域**         | Supply Chain Management - 主计划 |
| **部署选项**              | 仅限云。 本地部署不支持 Planning Optimization。 |
| **状态**                         | 已弃用。 到 2021 年 4 月 1 日，内置的 Dynamics 365 Supply Chain Management 主计划引擎将不再支持分发方案。 对于分发方案，客户必须将 Planning Optimization 用于主计划计算。 有关详细信息，请参阅[已弃用的主计划概述](../master-planning/deprecated-master-planning-overview.md)。 在 2021 年 4 月之后，在本地部署 Dynamics 365 Supply Chain Management 的客户可以继续将 Supply Chain Management 主计划引擎用于分发方案。 但是，将不再提供其他功能增强。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明

若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

