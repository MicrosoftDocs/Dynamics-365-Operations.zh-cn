---
title: "财务绩效 Power BI 内容"
description: "此主题描述财务绩效 Power BI 内容。 它介绍其中包含的仪表板和报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: kweekley
manager: AnnBe
ms.date: 12/01/2017
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
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 3638f5acf6a05ec419dc4308e861d95f0d7b2cea
ms.contentlocale: zh-cn
ms.lasthandoff: 12/01/2017

---

# <a name="financial-performance-power-bi-content"></a><span data-ttu-id="37cf3-104">财务绩效 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="37cf3-104">Financial performance Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37cf3-105">此主题描述**财务绩效** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="37cf3-105">This topic describes the **Financial performance** Microsoft Power BI content.</span></span> <span data-ttu-id="37cf3-106">它介绍其中包含的仪表板和报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="37cf3-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="37cf3-107">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="37cf3-107">Accessing the Power BI content</span></span>

<span data-ttu-id="37cf3-108">您可以从 Microsoft Dynamics Lifecycle Services (LCS) 和 PowerBI.com 访问**财务绩效** Power BI。</span><span class="sxs-lookup"><span data-stu-id="37cf3-108">You can access the **Financial performance** Power BI from Microsoft Dynamics Lifecycle Services (LCS) and from PowerBI.com.</span></span>

### <a name="available-from-lcs"></a><span data-ttu-id="37cf3-109">从 LCS 获取</span><span class="sxs-lookup"><span data-stu-id="37cf3-109">Available from LCS</span></span>
<span data-ttu-id="37cf3-110">从 LCS 获取的**财务绩效** Power BI 内容支持以下版本：</span><span class="sxs-lookup"><span data-stu-id="37cf3-110">The **Financial performance** Power BI content that is available from LCS supports the following versions:</span></span>

- <span data-ttu-id="37cf3-111">Microsoft Dynamics 365 for Finance and Operations Enterprise edition 版本</span><span class="sxs-lookup"><span data-stu-id="37cf3-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition versions</span></span>
- <span data-ttu-id="37cf3-112">Microsoft Dynamics 365 for Operations 版本 1611</span><span class="sxs-lookup"><span data-stu-id="37cf3-112">Microsoft Dynamics 365 for Operations version 1611</span></span> 

<span data-ttu-id="37cf3-113">您可以在 LCS 中的共享资产库内找到 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="37cf3-113">You can find the Power BI content in the Shared asset library in LCS.</span></span> <span data-ttu-id="37cf3-114">有关如何下载内容包并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。</span><span class="sxs-lookup"><span data-stu-id="37cf3-114">For more information about how to download the content pack and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="37cf3-115">若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。</span><span class="sxs-lookup"><span data-stu-id="37cf3-115">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

