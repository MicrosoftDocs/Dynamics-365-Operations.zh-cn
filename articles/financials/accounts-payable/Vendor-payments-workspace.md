---
title: "供应商付款工作区"
description: "此主题提供有关供应商付款工作区的信息。 供应商付款工作区显示与处理供应商付款有关的信息。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b6c1802a5d53299ac6be8c747146698778a9359c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-payments-workspace"></a><span data-ttu-id="ed248-104">供应商付款工作区</span><span class="sxs-lookup"><span data-stu-id="ed248-104">Vendor payments workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ed248-105">**供应商付款**工作区显示与处理供应商付款有关的信息。</span><span class="sxs-lookup"><span data-stu-id="ed248-105">The **Vendor payments** workspace shows information that is related to the processing of vendor payments.</span></span> <span data-ttu-id="ed248-106">该工作区包括一个**我的工作**视图和一个**分析**页。</span><span class="sxs-lookup"><span data-stu-id="ed248-106">This workspace includes a **My work** view and an **Analytics** page.</span></span> <span data-ttu-id="ed248-107">**我的工作**视图显示汇总磁贴、供应商交易记录网格和相关供应商信息。</span><span class="sxs-lookup"><span data-stu-id="ed248-107">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="ed248-108">**分析**页使用 Microsoft Power BI 的功能显示与供应商付款相关的视觉对象。</span><span class="sxs-lookup"><span data-stu-id="ed248-108">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to vendor payments.</span></span>

## <a name="my-work-view"></a><span data-ttu-id="ed248-109">我的工作视图</span><span class="sxs-lookup"><span data-stu-id="ed248-109">My work view</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="ed248-110">汇总磁贴</span><span class="sxs-lookup"><span data-stu-id="ed248-110">Summary tiles</span></span>

<span data-ttu-id="ed248-111">在**汇总**部分的磁贴提供您的付款信息状态的概览。</span><span class="sxs-lookup"><span data-stu-id="ed248-111">The tiles in the **Summary** section give an overview of the state of your payment information.</span></span> <span data-ttu-id="ed248-112">您可以查看未过帐的付款日记帐、逾期发票、所有供应商以及处于暂停状态的供应商。</span><span class="sxs-lookup"><span data-stu-id="ed248-112">You can see payment journals that aren't yet posted, invoices that are past due, all vendors, and vendors that are on hold.</span></span> <span data-ttu-id="ed248-113">从**汇总**部分，可以创建新的付薪周期。</span><span class="sxs-lookup"><span data-stu-id="ed248-113">From the **Summary** section, you can create a new pay run.</span></span>

<span data-ttu-id="ed248-114">**汇总**部分的信息适用于您登录到的公司。</span><span class="sxs-lookup"><span data-stu-id="ed248-114">The information in the **Summary** section is for the company that you're signed in to.</span></span>

### <a name="vendor-transactions-grids"></a><span data-ttu-id="ed248-115">供应商交易记录网格</span><span class="sxs-lookup"><span data-stu-id="ed248-115">Vendor transactions grids</span></span>

<span data-ttu-id="ed248-116">**供应商交易记录**部分包含显示逾期发票和未结算付款的网格。</span><span class="sxs-lookup"><span data-stu-id="ed248-116">The **Vendor transactions** section contains grids that show the invoices that are past due and payments that aren't settled.</span></span> <span data-ttu-id="ed248-117">从**逾期发票**网格可以查看所选发票的结算历史记录。</span><span class="sxs-lookup"><span data-stu-id="ed248-117">From the **Invoices past due** grid, you can view the settlement history for a selected invoice.</span></span> <span data-ttu-id="ed248-118">从**未结算付款**网格可以查看所选发票的结算历史记录和结算发票。</span><span class="sxs-lookup"><span data-stu-id="ed248-118">From the **Payments not settled** grid, you can view the settlement history for a selected invoice and settle an invoice.</span></span>

<span data-ttu-id="ed248-119">统一付款人员可以使用出现在各网格顶部的筛选器选择公司。</span><span class="sxs-lookup"><span data-stu-id="ed248-119">Centralized payment clerks can use a filter that appears at the top of each grid to select a company.</span></span> <span data-ttu-id="ed248-120">随后将筛选网格，使其仅显示在统一付款组织层次结构中定义且统一付款职员有权查看的公司。</span><span class="sxs-lookup"><span data-stu-id="ed248-120">The grid is then filtered so that it shows only those companies that are defined in the centralized payment organizational hierarchy that the centralized payment clerk has rights to view.</span></span>

<span data-ttu-id="ed248-121">**供应商交易记录**部分的**查找交易记录**选项卡允许您搜索供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="ed248-121">The **Find transactions** tab in the **Vendor transactions** section lets you search for a vendor transaction.</span></span>

### <a name="related-information"></a><span data-ttu-id="ed248-122">相关信息</span><span class="sxs-lookup"><span data-stu-id="ed248-122">Related information</span></span>

