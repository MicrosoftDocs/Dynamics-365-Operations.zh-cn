---
title: 现金流预测设置故障排除
description: 本主题提供对配置现金流预测时可能有的问题的解答。 可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985279"
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

验证实体商店中的“现金流度量 V2”和“LedgerCovLiquidityMeasurement”度量是否已配置。 有关如何使用实体商店中的数据的详细信息，请参阅 [Power BI 与实体商店的集成](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)验证查看 Power BI 内容所需的所有步骤均已完成。 有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。

## <a name="have-the-entity-store-entities-been-refreshed"></a>实体商店实体是否已刷新？

您必须定期刷新您的实体，以确保数据是最新的，而且准确。 要手动刷新特定实体，请转到 **系统管理 \> 设置 \> 实体商店**，选择实体，然后选择 **刷新**。 数据也可以自动更新。 在 **实体商店** 页上，将 **启用自动刷新** 选项设置为 **是**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]