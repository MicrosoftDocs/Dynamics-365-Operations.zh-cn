---
title: 现金流预测设置故障排除
description: 本主题提供对配置现金流预测时可能有的问题的解答。 可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e2b5a8df84ff5159a85526251a6367857afa1808
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724561"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>现金流预测设置故障排除

[!include [banner](../includes/banner.md)]

本主题提供对配置现金流预测时可能有的问题的解答。 可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>为什么只显示一个法人的现金流？

现金流预测是按法人配置和计算的。 Power BI 报表和 Finance insights 中的现金流预测功能显示结果。

必须为您要查看其预测的每个法人设置现金流预测。 查看所有法人中现金流预测的配置。 或者，查看所有法人的现金流预测的配置，确保其已按照您的期望设置。

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>为什么 Power BI 不显示所有现金流数据？

必须先完成几个步骤，现金流预测才能显示在 Power BI 视图中。 查看以下清单，确保每个步骤均已完成：

- 为每个法人设置现金流。
- 在总帐参数中，设置系统货币和系统汇率类型。
- 设置分类帐会计货币和汇率类型。
- 输入交易货币和会计货币之间的汇率。
- 输入会计货币和系统货币之间的汇率。
- 输入会计货币和每个银行货币之间的汇率。

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>为什么现金流 Power BI 在以前的版本中工作，但现在是空白的？

验证实体商店中的“现金流度量 V2”和“LedgerCovLiquidityMeasurement”度量是否已配置。 有关如何使用实体商店中的数据的详细信息，请参阅 [Power BI 与实体商店的集成](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)。 验证查看 Power BI 内容所需的所有步骤均已完成。 有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。

## <a name="have-the-entity-store-entities-been-refreshed"></a>实体商店实体是否已刷新？

您必须定期刷新您的实体，以确保数据是最新的，而且准确。 要手动刷新特定实体，请转到 **系统管理 \> 设置 \> 实体商店**，选择实体，然后选择 **刷新**。 数据也可以自动更新。 在 **实体商店** 页上，将 **启用自动刷新** 选项设置为 **是**。

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>计算现金流量预测时应使用哪种计算方法？

有两个重要的现金流量预测计算方法选项可供选择。 **新** 选项将计算新单据和自上一批处理作业运行以来更改的单据的现金流量预测。 此选项往往运行更快，因为它处理较小的单据子集。 **总计** 选项将重新计算系统中每个单据的现金流量预测。 此选项花费更多时间，因为它需要完成更多工作。

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>如何提高现金流量预测定期批处理作业的性能？

我们建议您每天在非高峰时段使用 **新** 计算方法运行现金流量预测一次。 我们建议每周六天使用此方法。 然后，每周在活动量最少的一天使用 **总计** 计算方法运行现金流量预测一次。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

