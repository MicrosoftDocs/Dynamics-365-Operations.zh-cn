---
title: 财务绩效 PowerBI.com 解决方案
description: 本文描述财务绩效 PowerBI.com 解决方案。
author: kweekley
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b6fb9643873178f1cb93e3da15e83598af51de0
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109541"
---
# <a name="financial-performance-powerbicom-solution"></a>财务绩效 PowerBI.com 解决方案

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 根据[财务和运营的移除或弃用功能](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource)中的说明，已弃用此 PowerBI.com 解决方案。

本文描述 **财务绩效** PowerBI.com 解决方案。 它介绍其中包含的仪表板和报表，并提供有关用于构建解决方案的数据模型和实体的信息。

## <a name="main-account-setup"></a>主科目设置
由于组织希望负债和收入金额在报表中显示为正金额，所以设置主科目很重要。 要让这些主科目显示为正金额，必须将主科目类型设置为 **负债** 或 **收入**。 在使用这些科目类型时，通过 Power BI 申报将逆转正负符号，将金额显示为正。

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>PowerBI.com 解决方案中包含的仪表板和报表
仪表板包含基于基础报表的数据的汇总磁贴。 每个磁贴包含组织中所有公司当前年度的汇总信息。 以下是这些磁贴中的一部分：

- 现金
- 本年收入总额
- 本年支出总额
- 本年度净收入
- 速动比率
- 按科目类别划分的本年度总支出
- 当前比率
- 债务总资产比
- 实际与预测收入
- 本年已计费收入
- 本年度运营费用比率
- 本年度利润率
- 实际与预算支出 – 所有公司

每个磁贴都由支持报表支持。 这些报告包含提供更多信息的图表和表。 下表对报表进行了描述。

| 报表                      | 报表中包含的信息 |
|-----------------------------|--------------------------------------|
| 现金分析               | 按法人分类的现金、按季度分类的现金、总现金和按帐户分类的现金<blockquote>[!NOTE] 按季度显示的现金信息不包括第一季度总计中的期初余额。 它显示每个季度过帐的新交易记录的总计。</blockquote> |
| 当前比率分析      | 按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额 |
| 速动比率分析        | 按法人分类的速动比率、按季度分类的速动比率和现金、应收帐款和当前负债的余额 |
| 所售货物成本分析 | 按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比 |
| 运营资本分析    | 按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额 |
| 资产和负债分析     | 按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债 |
| 利润率分析      | 按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率 |
| 净收入分析         | 按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比 |
| 收入分析           | 按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比 |
| 收入分析            | 总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入 |
| 支出分析            | 总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率 |
| 已计费收入分析     | 总应收帐款、按法人分类的总应收帐款、按季度分类的总应收帐款和应收帐款帐户的余额<blockquote>[!NOTE] 此信息不包括应收帐款会计科目的期初余额。 它显示过帐到应收帐款的新交易记录的总计。</blockquote> |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
以下实体用作 **财务绩效** PowerBI.com 解决方案的基础：

**聚合数据实体**

- **GeneralLedgerActivities** – 此实体按科目类别聚合总帐余额。
- **BudgetActivities** – 此实体按科目类别聚合预算余额。

**数据实体**

- FiscalCalendars
- MainAccounts
- LegalEntities
- 分类帐
- ChartofAccounts

这些实体用于在数据模型中创建计算度量值。 计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。 默认情况下，内容提供过去三年和未来一年的数据。 若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](/dynamics/s-e/)。 此工作簿是用于创建内容的默认数据模型。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
