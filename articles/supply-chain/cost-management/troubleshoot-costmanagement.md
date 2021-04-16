---
title: 成本管理疑难解答
description: 此主题介绍如何解决使用成本管理时可能遇到的问题。
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834281"
---
# <a name="troubleshoot-cost-management"></a>成本管理疑难解答

此主题介绍如何解决使用成本管理时可能遇到的问题。

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>库存值/帐龄报表与其存储版本之间的功能空白

[库龄报表存储](inventory-aging-report-storage.md)和[库存值存储报表](inventory-value-report-storage.md)功能让 Supply Chain Management 可以显示大量库存交易。 在每种情况下，都会保存报表结果以供浏览和导出，这与这些报表的非存储版本不同。 但是，这些报表的非存储版本中存在的某些功能在存储版本中不存在。 以下小节总结了存在的差异并提供了解决方法。

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>存储报表不包括小计，即使在报表布局中启用了小计

小计可能会在导出结果时导致问题，尤其是在用户更改记录序列时。

要检查小计，可以将结果导出到 Microsoft Excel。 或者，如果您要在 Supply Chain Management 中检查小计，请使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用 *新网格控件* 和 *在网格中分组* 功能，这提供了一种更加灵活的方式来按列查看任何组的小计。 有关详细信息，请参阅[网格功能](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md)。

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

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>当库存评估方法为“标准成本”或“移动平均”时，发生更新冲突

当同时发布如库存日记帐、采购订单发票或销售订单发票等文档以提高可扩展性和性能时，您可能会收到有关更新冲突以及某些文档可能未发布的错误消息。 当库存评估方法为 *标准成本* 或 *移动平均* 时，可能发生此问题。 这两种方法都是永久性成本计算方法。 换言之，最终成本在过帐时确定。

如果您使用的是 *移动平均* 方法，错误消息类似于以下示例：

> 按比例进行费用计算后，库存值 xx.xx 不是预期值

如果您使用的是 *标准成本* 方法，错误消息类似于以下示例：

> 标准成本在更新后与财务库存值不匹配。 值 = xx.xx，数量 = yy.yy，标准成本 = zz.zz

在 Microsoft 发布解决此问题的解决方案之前，请考虑使用以下方法来帮助避免或减少这些错误：

- 重新发布失败的文档。
- 创建行数较少的文档。
- 避免在标准成本中使用十进制值。 尝试定义标准成本，让 **价格数量** 字段设置为 *1*。 如果必须指定大于 *1* 的 **价格数量** 值，请尝试最小化单位标准成本中的小数位数。 （理想情况下，小数位数应少于两位。）例如，避免定义标准成本设置，如 **价格** = *10* 和 **价格数量** = *3*，因为它们会产生 3.333333 的单位标准成本（重复十进制值）。
- 在大多数文档中，避免有多个行包含产品和财务库存维度的相同组合。
- 减少并行度。 （这样，您的系统可能会变得更快，因为更新冲突和重试会更少发生。）


[!INCLUDE[footer-include](../../includes/footer-banner.md)]