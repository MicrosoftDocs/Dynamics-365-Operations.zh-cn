---
title: 库存值/帐龄报表与其存储版本之间的功能空白
description: 库存值/帐龄报表与其存储版本之间的功能空白
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686644"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>库存值/帐龄报表与其存储版本之间的功能空白

[库龄报表存储](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage)和[库存值存储报表](/dynamics365/supply-chain/cost-management/inventory-value-report-storage)功能让 Supply Chain Management 可以显示大量库存交易。 在每种情况下，都会保存报表结果以供浏览和导出，这与这些报表的非存储版本不同。 但是，这些报表的非存储版本中存在的某些功能在存储版本中不存在。 以下小节总结了存在的差异并提供了解决方法。

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>存储报表不包括小计，即使在报表布局中启用了小计

小计可能会在导出结果时导致问题，尤其是在用户更改记录序列时。

要检查小计，可以将结果导出到 Microsoft Excel。 或者，如果您要在 Supply Chain Management 中检查小计，请使用 [功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)启用 *新网格控件* 和 *在网格中分组* 功能，这提供了一种更加灵活的方式来按列查看任何组的小计。 有关详细信息，请参阅[网格功能](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities)。

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>库存值存储报表不支持会计科目信息

您可以运行试算平衡表来获取库存科目余额并将其与 **库存值存储** 报表进行比较。
