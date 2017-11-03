---
title: "项目合同"
description: "本文举例说明可以为不同类型的项目和融资来源创建的项目合同，以及如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中管理合同和发票项目客户。"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7a69036327c6e818c1d4a3da72ee2f4c2d19cfcd
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="project-contracts"></a><span data-ttu-id="f47ee-103">项目合同</span><span class="sxs-lookup"><span data-stu-id="f47ee-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f47ee-104">本文举例说明可以为不同类型的项目和融资来源创建的项目合同，以及如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中管理合同和发票项目客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="f47ee-105">为项目合同所创建项目的类型会确定用于向项目客户开票的方法。</span><span class="sxs-lookup"><span data-stu-id="f47ee-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="f47ee-106">您可以更改项目合同和相关的项目，但不能更改项目类型。</span><span class="sxs-lookup"><span data-stu-id="f47ee-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="f47ee-107">通过使用项目合同，可同时为一个或多个项目开具发票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="f47ee-108">项目合同还有助于确保为项目结构中的各个下级项目应用统一的开票程序。</span><span class="sxs-lookup"><span data-stu-id="f47ee-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="f47ee-109">要开票的每个项目都必须与项目合同相关联。</span><span class="sxs-lookup"><span data-stu-id="f47ee-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="f47ee-110">项目合同的设置会应用于与该项目合同关联的所有项目和下级项目。</span><span class="sxs-lookup"><span data-stu-id="f47ee-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="f47ee-111">项目合同可以指定投资的一个或多个来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="f47ee-112">因此，您能够将帐单拆分到多个出资者、设置融资限额（以便融资来源的出资不超出指定金额），以及配置收费支出的融资规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="f47ee-113">项目合同的融资</span><span class="sxs-lookup"><span data-stu-id="f47ee-113">Funding for project contracts</span></span>
<span data-ttu-id="f47ee-114">某些项目合同指定多个当事方将分担项目成本的融资责任。</span><span class="sxs-lookup"><span data-stu-id="f47ee-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="f47ee-115">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="f47ee-115">Here are some examples:</span></span>

