---
title: Financial Performance Power BI content
description: "此主题描述工序财务业绩内容包的 Microsoft Dynamics 365 Microsoft Power BI 的。 该描述在内容包包括的面板 (其中和报表，并且提供有关用于创建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Financial Performance Power BI content

此主题描述工序财务业绩内容包的 Microsoft Dynamics 365 Microsoft Power BI 的。 该描述在内容包包括的面板 (其中和报表，并且提供有关用于创建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

财务业绩内容包的两个版本。可用。 一版本从 Microsoft Dynamics Lifecycle Services (LCS) 获取，其他从 PowerBI.com 获取。

-   ** LCS 从可用的版本：** LCS 从可用的财务业绩内容包版本支持工序 365 的 Microsoft Dynamics 1611。 您可以找到内容包 LCS 中的份额资产的库中。 有关如何下载内容包和将它连接的详细信息。您的工序数据的 Microsoft Dynamics 365，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)
-   ** PowerBI.com 从可用的版本：** PowerBI.com 从可用的财务业绩内容包支持 Microsoft Dynamics AX 为版本 PowerBI.com 和 7.0.1。 有关连接方式和加载您的运营有关的数据 Dynamics 365 的详细信息，请参阅访问 PowerBI.com [] (从的主 page.md BI 的 Power BI 的内容。)

## <a name="main-account-setup"></a>主科目设置
由于要组织负债和收入金额在报表中显示为正金额，主科目的设置在 Dynamics 365 的工序的很重要。 为使这些主科目显示为正金额，则必须设置主科目类型**或负债** ** **收入。 在使用这些科目类型，报表通过 Microsoft Power BI 和查看要反转符号金额为正。

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>在内容包包括的面板 (其中和报表
在连接内容包到您的 Dynamics 365 for Operations 数据后，仪表板和报表将显示您的财务数据。 如果您选择"从不使用 Power BI "，您可以了解在此{{对：about}}引导了解 Power BI 的 [] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) 页。 仪表板包含基于基础报表的数据的汇总磁贴。 每个磁贴包含组织中所有公司当前年度的汇总信息。 这是某些平铺：

-   现金
-   本年收入总额
-   本年支出总额
-   本年度净收入
-   速动比率
-   按科目类别划分的本年度总支出
-   当前比率
-   债务总资产比
-   实际与预测收入
-   本年已计费收入
-   本年度运营费用比率
-   本年度利润率
-   实际与预算支出 – 所有公司

每个平铺按一个支持的报表使用。 这些报告包含提供更多信息的图表和表。 下表对报表进行了描述。

| 报表                      | 报表中包含的信息                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 现金分析               | 按法人的按季度的现金，现金，总现金和按帐户**注释：** **按季度的现金**不包括在报表合计的期初余额将的。 它显示在每个季度的新合计过帐的交易记录。                                                                                |
| 当前比率分析      | 按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额                                                                                                                                                                                                                              |
| 速动比率分析        | 按速动法人的比率，按季度的现金、应收帐款和负债中的当前速动比率和余额                                                                                                                                                                                                                      |
| 所售货物成本分析 | 按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比                                                                                                                                                                                   |
| 运营资本分析    | 按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额                                                                                                                                                                                                                   |
| 资产和负债分析     | 按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债                                                                                                                                                                                     |
| 利润率分析      | 按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率                                                                                                                                                                                                                       |
| 净收入分析         | 按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比                                                                                                                                                                                                                       |
| 收入分析           | 按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比                                                                                                                                                          |
| 收入分析            | 总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入                                                                                                                                                 |
| 支出分析            | 总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率                                                                                                                                                                 |
| 已计费收入分析     | 应收帐款的合计科目，合计科目由应收法人，应收帐款帐户的**注释合计科目应收按季度和余额：**报表不包括应收帐款会计科目的期初余额。 它们过帐到显示应收帐款的新合计的交易记录。 |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
填充此字段：时，会仪表板和报表。财务业绩内容打包的数据是 Dynamics 365 的工序数据。 使用的实体，以下内容包的基础：**聚合数据实体**

-   ** –此 GeneralLedgerActivities **实体按科目类别聚合总帐余额。
-   ** –此 BudgetActivities **实体按科目类别预算余额合计。

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   分类帐
-   ChartofAccounts

这些实体用于创建在数据模型的计算度量值。 计算度量值用于计算在内容包的关键绩效指标 (KPI) 和报表。 默认情况下，内容包提供过去三年和未来一年的数据。 若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)。 此工作簿是用于创建内容包的默认数据模型。 在您完成您的修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)



