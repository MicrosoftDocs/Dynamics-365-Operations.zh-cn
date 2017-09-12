---
title: "成本核算术语"
description: "本主题定义了成本核算中使用的重要术语。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1f12e8e82430c79ee93f2284e5fdf47ac559525d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="cost-accounting-terminology"></a><span data-ttu-id="1214f-103">成本核算术语</span><span class="sxs-lookup"><span data-stu-id="1214f-103">Cost accounting terminology</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1214f-104">本主题定义了成本核算中使用的重要术语。</span><span class="sxs-lookup"><span data-stu-id="1214f-104">This topic defines the key terms that are used in Cost accounting.</span></span>

<span data-ttu-id="1214f-105">**成本核算**</span><span class="sxs-lookup"><span data-stu-id="1214f-105">**Cost accounting**</span></span>

<span data-ttu-id="1214f-106">成本核算允许您从不同的数据源收集数据，如总帐、子分类帐、预算和统计信息。</span><span class="sxs-lookup"><span data-stu-id="1214f-106">Cost accounting lets you collect data from various sources, such as the general ledger, sub-ledgers, budgets, and statistical information.</span></span> <span data-ttu-id="1214f-107">然后可以分析、汇总和评估成本数据，因而管理层在价格更新、预算、成本控制等方面可以做出最有利的决策。</span><span class="sxs-lookup"><span data-stu-id="1214f-107">You can then analyze, summarize, and evaluate cost data, so that management can make the best possible decisions for price updates, budgets, cost control, and so on.</span></span> <span data-ttu-id="1214f-108">用于成本分析的源数据在成本核算中独立处理。</span><span class="sxs-lookup"><span data-stu-id="1214f-108">The source data that is used for cost analysis is treated independently in Cost accounting.</span></span> <span data-ttu-id="1214f-109">因此，在成本核算中更新不影响源数据。</span><span class="sxs-lookup"><span data-stu-id="1214f-109">Therefore, updates in Cost accounting don’t affect the source data.</span></span> <span data-ttu-id="1214f-110">但是，你从不同的数据源收集成本数据时，尤其是当您从 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本中的总帐中导入主科目作为成本元素时，存在数据冗余，因为相同的数据同时存在于总帐和成本核算中。</span><span class="sxs-lookup"><span data-stu-id="1214f-110">However, when you collect cost data from various sources, and especially when you import the main accounts from General ledger in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition as cost elements, there is data redundancy, because the same data exists in both General ledger and Cost accounting.</span></span> <span data-ttu-id="1214f-111">此冗余是必需的，因为您使用财务管理进行外部报告，使用成本核算进行内部报告。</span><span class="sxs-lookup"><span data-stu-id="1214f-111">This redundancy is required, because you use financial management for external reporting and Cost accounting for internal reporting.</span></span>

<span data-ttu-id="1214f-112">**成本核算分类帐**</span><span class="sxs-lookup"><span data-stu-id="1214f-112">**Cost accounting ledger**</span></span>

<span data-ttu-id="1214f-113">成本核算分类帐是一个专门的框架，确定在成本核算的特定区域输入和显示流程、值和数量的方式。</span><span class="sxs-lookup"><span data-stu-id="1214f-113">The cost accounting ledger is a specialized framework that determines how processes, values, and quantities are entered and presented for a particular area in Cost accounting.</span></span> <span data-ttu-id="1214f-114">成本核算分类帐定义衡量成本对象上的成本的流程和规则。</span><span class="sxs-lookup"><span data-stu-id="1214f-114">The cost accounting ledger defines processes and rules for measuring costs on cost objects.</span></span> <span data-ttu-id="1214f-115">它处理成本交易记录，管理记录成本交易产生的值和数量变更的文档。</span><span class="sxs-lookup"><span data-stu-id="1214f-115">It handles cost transactions, and manages documents that record the changes in values and quantities that cost transactions produce.</span></span>

<span data-ttu-id="1214f-116">**成本条目**</span><span class="sxs-lookup"><span data-stu-id="1214f-116">**Cost entry**</span></span>

