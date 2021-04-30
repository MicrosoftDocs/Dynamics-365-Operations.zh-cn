---
title: 总帐和财务报表概览
description: 使用总帐定义和管理法人的财务记录。
author: ShylaThompson
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 403cd616faef2f856c21a771d46607c41987f0bb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897520"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="afbba-103">总帐主页</span><span class="sxs-lookup"><span data-stu-id="afbba-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afbba-104">使用总帐定义和管理法人的财务记录。</span><span class="sxs-lookup"><span data-stu-id="afbba-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="afbba-105">总帐是借方和贷方登记条目。</span><span class="sxs-lookup"><span data-stu-id="afbba-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="afbba-106">这些条目进行分类使用在会计科目表中列出的科目。</span><span class="sxs-lookup"><span data-stu-id="afbba-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="afbba-107">计划您的会计科目表</span><span class="sxs-lookup"><span data-stu-id="afbba-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="afbba-108">主科目类型</span><span class="sxs-lookup"><span data-stu-id="afbba-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="afbba-109">分配是基于分配规则将金额分配到一个或多个帐户或帐户/维度组合的过程。</span><span class="sxs-lookup"><span data-stu-id="afbba-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="afbba-110">存在两种类型的分配：固定和可变。</span><span class="sxs-lookup"><span data-stu-id="afbba-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="afbba-111">您还可以在结算会计科目之间的交易记录和重估原币金额。</span><span class="sxs-lookup"><span data-stu-id="afbba-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="afbba-112">在某一会计年度结束时，您必须为下一会计年度准备您的科目，并且关闭当前会计年度。</span><span class="sxs-lookup"><span data-stu-id="afbba-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="afbba-113">您可以使用合并功能以合并若干子公司的财务结果为唯一的合并公司的财务结果。</span><span class="sxs-lookup"><span data-stu-id="afbba-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="afbba-114">这些字公司可以存在于相同的数据库中或在单独的数据库中。</span><span class="sxs-lookup"><span data-stu-id="afbba-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="afbba-115">合并和清除概览</span><span class="sxs-lookup"><span data-stu-id="afbba-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="afbba-116">总帐科目余额</span><span class="sxs-lookup"><span data-stu-id="afbba-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="afbba-117">财务维度</span><span class="sxs-lookup"><span data-stu-id="afbba-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="afbba-118">[![业务流程](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="afbba-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="afbba-119">销售税</span><span class="sxs-lookup"><span data-stu-id="afbba-119">Sales tax</span></span>
<span data-ttu-id="afbba-120">每个公司都需要向各种税务主管机构缴纳税款。</span><span class="sxs-lookup"><span data-stu-id="afbba-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="afbba-121">规则和比率根据国家/地区、省/市/自治区、县和城市而改变。</span><span class="sxs-lookup"><span data-stu-id="afbba-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="afbba-122">此外，当税务主管部门更改它们的要求时，必须定期更新规则。</span><span class="sxs-lookup"><span data-stu-id="afbba-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="afbba-123">增值税代码包含您收取以及支付给主管机构的金额数的信息。</span><span class="sxs-lookup"><span data-stu-id="afbba-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="afbba-124">当您设置增值税代码时，您定义了必须收取的金额或百分比。</span><span class="sxs-lookup"><span data-stu-id="afbba-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="afbba-125">您还定义了将这些金额或百分比应用到交易记录金额中的各种方法。</span><span class="sxs-lookup"><span data-stu-id="afbba-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="afbba-126">本节中的主题提供了如何针对您的税务主管机构要求的方法和比率设置增值税的信息。</span><span class="sxs-lookup"><span data-stu-id="afbba-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="afbba-127">销售税概览</span><span class="sxs-lookup"><span data-stu-id="afbba-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="afbba-128">基于“边际基数”和“计算方法”的销售税比率</span><span class="sxs-lookup"><span data-stu-id="afbba-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="afbba-129">销售税支付和化整规则</span><span class="sxs-lookup"><span data-stu-id="afbba-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="afbba-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="afbba-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="afbba-131">新增功能和开发中的功能</span><span class="sxs-lookup"><span data-stu-id="afbba-131">What's new and in development</span></span>

<span data-ttu-id="afbba-132">转到 [Microsoft Dynamics 365 版本计划](/dynamics365/release-plans/)，了解已经规划了哪些新功能。</span><span class="sxs-lookup"><span data-stu-id="afbba-132">Go to the [Microsoft Dynamics 365 release plans](/dynamics365/release-plans/) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="afbba-133">财务报告</span><span class="sxs-lookup"><span data-stu-id="afbba-133">Financial reporting</span></span>
<span data-ttu-id="afbba-134">转到 [Financial reporting 概述](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)主题，了解有关财务报表的信息。</span><span class="sxs-lookup"><span data-stu-id="afbba-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="afbba-135">博客</span><span class="sxs-lookup"><span data-stu-id="afbba-135">Blogs</span></span>

<span data-ttu-id="afbba-136">您可以在 [Microsoft Dynamics 365 博客](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)和 [Microsoft Dynamics 365 Finance and Operations - 财务博客](https://community.dynamics.com/365/financeandoperations/b/financials)上查找意见、新闻和其他信息。</span><span class="sxs-lookup"><span data-stu-id="afbba-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="afbba-137">[Microsoft Dynamics Operations 合作伙伴社区博客](https://community.dynamics.com/partner/b/operationspartnercommunityblog)可为 Microsoft Dynamics 合作伙伴提供了解 Dynamics 365 中的新增功能和趋势的单一资源。</span><span class="sxs-lookup"><span data-stu-id="afbba-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="afbba-138">视频</span><span class="sxs-lookup"><span data-stu-id="afbba-138">Videos</span></span>

<span data-ttu-id="afbba-139">查看当前在 [Microsoft Dynamics 365 YouTube 频道](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)上提供的操作方法视频。</span><span class="sxs-lookup"><span data-stu-id="afbba-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="afbba-140">社区博客</span><span class="sxs-lookup"><span data-stu-id="afbba-140">Community blogs</span></span>

- [<span data-ttu-id="afbba-141">Dynamics 365 for Finance and Operations 中应该了解的分类帐信息</span><span class="sxs-lookup"><span data-stu-id="afbba-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]