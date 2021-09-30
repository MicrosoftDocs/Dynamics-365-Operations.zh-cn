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
ms.openlocfilehash: 63f3bc6cb7563ee6ff719272a0795efffcb40bc8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500188"
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
| 安全存货履行 | 计划优化始终为 **物料覆盖范围** 页面的 **最小完成量** 字段使用 *今日日期 + 采购时间* 选项。 这将帮助防止不需要的计划订单和其他问题，因为如果安全存货未包括采购时间，为低现有库存量创建的计划订单始终会由于提前期而延迟。 |
| 安全存货限定标准和净要求 | *安全存货* 要求类型将不包括，不会显示在 **净要求** 页面上。 安全存货不代表需求，也没有与之关联的要求日期。 它会对必须始终存在的库存量设置约束。 但是，在主计划期间计算计划订单时仍会考虑 **最小** 字段值。 我们建议您检查 **净要求** 页面的 **累计数量** 列，查看是否考虑了此值。 |
| 运输日历 | 将忽略 **交货方式** 页面中的 **运输日历** 列。 |

## <a name="additional-resources"></a>其他资源

- [计划优化适应分析](planning-optimization-fit-analysis.md)
- [计划优化未使用的参数](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
