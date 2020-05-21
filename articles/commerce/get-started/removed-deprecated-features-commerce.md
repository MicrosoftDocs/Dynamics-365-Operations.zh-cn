---
title: Dynamics 365 Commerce 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335268"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

本主题介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。

- *已移除*的功能在产品中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 版本中已经删除或弃用的功能
### <a name="pos-operation-803---picking-and-receiving"></a>POS 操作 803 - 领料和接收
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 由于重新设计了新的操作，因此不建议执行领料和接收操作。 |
| **被另一个功能取代？**   | 是。 它被以下两个新的 POS 操作取代：入站操作 (804) 和出站操作 (805)。|
| **影响的产品区域**         | 销售点 (POS) 应用程序 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.10 开始，领料和接收操作将不再接收任何新功能更新。 在将来的版本中，将仅对此操作进行重要的 bug 修复。 鼓励所有客户迁移到新的[入站操作](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)和[出站操作](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)，它们将继续成为我们长期产品路线图的一部分。 |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 版本中已经删除或弃用的功能
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities 和 GetAvailableInventoryNearby API
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 已创建优化的新 API，以取代 GetProductAvailabilities 和 GetAvailableInventoryNearby API。 |
| **被另一个功能取代？**   | 是：它已被 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API 所取代。 |
| **影响的产品区域**         | 电子商务应用程序 SDK |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.7 开始，将不再对 GetProductAvailabilities 和 GetAvailableInventoryNearby 进行工程投资。 在电子商务部署中使用这些 API 的组织应转换为新的 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API，并启用[优化的产品可用性计算功能](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels)。  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)。