<span data-ttu-id="1214f-117">成本条目是通过数据连接器从总帐条目、成本分摊及成本日记帐中已过账成本条目转移的结果。</span><span class="sxs-lookup"><span data-stu-id="1214f-117">Cost entries are the result of a transfer via data connectors from general ledger entries, cost allocations, and posted cost entries in cost journals.</span></span>

<span data-ttu-id="1214f-118">**成本对象**</span><span class="sxs-lookup"><span data-stu-id="1214f-118">**Cost object**</span></span>

<span data-ttu-id="1214f-119">成本对象是指成本分摊到的任何类型的对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-119">Cost objects are any type of object that costs are allocated to.</span></span> <span data-ttu-id="1214f-120">以下是一些典型的成本对象：</span><span class="sxs-lookup"><span data-stu-id="1214f-120">Here are some typical cost objects:</span></span>

-   <span data-ttu-id="1214f-121">产品</span><span class="sxs-lookup"><span data-stu-id="1214f-121">Products</span></span>
-   <span data-ttu-id="1214f-122">项目</span><span class="sxs-lookup"><span data-stu-id="1214f-122">Projects</span></span>
-   <span data-ttu-id="1214f-123">资源</span><span class="sxs-lookup"><span data-stu-id="1214f-123">Resources</span></span>
-   <span data-ttu-id="1214f-124">部门</span><span class="sxs-lookup"><span data-stu-id="1214f-124">Departments</span></span>
-   <span data-ttu-id="1214f-125">成本中心</span><span class="sxs-lookup"><span data-stu-id="1214f-125">Cost centers</span></span>
-   <span data-ttu-id="1214f-126">地理区域</span><span class="sxs-lookup"><span data-stu-id="1214f-126">Geographic regions</span></span>

<span data-ttu-id="1214f-127">管理层使用成本对象量化成本，但也推动盈利分析。</span><span class="sxs-lookup"><span data-stu-id="1214f-127">Management uses cost objects to quantify costs, but also to drive profitability analysis.</span></span>

<span data-ttu-id="1214f-128">**成本元素**</span><span class="sxs-lookup"><span data-stu-id="1214f-128">**Cost element**</span></span>

<span data-ttu-id="1214f-129">成本元素作为跟踪和分类成本流向的功能使用。</span><span class="sxs-lookup"><span data-stu-id="1214f-129">Cost elements are used as a function to track and categorize where costs flow to.</span></span> <span data-ttu-id="1214f-130">成本元素有两种类型：主要成本和辅助成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-130">There are two types of cost elements: primary costs and secondary costs.</span></span> <span data-ttu-id="1214f-131">**主要成本** 主要成本元素表示从财务会计到成本核算的成本流动。</span><span class="sxs-lookup"><span data-stu-id="1214f-131">**Primary costs** The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="1214f-132">成本元素结构对应于总帐中的损益科目结构，其中成本元素可能对应于主科目。</span><span class="sxs-lookup"><span data-stu-id="1214f-132">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="1214f-133">并非所有的主科目都必须表示为成本元素，具体取决于业务要求。</span><span class="sxs-lookup"><span data-stu-id="1214f-133">Not all main accounts must be represented as cost elements, depending on business requirements.</span></span> <span data-ttu-id="1214f-134">以下是主要成本元素的一些示例：</span><span class="sxs-lookup"><span data-stu-id="1214f-134">Here are some examples of primary cost elements:</span></span>

-   <span data-ttu-id="1214f-135">所售货物成本 (COG)</span><span class="sxs-lookup"><span data-stu-id="1214f-135">Costs of goods sold (COGs)</span></span>
-   <span data-ttu-id="1214f-136">间接物料成本</span><span class="sxs-lookup"><span data-stu-id="1214f-136">Indirect material costs</span></span>
-   <span data-ttu-id="1214f-137">人员成本</span><span class="sxs-lookup"><span data-stu-id="1214f-137">Personnel costs</span></span>
-   <span data-ttu-id="1214f-138">能源成本</span><span class="sxs-lookup"><span data-stu-id="1214f-138">Energy costs</span></span>

<span data-ttu-id="1214f-139">**次要成本元素**</span><span class="sxs-lookup"><span data-stu-id="1214f-139">**Secondary cost element**</span></span> 

