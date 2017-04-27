---
title: "财务绩效 Power BI 内容"
description: "此主题说明访问 Microsoft Power BI 的 Microsoft Dynamics 365 for Operations 财务绩效内容包的位置。 它介绍内容包中包括的仪表板和报表，并提供有关用于构建内容包的数据模型和实体的信息。"
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

# <a name="financial-performance-power-bi-content"></a>财务绩效 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题说明访问 Microsoft Power BI 的 Microsoft Dynamics 365 for Operations 财务绩效内容包的位置。 它介绍内容包中包括的仪表板和报表，并提供有关用于构建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

财务绩效内容包有两个版本。 一个版本可从 Microsoft Dynamics Lifecycle Services (LCS) 获取，另一个版本可从 PowerBI.com 获取。

-   **可从 LCS 获取的版本：**可从 LCS 获取的财务绩效内容包支持 Microsoft Dynamics 365 for Operations 版本 1611。 可在 LCS 中的共用资产库内找到该内容包。 有关如何下载该内容包并将其连接到您的 Microsoft Dynamics 365 for Operations 数据的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。
-   **可从 PowerBI.com 获取的版本：**可从 PowerBI.com 获取的财务绩效内容包支持 Microsoft Dynamics AX 版本 7.0 和 7.0.1。 有关如何连接和加载您的 Dynamics 365 for Operations 数据的详细信息，请参阅[从 PowerBI.com 访问 Power BI 内容](power-bi-home-page.md)。

## <a name="main-account-setup"></a>主科目设置
由于组织希望负债和收入金额在报表中显示为正金额，所以在 Dynamics 365 for Operations 中设置主科目很重要。 要让这些主科目显示为正金额，必须将主科目类型设置为**负债**或**收入**。 在使用这些科目类型时，通过 Microsoft Power BI 申报将逆转正负符号，将金额显示为正。

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>此内容包中包含的仪表板和报表
在连接内容包到您的 Dynamics 365 for Operations 数据后，仪表板和报表将显示您的财务数据。 如果您之前从未使用 Power BI，请可以通过 [Power BI 的指导学习页](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)了解更多相关信息。 仪表板包含基于基础报表的数据的汇总磁贴。 每个磁贴包含组织中所有公司当前年度的汇总信息。 以下是这些磁贴中的一部分：

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

每个磁贴都由支持报表支持。 这些报告包含提供更多信息的图表和表。 下表对报表进行了描述。

| 报表                      | 报表中包含的信息                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 现金分析               | 按法人分类的现金、按季度分类的现金、总现金和按帐户分类的现金 **注释：****按季度分类的现金**报表中的总计内不包含第一季度的期初余额。 它显示每个季度过帐的新交易记录的总计。                                                                                |
| 当前比率分析      | 按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额                                                                                                                                                                                                                              |
| 速动比率分析        | 按法人分类的速动比率、按季度分类的速动比率和现金、应收帐款和当前负债的余额                                                                                                                                                                                                                      |
| 所售货物成本分析 | 按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比                                                                                                                                                                                   |
| 运营资本分析    | 按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额                                                                                                                                                                                                                   |
| 资产和负债分析     | 按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债                                                                                                                                                                                     |
| 利润率分析      | 按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率                                                                                                                                                                                                                       |
| 净收入分析         | 按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比                                                                                                                                                                                                                       |
| 收入分析           | 按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比                                                                                                                                                          |
| 收入分析            | 总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入                                                                                                                                                 |
| 支出分析            | 总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率                                                                                                                                                                 |
| 已计费收入分析     | 应收帐款总计、按法人分类的总应收帐款、按季度分类的总应收帐款和应收帐款帐户的余额 **注释：**报表中不包含应收帐款会计科目的期初余额。 它们显示过帐到应收帐款的新交易记录的总计。 |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
在财务绩效内容包中填充仪表板和报表的数据是 Dynamics 365 for Operations 数据。 以下实体用作内容包的基础：**聚合数据实体**

-   **GeneralLedgerActivities** – 此实体按科目类别聚合总帐余额。
-   **BudgetActivities** – 此实体按科目类别聚合预算余额。

**数据实体**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   分类帐
-   ChartofAccounts

这些实体用于在数据模型中创建计算度量值。 计算的度量值用于计算在数据模型中使用的关键绩效指标 (KPI) 和报表。 默认情况下，内容包提供过去三年和未来一年的数据。 若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)。 此工作簿是用于创建内容包的默认数据模型。 在您完成您的修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)





