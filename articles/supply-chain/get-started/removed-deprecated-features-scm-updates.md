---
title: Dynamics 365 Supply Chain Management 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Supply Chain Management 中已经删除或计划删除的功能。
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d4d2805e36f132660152370cbeee856862ad6faa
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689511"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

随着记录 Dynamics 365 Supply Chain Management 的已删除或已弃用功能，将更新此主题。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 版本中已经删除或弃用的功能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 的 Internet Explorer 11 支持已弃用

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 所有|
| **状态**                         | 已弃用。 2021 年 8 月之后将不再支持 Internet Explorer 11。|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>将内置的 Supply Chain Management 主计划引擎用于制造方案

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 为了在主计划运行期间提高性能并最大限度减小 SQL 数据库负荷，Planning Optimization 已取代了内置的 Supply Chain Management 主计划引擎。 通过 Planning Optimization，即使在办公时间也可以执行快速计划运行。 这使计划人员可以立即对需求或计划参数的变化做出反应。 |
| **被另一个功能取代？**   | 是的，Planning Optimization 将取代现有的内置 Supply Chain Management 主计划引擎。 |
| **影响的产品区域**         | Supply Chain Management - 主计划 |
| **部署选项**              | 仅限云。 本地部署不支持 Planning Optimization。 |
| **状态**                         | 已弃用。 到 2021 年 10 月 1 日，内置的 Dynamics 365 Supply Chain Management 主计划引擎将不再支持制造方案。 对于制造方案，客户必须将计划优化用于主计划计算。 有关详细信息，请参阅 [Planning Optimization 文档](https://go.microsoft.com/fwlink/?linkid=2105830)。 在 2021 年 10 月之后，在本地部署 Dynamics 365 Supply Chain Management 的客户可以继续将 Supply Chain Management 主计划引擎用于制造方案。 但是，将不再提供其他功能增强。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 版本中已经删除或弃用的功能

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>将内置的 Supply Chain Management 主计划引擎用于分发方案

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 为了在主计划运行期间提高性能并最大限度减小 SQL 数据库负荷，Planning Optimization 已取代了内置的 Supply Chain Management 主计划引擎。 通过 Planning Optimization，即使在办公时间也可以执行快速计划运行。 这使计划人员可以立即对需求或计划参数的变化做出反应。 |
| **被另一个功能取代？**   | 是的，Planning Optimization 将取代现有的内置 Supply Chain Management 主计划引擎。 |
| **影响的产品区域**         | Supply Chain Management - 主计划 |
| **部署选项**              | 仅限云。 本地部署不支持 Planning Optimization。 |
| **状态**                         | 已弃用。 到 2021 年 4 月 1 日，内置的 Dynamics 365 Supply Chain Management 主计划引擎将不再支持分发方案。 对于分发方案，客户必须将 Planning Optimization 用于主计划计算。 有关详细信息，请参阅 [Planning Optimization 文档](https://go.microsoft.com/fwlink/?linkid=2105830)。 在 2021 年 4 月之后，在本地部署 Dynamics 365 Supply Chain Management 的客户可以继续将 Supply Chain Management 主计划引擎用于分发方案。 但是，将不再提供其他功能增强。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明

若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]