<span data-ttu-id="1214f-140">辅助成本元素表示内部成本流，因为这些成本仅在成本核算中创建和使用。</span><span class="sxs-lookup"><span data-stu-id="1214f-140">The secondary cost elements represent the internal flow of costs, because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="1214f-141">辅助成本元素有助于保障成本来源可以跟踪。</span><span class="sxs-lookup"><span data-stu-id="1214f-141">Secondary cost elements help guarantee that the source of costs can be traced.</span></span> <span data-ttu-id="1214f-142">这些成本元素在成本分摊和开销计算中使用。</span><span class="sxs-lookup"><span data-stu-id="1214f-142">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="1214f-143">以下是辅助成本元素的一些示例：</span><span class="sxs-lookup"><span data-stu-id="1214f-143">Here are some examples of secondary cost elements:</span></span>

-   <span data-ttu-id="1214f-144">生产成本</span><span class="sxs-lookup"><span data-stu-id="1214f-144">Production costs</span></span>
-   <span data-ttu-id="1214f-145">生产、物料和营销开销</span><span class="sxs-lookup"><span data-stu-id="1214f-145">Production, material, and marketing overheads</span></span>

<span data-ttu-id="1214f-146">**成本控制单元**</span><span class="sxs-lookup"><span data-stu-id="1214f-146">**Cost control unit**</span></span>

<span data-ttu-id="1214f-147">成本控制单元表示成本结构。</span><span class="sxs-lookup"><span data-stu-id="1214f-147">A cost control unit represents the cost structure.</span></span> <span data-ttu-id="1214f-148">它必须与成本核算分类帐中的成本对象维度相关联。</span><span class="sxs-lookup"><span data-stu-id="1214f-148">It must be associated with cost object dimensions in a cost accounting ledger.</span></span>

<span data-ttu-id="1214f-149">**版本**</span><span class="sxs-lookup"><span data-stu-id="1214f-149">**Version**</span></span>

<span data-ttu-id="1214f-150">版本用于模拟、查看和比较不同结果。</span><span class="sxs-lookup"><span data-stu-id="1214f-150">Versions are used to simulate, view, and compare various outcomes.</span></span> <span data-ttu-id="1214f-151">默认情况下，所有实际成本在一个名为“*实际*”的基础版本中查看。</span><span class="sxs-lookup"><span data-stu-id="1214f-151">By default, all actual costs are viewed in one base version that is known as *actual*.</span></span> <span data-ttu-id="1214f-152">对于预算和计算，您可以视需要处理任意数量的版本。</span><span class="sxs-lookup"><span data-stu-id="1214f-152">For budgets and calculations, you can work with as many versions as you require.</span></span> <span data-ttu-id="1214f-153">例如，您可以将预算数据导入到原始版本中，然后在修订版本中修订预算。</span><span class="sxs-lookup"><span data-stu-id="1214f-153">For example, you can import budget data into an original version and then revise the budget in a revised version.</span></span> <span data-ttu-id="1214f-154">对于计算，您可以创建多个版本。</span><span class="sxs-lookup"><span data-stu-id="1214f-154">For calculations, you can create multiple versions.</span></span> <span data-ttu-id="1214f-155">然后，您可以在这些不同的版本中使用适用于成本分摊的不同计算规则创建计算。</span><span class="sxs-lookup"><span data-stu-id="1214f-155">In these various versions, you can then create calculations by using different calculation rules that will be applied for cost allocation.</span></span>

<span data-ttu-id="1214f-156">**报表**</span><span class="sxs-lookup"><span data-stu-id="1214f-156">**Statement**</span></span>

<span data-ttu-id="1214f-157">报表是为负责控制成本的经理提供的视图。</span><span class="sxs-lookup"><span data-stu-id="1214f-157">Statements are views for the managers who are responsible for controlling costs.</span></span> <span data-ttu-id="1214f-158">报表由成本控制员定义，它们提供实际和预算成本的快速概览，甚至是偏差和计算版本。</span><span class="sxs-lookup"><span data-stu-id="1214f-158">Statements are defined by a cost controller, and they give a quick overview of actual and budgeted costs, and even deviations and calculation versions.</span></span> <span data-ttu-id="1214f-159">为了帮助保证经理仅查看由他们负责的数据，报表中显示的数据服从访问规则。</span><span class="sxs-lookup"><span data-stu-id="1214f-159">To help guarantee that managers view only data that they are accountable for, data that appears in the statements is subject to access rules.</span></span>

