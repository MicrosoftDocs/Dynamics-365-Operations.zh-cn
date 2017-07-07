---
title: "现金概览 Power BI 内容"
description: "此主题介绍现金概览 Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: saraschi2
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e969c2033463d565ce782c7dc8cfc4b458349289
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017

---

# <a name="cash-overview-power-bi-content"></a>现金概览 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题介绍**现金概览** Microsoft Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**现金概览** Power BI 内容面向负责组织中的现金的人员创建。 **现金概览** Power BI 内容提供对您的现金流量的可见性。 它还提供预测，可以帮助您做出更好的决策并改进您的现金流量的健康状况。 您可按法人、币种和银行帐户分析现金以更好地了解盈余和赤字。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

如果您正在使用 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月更新，则来自**现金概览** Power BI 内容的报表在**现金概览**和**银行管理**工作区显示。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表
下表提供有关在**现金概览** Power BI 内容中的每个报表页找到的指标的详细信息。

| 报告                                | 内容 |
|---------------------------------------|----------|
| 现金概览 - 所有公司         | <ul><li>系统币种的流入量和流出量</li><li>预测币种余额</li><li>系统币种的银行总余额</li><li>按法人分类的余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li></ul> |
| 现金概览 - 当前公司       | <ul><li>记帐币种的流入量和流出量</li><li>预测币种余额</li><li>记帐币种的银行总余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li></ul> |
| 现金流量预测 - 所有公司    | <ul><li>系统币种的流入量和流出量</li><li>每日预测汇总</li><li>预测详细信息</li></ul> |
| 现金流量预测 - 公司币种 | <ul><li>记帐币种的流入量和流出量</li><li>每日预测汇总</li><li>预测详细信息</li></ul> |
| 币种预测                     | <ul><li>预测币种余额</li><li>每日币种汇总</li><li>预测详细信息</li></ul> |
| 银行余额                         | <ul><li>系统币种的银行总余额</li><li>按法人分类的余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li><li>按银行帐户分类的余额</li><li>原币余额</li></ul> |

## <a name="extending-the-power-bi-content"></a>扩展 Power BI 内容
您可以使用在 Lifecycle Services (LCS) 中可用的内容包对未登录到 Dynamics 365 的人员提供出色分析。 您可以修改这些内容包，使它们包含其他报表或视觉对象，然后发布到您的 Power BI.com 租户进行分析。 

可在 LCS 中的共享资产库内找到**现金概览** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

下表显示**现金概览** Power BI 内容所基于的实体。

| 实体                                                                          | 内容 |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | 充当报表筛选依据的公司 |
| LedgerCovLiquidityMeasurement\_Date                                             | 充当报表筛选依据的日期 |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | 实际银行余额与上次预测的银行余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | 预测交易记录详细信息 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | 使用公司记帐币种的汇总的现金流入量、流出量和余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | 使用系统币种的用于所有公司的汇总的现金流入量、流出量和余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | 使用交易币种的汇总的净交易记录金额和币种余额 |

这些实体用于在数据模型中创建计算度量值。 然后，这些计算的度量值用于计算在**现金概览** Power BI 内容中使用的图表和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 Power BI 文件并修改。 此文件是用于创建内容的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容和仪表板。