-   <span data-ttu-id="f47ee-116">具有多个部门的一个大客户请求项目融资按部门拆分。</span><span class="sxs-lookup"><span data-stu-id="f47ee-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="f47ee-117">您的公司与外部组织分担大型项目的成本。</span><span class="sxs-lookup"><span data-stu-id="f47ee-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="f47ee-118">某个道路项目由两个城市共同出资。</span><span class="sxs-lookup"><span data-stu-id="f47ee-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="f47ee-119">某个桥梁项目通过政府拨款和私营公司提供资金。</span><span class="sxs-lookup"><span data-stu-id="f47ee-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="f47ee-120">在 Finance and Operations 中，您可以将一个交易记录或整个项目的帐单拆分到多个客户、拨款或组织中。</span><span class="sxs-lookup"><span data-stu-id="f47ee-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="f47ee-121">在具有过个出资者的项目中，对一个高级投资项目的融资做出贡献的所有当事方都被称作“融资来源”。</span><span class="sxs-lookup"><span data-stu-id="f47ee-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="f47ee-122">当将客户、组织或拨款定义为融资来源后，可以将它分配给一个或多个“融资规则”。</span><span class="sxs-lookup"><span data-stu-id="f47ee-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="f47ee-123">融资规则包含确定如何将费用分配给项目的不同融资来源的条件。</span><span class="sxs-lookup"><span data-stu-id="f47ee-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="f47ee-124">由于库存物料（例如出现在采购申请和采购订单上的那些）不能拆分，因此成本金额不能在分配时拆分到多个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="f47ee-125">因此，直到完成库存发货过帐，融资来源值一直保持为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="f47ee-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="f47ee-126">过帐库存发货后，则根据项目的科目分配规则分配成本金额。</span><span class="sxs-lookup"><span data-stu-id="f47ee-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="f47ee-127">以下是可帮助您更轻松地将帐单拆分到多个融资来源的一些步骤：</span><span class="sxs-lookup"><span data-stu-id="f47ee-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="f47ee-128">指定为项目所输入的所有交易记录按照合同使用相同的销售币种。</span><span class="sxs-lookup"><span data-stu-id="f47ee-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="f47ee-129">设置融资限额，以便融资来源对项目的开票不会多过指定金额。</span><span class="sxs-lookup"><span data-stu-id="f47ee-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="f47ee-130">为每个工作人员、物料、类别、类别组合交易记录类型（或所有交易记录类型）配置融资规则和融资限额。</span><span class="sxs-lookup"><span data-stu-id="f47ee-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="f47ee-131">选择可选的开始日期和结束日期以定义每个融资规则的有效时段。</span><span class="sxs-lookup"><span data-stu-id="f47ee-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="f47ee-132">指定每个融资来源负责的百分比。</span><span class="sxs-lookup"><span data-stu-id="f47ee-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="f47ee-133">指定对融资分配计算导致的舍入尾差负责的融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="f47ee-134">设置确定如何针对项目成本给外部客户开发票以及向内部组织收费的规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="f47ee-135">将这些交易记录记录到处于暂停状态的融资科目中，直到获得其他融资或直到您决定在内部承担成本。</span><span class="sxs-lookup"><span data-stu-id="f47ee-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="f47ee-136">为了确定与交易记录相关联的纳税组，将搜索该项目以获得纳税组分配。</span><span class="sxs-lookup"><span data-stu-id="f47ee-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="f47ee-137">如果没有在该项目级别中进行纳税组分配，将搜索项目合同。</span><span class="sxs-lookup"><span data-stu-id="f47ee-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="f47ee-138">示例：多个融资来源（简单）</span><span class="sxs-lookup"><span data-stu-id="f47ee-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="f47ee-139">下表为多个融资来源中的管理融资分配提供方案。</span><span class="sxs-lookup"><span data-stu-id="f47ee-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="f47ee-140">这些方案基于以下假设：</span><span class="sxs-lookup"><span data-stu-id="f47ee-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="f47ee-141">在应用其他融资规则条件前，融资分配会考虑优先级设置。</span><span class="sxs-lookup"><span data-stu-id="f47ee-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="f47ee-142">没有指定用以定义融资规则的有效时段的日期范围。</span><span class="sxs-lookup"><span data-stu-id="f47ee-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f47ee-143"><strong>方案</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="f47ee-144"><strong>融资来源</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="f47ee-145"><strong>分配百分比</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="f47ee-146"><strong>分配优先级</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f47ee-147">在其融资用尽前，要将成本分配到某一融资来源，在其融资用尽前，将成本分配到第二个融资来源，最后将剩余成本分配到第三个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-148">融资来源 1</span><span class="sxs-lookup"><span data-stu-id="f47ee-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="f47ee-149">融资来源 2</span><span class="sxs-lookup"><span data-stu-id="f47ee-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="f47ee-150">融资来源 3</span><span class="sxs-lookup"><span data-stu-id="f47ee-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-151">100%</span><span class="sxs-lookup"><span data-stu-id="f47ee-151">100%</span></span></li>
<li><span data-ttu-id="f47ee-152">100%</span><span class="sxs-lookup"><span data-stu-id="f47ee-152">100%</span></span></li>
<li><span data-ttu-id="f47ee-153">100%</span><span class="sxs-lookup"><span data-stu-id="f47ee-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-154">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-154">1</span></span></li>
<li><span data-ttu-id="f47ee-155">2</span><span class="sxs-lookup"><span data-stu-id="f47ee-155">2</span></span></li>
<li><span data-ttu-id="f47ee-156">3</span><span class="sxs-lookup"><span data-stu-id="f47ee-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f47ee-157">要分配的 75% 的成本到某一投资来源，并分配 25% 的成本到第二个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="f47ee-158">在这些融资来源中任何一个用尽时，要支付来自第三个融资来源的剩余成本。</span><span class="sxs-lookup"><span data-stu-id="f47ee-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-159">融资来源 1</span><span class="sxs-lookup"><span data-stu-id="f47ee-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="f47ee-160">融资来源 2</span><span class="sxs-lookup"><span data-stu-id="f47ee-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="f47ee-161">融资来源 3</span><span class="sxs-lookup"><span data-stu-id="f47ee-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-162">75%</span><span class="sxs-lookup"><span data-stu-id="f47ee-162">75%</span></span></li>
<li><span data-ttu-id="f47ee-163">25%</span><span class="sxs-lookup"><span data-stu-id="f47ee-163">25%</span></span></li>
<li><span data-ttu-id="f47ee-164">100%</span><span class="sxs-lookup"><span data-stu-id="f47ee-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-165">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-165">1</span></span></li>
<li><span data-ttu-id="f47ee-166">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-166">1</span></span></li>
<li><span data-ttu-id="f47ee-167">2</span><span class="sxs-lookup"><span data-stu-id="f47ee-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f47ee-168">要分配的 75% 的成本到某一投资来源，并分配 25% 的成本到第二个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="f47ee-169">在这些融资来源中的任何一个用尽时，要将剩余成本分拆到第三个融资来源和第四个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-170">融资来源 1</span><span class="sxs-lookup"><span data-stu-id="f47ee-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="f47ee-171">融资来源 2</span><span class="sxs-lookup"><span data-stu-id="f47ee-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="f47ee-172">融资来源 3</span><span class="sxs-lookup"><span data-stu-id="f47ee-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="f47ee-173">融资来源 4</span><span class="sxs-lookup"><span data-stu-id="f47ee-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-174">75%</span><span class="sxs-lookup"><span data-stu-id="f47ee-174">75%</span></span></li>
<li><span data-ttu-id="f47ee-175">25%</span><span class="sxs-lookup"><span data-stu-id="f47ee-175">25%</span></span></li>
<li><span data-ttu-id="f47ee-176">50%</span><span class="sxs-lookup"><span data-stu-id="f47ee-176">50%</span></span></li>
<li><span data-ttu-id="f47ee-177">50%</span><span class="sxs-lookup"><span data-stu-id="f47ee-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-178">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-178">1</span></span></li>
<li><span data-ttu-id="f47ee-179">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-179">1</span></span></li>
<li><span data-ttu-id="f47ee-180">2</span><span class="sxs-lookup"><span data-stu-id="f47ee-180">2</span></span></li>
<li><span data-ttu-id="f47ee-181">2</span><span class="sxs-lookup"><span data-stu-id="f47ee-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f47ee-182">要将前 25% 的成本分配到某一投资来源，并将剩余成本分配到另一个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-183">融资来源 1</span><span class="sxs-lookup"><span data-stu-id="f47ee-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="f47ee-184">融资来源 2</span><span class="sxs-lookup"><span data-stu-id="f47ee-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-185">25%</span><span class="sxs-lookup"><span data-stu-id="f47ee-185">25%</span></span></li>
<li><span data-ttu-id="f47ee-186">100%</span><span class="sxs-lookup"><span data-stu-id="f47ee-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f47ee-187">1</span><span class="sxs-lookup"><span data-stu-id="f47ee-187">1</span></span></li>
<li><span data-ttu-id="f47ee-188">2</span><span class="sxs-lookup"><span data-stu-id="f47ee-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="f47ee-189">示例：多个融资来源（复杂）</span><span class="sxs-lookup"><span data-stu-id="f47ee-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="f47ee-190">您有三个融资来源，并且要按以下顺序使用：</span><span class="sxs-lookup"><span data-stu-id="f47ee-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="f47ee-191">请在融资来源 2 用尽前平均使用融资来源 2 和融资来源 3。</span><span class="sxs-lookup"><span data-stu-id="f47ee-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="f47ee-192">继续使用融资来源 3 直到用尽。</span><span class="sxs-lookup"><span data-stu-id="f47ee-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="f47ee-193">在融资来源 3 用尽后使用融资来源 1。</span><span class="sxs-lookup"><span data-stu-id="f47ee-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="f47ee-194">若要实现此目标，您必须执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f47ee-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="f47ee-195">为融资来源 2 和融资来源 3 设置融资限额（针对它们各自的金额）。</span><span class="sxs-lookup"><span data-stu-id="f47ee-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="f47ee-196">创建以下融资规则：</span><span class="sxs-lookup"><span data-stu-id="f47ee-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="f47ee-197">规则 1（优先级 1）：分配 50% 的交易记录到融资来源 2 和 50% 的交易记录到融资来源 3。</span><span class="sxs-lookup"><span data-stu-id="f47ee-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="f47ee-198">规则 2（优先级 2）：分配 100% 的交易记录到融资来源 3。</span><span class="sxs-lookup"><span data-stu-id="f47ee-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="f47ee-199">规则 3（优先级 3）：分配 100% 的交易记录到融资来源 1。</span><span class="sxs-lookup"><span data-stu-id="f47ee-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="f47ee-200">此设置之所以能够发挥作用，是因为系统会比对规则和限额来检查交易记录，以确定是否将它们中的任何一个应用于交易记录。</span><span class="sxs-lookup"><span data-stu-id="f47ee-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="f47ee-201">如果没有指定规则或限额应用于该交易记录，则“所有交易记录”规则适用。</span><span class="sxs-lookup"><span data-stu-id="f47ee-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="f47ee-202">所有交易记录规则与所有交易记录匹配。</span><span class="sxs-lookup"><span data-stu-id="f47ee-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="f47ee-203">如果找到了与交易记录匹配的规则，只有在比对所设置的限额检查匹配后，才会首先应用分配到该规则的百分比。</span><span class="sxs-lookup"><span data-stu-id="f47ee-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="f47ee-204">如果满足某一限额，并且融资来源的资金已用尽，则不考虑与融资限额关联的融资规则，并且程序会检查要应用的下一个规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="f47ee-205">在某些情况下，只有部分交易记录可根据规则进行分配。</span><span class="sxs-lookup"><span data-stu-id="f47ee-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="f47ee-206">因为在分配交易记录时已到达限额，可能发送此情况。</span><span class="sxs-lookup"><span data-stu-id="f47ee-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="f47ee-207">在这种情况下，根据规则仅分配某些金额，例如分配 50% 到每个融资来源。</span><span class="sxs-lookup"><span data-stu-id="f47ee-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="f47ee-208">这是在本节中先前描述的规则 1 中的情况。</span><span class="sxs-lookup"><span data-stu-id="f47ee-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="f47ee-209">剩余金额则根据序列中的下一个规则进行分配。</span><span class="sxs-lookup"><span data-stu-id="f47ee-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="f47ee-210">下表进一步检查此情况。</span><span class="sxs-lookup"><span data-stu-id="f47ee-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f47ee-211"><strong>焦点</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="f47ee-212"><strong>详细信息</strong></span><span class="sxs-lookup"><span data-stu-id="f47ee-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f47ee-213">融资规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-214">规则 1（优先级 1）：所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="f47ee-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="f47ee-215">将融资来源 2 分配为 50% 和将融资来源 3 分配为 50%。</span><span class="sxs-lookup"><span data-stu-id="f47ee-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="f47ee-216">规则 2（优先级 2）：所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="f47ee-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="f47ee-217">将融资来源 3 分配为 100%。</span><span class="sxs-lookup"><span data-stu-id="f47ee-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="f47ee-218">规则 3（优先级 2）：所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="f47ee-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="f47ee-219">将融资来源 1 分配为 100%。</span><span class="sxs-lookup"><span data-stu-id="f47ee-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f47ee-220">融资限额</span><span class="sxs-lookup"><span data-stu-id="f47ee-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-221">融资来源 1 限额 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="f47ee-222">融资来源 2 限额 = 500.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="f47ee-223">融资来源 3 限额 = 750.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f47ee-224">交易记录 1</span><span class="sxs-lookup"><span data-stu-id="f47ee-224">Transaction 1</span></span></td>
<td><span data-ttu-id="f47ee-225"><strong>交易记录金额：</strong>100.00<strong>融资：</strong>交易记录将只根据规则 1 支付，因为在应用规则 1 后交易记录已完全支付。</span><span class="sxs-lookup"><span data-stu-id="f47ee-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="f47ee-226">在融资来源 2 和融资来源 3 之间平均投资该交易记录。</span><span class="sxs-lookup"><span data-stu-id="f47ee-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="f47ee-227">融资来源 2：50.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="f47ee-228">融资来源 3：50.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f47ee-229">交易记录 2</span><span class="sxs-lookup"><span data-stu-id="f47ee-229">Transaction 2</span></span></td>
<td><span data-ttu-id="f47ee-230"><strong>交易记录金额：</strong>5,000.00<strong>融资： </strong>交易记录将根据所有三个规则支付。<strong>规则 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="f47ee-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="f47ee-231">融资来源 2：450.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="f47ee-232">融资来源 3：450.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="f47ee-233">
<strong>规则 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="f47ee-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="f47ee-234">融资来源 3：250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="f47ee-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="f47ee-235">
<strong>规则 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="f47ee-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="f47ee-236">融资来源 1：3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="f47ee-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f47ee-237">为每个投资源分配的总投资</span><span class="sxs-lookup"><span data-stu-id="f47ee-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="f47ee-238">融资来源 1：3,850.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="f47ee-239">融资来源 2：500.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="f47ee-240">融资来源 3：750.00</span><span class="sxs-lookup"><span data-stu-id="f47ee-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="f47ee-241">记帐规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-241">Billing rules</span></span>
<span data-ttu-id="f47ee-242">在您与客户协商项目合同时，您定义如何以及何时可以为从事于项目合同的客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="f47ee-243">在设置项目合同和项目后，可以设置项目的计费规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="f47ee-244">计费规则基于项目合同中指定的项目条款。</span><span class="sxs-lookup"><span data-stu-id="f47ee-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="f47ee-245">可基于项目合同和项目类型的条款来创建计费规则，如与计费规则相关的时间、材料或固定价格。</span><span class="sxs-lookup"><span data-stu-id="f47ee-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="f47ee-246">您可以为项目合同创建多个汇票规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="f47ee-247">还可以分配计费规则到与同一项目合同相关的且有相似计费条目的多个项目。</span><span class="sxs-lookup"><span data-stu-id="f47ee-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="f47ee-248">您可以设置以下计费规则类型：</span><span class="sxs-lookup"><span data-stu-id="f47ee-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="f47ee-249">**交货单位** – 在您完成交货单位时对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="f47ee-250">在合同中定义交货单位。</span><span class="sxs-lookup"><span data-stu-id="f47ee-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="f47ee-251">**进度** – 在您完成相应项目的指定百分比时对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="f47ee-252">您可以设置计费规则自动计算已完成工作百分比，或可以手动计算已完成工作百分比以及向该客户开票的金额。</span><span class="sxs-lookup"><span data-stu-id="f47ee-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="f47ee-253">**里程碑** – 在里程碑到来时，针对项目里程碑全部金额对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="f47ee-254">**费用** – 针对您的服务再加上管理费用（通常是服务成本的百分比）对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="f47ee-255">**时间和材料** – 针对用在项目上的时间和材料对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="f47ee-256">对于计费规则的所有类型，可以指定从客户发票中扣减的保留百分比，直至项目达到商定的阶段。</span><span class="sxs-lookup"><span data-stu-id="f47ee-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="f47ee-257">在项目合同中指定付款保留百分比。</span><span class="sxs-lookup"><span data-stu-id="f47ee-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="f47ee-258">该金额基于客户发票中相应行的总值计算并从中扣除。</span><span class="sxs-lookup"><span data-stu-id="f47ee-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="f47ee-259">对于**“时间和材料”**和**“进度”**计费规则，您可以分配可计费的类别。</span><span class="sxs-lookup"><span data-stu-id="f47ee-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="f47ee-260">计费类别指示这些交易记录应包括在客户发票中。</span><span class="sxs-lookup"><span data-stu-id="f47ee-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="f47ee-261">当您准备为客户开票数时，发票项目的金额是基于计费规则计算的，并且将产生一个项目发票提案。</span><span class="sxs-lookup"><span data-stu-id="f47ee-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="f47ee-262">以下各节提供的示例展示了如何设置和管理项目的计费规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="f47ee-263">示例：创建基于已交货单位数量的计费规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="f47ee-264">您的组织加入协议，从而按照每次培训 10,000 的成本为客户的员工提供合计五次培训。</span><span class="sxs-lookup"><span data-stu-id="f47ee-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="f47ee-265">您在每次培训后对该客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="f47ee-266">当您设置合同的计费规则时，您会使用以下值：</span><span class="sxs-lookup"><span data-stu-id="f47ee-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="f47ee-267">交货单位是一个培训。</span><span class="sxs-lookup"><span data-stu-id="f47ee-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="f47ee-268">每次培训的单位价格是 $10,000 美元。</span><span class="sxs-lookup"><span data-stu-id="f47ee-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="f47ee-269">总单位的数量为五次培训。</span><span class="sxs-lookup"><span data-stu-id="f47ee-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="f47ee-270">在您完成了一个培训时，可以为交付的第一个单位创建 10,000 的发票，并将发票发送给客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="f47ee-271">示例：创建基于项目的指定完成百分比的计费规则（手动计算）</span><span class="sxs-lookup"><span data-stu-id="f47ee-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="f47ee-272">您的组织，软件参考公司，进入与客户的协议，以开发客户开发产品的一个方面。</span><span class="sxs-lookup"><span data-stu-id="f47ee-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="f47ee-273">您的组织同意在六个月中交付软件代码。</span><span class="sxs-lookup"><span data-stu-id="f47ee-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="f47ee-274">客户同意为工作付款给您的组织合计 $100,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="f47ee-275">您创建一个计费规则，根据项目的完成百分比（正如在合同中所指定的）来对客户开票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="f47ee-276">在第一个月结束时，您满足客户确定工作已完成百分比。</span><span class="sxs-lookup"><span data-stu-id="f47ee-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="f47ee-277">在您和客户审查项目后，您决定项目已完成 15%。</span><span class="sxs-lookup"><span data-stu-id="f47ee-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="f47ee-278">创建 15,000 的发票（100,000 的 15%）并将其发送给客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="f47ee-279">示例：创建基于项目的指定完成百分比的计费规则（自动计算）</span><span class="sxs-lookup"><span data-stu-id="f47ee-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="f47ee-280">您的组织（一家软件开发公司）同意用 30,000 的成本为客户开发一个工资计费程序数据包。</span><span class="sxs-lookup"><span data-stu-id="f47ee-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="f47ee-281">客户同意基于工作已完成百分比付款给您的组织。</span><span class="sxs-lookup"><span data-stu-id="f47ee-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="f47ee-282">您估计项目成本是 20,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="f47ee-283">项目合同指定了您在计费流程中使用的工作类别。</span><span class="sxs-lookup"><span data-stu-id="f47ee-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="f47ee-284">您为每个类别完成的工作的百分比自动计算发票金额设置计费规则。</span><span class="sxs-lookup"><span data-stu-id="f47ee-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="f47ee-285">您为每个类别设置预算：</span><span class="sxs-lookup"><span data-stu-id="f47ee-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="f47ee-286">**开发** – 15,000 的成本和 20,000 的收入</span><span class="sxs-lookup"><span data-stu-id="f47ee-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="f47ee-287">**安装** – 5,000 的成本和 10,000 的收入</span><span class="sxs-lookup"><span data-stu-id="f47ee-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="f47ee-288">在您第一次创建客户发票时，发票金额基于以下信息自动计算：</span><span class="sxs-lookup"><span data-stu-id="f47ee-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="f47ee-289">在一个月后，该项目的工作人员提交其工时表。</span><span class="sxs-lookup"><span data-stu-id="f47ee-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="f47ee-290">工作人员的工时的成本是开发 5,000 和安装 1,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="f47ee-291">开发工作完成 33%（5,000 实际成本/15,000 预算成本），并且安装工作完成为 20%（1,000 实际成本/5,000 预算成本）。</span><span class="sxs-lookup"><span data-stu-id="f47ee-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="f47ee-292">自动计算得出 8,667 的发票金额（20,000 的 33% + 10,000 的20%）。</span><span class="sxs-lookup"><span data-stu-id="f47ee-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="f47ee-293">创建 8,667 的发票并将其发送给客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="f47ee-294">示例：创建基于议定里程碑的计费规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="f47ee-295">您的组织（一家管理咨询公司）同意就客户计划销售的某个客户产品进行市场调查。</span><span class="sxs-lookup"><span data-stu-id="f47ee-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="f47ee-296">在 3 月，客户同意使用您的服务三个月的期间，并且同意付款 50,000 给您的组织。</span><span class="sxs-lookup"><span data-stu-id="f47ee-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="f47ee-297">项目有三个里程碑：</span><span class="sxs-lookup"><span data-stu-id="f47ee-297">The project has three milestones:</span></span>

