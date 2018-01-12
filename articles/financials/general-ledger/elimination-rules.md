---
title: "清除规则"
description: "本主题提供有关清除规则和有关清除的不同报告选项的信息。"
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 47336a19899b1fad0e63265173fd7fd02fc74ec3
ms.openlocfilehash: 2a0897bd80a508474be384e8086ca47dd9de7efb
ms.contentlocale: zh-cn
ms.lasthandoff: 01/12/2018

---

# <a name="elimination-rules"></a><span data-ttu-id="6ace5-103">清除规则</span><span class="sxs-lookup"><span data-stu-id="6ace5-103">Elimination rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ace5-104">本主题提供有关清除规则和有关清除的不同报告选项的信息。</span><span class="sxs-lookup"><span data-stu-id="6ace5-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="6ace5-105">在母法人与一家或多家法人开展业务并使用合并的财务申报时，需要清除交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ace5-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="6ace5-106">合并的财务报表必须仅包含在合并的组织与该组织外的其他实体之间发生的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ace5-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="6ace5-107">因此，必须从总帐中删除或清除属于同一组织的法人之间的交易记录，以便其不显示在财务报表中。</span><span class="sxs-lookup"><span data-stu-id="6ace5-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="6ace5-108">可通过多种方式来报告清除：</span><span class="sxs-lookup"><span data-stu-id="6ace5-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="6ace5-109">可在合并或清除公司中创建和处理清除规则。</span><span class="sxs-lookup"><span data-stu-id="6ace5-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="6ace5-110">财务报告可用于显示某个特定行或列上的清除帐户和维度。</span><span class="sxs-lookup"><span data-stu-id="6ace5-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="6ace5-111">单独的法人可用于过帐手动交易记录输入以跟踪清除。</span><span class="sxs-lookup"><span data-stu-id="6ace5-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="6ace5-112">本主题重点说明在合并或清除公司中处理的清除规则。</span><span class="sxs-lookup"><span data-stu-id="6ace5-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="6ace5-113">您可以设置清除规则，以便在指定为清除的目标法人的法人中创建清除交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ace5-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="6ace5-114">此目标法人称作清除法人。</span><span class="sxs-lookup"><span data-stu-id="6ace5-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="6ace5-115">清除日志可以在合并过程中生成，也可以使用清除日志方案生成。</span><span class="sxs-lookup"><span data-stu-id="6ace5-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="6ace5-116">您应该首先熟悉以下术语，然后才可以设置清除规则：</span><span class="sxs-lookup"><span data-stu-id="6ace5-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="6ace5-117">**源法人** - 已过帐要清除金额的法人。</span><span class="sxs-lookup"><span data-stu-id="6ace5-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="6ace5-118">**目标法人** - 过帐清除规则的法人。</span><span class="sxs-lookup"><span data-stu-id="6ace5-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="6ace5-119">**清除法人** - 指定为用于清除的目标法人的法人。</span><span class="sxs-lookup"><span data-stu-id="6ace5-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="6ace5-120">**合并法人** - 为报告一组法人的财务结果而创建的法人。</span><span class="sxs-lookup"><span data-stu-id="6ace5-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="6ace5-121">来自这些法人的财务数据将合并到此法人中，然后使用合并后的数据创建财务报表。</span><span class="sxs-lookup"><span data-stu-id="6ace5-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="6ace5-122">下表显示可能已清除的交易记录的类型。</span><span class="sxs-lookup"><span data-stu-id="6ace5-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ace5-123">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="6ace5-123">Transaction type</span></span></th>
<th><span data-ttu-id="6ace5-124">示例</span><span class="sxs-lookup"><span data-stu-id="6ace5-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ace5-125">销售订单分录和开票（集中处理）</span><span class="sxs-lookup"><span data-stu-id="6ace5-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="6ace5-126">您代表您的组织中其他法人向客户销售产品。</span><span class="sxs-lookup"><span data-stu-id="6ace5-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-127">销售订单分录（公司内部/公司间）和开票</span><span class="sxs-lookup"><span data-stu-id="6ace5-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="6ace5-128">在您组织中的法人之间销售产品。</span><span class="sxs-lookup"><span data-stu-id="6ace5-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ace5-129">采购订单（集中处理）</span><span class="sxs-lookup"><span data-stu-id="6ace5-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="6ace5-130">采购来自代表您的组织中的其他法人的供应商的库存、耗材、服务、固定资产和其他产品。</span><span class="sxs-lookup"><span data-stu-id="6ace5-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-131">库存管理（公司内部/公司间）</span><span class="sxs-lookup"><span data-stu-id="6ace5-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="6ace5-132">您将一个法人的库存转移到您的组织中的其他法人的固定资产中。</span><span class="sxs-lookup"><span data-stu-id="6ace5-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="6ace5-133">您将一个法人的库存转移到您的组织中的其他法人的库存中。</span><span class="sxs-lookup"><span data-stu-id="6ace5-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ace5-134">中转库存跟踪</span><span class="sxs-lookup"><span data-stu-id="6ace5-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="6ace5-135">将物料在同一法人中的仓库之间转移，但跨处于不同地理位置的站点。</span><span class="sxs-lookup"><span data-stu-id="6ace5-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-136">应付账款的集中的发票处理</span><span class="sxs-lookup"><span data-stu-id="6ace5-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="6ace5-137">您代表您的组织中的其他法人记录发票。</span><span class="sxs-lookup"><span data-stu-id="6ace5-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ace5-138">应收账款的集中的付款处理</span><span class="sxs-lookup"><span data-stu-id="6ace5-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="6ace5-139">您代表您的组织中的其他法人支付发票。</span><span class="sxs-lookup"><span data-stu-id="6ace5-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-140">现金管理和库存（集中处理）</span><span class="sxs-lookup"><span data-stu-id="6ace5-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="6ace5-141">处理税金支付、退税、利息收费、贷款、预付、股息支付和预付管理费或佣金。</span><span class="sxs-lookup"><span data-stu-id="6ace5-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="6ace5-142">您代表您的组织中的其他法人支付支出。</span><span class="sxs-lookup"><span data-stu-id="6ace5-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="6ace5-143">在目标法人的帐簿中输入发票，并且您必须在法人之间交叉结算。</span><span class="sxs-lookup"><span data-stu-id="6ace5-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="6ace5-144">例如，一个法人支付其他中法人中某一员工的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6ace5-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="6ace5-145">在这种情况下，该员工的支出报表有与其他法人相关的费用。</span><span class="sxs-lookup"><span data-stu-id="6ace5-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="6ace5-146">您将现金从一个法人转移到您的组织中的其他法人处。</span><span class="sxs-lookup"><span data-stu-id="6ace5-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ace5-147">应收账款（集中处理）</span><span class="sxs-lookup"><span data-stu-id="6ace5-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="6ace5-148">接收其他法人的客户发票的现金，并且将支票存入该法人的银行帐户中。</span><span class="sxs-lookup"><span data-stu-id="6ace5-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-149">工资单（集中处理，内部公司/公司间）</span><span class="sxs-lookup"><span data-stu-id="6ace5-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="6ace5-150">您支付其他法人的工资单。</span><span class="sxs-lookup"><span data-stu-id="6ace5-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="6ace5-151">例如，一个法人为其员工支付自己的工资单，但拒付员工在付薪周期为其他法人执行的工作。</span><span class="sxs-lookup"><span data-stu-id="6ace5-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="6ace5-152">或者，某一员工为法人 A 工作了半天，为法人 B 工作了半天，并且福利涵盖所有付薪。</span><span class="sxs-lookup"><span data-stu-id="6ace5-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="6ace5-153">在此类情况下，该员工的薪酬包括两个法人的付薪。</span><span class="sxs-lookup"><span data-stu-id="6ace5-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="6ace5-154">不仅过帐薪酬，而且还过帐与薪酬有关的税款、福利、扣减和应计。</span><span class="sxs-lookup"><span data-stu-id="6ace5-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="6ace5-155">你将人工从一个部门或分部转移到另一个部门或分部。</span><span class="sxs-lookup"><span data-stu-id="6ace5-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ace5-156">固定资产（公司内部/公司间）</span><span class="sxs-lookup"><span data-stu-id="6ace5-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="6ace5-157">您将固定资产转移到其他法人的固定资产或库存中。</span><span class="sxs-lookup"><span data-stu-id="6ace5-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ace5-158">分配（公司内部/公司间）</span><span class="sxs-lookup"><span data-stu-id="6ace5-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="6ace5-159">您处理公司分配。</span><span class="sxs-lookup"><span data-stu-id="6ace5-159">You process corporate allocations.</span></span> <span data-ttu-id="6ace5-160">分配是针对分配的任何帐户的活动，而与来源模块无关。</span><span class="sxs-lookup"><span data-stu-id="6ace5-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="6ace5-161">示例</span><span class="sxs-lookup"><span data-stu-id="6ace5-161">Example</span></span>
<span data-ttu-id="6ace5-162">您的法人（法人 A）向您的组织中的其他法人（法人 B）销售小机械。以下示例显示在两个法人之间引发的交易记录可能已清除：</span><span class="sxs-lookup"><span data-stu-id="6ace5-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="6ace5-163">法人 A 向法人 B 以金额 10.00 销售成本为 10.00 的小机械。</span><span class="sxs-lookup"><span data-stu-id="6ace5-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="6ace5-164">法人 A 向法人 B 以金额 10.00 销售成本为 10.00 的小机械，外加 2.00 的实际装运成本。</span><span class="sxs-lookup"><span data-stu-id="6ace5-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="6ace5-165">法人 A 向法人 B 以金额 15.00 销售成本为 10.00 的小机械，并且具结该销售的毛利。</span><span class="sxs-lookup"><span data-stu-id="6ace5-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="6ace5-166">法人 A 向法人 B 以金额 15.00 销售成本为 10.00 的小机械，并且具结该销售的一半毛利。</span><span class="sxs-lookup"><span data-stu-id="6ace5-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="6ace5-167">法人 B 具结该销售的另一半毛利。</span><span class="sxs-lookup"><span data-stu-id="6ace5-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="6ace5-168">因此，收入将被拆分。</span><span class="sxs-lookup"><span data-stu-id="6ace5-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="6ace5-169">拆分收入提供了从组织内的其他法人（而不是外部组织）订购的激励。</span><span class="sxs-lookup"><span data-stu-id="6ace5-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="6ace5-170">所有这些交易记录创建过帐到应付帐户和应收帐户的内部公司交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ace5-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="6ace5-171">此外，在内部公司销售金额和所售货物成本金额不相等时，这些交易记录可能包括加价和减价金额。</span><span class="sxs-lookup"><span data-stu-id="6ace5-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="6ace5-172">设置清除规则</span><span class="sxs-lookup"><span data-stu-id="6ace5-172">Set up elimination rules</span></span>
<span data-ttu-id="6ace5-173">在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中设置清除规则时，建议专门为清除目的创建财务维度。</span><span class="sxs-lookup"><span data-stu-id="6ace5-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="6ace5-174">大多数客户将其命名为“贸易合作伙伴”或类似名称。</span><span class="sxs-lookup"><span data-stu-id="6ace5-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="6ace5-175">如果决定不使用财务维度，请务必设置专用于内部公司交易记录的主科目。</span><span class="sxs-lookup"><span data-stu-id="6ace5-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="6ace5-176">“合并”模块的“设置”区域中包含清除设置。</span><span class="sxs-lookup"><span data-stu-id="6ace5-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="6ace5-177">输入规则的描述之后，必须选择消除日记帐将过帐到的公司。</span><span class="sxs-lookup"><span data-stu-id="6ace5-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="6ace5-178">该公司应该是可过帐到在法人设置中选择了**用于财务清除过程**的所有公司。</span><span class="sxs-lookup"><span data-stu-id="6ace5-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="6ace5-179">如果需要，可以为清除规则设置生效日期和到期时间。</span><span class="sxs-lookup"><span data-stu-id="6ace5-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="6ace5-180">如果要使其在清除方案流程中可用，必须将**有效**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="6ace5-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="6ace5-181">选择类型为**清除**的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="6ace5-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="6ace5-182">定义基本信息之后，可以通过单击**行**定义实际处理规则。</span><span class="sxs-lookup"><span data-stu-id="6ace5-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="6ace5-183">清除选项有两种，一种清除净更改金额，一种定义固定金额。</span><span class="sxs-lookup"><span data-stu-id="6ace5-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="6ace5-184">选择源科目。</span><span class="sxs-lookup"><span data-stu-id="6ace5-184">Select your source account.</span></span> <span data-ttu-id="6ace5-185">您可以使用星号 (\\*) 作为通配符。</span><span class="sxs-lookup"><span data-stu-id="6ace5-185">You can use an asterisk (\\*) as a wild card.</span></span> <span data-ttu-id="6ace5-186">例如，1\** 将选择以 1 开头的所有科目作为分配的数据源。</span><span class="sxs-lookup"><span data-stu-id="6ace5-186">For example, 1\\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="6ace5-187">选择源科目帐户，**科目说明**决定所用目标公司的科目。</span><span class="sxs-lookup"><span data-stu-id="6ace5-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="6ace5-188">如果要使用**源**科目中定义的同一个主科目，请选择**源**。</span><span class="sxs-lookup"><span data-stu-id="6ace5-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="6ace5-189">如果选择**用户定义的**，则必须指定目标科目。</span><span class="sxs-lookup"><span data-stu-id="6ace5-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="6ace5-190">维度说明的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="6ace5-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="6ace5-191">如果选择**源**，将在目标公司中使用与源公司相同的维度。</span><span class="sxs-lookup"><span data-stu-id="6ace5-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="6ace5-192">如果选择**用户定义的**，则需要通过单击**目标维度**菜单项指定目标公司中的维度。</span><span class="sxs-lookup"><span data-stu-id="6ace5-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="6ace5-193">选择源维度和财务维度，以及用作清除源的值。</span><span class="sxs-lookup"><span data-stu-id="6ace5-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="6ace5-194">处理清除交易记录</span><span class="sxs-lookup"><span data-stu-id="6ace5-194">Process elimination transactions</span></span>
<span data-ttu-id="6ace5-195">可通过两种方法处理清除交易记录：在在线合并流程期间，或者通过创建清除日记帐并运行清除方案流程。</span><span class="sxs-lookup"><span data-stu-id="6ace5-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="6ace5-196">此部分重点介绍创建日记帐和运行清除流程。</span><span class="sxs-lookup"><span data-stu-id="6ace5-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="6ace5-197">在定义为清除公司的公司中，在“合并”模块中选择**清除日记帐**，</span><span class="sxs-lookup"><span data-stu-id="6ace5-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="6ace5-198">已选择了日记帐名称之后，单击**行**。</span><span class="sxs-lookup"><span data-stu-id="6ace5-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="6ace5-199">可以通过选择**方案**菜单，然后选择**清除方案**来运行方案。</span><span class="sxs-lookup"><span data-stu-id="6ace5-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="6ace5-200">选择充当合并的数据的源的公司，然后选择要处理的规则。</span><span class="sxs-lookup"><span data-stu-id="6ace5-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="6ace5-201">输入开始搜索清除金额的开始日期，以及结束清除金额的搜索日期的结束日期。</span><span class="sxs-lookup"><span data-stu-id="6ace5-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="6ace5-202">**GL 过帐日期**字段是用于将日记帐过帐到总帐的日期。</span><span class="sxs-lookup"><span data-stu-id="6ace5-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="6ace5-203">单击**确定**之后，可以查看金额和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="6ace5-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




