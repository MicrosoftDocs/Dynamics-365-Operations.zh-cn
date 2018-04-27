---
title: "财务绩效 Power BI 内容"
description: "此主题描述财务绩效 Power BI 内容。"
author: kweekley
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1fc3ab4f2a4b4604126ff72c570fc9d85e209f3c
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="financial-performance-power-bi-content"></a>财务绩效 Power BI 内容

[!INCLUDE [banner](../includes/banner.md)]

> [!Note]
> 根据 [Power BI 内容包发布到 PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom) 中的说明，已弃用此内容包。

此主题描述**财务绩效** Microsoft Power BI 内容。 它介绍其中包含的仪表板和报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="main-account-setup"></a>主科目设置
由于组织希望负债和收入金额在报表中显示为正金额，所以设置主科目很重要。 要让这些主科目显示为正金额，必须将主科目类型设置为**负债**或**收入**。 在使用这些科目类型时，通过 Power BI 申报将逆转正负符号，将金额显示为正。

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Power BI 内容中包含的仪表板和报表
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
| 现金分析               | 按法人分类的现金、按季度分类的现金、总现金和按帐户分类的现金<br><br>**注意：**按季度显示的现金信息不包括第一季度总计中的期初余额。 它显示每个季度过帐的新交易记录的总计。|
| 当前比率分析      | 按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额 |
| 速动比率分析        | 按法人分类的速动比率、按季度分类的速动比率和现金、应收账款和当前负债的余额 |
| 所售货物成本分析 | 按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比 |
| 运营资本分析    | 按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额 |
| 资产和负债分析     | 按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债 |
| 利润率分析      | 按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率 |
| 净收入分析         | 按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比 |
| 收入分析           | 按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比 |
| 收入分析            | 总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入 |
| 支出分析            | 总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率 |
| 已计费收入分析     | 总应收账款、按法人分类的总应收账款、按季度分类的总应收账款和应收账款帐户的余额<br><br>**注意：**此信息不包括应收帐款会计科目的期初余额。 它显示过帐到应收账款的新交易记录的总计。 |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
以下实体用作**财务绩效** Power BI 内容的基础：

**聚合数据实体**

- **GeneralLedgerActivities** – 此实体按科目类别聚合总帐余额。
- **BudgetActivities** – 此实体按科目类别聚合预算余额。

**数据实体**

- FiscalCalendars
- MainAccounts
- LegalEntities
- 分类帐
- ChartofAccounts

这些实体用于在数据模型中创建计算度量值。 计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。 默认情况下，内容提供过去三年和未来一年的数据。 若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)。 此工作簿是用于创建内容的默认数据模型。 