-   <span data-ttu-id="f47ee-298">里程碑 1：收集客户数据– 3 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="f47ee-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="f47ee-299">里程碑 2：分析客户数据– 4 月 30 日。</span><span class="sxs-lookup"><span data-stu-id="f47ee-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="f47ee-300">里程碑 3：存在产品可用性方案– 3 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="f47ee-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="f47ee-301">客户同意为第一个里程碑付款 10,000 给您的组织，为第二个里程碑付款 20,000，为第三个里程碑付款 20,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="f47ee-302">在您设置项目合同时，您同意基于已完成的里程碑向客户收费。</span><span class="sxs-lookup"><span data-stu-id="f47ee-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="f47ee-303">计费规则设置包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="f47ee-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="f47ee-304">定义项目里程碑。</span><span class="sxs-lookup"><span data-stu-id="f47ee-304">Define the project milestones.</span></span>
-   <span data-ttu-id="f47ee-305">定义完成每个里程碑时对客户开票的金额。</span><span class="sxs-lookup"><span data-stu-id="f47ee-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="f47ee-306">在 3 月 31 日，当第一个里程碑完成时，您将里程碑标记为已完成，然后创建一个 10,000 的发票并将其提交给客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="f47ee-307">只有在将里程碑标记为完成后，您才能创建一个里程碑发票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="f47ee-308">示例：创建基于服务外加管理费用的计费规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="f47ee-309">您的组织（一家管理咨询公司）同意进行一项市场调查，来评估客户（一个零售公司）正在开发的产品的可用性。</span><span class="sxs-lookup"><span data-stu-id="f47ee-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="f47ee-310">该协议的条款指定，您将委派自己排名前三的管理顾问为其进行服务，三位顾问将基于时间和材料进行该调查。</span><span class="sxs-lookup"><span data-stu-id="f47ee-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="f47ee-311">客户同意每小时支付 100，外加相当于项目总咨询时间收费 10% 的管理费用。</span><span class="sxs-lookup"><span data-stu-id="f47ee-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="f47ee-312">在您设置项目合同时，创建一个计费规则，在项目咨询时间收费的基础上再加上 10% 的管理费。</span><span class="sxs-lookup"><span data-stu-id="f47ee-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="f47ee-313">在您为客户创建发票时，客户支付 10% 管理费加上顾问时间的成本。</span><span class="sxs-lookup"><span data-stu-id="f47ee-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="f47ee-314">例如，如果三个顾问在项目上工作总计 200 小时，基于以下计算公式创建金额为 22,000 的发票：</span><span class="sxs-lookup"><span data-stu-id="f47ee-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="f47ee-315">200 小时每小时 100 = 20,000</span><span class="sxs-lookup"><span data-stu-id="f47ee-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="f47ee-316">管理费用的 10% = 2,000</span><span class="sxs-lookup"><span data-stu-id="f47ee-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="f47ee-317">发票总金额= 22,000</span><span class="sxs-lookup"><span data-stu-id="f47ee-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="f47ee-318">如果收费是客户的应课税，则在项目合同中选择一个销售税组,该销售税组自动将输入到资费的记帐规则中。</span><span class="sxs-lookup"><span data-stu-id="f47ee-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="f47ee-319">示例：创建针对时间和物料值的计费规则</span><span class="sxs-lookup"><span data-stu-id="f47ee-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="f47ee-320">您的组织（一家软件咨询公司）同意提供五个技术顾问来为客户从事接下来六个月的软件开发项目。</span><span class="sxs-lookup"><span data-stu-id="f47ee-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="f47ee-321">客户同意为每小时的咨询服务支付 150，外加办公用品成本。</span><span class="sxs-lookup"><span data-stu-id="f47ee-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="f47ee-322">您的组织在每个月的月末发送发票给客户。</span><span class="sxs-lookup"><span data-stu-id="f47ee-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="f47ee-323">在您设置项目合同时，您同意就该项目的时间和物料每月向客户收费。</span><span class="sxs-lookup"><span data-stu-id="f47ee-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="f47ee-324">您创建包括以下信息的计费规则：</span><span class="sxs-lookup"><span data-stu-id="f47ee-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="f47ee-325">合同时段为六个月。</span><span class="sxs-lookup"><span data-stu-id="f47ee-325">The contract period is six months.</span></span>
-   <span data-ttu-id="f47ee-326">咨询时间将以每小时 150 的单价计算。</span><span class="sxs-lookup"><span data-stu-id="f47ee-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="f47ee-327">办公用品按成本开票，项目的总计成本不得超过 10,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="f47ee-328">在项目进行过程中，您在每个日历月末创建客户发票。</span><span class="sxs-lookup"><span data-stu-id="f47ee-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="f47ee-329">在第一个月期间，由该项目的顾问记录总计 800 个小时。</span><span class="sxs-lookup"><span data-stu-id="f47ee-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="f47ee-330">向项目收取的办公用品成本为 2,000。</span><span class="sxs-lookup"><span data-stu-id="f47ee-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="f47ee-331">因此，在本月底，创建了 122,000 的发票：以 800 个小时，每小时 150 进行计算，外加 2,000 的办公用品费用。</span><span class="sxs-lookup"><span data-stu-id="f47ee-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




