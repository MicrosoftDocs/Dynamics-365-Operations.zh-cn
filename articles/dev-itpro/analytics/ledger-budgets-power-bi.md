---
title: "实际与预算 Power BI 内容"
description: "此主题描述实际与预算 Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f09af96fb1c76d8737d2c535f1a46565a18deca0
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="75a5c-104">实际与预算 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="75a5c-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="75a5c-105">此主题描述**实际与预算** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="75a5c-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="75a5c-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="75a5c-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="75a5c-107">概览</span><span class="sxs-lookup"><span data-stu-id="75a5c-107">Overview</span></span>

<span data-ttu-id="75a5c-108">**实际与预算** Power BI 内容为负责监督组织中的实际与预算绩效的人员而创建。</span><span class="sxs-lookup"><span data-stu-id="75a5c-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="75a5c-109">**实际与预算** Power BI 内容可用于查看您的预算差异。</span><span class="sxs-lookup"><span data-stu-id="75a5c-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="75a5c-110">您可以按科目类别、预算代码、主科目、主科目描述或会计期间分析当前年度的预算，以更好地了解任何差异的原因。</span><span class="sxs-lookup"><span data-stu-id="75a5c-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="75a5c-111">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="75a5c-111">Accessing the Power BI content</span></span>
<span data-ttu-id="75a5c-112">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月），则来自**实际与预算** Power BI 内容的报表显示在**分类帐预算和预测**和 **CFO** 工作区。</span><span class="sxs-lookup"><span data-stu-id="75a5c-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="75a5c-113">此 Power BI 内容中包含的报表</span><span class="sxs-lookup"><span data-stu-id="75a5c-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="75a5c-114">下表提供有关在**实际与预算** Power BI 内容中的每个报表页找到的指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="75a5c-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="75a5c-115">报告</span><span class="sxs-lookup"><span data-stu-id="75a5c-115">Report</span></span>                      | <span data-ttu-id="75a5c-116">指标</span><span class="sxs-lookup"><span data-stu-id="75a5c-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="75a5c-117">支出 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="75a5c-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="75a5c-118">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="75a5c-118">Total expenses this year</span></span></li><li><span data-ttu-id="75a5c-119">本年支出总额预算</span><span class="sxs-lookup"><span data-stu-id="75a5c-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="75a5c-120">收入 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="75a5c-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="75a5c-121">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="75a5c-121">Total revenue this year</span></span></li><li><span data-ttu-id="75a5c-122">本年收入总额预算</span><span class="sxs-lookup"><span data-stu-id="75a5c-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="75a5c-123">费用</span><span class="sxs-lookup"><span data-stu-id="75a5c-123">Expense</span></span>                     | <ul><li><span data-ttu-id="75a5c-124">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="75a5c-124">Total expenses this year</span></span></li><li><span data-ttu-id="75a5c-125">基于预算的支出目标</span><span class="sxs-lookup"><span data-stu-id="75a5c-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="75a5c-126">收入</span><span class="sxs-lookup"><span data-stu-id="75a5c-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="75a5c-127">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="75a5c-127">Total revenue this year</span></span></li><li><span data-ttu-id="75a5c-128">基于预算的收入目标</span><span class="sxs-lookup"><span data-stu-id="75a5c-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="75a5c-129">净收益</span><span class="sxs-lookup"><span data-stu-id="75a5c-129">Net income</span></span>                  | <ul><li><span data-ttu-id="75a5c-130">本年度净收益</span><span class="sxs-lookup"><span data-stu-id="75a5c-130">Net income this year</span></span></li><li><span data-ttu-id="75a5c-131">基于预算的净收益目标</span><span class="sxs-lookup"><span data-stu-id="75a5c-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="75a5c-132">扩展 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="75a5c-132">Extending the Power BI content</span></span>
<span data-ttu-id="75a5c-133">使用在 Microsoft Dynamics Lifecycle Services (LCS) 中可用的内容包可以对未登录到 Microsoft Dynamics 365 的人员提供出色的分析。</span><span class="sxs-lookup"><span data-stu-id="75a5c-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="75a5c-134">您可以修改这些内容包，使它们包含其他报表或视觉对象，然后将内容包发布到您的 Power BI.com 租户进行分析。</span><span class="sxs-lookup"><span data-stu-id="75a5c-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="75a5c-135">可在 LCS 中的共享资产库内找到**实际与预算** Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="75a5c-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="75a5c-136">有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。</span><span class="sxs-lookup"><span data-stu-id="75a5c-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="75a5c-137">若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。</span><span class="sxs-lookup"><span data-stu-id="75a5c-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="75a5c-138">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="75a5c-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="75a5c-139">实体</span><span class="sxs-lookup"><span data-stu-id="75a5c-139">Entity</span></span>                    | <span data-ttu-id="75a5c-140">内容</span><span class="sxs-lookup"><span data-stu-id="75a5c-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="75a5c-141">总帐活动</span><span class="sxs-lookup"><span data-stu-id="75a5c-141">General Ledger Activities</span></span> | <span data-ttu-id="75a5c-142">总帐交易金额</span><span class="sxs-lookup"><span data-stu-id="75a5c-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="75a5c-143">预算活动</span><span class="sxs-lookup"><span data-stu-id="75a5c-143">Budget Activities</span></span>         | <span data-ttu-id="75a5c-144">预算登记的交易金额</span><span class="sxs-lookup"><span data-stu-id="75a5c-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="75a5c-145">主科目</span><span class="sxs-lookup"><span data-stu-id="75a5c-145">Main Accounts</span></span>             | <span data-ttu-id="75a5c-146">充当报表筛选依据的主科目</span><span class="sxs-lookup"><span data-stu-id="75a5c-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="75a5c-147">会计日历</span><span class="sxs-lookup"><span data-stu-id="75a5c-147">Fiscal Calendars</span></span>          | <span data-ttu-id="75a5c-148">充当报表筛选依据的会计日历</span><span class="sxs-lookup"><span data-stu-id="75a5c-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="75a5c-149">分类帐</span><span class="sxs-lookup"><span data-stu-id="75a5c-149">Ledgers</span></span>                   | <span data-ttu-id="75a5c-150">可用于筛选报表到当前分类帐的分类帐</span><span class="sxs-lookup"><span data-stu-id="75a5c-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="75a5c-151">预算代码</span><span class="sxs-lookup"><span data-stu-id="75a5c-151">Budget Codes</span></span>              | <span data-ttu-id="75a5c-152">充当报表筛选依据的预算代码</span><span class="sxs-lookup"><span data-stu-id="75a5c-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="75a5c-153">法人</span><span class="sxs-lookup"><span data-stu-id="75a5c-153">Legal Entities</span></span>            | <span data-ttu-id="75a5c-154">可用于筛选报表到当前法人的法人</span><span class="sxs-lookup"><span data-stu-id="75a5c-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