<span data-ttu-id="1214f-160">**数据连接器**</span><span class="sxs-lookup"><span data-stu-id="1214f-160">**Data connector**</span></span>

<span data-ttu-id="1214f-161">数据可以通过数据连接器从外部系统导入到成本核算中。</span><span class="sxs-lookup"><span data-stu-id="1214f-161">Data can be imported into Cost accounting from external systems via data connectors.</span></span> <span data-ttu-id="1214f-162">例如，您可以导入科目结构、维度、总帐条目和预算条目。</span><span class="sxs-lookup"><span data-stu-id="1214f-162">For example, you can import account structures, dimensions, general ledger entries, and budget entries.</span></span> <span data-ttu-id="1214f-163">您可以使用预先配置的数据连接器或自定义连接器导入数据和创建数据连接。</span><span class="sxs-lookup"><span data-stu-id="1214f-163">You can use preconfigured data connectors or custom connectors to import data and create data connections.</span></span>

<span data-ttu-id="1214f-164">**成本分类**</span><span class="sxs-lookup"><span data-stu-id="1214f-164">**Cost classification**</span></span>

<span data-ttu-id="1214f-165">成本分类根据其共享特征将成本分组。</span><span class="sxs-lookup"><span data-stu-id="1214f-165">Cost classification groups costs according to their shared characteristics.</span></span> <span data-ttu-id="1214f-166">例如，成本可按照元素、可追溯性和行为进行分组。</span><span class="sxs-lookup"><span data-stu-id="1214f-166">For example, costs can be grouped by elements, traceability, and behavior.</span></span>

-   <span data-ttu-id="1214f-167">**按元素分组** - 物料、人工和支出。</span><span class="sxs-lookup"><span data-stu-id="1214f-167">**By elements** – Materials, labor, and expenses.</span></span>
-   <span data-ttu-id="1214f-168">**按可追溯性分组** – 直接成本和间接成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-168">**By traceability** – Direct costs and indirect costs.</span></span> <span data-ttu-id="1214f-169">直接成本直接分配给成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-169">Direct costs are assigned directly to cost objects.</span></span> <span data-ttu-id="1214f-170">间接成本无法直接追溯到成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-170">Indirect costs aren't directly traceable to cost objects.</span></span> <span data-ttu-id="1214f-171">间接成本分配给成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-171">Indirect costs are allocated to cost objects.</span></span>
-   <span data-ttu-id="1214f-172">**按行为分组** – 固定，可变和半可变。</span><span class="sxs-lookup"><span data-stu-id="1214f-172">**By behavior** – Fixed, variable, and semi-variable.</span></span>

<span data-ttu-id="1214f-173">**成本行为**</span><span class="sxs-lookup"><span data-stu-id="1214f-173">**Cost behavior**</span></span>

<span data-ttu-id="1214f-174">成本行为根据成本在关键业务活动变化方面的行为对成本分类。</span><span class="sxs-lookup"><span data-stu-id="1214f-174">Cost behavior classifies costs according to their behavior in relation to changes in key business activities.</span></span> <span data-ttu-id="1214f-175">若要控制有效成本，管理层必须了解成本行为。</span><span class="sxs-lookup"><span data-stu-id="1214f-175">To control costs effectively, management must understand the cost behavior.</span></span> <span data-ttu-id="1214f-176">成本行为模式有三种类型：固定，可变和半可变。</span><span class="sxs-lookup"><span data-stu-id="1214f-176">There are three types of cost behavior pattern: fixed, variable, and semi-variable.</span></span>

- <span data-ttu-id="1214f-177">**固定成本** - 固定成本是在短期内不会变化的成本，无论活动水平是否发生变化。</span><span class="sxs-lookup"><span data-stu-id="1214f-177">**Fixed cost** - A fixed cost is a cost that doesn't vary in the short term, regardless of changes in activity level.</span></span> <span data-ttu-id="1214f-178">例如，固定成本可以是公司的基本运营费用，例如租金，不会因活动水平的增加或减少而受到影响。</span><span class="sxs-lookup"><span data-stu-id="1214f-178">For example, a fixed cost can be a basic operating expense of a business, such as rent, that won't be affected even if the activity level increases or decreases.</span></span>

