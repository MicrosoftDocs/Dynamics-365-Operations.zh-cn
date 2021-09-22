---
title: 库存评估方法为“标准成本”或“移动平均”时发生更新冲突
description: 库存评估方法为“标准成本”或“移动平均”时发生更新冲突
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475718"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>库存评估方法为“标准成本”或“移动平均”时发生更新冲突

## <a name="symptoms"></a>故障特征

当同时发布如库存日记帐、采购订单发票或销售订单发票等文档以提高可扩展性和性能时，您可能会收到有关更新冲突以及某些文档可能未发布的错误消息。 当库存评估方法为 *标准成本* 或 *移动平均* 时，可能发生此问题。 这两种方法都是永久性成本计算方法。 换言之，最终成本在过帐时确定。

如果您使用的是 *移动平均* 方法，错误消息类似于以下示例：

> 按比例进行费用计算后，库存值 xx.xx 不是预期值

如果您使用的是 *标准成本* 方法，错误消息类似于以下示例：

> 标准成本在更新后与财务库存值不匹配。 值 = xx.xx，数量 = yy.yy，标准成本 = zz.zz

## <a name="workaround"></a>解决方法

在 Microsoft 发布解决此问题的解决方案之前，请考虑使用以下方法来帮助避免或减少这些错误：

- 重新发布失败的文档。
- 创建行数较少的文档。
- 避免在标准成本中使用十进制值。 尝试定义标准成本，让 **价格数量** 字段设置为 *1*。 如果必须指定大于 *1* 的 **价格数量** 值，请尝试最小化单位标准成本中的小数位数。 （理想情况下，小数位数应少于两位。）例如，避免定义标准成本设置，如 **价格** = *10* 和 **价格数量** = *3*，因为它们会产生 3.333333 的单位标准成本（重复十进制值）。
- 在大多数文档中，避免有多个行包含产品和财务库存维度的相同组合。
- 减少并行度。 （这样，您的系统可能会变得更快，因为更新冲突和重试会更少发生。）