<span data-ttu-id="ed248-123">您可以使用工作区的**相关信息**部分中的链接查看**供应商帐龄**报表和**付款汇总(按日期)**报表。</span><span class="sxs-lookup"><span data-stu-id="ed248-123">You can view the **Vendor aging** report and the **Payment summary by date** report by using the links in the **Related information** section of the workspace.</span></span>

## <a name="analytics-page"></a><span data-ttu-id="ed248-124">分析页</span><span class="sxs-lookup"><span data-stu-id="ed248-124">Analytics page</span></span>

<span data-ttu-id="ed248-125">**分析**页提供重要指标，例如逾期的供应商发票和在将来到期的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="ed248-125">The **Analytics** page provides important metrics, such as vendor invoices that are past due and vendor invoices that are due in the future.</span></span> <span data-ttu-id="ed248-126">此页包含九个报表页。</span><span class="sxs-lookup"><span data-stu-id="ed248-126">This page contains nine report pages.</span></span> <span data-ttu-id="ed248-127">一页提供概览，另外八页提供关于应付账款付款指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ed248-127">One page provides an overview, and the other eight pages provide details about Accounts payable payment metrics.</span></span>

<span data-ttu-id="ed248-128">下表显示在每个报表页上可用的可视化项。</span><span class="sxs-lookup"><span data-stu-id="ed248-128">The following table shows the visualizations that are available on each report page.</span></span>