- <span data-ttu-id="1214f-179">**可变成本** - 可变成本根据活动水平的变化而变化。</span><span class="sxs-lookup"><span data-stu-id="1214f-179">**Variable cost** - A variable cost changes according to changes in activity level.</span></span> <span data-ttu-id="1214f-180">例如，特定直接物料成本与出售的每个产品相关联。</span><span class="sxs-lookup"><span data-stu-id="1214f-180">For example, a specific direct materials cost is associated with each product that is sold.</span></span> <span data-ttu-id="1214f-181">售出的产品越多，直接物料成本越高。</span><span class="sxs-lookup"><span data-stu-id="1214f-181">The more products that are sold, the more direct materials costs there are.</span></span>

- <span data-ttu-id="1214f-182">**半可变成本** 半可变成本的部分为固定成本，部分为可变成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-182">**Semi-variable cost** - Semi-variable costs are partly fixed and partly variable costs.</span></span> <span data-ttu-id="1214f-183">例如，网络接入费用包括每月标准接入费和宽带使用费。</span><span class="sxs-lookup"><span data-stu-id="1214f-183">For example, an Internet access fee includes a standard monthly access fee and a broadband usage fee.</span></span> <span data-ttu-id="1214f-184">每月标准接入费是固定成本，宽带使用费是可变成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-184">The standard monthly access fee is a fixed cost, whereas the broadband usage fee is a variable cost.</span></span>

<span data-ttu-id="1214f-185">**间接成本**</span><span class="sxs-lookup"><span data-stu-id="1214f-185">**Overhead cost**</span></span>

<span data-ttu-id="1214f-186">开销成本是指经营业务的持续支出。</span><span class="sxs-lookup"><span data-stu-id="1214f-186">Overhead costs refer to the ongoing expenses of operating a business.</span></span> <span data-ttu-id="1214f-187">这些成本无法直接关联到具体的业务活动。</span><span class="sxs-lookup"><span data-stu-id="1214f-187">They are the costs that can’t be linked directly to specific business activities.</span></span> <span data-ttu-id="1214f-188">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="1214f-188">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="1214f-189">会计费用</span><span class="sxs-lookup"><span data-stu-id="1214f-189">Accounting fees</span></span>
-   <span data-ttu-id="1214f-190">折旧</span><span class="sxs-lookup"><span data-stu-id="1214f-190">Depreciations</span></span>
-   <span data-ttu-id="1214f-191">保险</span><span class="sxs-lookup"><span data-stu-id="1214f-191">Insurance</span></span>
-   <span data-ttu-id="1214f-192">兴趣</span><span class="sxs-lookup"><span data-stu-id="1214f-192">Interest</span></span>
-   <span data-ttu-id="1214f-193">法律费用</span><span class="sxs-lookup"><span data-stu-id="1214f-193">Legal fees</span></span>
-   <span data-ttu-id="1214f-194">税金</span><span class="sxs-lookup"><span data-stu-id="1214f-194">Taxes</span></span>
-   <span data-ttu-id="1214f-195">公共设施费用</span><span class="sxs-lookup"><span data-stu-id="1214f-195">Utilities costs</span></span>

<span data-ttu-id="1214f-196">**成本分配**</span><span class="sxs-lookup"><span data-stu-id="1214f-196">**Cost distribution**</span></span>

<span data-ttu-id="1214f-197">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-197">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="1214f-198">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="1214f-198">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

<span data-ttu-id="1214f-199">**成本分摊**</span><span class="sxs-lookup"><span data-stu-id="1214f-199">**Cost allocation**</span></span>

<span data-ttu-id="1214f-200">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-200">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="1214f-201">Finance and Operations 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="1214f-201">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="1214f-202">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="1214f-202">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="1214f-203">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="1214f-203">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="1214f-204">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="1214f-204">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="1214f-205">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="1214f-205">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="1214f-206">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="1214f-206">The allocation order is controlled by the cost control unit.</span></span>

