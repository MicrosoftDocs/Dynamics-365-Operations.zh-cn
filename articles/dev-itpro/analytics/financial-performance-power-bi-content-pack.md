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
ms.sourcegitcommit: 7b5c4428c8610a7b2d4cf1a28287ba2bb1f9c2ea
ms.openlocfilehash: b7cb5f2096f0be5211024fc6ecbfaa61d6c48c9a
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---

# <a name="financial-performance-power-bi-content"></a><span data-ttu-id="2ff9c-103">财务绩效 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="2ff9c-103">Financial performance Power BI content</span></span>

[!include[banner](../includes/banner.md)]

> [!Note]
> <span data-ttu-id="2ff9c-104">根据 [Power BI 内容包发布到 PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom) 中的说明，已弃用此内容包。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-104">This content pack has been deprecated as documented in [Power BI content packs published to PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).</span></span>

<span data-ttu-id="2ff9c-105">此主题描述**财务绩效** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-105">This topic describes the **Financial performance** Microsoft Power BI content.</span></span> <span data-ttu-id="2ff9c-106">它介绍其中包含的仪表板和报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="2ff9c-107">主科目设置</span><span class="sxs-lookup"><span data-stu-id="2ff9c-107">Main account setup</span></span>
<span data-ttu-id="2ff9c-108">由于组织希望负债和收入金额在报表中显示为正金额，所以设置主科目很重要。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-108">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="2ff9c-109">要让这些主科目显示为正金额，必须将主科目类型设置为**负债**或**收入**。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-109">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="2ff9c-110">在使用这些科目类型时，通过 Power BI 申报将逆转正负符号，将金额显示为正。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-110">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="2ff9c-111">Power BI 内容中包含的仪表板和报表</span><span class="sxs-lookup"><span data-stu-id="2ff9c-111">Dashboard and reports that are included in the Power BI content</span></span>
<span data-ttu-id="2ff9c-112">仪表板包含基于基础报表的数据的汇总磁贴。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-112">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="2ff9c-113">每个磁贴包含组织中所有公司当前年度的汇总信息。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-113">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="2ff9c-114">以下是这些磁贴中的一部分：</span><span class="sxs-lookup"><span data-stu-id="2ff9c-114">Here are some of the tiles:</span></span>

- <span data-ttu-id="2ff9c-115">现金</span><span class="sxs-lookup"><span data-stu-id="2ff9c-115">Cash</span></span>
- <span data-ttu-id="2ff9c-116">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-116">Total Revenue this year</span></span>
- <span data-ttu-id="2ff9c-117">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-117">Total Expenses this year</span></span>
- <span data-ttu-id="2ff9c-118">本年度净收入</span><span class="sxs-lookup"><span data-stu-id="2ff9c-118">Net Income this year</span></span>
- <span data-ttu-id="2ff9c-119">速动比率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-119">Quick Ratio</span></span>
- <span data-ttu-id="2ff9c-120">按科目类别划分的本年度总支出</span><span class="sxs-lookup"><span data-stu-id="2ff9c-120">Total Expenses this year by account category</span></span>
- <span data-ttu-id="2ff9c-121">当前比率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-121">Current Ratio</span></span>
- <span data-ttu-id="2ff9c-122">债务总资产比</span><span class="sxs-lookup"><span data-stu-id="2ff9c-122">Debt to Total Assets</span></span>
- <span data-ttu-id="2ff9c-123">实际与预测收入</span><span class="sxs-lookup"><span data-stu-id="2ff9c-123">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="2ff9c-124">本年已计费收入</span><span class="sxs-lookup"><span data-stu-id="2ff9c-124">Billed Revenue this Year</span></span>
- <span data-ttu-id="2ff9c-125">本年度运营费用比率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-125">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="2ff9c-126">本年度利润率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-126">Profit Margin this year</span></span>
- <span data-ttu-id="2ff9c-127">实际与预算支出 – 所有公司</span><span class="sxs-lookup"><span data-stu-id="2ff9c-127">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="2ff9c-128">每个磁贴都由支持报表支持。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-128">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="2ff9c-129">这些报告包含提供更多信息的图表和表。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-129">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="2ff9c-130">下表对报表进行了描述。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-130">The following table describes the reports.</span></span>

