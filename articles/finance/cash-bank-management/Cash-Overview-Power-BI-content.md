---
title: 现金概览 Power BI 内容
description: 此主题介绍现金概览 Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。
author: saraschi2
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 59ef57d3684cfa3b7063af76cc7ee7b7f0eaceb5e1f1cceb0845ebd9057ded07
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728071"
---
# <a name="cash-overview-power-bi-content"></a>现金概览 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍 **现金概览** Microsoft Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**现金概览** Power BI 内容面向负责组织中的现金的人员创建。 **现金概览** Power BI 内容提供对您的现金流量的可见性。 它还提供预测，可以帮助您做出更好的决策并改进您的现金流量的健康状况。 您可按法人、币种和银行帐户分析现金以更好地了解盈余和赤字。

## <a name="setup-needed-to-view-power-bi-content"></a>查看 Power BI 内容所需设置

必须完成以下设置，才能在 **现金概览** 和 **银行管理** Power BI 视觉对象中显示数据。

1. 转到 **系统管理 > 设置 > 系统参数** 以设置 **系统币种** 和 **系统汇率**。
2. 转到 **总帐 > 日历 > 会计日历** 验证分配到有效时段的会计日历日期。
3. 转到 **总帐 > 设置 > 分类帐** 以设置 **记帐币种** 和 **汇率类型**。
4. 定义交易币种与记帐币种、记帐币种与系统币种，以记帐币种与银行币种之间的汇率。 方法是，转到 **总帐 > 币种 > 币种汇率**。
5. 配置和运行现金流预测。 有关如何设置现金流预测的详细信息，请参阅[现金流预测](./cash-flow-forecasting.md)。 
6. 转到 **系统管理 > 设置 > 实体商店** 以刷新 **LedgerCovLiquidityMeasurement** 聚合度量。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

来自 **现金概览** Power BI 内容的报表显示在 **现金概览** 和 **银行管理** 工作区。

若要查看带数据的现金流量预测报表，你必须先从“现金和银行管理”区域使用 **计算现金流量预测** 功能运行预测计算流程。 需要为包括在预测中的每个公司完成此操作。  然后，你需刷新 **实体商店** 页上的 LedgerCovLiquidityMeasurement 聚合度量。  

为了演示目的，你可以从演示数据模块使用 **生成数据** 页添加现金流量预测演示数据。  此脚本将数据插入到现金流量预测表以快速填充报表所需的信息。  仅当你在环境上部署演示数据套件模型时，此模块才可用。 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

下表提供有关在 **现金概览** Power BI 内容中的每个报表页找到的指标的详细信息。

| 报表                                | 内容 |
|---------------------------------------|----------|
| 现金概览 - 所有公司         | <ul><li>系统币种的流入量和流出量</li><li>预测币种余额</li><li>系统币种的银行总余额</li><li>按法人分类的余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li></ul> |
| 现金概览 - 当前公司       | <ul><li>记帐币种的流入量和流出量</li><li>预测币种余额</li><li>记帐币种的银行总余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li></ul> |
| 现金流量预测 - 所有公司    | <ul><li>系统币种的流入量和流出量</li><li>每日预测汇总</li><li>预测详细信息</li></ul> |
| 现金流量预测 - 公司币种 | <ul><li>记帐币种的流入量和流出量</li><li>每日预测汇总</li><li>预测详细信息</li></ul> |
| 币种预测                     | <ul><li>预测币种余额</li><li>每日币种汇总</li><li>预测详细信息</li></ul> |
| 银行余额                         | <ul><li>系统币种的银行总余额</li><li>按法人分类的余额</li><li>银行帐户币种的今日实际余额与预测余额比较</li><li>按银行帐户分类的余额</li><li>原币余额</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

下表显示 **现金概览** Power BI 内容所基于的实体。

| 实体                                                                          | 内容 |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | 充当报表筛选依据的公司 |
| LedgerCovLiquidityMeasurement\_Date                                             | 充当报表筛选依据的日期 |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | 实际银行余额与上次预测的银行余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | 预测交易记录详细信息 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | 使用公司记帐币种的汇总的现金流入量、流出量和余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | 使用系统币种的用于所有公司的汇总的现金流入量、流出量和余额 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | 使用交易币种的汇总的净交易记录金额和币种余额 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]