<span data-ttu-id="1214f-207">**成本分摊政策**</span><span class="sxs-lookup"><span data-stu-id="1214f-207">**Cost allocation policy**</span></span>

<span data-ttu-id="1214f-208">成本分摊策略定义必须分配的金额和数量。</span><span class="sxs-lookup"><span data-stu-id="1214f-208">A cost allocation policy defines the amounts and quantities that must be allocated.</span></span> <span data-ttu-id="1214f-209">分摊规则包括确定要分摊的成本的分摊源规则和确定成本分配到哪些目标的分摊目标规则。</span><span class="sxs-lookup"><span data-stu-id="1214f-209">Allocation rules include allocation source rules, which determine the costs that are allocated, and allocation targets rules, which determine where the costs are allocated.</span></span> <span data-ttu-id="1214f-210">例如，所有设施服务成本为分摊源，可以分摊到一个组织中的不同部门（即分摊目标）。</span><span class="sxs-lookup"><span data-stu-id="1214f-210">For example, all costs for facility services are an allocation source that can be allocated to various departments in an organization (that is, to allocation targets).</span></span>

<span data-ttu-id="1214f-211">**分摊基础**</span><span class="sxs-lookup"><span data-stu-id="1214f-211">**Allocation base**</span></span>

<span data-ttu-id="1214f-212">分摊基础是指可以用来衡量和量化活动的基础，例如使用的计时，消耗的千瓦时，花费的直接人工小时，或者占用的平方英尺数。</span><span class="sxs-lookup"><span data-stu-id="1214f-212">The allocation base is the basis that can be used to measure and quantify activities, such as machine hours that are used, kilowatt hours that are consumed, direct labor hours that are spent, or square footage that is occupied.</span></span> <span data-ttu-id="1214f-213">它用于将成本分摊到一个或多个成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-213">It's used to allocate costs to one or more cost objects.</span></span>

<span data-ttu-id="1214f-214">**分摊原则**</span><span class="sxs-lookup"><span data-stu-id="1214f-214">**Allocation principle**</span></span>

<span data-ttu-id="1214f-215">其中一个分摊原则是按照成本率分摊成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-215">One of the allocation principles is to allocate cost by cost rate.</span></span> <span data-ttu-id="1214f-216">您可以使用实际期间成本率或历史成本率分摊成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-216">You can choose to allocate costs by using the actual period rate or a historical rate.</span></span> <span data-ttu-id="1214f-217">使用互惠方法进行的分摊有助于保证在使用实际期间成本率执行分摊前，通过一系列联立方程式确定分摊基数。</span><span class="sxs-lookup"><span data-stu-id="1214f-217">Allocation that uses the reciprocal method helps guarantee that the allocation base is determined by a series of simultaneous equations before allocation is done by using the actual period rate.</span></span>

<span data-ttu-id="1214f-218">**成本累积**</span><span class="sxs-lookup"><span data-stu-id="1214f-218">**Cost roll-up**</span></span>

<span data-ttu-id="1214f-219">成本累积的目的是包括特定成本对象的所有成本。</span><span class="sxs-lookup"><span data-stu-id="1214f-219">The purpose of cost roll-up is to include all costs for a given cost object.</span></span> <span data-ttu-id="1214f-220">合并水平由用户定义。</span><span class="sxs-lookup"><span data-stu-id="1214f-220">The level of aggregation is user-defined.</span></span> <span data-ttu-id="1214f-221">通过使用成本累积，您可以合并必须从一个成本对象分配到另一个成本对象的成本元素。</span><span class="sxs-lookup"><span data-stu-id="1214f-221">By using cost roll-up, you can aggregate elements of costs that must be allocated from one cost object to another.</span></span> <span data-ttu-id="1214f-222">不使用成本累积时，每一个成本元素都从一个成本对象分配到另一个成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-222">When cost roll-up isn't used, every single element of costs is allocated from one cost object to another.</span></span>

<span data-ttu-id="1214f-223">**成本率策略**</span><span class="sxs-lookup"><span data-stu-id="1214f-223">**Cost rate policy**</span></span>

