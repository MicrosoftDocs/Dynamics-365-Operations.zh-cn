---
title: 成本管理疑难解答
description: 此主题介绍如何解决使用成本管理时可能遇到的问题。
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4423443"
---
# <a name="troubleshoot-cost-management"></a>成本管理疑难解答

此主题介绍如何解决使用成本管理时可能遇到的问题。

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>库存值/帐龄报表与其存储版本之间的功能空白

[库龄报表存储](inventory-aging-report-storage.md)和[库存值存储报表](inventory-value-report-storage.md)功能让 Supply Chain Management 可以显示大量库存交易。 在每种情况下，都会保存报表结果以供浏览和导出，这与这些报表的非存储版本不同。 但是，这些报表的非存储版本中存在的某些功能在存储版本中不存在。 以下小节总结了存在的差异并提供了解决方法。

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>存储报表不包括小计，即使在报表布局中启用了小计

小计可能会在导出结果时导致问题，尤其是在用户更改记录序列时。

要检查小计，可以将结果导出到 Microsoft Excel。 或者，如果您要在 Supply Chain Management 中检查小计，请使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用 *新网格控件* 和 *(预览)在网格中分组* 功能，这提供了一种更加灵活的方式来按列查看任何一个组的小计。 有关详细信息，请参阅[网格功能](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md)。

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>库存值存储报表不支持会计科目信息

您可以运行试算平衡表来获取库存科目余额并将其与 **库存值存储** 报表进行比较。

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>在不结转库存的情况下更改分类帐期间状态时会显示警告或错误

Microsoft 引入了以下验证，以防止由于围绕成本计算的不正确期间结束流程而导致的问题。 如果遇到以下任何错误消息，请参阅 [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) 了解如何解决这些问题的详细信息。

- 您将要执行日期为 %1 (10-02-2019) 的重新计算。 上次登记的重新计算已在日期为 %2 (20-01-2019) 的上一个期间内执行。 其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。 请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

- 您即将将分类帐期间 %1 的状态更改为 %2。 其日期 %3 与期间结束匹配的库存结转未执行已登记。 请在更改状态之前在与期间结束匹配的 %3 前执行库存结转。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。 从法人 %4 报告。 现在，它只是提供信息，但将来会要求您执行此类操作。

- 科目结构 %1 已更改。 一个或多个主科目 %2 不再存在。 这些主科目是日期为 %4 的 %3 所需要的。 请先将这些主科目添加到科目结构 %1 中，然后才能继续 %3 作业。 现在，它只是提供信息，但将来会要求您执行此类操作。

- 您将要执行日期为 %1 (31-01-2019) 的库存结转。 其日期 %2 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算未执行已登记。 请记住执行其日期 %3 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

- 您将要执行日期为 %1 (28-02-2019) 的倒冲成本计算法计算。 上次登记的倒冲成本计算法计算已在日期为 %2 (31-01-2019) 的上一个期间内执行。 其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。
请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。 执行库存结转之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

## <a name="inventory-aging-report-discrepancies"></a>库龄报表差异

**库龄报表** 在不同的存储维度（如站点或仓库）查看时，显示不同的值。 有关报告逻辑的详细信息，请参阅[库龄报表示例和逻辑](inventory-aging-report.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]