| <span data-ttu-id="ed248-129">报表页</span><span class="sxs-lookup"><span data-stu-id="ed248-129">Report page</span></span> | <span data-ttu-id="ed248-130">可视化</span><span class="sxs-lookup"><span data-stu-id="ed248-130">Visualization</span></span> |
|-------------|---------------|
| <span data-ttu-id="ed248-131">供应商付款概览</span><span class="sxs-lookup"><span data-stu-id="ed248-131">Vendor payments overview</span></span> | <ul><li><span data-ttu-id="ed248-132">逾期未付的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-132">Invoices past due</span></span></li><li><span data-ttu-id="ed248-133">今日到期发票</span><span class="sxs-lookup"><span data-stu-id="ed248-133">Invoices due today</span></span></li><li><span data-ttu-id="ed248-134">已采用的折扣到已丢失的折扣</span><span class="sxs-lookup"><span data-stu-id="ed248-134">Discounts taken to discounts lost</span></span></li><li><span data-ttu-id="ed248-135">在现金折扣日期之前将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-135">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="ed248-136">在到期日期之前将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-136">Invoices due in future by due date</span></span></li><li><span data-ttu-id="ed248-137">延期付款的发票到按时付款的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-137">Invoices paid late to invoices paid on time</span></span></li><li><span data-ttu-id="ed248-138">付款工作流分配</span><span class="sxs-lookup"><span data-stu-id="ed248-138">Payment workflow assignment</span></span></li><li><span data-ttu-id="ed248-139">供应商到客户余额</span><span class="sxs-lookup"><span data-stu-id="ed248-139">Vendor to customer balance</span></span></li><li><span data-ttu-id="ed248-140">具有付款暂停的未结发票</span><span class="sxs-lookup"><span data-stu-id="ed248-140">Open invoices with payment hold</span></span></li></ul> |
| <span data-ttu-id="ed248-141">逾期未付的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-141">Invoices past due</span></span> | <ul><li><span data-ttu-id="ed248-142">逾期未付的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-142">Invoices past due</span></span></li><li><span data-ttu-id="ed248-143">发票逾期明细</span><span class="sxs-lookup"><span data-stu-id="ed248-143">Invoices past due details</span></span></li><li><span data-ttu-id="ed248-144">未结发票合计</span><span class="sxs-lookup"><span data-stu-id="ed248-144">Total open invoices</span></span></li><li><span data-ttu-id="ed248-145">逾期发票(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-145">Invoices past due per vendor group</span></span></li><li><span data-ttu-id="ed248-146">逾期发票(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-146">Invoices past due per company</span></span></li></ul> |
| <span data-ttu-id="ed248-147">今日到期发票</span><span class="sxs-lookup"><span data-stu-id="ed248-147">Invoices due today</span></span> | <ul><li><span data-ttu-id="ed248-148">今日到期发票</span><span class="sxs-lookup"><span data-stu-id="ed248-148">Invoices due today</span></span></li><li><span data-ttu-id="ed248-149">今日到期发票明细</span><span class="sxs-lookup"><span data-stu-id="ed248-149">Invoices due today details</span></span></li><li><span data-ttu-id="ed248-150">今日到期发票(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-150">Invoices due today per company</span></span></li><li><span data-ttu-id="ed248-151">今日到期发票(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-151">Invoices due today per vendor group</span></span></li></ul> |
| <span data-ttu-id="ed248-152">已采用的折扣到已丢失的折扣</span><span class="sxs-lookup"><span data-stu-id="ed248-152">Discounts taken to discounts lost</span></span> | <ul><li><span data-ttu-id="ed248-153">已采用的折扣到已丢失的折扣</span><span class="sxs-lookup"><span data-stu-id="ed248-153">Discounts taken to discount lost</span></span></li><li><span data-ttu-id="ed248-154">已采用的折扣到已丢失的折扣明细</span><span class="sxs-lookup"><span data-stu-id="ed248-154">Discounts taken to discount lost details</span></span></li><li><span data-ttu-id="ed248-155">已采用的折扣到已丢失的折扣(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-155">Discounts taken to discount lost per company</span></span></li><li><span data-ttu-id="ed248-156">已采用的折扣到已丢失的折扣(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-156">Discounts taken to discount lost per vendor group</span></span></li></ul> |
| <span data-ttu-id="ed248-157">将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-157">Invoices due in future</span></span> | <ul><li><span data-ttu-id="ed248-158">将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-158">Invoices due in future</span></span></li><li><span data-ttu-id="ed248-159">将来到期的发票明细</span><span class="sxs-lookup"><span data-stu-id="ed248-159">Invoices due in future details</span></span></li><li><span data-ttu-id="ed248-160">将来到期的发票(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-160">Invoices due in future per company</span></span></li><li><span data-ttu-id="ed248-161">将来到期的发票(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-161">Invoices due in future per vendor group</span></span></li><li><span data-ttu-id="ed248-162">在现金折扣日期之前将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-162">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="ed248-163">在到期日期之前将来到期的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-163">Invoices due in future by due date</span></span></li></ul> |
| <span data-ttu-id="ed248-164">延期付款的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-164">Invoices paid late</span></span> | <ul><li><span data-ttu-id="ed248-165">在到期日期后付款的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-165">Invoices paid after due date</span></span></li><li><span data-ttu-id="ed248-166">在到期日期后付款的发票明细</span><span class="sxs-lookup"><span data-stu-id="ed248-166">Invoices paid after due date details</span></span></li><li><span data-ttu-id="ed248-167">在到期日期后付款的发票(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-167">Invoices paid after due date per company</span></span></li><li><span data-ttu-id="ed248-168">在到期日期后付款的发票(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-168">Invoices paid after due date per vendor group</span></span></li><li><span data-ttu-id="ed248-169">延期付款的发票与按时付款的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-169">Invoices paid late versus invoices paid on time</span></span></li></ul> |
| <span data-ttu-id="ed248-170">付款工作流</span><span class="sxs-lookup"><span data-stu-id="ed248-170">Payment workflow</span></span> | <ul><li><span data-ttu-id="ed248-171">供应商付款工作流实例</span><span class="sxs-lookup"><span data-stu-id="ed248-171">Vendor payment workflow instances</span></span></li><li><span data-ttu-id="ed248-172">供应商付款工作流实例(按审批人)</span><span class="sxs-lookup"><span data-stu-id="ed248-172">Vendor payment workflow instances per approver</span></span></li><li><span data-ttu-id="ed248-173">供应商付款工作流实例(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-173">Vendor payment workflow instances per company</span></span></li><li><span data-ttu-id="ed248-174">工作流中的平均天数(按审批人)</span><span class="sxs-lookup"><span data-stu-id="ed248-174">Average days in workflow by approver</span></span></li></ul> |
| <span data-ttu-id="ed248-175">供应商到客户余额</span><span class="sxs-lookup"><span data-stu-id="ed248-175">Vendor to customer balance</span></span> | <ul><li><span data-ttu-id="ed248-176">供应商到客户余额</span><span class="sxs-lookup"><span data-stu-id="ed248-176">Vendor to customer balance</span></span></li><li><span data-ttu-id="ed248-177">供应商到客户余额(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-177">Vendor to customer balance per company</span></span></li><li><span data-ttu-id="ed248-178">供应商到客户余额明细</span><span class="sxs-lookup"><span data-stu-id="ed248-178">Vendor to customer balance details</span></span></li></ul> |
| <span data-ttu-id="ed248-179">具有付款暂停的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-179">Invoices with payment hold</span></span> | <ul><li><span data-ttu-id="ed248-180">具有付款暂停的发票</span><span class="sxs-lookup"><span data-stu-id="ed248-180">Invoices with payment hold</span></span></li><li><span data-ttu-id="ed248-181">具有付款暂停的发票明细</span><span class="sxs-lookup"><span data-stu-id="ed248-181">Invoices with payment hold details</span></span></li><li><span data-ttu-id="ed248-182">具有付款暂停的发票(按公司)</span><span class="sxs-lookup"><span data-stu-id="ed248-182">Invoices with payment hold per company</span></span></li><li><span data-ttu-id="ed248-183">具有付款暂停的发票(按供应商组)</span><span class="sxs-lookup"><span data-stu-id="ed248-183">Invoices with payment hold per vendor group</span></span></li></ul> |