<span data-ttu-id="1214f-224">成本率用于计算每个成本对象的价格。</span><span class="sxs-lookup"><span data-stu-id="1214f-224">The cost rate is used to calculate price per cost object.</span></span> <span data-ttu-id="1214f-225">若要了解价格的元素，您要定义成本率策略。</span><span class="sxs-lookup"><span data-stu-id="1214f-225">To understand the elements of the price, you define cost rate policies.</span></span> <span data-ttu-id="1214f-226">成本率有两种类型：历史成本率和计划成本率。</span><span class="sxs-lookup"><span data-stu-id="1214f-226">There are two types of cost rate: historical cost rate and planned cost rate.</span></span> <span data-ttu-id="1214f-227">历史成本率是经过计算的成本率，作为成本对象分摊基数的倍数使用。</span><span class="sxs-lookup"><span data-stu-id="1214f-227">A historical cost rate is a calculated rate that is used as a multiplier for the allocation base of a cost object.</span></span> <span data-ttu-id="1214f-228">此成本率是基于上一期的成本分摊计算而得。</span><span class="sxs-lookup"><span data-stu-id="1214f-228">The rate is calculated based on the cost allocations in the previous period.</span></span> <span data-ttu-id="1214f-229">计划成本率是由用户定义的成本率。</span><span class="sxs-lookup"><span data-stu-id="1214f-229">A planned rate is a user-defined rate.</span></span>

<span data-ttu-id="1214f-230">**维度层次结构**</span><span class="sxs-lookup"><span data-stu-id="1214f-230">**Dimensional hierarchy**</span></span>

<span data-ttu-id="1214f-231">维度层次结构用作您定义分摊规则、成本率和成本累积时，查看 Microsoft Excel 中的报表或数据时，以及定义合并数据访问权限时的报告结构。</span><span class="sxs-lookup"><span data-stu-id="1214f-231">Dimension hierarchies are used as reporting structures when you define rules for allocation, cost rate, and cost roll-up, view statements or data in Microsoft Excel, and define access to the aggregated data.</span></span> <span data-ttu-id="1214f-232">有两种维度层次结构：分类层次结构和分级层次结构。</span><span class="sxs-lookup"><span data-stu-id="1214f-232">There are two dimension hierarchies: categorization hierarchy and classification hierarchy.</span></span> <span data-ttu-id="1214f-233">定义分类层次结构的基础是成本元素，而定义分级层次结构的基础是成本对象。</span><span class="sxs-lookup"><span data-stu-id="1214f-233">A categorization hierarchy is defined based on cost elements, whereas a classification hierarchy is defined based on cost objects.</span></span>

<span data-ttu-id="1214f-234">**统计维度**</span><span class="sxs-lookup"><span data-stu-id="1214f-234">**Statistical dimension**</span></span>

<span data-ttu-id="1214f-235">统计维度是对象盘点或总和的表达式，可以用作分摊或成本率计算的基础。</span><span class="sxs-lookup"><span data-stu-id="1214f-235">A statistical dimension is the expression of a count or sum of an object that can be used as the basis for allocations or cost rate calculations.</span></span> <span data-ttu-id="1214f-236">它可以手动创建或从源系统中导入。</span><span class="sxs-lookup"><span data-stu-id="1214f-236">It's either created manually or imported from source systems.</span></span> <span data-ttu-id="1214f-237">统计维度的例子包括员工人数、各设备上的许可软件的数量、每台机器的耗电量或者成本中心的面积。</span><span class="sxs-lookup"><span data-stu-id="1214f-237">Examples of statistical dimensions include the number of employees, the count of licensed software on each device, power consumption of each machine, or square meters for a cost center.</span></span>

<span data-ttu-id="1214f-238">**统计条目**</span><span class="sxs-lookup"><span data-stu-id="1214f-238">**Statistical entry**</span></span>

<span data-ttu-id="1214f-239">统计条目保留特定统计维度的已记录的总和或盘点值。</span><span class="sxs-lookup"><span data-stu-id="1214f-239">Statistical entries hold the recorded sum or count value for a given statistical dimension.</span></span> <span data-ttu-id="1214f-240">记录的总和或盘点值也称作度量值。</span><span class="sxs-lookup"><span data-stu-id="1214f-240">The recorded sum or count value is also referred to as the magnitude.</span></span>




