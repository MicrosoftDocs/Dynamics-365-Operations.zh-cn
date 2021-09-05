---
title: 内置主计划与计划优化之间的差异
description: 本主题列出了计划优化尚不支持的功能，以及“计划优化适合分析”页面上未列出的功能。
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344946"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>内置主计划与计划优化之间的差异

[!include [banner](../../includes/banner.md)]

计划优化结果可能不同于内置主计划引擎的结果。 这些差异可能是待定功能导致的。 本主题列出了计划优化尚不支持的功能，以及 **[计划优化适合分析](planning-optimization-fit-analysis.md)** 页面]上未列出的功能。

| 功能 | 计划优化中的当前行为 |
|---|---|
| 实际称重产品 | 实际称重产品视为常见产品。|
| 可扩展维度 | 计划订单中的可扩展维度为空，即使选中了 **存储维度组** 或 **跟踪维度组** 页面上的 **按维度的覆盖范围计划** 复选框也不例外。 |
| 筛选的生产运行 | 有关详细信息，请参阅[生产计划 - 筛选器](production-planning.md#filters)。 |
| 预测计划 | 不支持预测计划。 我们建议您使用主计划，在主计划中，预测模型分配给主计划。 |
| 计划订单的编号规则 | 不支持计划订单的编号规则。 计划订单编号在服务端生成。 |
| 计划副本，删除计划和计划版本清除 | <p>已禁用了导航窗格中 **主计划 \> 主计划 \> 维护计划** 下的以下项：</p><ul><li>计划副本</li><li>删除计划</li><li>计划版本清除</li></ul> |
| 退货单 | 不考虑退货单。 |
| 计划相关功能 | 有关详细信息，请参阅[具有无限容量的计划](infinite-capacity-planning.md#limitations)。 |
| 运输日历 | 将忽略 **交货方式** 页面中的 **运输日历** 列。 |

## <a name="additional-resources"></a>其他资源

- [计划优化适应分析](planning-optimization-fit-analysis.md)
- [计划优化未使用的参数](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