### <a name="available-from-powerbicom"></a><span data-ttu-id="37cf3-116">从 PowerBI.com 获取</span><span class="sxs-lookup"><span data-stu-id="37cf3-116">Available from PowerBI.com</span></span>
<span data-ttu-id="37cf3-117">从 PowerBI.com 获取的**财务绩效** Power BI 内容支持 Microsoft Dynamics AX 版本 7.0 和 7.0.1。</span><span class="sxs-lookup"><span data-stu-id="37cf3-117">The **Financial performance** Power BI content that is available from PowerBI.com supports Microsoft Dynamics AX versions 7.0 and 7.0.1.</span></span> <span data-ttu-id="37cf3-118">有关如何连接和加载您的 Dynamics AX 数据的详细信息，请参阅 [从 PowerBI.com 访问 Power BI 内容](power-bi-home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="37cf3-118">For more information about how to connect and load your Dynamics AX data, see [Access Power BI content from PowerBI.com](power-bi-home-page.md).</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="37cf3-119">主科目设置</span><span class="sxs-lookup"><span data-stu-id="37cf3-119">Main account setup</span></span>
<span data-ttu-id="37cf3-120">由于组织希望负债和收入金额在报表中显示为正金额，所以设置主科目很重要。</span><span class="sxs-lookup"><span data-stu-id="37cf3-120">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="37cf3-121">要让这些主科目显示为正金额，必须将主科目类型设置为**负债**或**收入**。</span><span class="sxs-lookup"><span data-stu-id="37cf3-121">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="37cf3-122">在使用这些科目类型时，通过 Power BI 申报将逆转正负符号，将金额显示为正。</span><span class="sxs-lookup"><span data-stu-id="37cf3-122">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="37cf3-123">Power BI 内容中包含的仪表板和报表</span><span class="sxs-lookup"><span data-stu-id="37cf3-123">Dashboard and reports that are included in the Power BI content</span></span>
<span data-ttu-id="37cf3-124">仪表板包含基于基础报表的数据的汇总磁贴。</span><span class="sxs-lookup"><span data-stu-id="37cf3-124">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="37cf3-125">每个磁贴包含组织中所有公司当前年度的汇总信息。</span><span class="sxs-lookup"><span data-stu-id="37cf3-125">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="37cf3-126">以下是这些磁贴中的一部分：</span><span class="sxs-lookup"><span data-stu-id="37cf3-126">Here are some of the tiles:</span></span>

- <span data-ttu-id="37cf3-127">现金</span><span class="sxs-lookup"><span data-stu-id="37cf3-127">Cash</span></span>
- <span data-ttu-id="37cf3-128">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="37cf3-128">Total Revenue this year</span></span>
- <span data-ttu-id="37cf3-129">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="37cf3-129">Total Expenses this year</span></span>
- <span data-ttu-id="37cf3-130">本年度净收入</span><span class="sxs-lookup"><span data-stu-id="37cf3-130">Net Income this year</span></span>
- <span data-ttu-id="37cf3-131">速动比率</span><span class="sxs-lookup"><span data-stu-id="37cf3-131">Quick Ratio</span></span>
- <span data-ttu-id="37cf3-132">按科目类别划分的本年度总支出</span><span class="sxs-lookup"><span data-stu-id="37cf3-132">Total Expenses this year by account category</span></span>
- <span data-ttu-id="37cf3-133">当前比率</span><span class="sxs-lookup"><span data-stu-id="37cf3-133">Current Ratio</span></span>
- <span data-ttu-id="37cf3-134">债务总资产比</span><span class="sxs-lookup"><span data-stu-id="37cf3-134">Debt to Total Assets</span></span>
- <span data-ttu-id="37cf3-135">实际与预测收入</span><span class="sxs-lookup"><span data-stu-id="37cf3-135">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="37cf3-136">本年已计费收入</span><span class="sxs-lookup"><span data-stu-id="37cf3-136">Billed Revenue this Year</span></span>
- <span data-ttu-id="37cf3-137">本年度运营费用比率</span><span class="sxs-lookup"><span data-stu-id="37cf3-137">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="37cf3-138">本年度利润率</span><span class="sxs-lookup"><span data-stu-id="37cf3-138">Profit Margin this year</span></span>
- <span data-ttu-id="37cf3-139">实际与预算支出 – 所有公司</span><span class="sxs-lookup"><span data-stu-id="37cf3-139">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="37cf3-140">每个磁贴都由支持报表支持。</span><span class="sxs-lookup"><span data-stu-id="37cf3-140">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="37cf3-141">这些报告包含提供更多信息的图表和表。</span><span class="sxs-lookup"><span data-stu-id="37cf3-141">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="37cf3-142">下表对报表进行了描述。</span><span class="sxs-lookup"><span data-stu-id="37cf3-142">The following table describes the reports.</span></span>

| <span data-ttu-id="37cf3-143">报表</span><span class="sxs-lookup"><span data-stu-id="37cf3-143">Report</span></span>                      | <span data-ttu-id="37cf3-144">报表中包含的信息</span><span class="sxs-lookup"><span data-stu-id="37cf3-144">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="37cf3-145">现金分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-145">Cash Analysis</span></span>               | <span data-ttu-id="37cf3-146">按法人分类的现金、按季度分类的现金、总现金和按帐户分类的现金</span><span class="sxs-lookup"><span data-stu-id="37cf3-146">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE]<br><span data-ttu-id="37cf3-147">按季度显示的现金信息不包括第一季度总计中的期初余额。</span><span class="sxs-lookup"><span data-stu-id="37cf3-147">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="37cf3-148">它显示每个季度过帐的新交易记录的总计。</span><span class="sxs-lookup"><span data-stu-id="37cf3-148">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="37cf3-149">当前比率分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-149">Current Ratio Analysis</span></span>      | <span data-ttu-id="37cf3-150">按法人分类的当前比率、按季度分类的当前比率和当前资产和当前负债的余额</span><span class="sxs-lookup"><span data-stu-id="37cf3-150">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="37cf3-151">速动比率分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-151">Quick Ratio Analysis</span></span>        | <span data-ttu-id="37cf3-152">按法人分类的速动比率、按季度分类的速动比率和现金、应收账款和当前负债的余额</span><span class="sxs-lookup"><span data-stu-id="37cf3-152">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="37cf3-153">所售货物成本分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-153">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="37cf3-154">按法人分类的所售货物成本 (COGS)、按季度分类的今年和去年的 COGS、按法人分类的要销售的 COGS，COGS 总计和要销售的 COGS 百分比</span><span class="sxs-lookup"><span data-stu-id="37cf3-154">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="37cf3-155">运营资本分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-155">Working Capital Analysis</span></span>    | <span data-ttu-id="37cf3-156">按法人分类的营运资、按季度分类的运营资本、当前资产、当前负债和运营资本总额</span><span class="sxs-lookup"><span data-stu-id="37cf3-156">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="37cf3-157">资产和负债分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-157">Asset and Debt Analysis</span></span>     | <span data-ttu-id="37cf3-158">按法人分类的总资产回报率和债务总资产比、上季度迄今的债务总资产比和总资产回报率、资产和负债</span><span class="sxs-lookup"><span data-stu-id="37cf3-158">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="37cf3-159">利润率分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-159">Profit Margin Analysis</span></span>      | <span data-ttu-id="37cf3-160">按法人分类的实际和预算利润率、按季度分类的利润标记、利润率百分比和利润率</span><span class="sxs-lookup"><span data-stu-id="37cf3-160">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="37cf3-161">净收入分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-161">Net Income Analysis</span></span>         | <span data-ttu-id="37cf3-162">按法人分类的实际和预算净收入、今年和去年的将收入和支出净收入比</span><span class="sxs-lookup"><span data-stu-id="37cf3-162">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="37cf3-163">收入分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-163">Earnings Analysis</span></span>           | <span data-ttu-id="37cf3-164">按法人分类的息税前实际和预算收入 (EBIT)、今年和去年的 EBIT、支出收入百分比率和实际和预算支出收入比</span><span class="sxs-lookup"><span data-stu-id="37cf3-164">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="37cf3-165">收入分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-165">Revenue Analysis</span></span>            | <span data-ttu-id="37cf3-166">总收入、按法人分类的实际和预算总收入、今年和去年的总收入、按法人分类的收入预算差异和此期间和上一期间的总收入</span><span class="sxs-lookup"><span data-stu-id="37cf3-166">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="37cf3-167">支出分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-167">Expense Analysis</span></span>            | <span data-ttu-id="37cf3-168">总支出、按法人分类的实际和预算总支出、按季度分类的实际和预算总支持、按帐户类别分类的总支出和运营费用比率</span><span class="sxs-lookup"><span data-stu-id="37cf3-168">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="37cf3-169">已计费收入分析</span><span class="sxs-lookup"><span data-stu-id="37cf3-169">Billed Revenue Analysis</span></span>     | <span data-ttu-id="37cf3-170">总应收账款、按法人分类的总应收账款、按季度分类的总应收账款和应收账款帐户的余额</span><span class="sxs-lookup"><span data-stu-id="37cf3-170">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE]<br><span data-ttu-id="37cf3-171">此信息不包括应收账款会计科目的期初余额。</span><span class="sxs-lookup"><span data-stu-id="37cf3-171">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="37cf3-172">它显示过帐到应收账款的新交易记录的总计。</span><span class="sxs-lookup"><span data-stu-id="37cf3-172">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="37cf3-173">所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。</span><span class="sxs-lookup"><span data-stu-id="37cf3-173">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="37cf3-174">有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。</span><span class="sxs-lookup"><span data-stu-id="37cf3-174">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="37cf3-175">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="37cf3-175">Understanding the data model and entities</span></span>
<span data-ttu-id="37cf3-176">以下实体用作**财务绩效** Power BI 内容的基础：</span><span class="sxs-lookup"><span data-stu-id="37cf3-176">The following entities were used as the basis of the **Financial performance** Power BI content:</span></span>

<span data-ttu-id="37cf3-177">**聚合数据实体**</span><span class="sxs-lookup"><span data-stu-id="37cf3-177">**Aggregate data entities**</span></span>

- <span data-ttu-id="37cf3-178">**GeneralLedgerActivities** – 此实体按科目类别聚合总帐余额。</span><span class="sxs-lookup"><span data-stu-id="37cf3-178">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="37cf3-179">**BudgetActivities** – 此实体按科目类别聚合预算余额。</span><span class="sxs-lookup"><span data-stu-id="37cf3-179">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="37cf3-180">**数据实体**</span><span class="sxs-lookup"><span data-stu-id="37cf3-180">**Data entities**</span></span>

- <span data-ttu-id="37cf3-181">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="37cf3-181">FiscalCalendars</span></span>
- <span data-ttu-id="37cf3-182">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="37cf3-182">MainAccounts</span></span>
- <span data-ttu-id="37cf3-183">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="37cf3-183">LegalEntities</span></span>
- <span data-ttu-id="37cf3-184">分类帐</span><span class="sxs-lookup"><span data-stu-id="37cf3-184">Ledgers</span></span>
- <span data-ttu-id="37cf3-185">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="37cf3-185">ChartofAccounts</span></span>

<span data-ttu-id="37cf3-186">这些实体用于在数据模型中创建计算度量值。</span><span class="sxs-lookup"><span data-stu-id="37cf3-186">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="37cf3-187">计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。</span><span class="sxs-lookup"><span data-stu-id="37cf3-187">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="37cf3-188">默认情况下，内容提供过去三年和未来一年的数据。</span><span class="sxs-lookup"><span data-stu-id="37cf3-188">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="37cf3-189">若要在报表和仪表板中包括其他计算，您可以修改 [Microsoft Excel 工作簿](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)。</span><span class="sxs-lookup"><span data-stu-id="37cf3-189">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span></span> <span data-ttu-id="37cf3-190">此工作簿是用于创建内容的默认数据模型。</span><span class="sxs-lookup"><span data-stu-id="37cf3-190">This workbook is the default data model that was used to create the content.</span></span> <span data-ttu-id="37cf3-191">在您完成您的修改后，可以创建包含您已添加的信息的组织内容包和仪表板。</span><span class="sxs-lookup"><span data-stu-id="37cf3-191">After you've finished making your modifications, you can create an organizational content pack and dashboard that contain the information that you’ve added.</span></span>