| <span data-ttu-id="2ff9c-131">报表</span><span class="sxs-lookup"><span data-stu-id="2ff9c-131">Report</span></span>                      | <span data-ttu-id="2ff9c-132">报表中包含的信息</span><span class="sxs-lookup"><span data-stu-id="2ff9c-132">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="2ff9c-133">现金分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-133">Cash Analysis</span></span>               | <span data-ttu-id="2ff9c-134">按法人分类的现金、按季度分类的现金、总现金和按帐户分类的现金</span><span class="sxs-lookup"><span data-stu-id="2ff9c-134">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE]<br><span data-ttu-id="2ff9c-135">按季度显示的现金信息不包括第一季度总计中的期初余额。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-135">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="2ff9c-136">它显示每个季度过帐的新交易记录的总计。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-136">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="2ff9c-137">当前比率分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-137">Current Ratio Analysis</span></span>      | <span data-ttu-id="2ff9c-138">按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-138">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="2ff9c-139">速动比率分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-139">Quick Ratio Analysis</span></span>        | <span data-ttu-id="2ff9c-140">按法人分类的速动比率、按季度分类的速动比率和现金、应收账款和当前负债的余额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-140">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="2ff9c-141">所售货物成本分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-141">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="2ff9c-142">按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比</span><span class="sxs-lookup"><span data-stu-id="2ff9c-142">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="2ff9c-143">运营资本分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-143">Working Capital Analysis</span></span>    | <span data-ttu-id="2ff9c-144">按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-144">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="2ff9c-145">资产和负债分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-145">Asset and Debt Analysis</span></span>     | <span data-ttu-id="2ff9c-146">按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债</span><span class="sxs-lookup"><span data-stu-id="2ff9c-146">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="2ff9c-147">利润率分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-147">Profit Margin Analysis</span></span>      | <span data-ttu-id="2ff9c-148">按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-148">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="2ff9c-149">净收入分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-149">Net Income Analysis</span></span>         | <span data-ttu-id="2ff9c-150">按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比</span><span class="sxs-lookup"><span data-stu-id="2ff9c-150">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="2ff9c-151">收入分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-151">Earnings Analysis</span></span>           | <span data-ttu-id="2ff9c-152">按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比</span><span class="sxs-lookup"><span data-stu-id="2ff9c-152">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="2ff9c-153">收入分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-153">Revenue Analysis</span></span>            | <span data-ttu-id="2ff9c-154">总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入</span><span class="sxs-lookup"><span data-stu-id="2ff9c-154">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="2ff9c-155">支出分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-155">Expense Analysis</span></span>            | <span data-ttu-id="2ff9c-156">总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率</span><span class="sxs-lookup"><span data-stu-id="2ff9c-156">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="2ff9c-157">已计费收入分析</span><span class="sxs-lookup"><span data-stu-id="2ff9c-157">Billed Revenue Analysis</span></span>     | <span data-ttu-id="2ff9c-158">总应收账款、按法人分类的总应收账款、按季度分类的总应收账款和应收账款帐户的余额</span><span class="sxs-lookup"><span data-stu-id="2ff9c-158">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE]<br><span data-ttu-id="2ff9c-159">此信息不包括应收账款会计科目的期初余额。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-159">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="2ff9c-160">它显示过帐到应收账款的新交易记录的总计。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-160">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="2ff9c-161">所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-161">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="2ff9c-162">有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-162">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="2ff9c-163">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="2ff9c-163">Understanding the data model and entities</span></span>
<span data-ttu-id="2ff9c-164">以下实体用作**财务绩效** Power BI 内容的基础：</span><span class="sxs-lookup"><span data-stu-id="2ff9c-164">The following entities were used as the basis of the **Financial performance** Power BI content:</span></span>

<span data-ttu-id="2ff9c-165">**聚合数据实体**</span><span class="sxs-lookup"><span data-stu-id="2ff9c-165">**Aggregate data entities**</span></span>

- <span data-ttu-id="2ff9c-166">**GeneralLedgerActivities** – 此实体按科目类别聚合总帐余额。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-166">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="2ff9c-167">**BudgetActivities** – 此实体按科目类别聚合预算余额。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-167">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="2ff9c-168">**数据实体**</span><span class="sxs-lookup"><span data-stu-id="2ff9c-168">**Data entities**</span></span>

- <span data-ttu-id="2ff9c-169">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="2ff9c-169">FiscalCalendars</span></span>
- <span data-ttu-id="2ff9c-170">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="2ff9c-170">MainAccounts</span></span>
- <span data-ttu-id="2ff9c-171">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="2ff9c-171">LegalEntities</span></span>
- <span data-ttu-id="2ff9c-172">分类帐</span><span class="sxs-lookup"><span data-stu-id="2ff9c-172">Ledgers</span></span>
- <span data-ttu-id="2ff9c-173">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="2ff9c-173">ChartofAccounts</span></span>

<span data-ttu-id="2ff9c-174">这些实体用于在数据模型中创建计算度量值。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-174">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="2ff9c-175">计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-175">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="2ff9c-176">默认情况下，内容提供过去三年和未来一年的数据。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-176">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="2ff9c-177">若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-177">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span></span> <span data-ttu-id="2ff9c-178">此工作簿是用于创建内容的默认数据模型。</span><span class="sxs-lookup"><span data-stu-id="2ff9c-178">This workbook is the default data model that was used to create the content.</span></span> 

