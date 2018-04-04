---
title: "成本核算术语"
description: "本主题定义了成本核算中使用的重要术语。"
author: YuyuScheller
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1ec2f4a407c705fb37681f5593d0f7ea31f4cf0f
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="cost-accounting-terminology"></a><span data-ttu-id="c5ee5-103">成本核算术语</span><span class="sxs-lookup"><span data-stu-id="c5ee5-103">Cost accounting terminology</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c5ee5-104">本主题定义了成本核算中使用的重要术语。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-104">This topic defines the key terms that are used in Cost accounting.</span></span>

<span data-ttu-id="c5ee5-105">**分配基数**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-105">**Allocation base**</span></span>

<span data-ttu-id="c5ee5-106">分配基础用于衡量和量化活动，例如使用机器的时间、消耗的千瓦时或占用的平方英尺。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-106">The allocation base is used to measure and quantify activities, such as machine hours that are used, kilowatt hours that are consumed, or square footage that is occupied.</span></span> <span data-ttu-id="c5ee5-107">它被用作将成本分摊到一个或多个成本对象的基础。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-107">It's used as basis for allocating costs to one or more cost objects</span></span>

<span data-ttu-id="c5ee5-108">**成本核算**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-108">**Cost accounting**</span></span>

<span data-ttu-id="c5ee5-109">成本核算允许您从不同的数据源收集数据，如总帐、子分类帐、预算和统计信息。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-109">Cost accounting lets you collect data from various sources, such as the general ledger, sub-ledgers, budgets, and statistical information.</span></span> <span data-ttu-id="c5ee5-110">然后可以分析、汇总和评估成本数据，因而管理层在价格更新、预算、成本控制等方面可以做出最有利的决策。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-110">You can then analyze, summarize, and evaluate cost data, so that management can make the best possible decisions for price updates, budgets, cost control, and so on.</span></span> <span data-ttu-id="c5ee5-111">用于成本分析的源数据在成本核算中独立处理。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-111">The source data that is used for cost analysis is treated independently in Cost accounting.</span></span> <span data-ttu-id="c5ee5-112">因此，在成本核算中更新不影响源数据。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-112">Therefore, updates in Cost accounting don’t affect the source data.</span></span> <span data-ttu-id="c5ee5-113">但是，你从不同的数据源收集成本数据时，尤其是当您从 Microsoft Dynamics 365 for Finance and Operations 中的总帐中导入主科目作为成本元素时，存在数据冗余，因为相同的数据同时存在于总帐和成本核算中。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-113">However, when you collect cost data from various sources, and especially when you import the main accounts from General ledger in Microsoft Dynamics 365 for Finance and Operations as cost elements, there is data redundancy, because the same data exists in both General ledger and Cost accounting.</span></span> <span data-ttu-id="c5ee5-114">此冗余是必需的，因为您使用财务管理进行外部报告，使用成本核算进行内部报告。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-114">This redundancy is required, because you use financial management for external reporting and Cost accounting for internal reporting.</span></span>

<span data-ttu-id="c5ee5-115">**成本核算分类帐**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-115">**Cost accounting ledger**</span></span>

<span data-ttu-id="c5ee5-116">它按日历、币种和成本元素维度进行定义，控制用于衡量成本的流程和政策。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-116">Defined by calendar, currency, and cost element dimension, it controls processes and policies for measuring costs.</span></span> 

<span data-ttu-id="c5ee5-117">**成本条目**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-117">**Cost entry**</span></span>

<span data-ttu-id="c5ee5-118">成本条目是通过数据连接器从总帐条目、成本分摊及成本日记帐中已过账成本条目转移的结果。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-118">Cost entries are the result of a transfer via data connectors from general ledger entries, cost allocations, and posted cost entries in cost journals.</span></span>

<span data-ttu-id="c5ee5-119">**成本对象**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-119">**Cost object**</span></span>

<span data-ttu-id="c5ee5-120">被选定用于成本控制的任何对象类型。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-120">Any type of object that is selected for cost control.</span></span> <span data-ttu-id="c5ee5-121">在成本对象上直接过帐或分配到成本对象的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-121">Costs or revenues are either directly posted on or allocated to cost objects.</span></span> <span data-ttu-id="c5ee5-122">一些典型的成本对象是：</span><span class="sxs-lookup"><span data-stu-id="c5ee5-122">Some typical cost objects are:</span></span>

-  <span data-ttu-id="c5ee5-123">产品</span><span class="sxs-lookup"><span data-stu-id="c5ee5-123">Products</span></span>
-  <span data-ttu-id="c5ee5-124">项目</span><span class="sxs-lookup"><span data-stu-id="c5ee5-124">Projects</span></span>
-  <span data-ttu-id="c5ee5-125">部门</span><span class="sxs-lookup"><span data-stu-id="c5ee5-125">Departments</span></span>
-  <span data-ttu-id="c5ee5-126">成本中心</span><span class="sxs-lookup"><span data-stu-id="c5ee5-126">Cost centers</span></span>

<span data-ttu-id="c5ee5-127">管理层使用成本对象量化成本，但也推动盈利分析。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-127">Management uses cost objects to quantify costs, but also to drive profitability analysis.</span></span>

<span data-ttu-id="c5ee5-128">**成本元素**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-128">**Cost element**</span></span>

<span data-ttu-id="c5ee5-129">作为跟踪成本和对成本分类的功能使用。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-129">Used as a function to track and categorize costs.</span></span> <span data-ttu-id="c5ee5-130">成本元素有两种类型：主要成本和辅助成本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-130">There are two types of cost elements: primary and secondary.</span></span>

<span data-ttu-id="c5ee5-131">主要成本元素表示从财务会计到成本核算的成本流动。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-131">Primary cost elements represent the cost flow from financial accounting to Cost accounting.</span></span> <span data-ttu-id="c5ee5-132">结构通常对应于总帐中的损益科目结构，其中成本元素可能对应于主科目。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-132">The structure typically corresponds to the profit and loss account structure in the general ledger where a cost element can correspond to a main account.</span></span> <span data-ttu-id="c5ee5-133">并非所有的主科目都必须表示为成本元素，具体取决于业务要求。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-133">Not all main accounts must be represented as cost elements, depending on business requirements.</span></span> 

<span data-ttu-id="c5ee5-134">辅助成本元素表示内部成本流，因为这些成本仅在成本核算中使用。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-134">Secondary cost elements represent the internal cost flow because these costs are only used in Cost accounting.</span></span> <span data-ttu-id="c5ee5-135">它们在成本累积规则中使用，用于将成本聚合到开销计算所使用的有意义的时段。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-135">They are used in cost roll-up rules to aggregate costs into meaningful buckets used by overhead calculation.</span></span> 

<span data-ttu-id="c5ee5-136">**成本分类**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-136">**Cost classification**</span></span>

<span data-ttu-id="c5ee5-137">成本分类根据其共享特征将成本分组。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-137">Cost classification groups costs according to their shared characteristics.</span></span> <span data-ttu-id="c5ee5-138">例如，成本可按照元素、可追溯性和行为进行分组。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-138">For example, costs can be grouped by elements, traceability, and behavior.</span></span>

-   <span data-ttu-id="c5ee5-139">**按元素分组** - 物料、人工和支出。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-139">**By elements** – Materials, labor, and expenses.</span></span>
-   <span data-ttu-id="c5ee5-140">**按可追溯性分组** – 直接成本和间接成本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-140">**By traceability** – Direct costs and indirect costs.</span></span> <span data-ttu-id="c5ee5-141">直接成本直接分配给成本对象。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-141">Direct costs are assigned directly to cost objects.</span></span> <span data-ttu-id="c5ee5-142">间接成本无法直接追溯到成本对象。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-142">Indirect costs aren't directly traceable to cost objects.</span></span> <span data-ttu-id="c5ee5-143">间接成本分配给成本对象。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-143">Indirect costs are allocated to cost objects.</span></span>
-   <span data-ttu-id="c5ee5-144">**按行为分组** – 固定，可变和半可变。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-144">**By behavior** – Fixed, variable, and semi-variable.</span></span>

<span data-ttu-id="c5ee5-145">**成本行为**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-145">**Cost behavior**</span></span>

<span data-ttu-id="c5ee5-146">成本行为根据成本在关键业务活动变化方面的行为对成本分类。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-146">Cost behavior classifies costs according to their behavior in relation to changes in key business activities.</span></span> <span data-ttu-id="c5ee5-147">若要控制有效成本，管理层必须了解成本行为。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-147">To control costs effectively, management must understand the cost behavior.</span></span> <span data-ttu-id="c5ee5-148">成本行为模式有三种类型：固定，可变和半可变。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-148">There are three types of cost behavior pattern: fixed, variable, and semi-variable.</span></span>

- <span data-ttu-id="c5ee5-149">**固定成本** - 固定成本是在短期内不会变化的成本，无论活动水平是否发生变化。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-149">**Fixed cost** - A fixed cost is a cost that doesn't vary in the short term, regardless of changes in activity level.</span></span> <span data-ttu-id="c5ee5-150">例如，固定成本可以是公司的基本运营费用，例如租金，不会因活动水平的增加或减少而受到影响。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-150">For example, a fixed cost can be a basic operating expense of a business, such as rent, that won't be affected even if the activity level increases or decreases.</span></span>

- <span data-ttu-id="c5ee5-151">**可变成本** - 可变成本根据活动水平的变化而变化。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-151">**Variable cost** - A variable cost changes according to changes in activity level.</span></span> <span data-ttu-id="c5ee5-152">例如，特定直接物料成本与出售的每个产品相关联。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-152">For example, a specific direct materials cost is associated with each product that is sold.</span></span> <span data-ttu-id="c5ee5-153">售出的产品越多，直接物料成本越高。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-153">The more products that are sold, the more direct materials costs there are.</span></span>

- <span data-ttu-id="c5ee5-154">**半可变成本** 半可变成本的部分为固定成本，部分为可变成本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-154">**Semi-variable cost** - Semi-variable costs are partly fixed and partly variable costs.</span></span> <span data-ttu-id="c5ee5-155">例如，网络接入费用包括每月标准接入费和宽带使用费。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-155">For example, an Internet access fee includes a standard monthly access fee and a broadband usage fee.</span></span> <span data-ttu-id="c5ee5-156">每月标准接入费是固定成本，宽带使用费是可变成本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-156">The standard monthly access fee is a fixed cost, whereas the broadband usage fee is a variable cost.</span></span>

<span data-ttu-id="c5ee5-157">**成本控制单元**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-157">**Cost control unit**</span></span>

<span data-ttu-id="c5ee5-158">成本控制单元表示成本结构。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-158">The cost control unit represents the cost structure.</span></span> <span data-ttu-id="c5ee5-159">结构确定成本如何按层次结构顺序在成本对象维度与其各自的成本对象之间流动。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-159">The structure determines how cost flows in a hierarchical order between cost object dimensions and their respective cost objects.</span></span> 

<span data-ttu-id="c5ee5-160">**成本分配**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-160">**Cost distribution**</span></span>

<span data-ttu-id="c5ee5-161">用于通过应用相关的分配基础将成本从一个成本对象分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-161">Is used to distribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c5ee5-162">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别，且无互惠处理。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-162">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost and no reciprocal processing.</span></span>

<span data-ttu-id="c5ee5-163">**成本分摊**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-163">**Cost allocation**</span></span>

<span data-ttu-id="c5ee5-164">用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-164">Is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c5ee5-165">Finance and Operations 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-165">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c5ee5-166">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-166">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c5ee5-167">系统自动确定执行分摊的正确顺序且对其进行循环访问。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-167">The system automatically determines the order to perform the allocations in and iterate over it.</span></span> <span data-ttu-id="c5ee5-168">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-168">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c5ee5-169">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-169">Allocations across cost object dimensions and their respective members are supported.</span></span> <span data-ttu-id="c5ee5-170">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-170">The allocation order is controlled by the cost control unit.</span></span>

<span data-ttu-id="c5ee5-171">**成本分摊政策**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-171">**Cost allocation policy**</span></span>

<span data-ttu-id="c5ee5-172">成本分摊策略定义必须分配的金额和数量。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-172">A cost allocation policy defines the amounts and quantities that must be allocated.</span></span> <span data-ttu-id="c5ee5-173">分摊规则包括确定要分摊的成本的分摊源规则和确定成本分配到哪些目标的分摊目标规则。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-173">Allocation rules include allocation source rules, which determine the costs that are allocated, and allocation targets rules, which determine where the costs are allocated.</span></span> <span data-ttu-id="c5ee5-174">例如，所有设施服务成本为分摊源，可以分摊到一个组织中的不同部门（即分摊目标）。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-174">For example, all costs for facility services are an allocation source that can be allocated to various departments in an organization (that is, to allocation targets).</span></span>

<span data-ttu-id="c5ee5-175">**成本累积**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-175">**Cost roll-up**</span></span>

<span data-ttu-id="c5ee5-176">成本累积规则的目的是将成本聚合到有意义的时段。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-176">The purpose of cost roll-up rules is to aggregate costs into meaningful buckets.</span></span> <span data-ttu-id="c5ee5-177">聚合级别由用户定义，涉及辅助成本元素的分配。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-177">The level of aggregation is user-defined and involves the assignment of a secondary cost element.</span></span> <span data-ttu-id="c5ee5-178">如果不使用成本累积，每一个成本元素都从一个成本对象分配到另一个成本对象</span><span class="sxs-lookup"><span data-stu-id="c5ee5-178">If cost roll-up is not used, every element of a cost is allocated from one cost object to another</span></span>

<span data-ttu-id="c5ee5-179">**成本率策略**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-179">**Cost rate policy**</span></span>

<span data-ttu-id="c5ee5-180">成本率用于计算每个成本对象的价格。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-180">The cost rate is used to calculate price per cost object.</span></span> <span data-ttu-id="c5ee5-181">若要了解价格的元素，您要定义成本率策略。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-181">To understand the elements of the price, you define cost rate policies.</span></span> <span data-ttu-id="c5ee5-182">成本率有两种类型：历史成本率和计划成本率。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-182">There are two types of cost rate: historical cost rate and planned cost rate.</span></span> <span data-ttu-id="c5ee5-183">历史成本率是经过计算的成本率，作为成本对象分摊基数的倍数使用。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-183">A historical cost rate is a calculated rate that is used as a multiplier for the allocation base of a cost object.</span></span> <span data-ttu-id="c5ee5-184">此成本率是基于上一期的成本分摊计算而得。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-184">The rate is calculated based on the cost allocations in the previous period.</span></span> <span data-ttu-id="c5ee5-185">计划成本率是由用户定义的成本率。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-185">A planned rate is a user-defined rate.</span></span>

<span data-ttu-id="c5ee5-186">**维度层次结构**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-186">**Dimension hierarchy**</span></span>

<span data-ttu-id="c5ee5-187">有两种维度层次结构：分类层次结构和分级层次结构。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-187">There are two dimension hierarchies: categorization hierarchy and classification hierarchy.</span></span> <span data-ttu-id="c5ee5-188">维度分类层次结构类型用于报告目的。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-188">The dimension categorization hierarchy type is used for reporting purposes.</span></span> <span data-ttu-id="c5ee5-189">它仅支持成本元素维度。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-189">It supports only the cost element dimensions.</span></span> <span data-ttu-id="c5ee5-190">维度分级层次结构类型用于定义策略和用于报告目的。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-190">The dimension classification hierarchy type is used to define policies and for reporting purposes.</span></span> <span data-ttu-id="c5ee5-191">它支持所有维度，例如成本对象、成本元素和统计维度。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-191">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span> 

<span data-ttu-id="c5ee5-192">**数据连接器**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-192">**Data connector**</span></span>

<span data-ttu-id="c5ee5-193">成本核算支持通过一组数据连接器集成来自源系统的数据。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-193">Cost accounting supports integration of data from source systems via a set of data connectors.</span></span> <span data-ttu-id="c5ee5-194">提供以下数据连接器：</span><span class="sxs-lookup"><span data-stu-id="c5ee5-194">The following data connectors are available:</span></span>

-  <span data-ttu-id="c5ee5-195">已导入的交易记录（预配置）</span><span class="sxs-lookup"><span data-stu-id="c5ee5-195">Imported transactions (pre-configured)</span></span>
-  <span data-ttu-id="c5ee5-196">Dynamics 365 for Finance and Operations（预配置）</span><span class="sxs-lookup"><span data-stu-id="c5ee5-196">Dynamics 365 for Finance and Operations (pre-configured)</span></span>
-  <span data-ttu-id="c5ee5-197">Dynamics AX（需要配置）</span><span class="sxs-lookup"><span data-stu-id="c5ee5-197">Dynamics AX (configuration required)</span></span>

<span data-ttu-id="c5ee5-198">**注意：**数据连接器导入的交易记录基于数据实体。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-198">**Note:** The data connector Imported transactions is based on data entities.</span></span>

<span data-ttu-id="c5ee5-199">**数据提供程序**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-199">**Data provider**</span></span>

<span data-ttu-id="c5ee5-200">大多数源系统可以提供与成本核算中的一个或多个数据源匹配的数据。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-200">Most source systems can provide data that matches one or more data sources in Cost accounting.</span></span> <span data-ttu-id="c5ee5-201">若要根据成本核算中的数据源调整来自源系统的数据，需要配置一个数据提供程序。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-201">To align data from the source systems with the data source in Cost accounting, a data provider needs to be configured.</span></span> <span data-ttu-id="c5ee5-202">下表按数据连接器和数据源列出了数据提供程序的可用性。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-202">The following table lists the availability of data providers per data connector and data source.</span></span>

|  <span data-ttu-id="c5ee5-203">**数据源**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-203">**Data sources**</span></span> |  <span data-ttu-id="c5ee5-204">**导入的交易记录数据连接器**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-204">**Imported transactions data connector**</span></span> | <span data-ttu-id="c5ee5-205">**Dynamics 365 for Finance and Operations 数据连接器**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-205">**Dynamics 365 for Finance and Operations data connector**</span></span>  | <span data-ttu-id="c5ee5-206">**Dynamics AX 数据连接器**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-206">**Dynamics AX data connector**</span></span>  |
|---|---|---|---|
| <span data-ttu-id="c5ee5-207">成本元素维度成员</span><span class="sxs-lookup"><span data-stu-id="c5ee5-207">Cost element dimension members</span></span>  |  <span data-ttu-id="c5ee5-208">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-208">Yes</span></span> | <span data-ttu-id="c5ee5-209">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-209">Yes</span></span>  | <span data-ttu-id="c5ee5-210">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-210">Yes</span></span>  |
|  <span data-ttu-id="c5ee5-211">成本对象维度成员</span><span class="sxs-lookup"><span data-stu-id="c5ee5-211">Cost object dimension members</span></span> |  <span data-ttu-id="c5ee5-212">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-212">Yes</span></span> | <span data-ttu-id="c5ee5-213">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-213">Yes</span></span>  | <span data-ttu-id="c5ee5-214">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-214">Yes</span></span>  |
|  <span data-ttu-id="c5ee5-215">统计维度成员</span><span class="sxs-lookup"><span data-stu-id="c5ee5-215">Statistical dimension members</span></span> | <span data-ttu-id="c5ee5-216">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-216">Yes</span></span>  | <span data-ttu-id="c5ee5-217">无</span><span class="sxs-lookup"><span data-stu-id="c5ee5-217">No</span></span>  | <span data-ttu-id="c5ee5-218">无</span><span class="sxs-lookup"><span data-stu-id="c5ee5-218">No</span></span>  |
|  <span data-ttu-id="c5ee5-219">总帐</span><span class="sxs-lookup"><span data-stu-id="c5ee5-219">General ledger</span></span> | <span data-ttu-id="c5ee5-220">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-220">Yes</span></span>  | <span data-ttu-id="c5ee5-221">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-221">Yes</span></span>  | <span data-ttu-id="c5ee5-222">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-222">Yes</span></span>  |
|  <span data-ttu-id="c5ee5-223">预算条目</span><span class="sxs-lookup"><span data-stu-id="c5ee5-223">Budget entries</span></span>  | <span data-ttu-id="c5ee5-224">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-224">Yes</span></span>  | <span data-ttu-id="c5ee5-225">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-225">Yes</span></span>  | <span data-ttu-id="c5ee5-226">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-226">Yes</span></span>  |
|  <span data-ttu-id="c5ee5-227">统计度量</span><span class="sxs-lookup"><span data-stu-id="c5ee5-227">Statistical measures</span></span> | <span data-ttu-id="c5ee5-228">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-228">Yes</span></span>  | <span data-ttu-id="c5ee5-229">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-229">Yes</span></span>  | <span data-ttu-id="c5ee5-230">是</span><span class="sxs-lookup"><span data-stu-id="c5ee5-230">Yes</span></span>  |

<span data-ttu-id="c5ee5-231">**配方**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-231">**Formula**</span></span>

<span data-ttu-id="c5ee5-232">公式分配基础可以定义高级公式以实现正确的分配基础。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-232">Formula allocation bases let you define advanced formulas to achieve the correct allocation basis.</span></span> <span data-ttu-id="c5ee5-233">您可以手动创建公式分配基础。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-233">You can manually create formula allocation bases.</span></span> <span data-ttu-id="c5ee5-234">可以使用以下运算符定义您的公式。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-234">You can use the following operators to define your formula.</span></span>

|  <span data-ttu-id="c5ee5-235">**符号**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-235">**Symbols**</span></span> | <span data-ttu-id="c5ee5-236">**文本**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-236">**Text**</span></span>  |
|---|---|
|  <span data-ttu-id="c5ee5-237">( )</span><span class="sxs-lookup"><span data-stu-id="c5ee5-237">( )</span></span> | <span data-ttu-id="c5ee5-238">括号</span><span class="sxs-lookup"><span data-stu-id="c5ee5-238">Parentheses</span></span>  |
|  < |  <span data-ttu-id="c5ee5-239">小于</span><span class="sxs-lookup"><span data-stu-id="c5ee5-239">Smaller than</span></span> |
|  > |  <span data-ttu-id="c5ee5-240">大于</span><span class="sxs-lookup"><span data-stu-id="c5ee5-240">Larger than</span></span> |
|  + |  <span data-ttu-id="c5ee5-241">增加额</span><span class="sxs-lookup"><span data-stu-id="c5ee5-241">Addition</span></span> |
|  <span data-ttu-id="c5ee5-242">–</span><span class="sxs-lookup"><span data-stu-id="c5ee5-242">–</span></span> |  <span data-ttu-id="c5ee5-243">减</span><span class="sxs-lookup"><span data-stu-id="c5ee5-243">Subtraction</span></span> |
| *  | <span data-ttu-id="c5ee5-244">乘</span><span class="sxs-lookup"><span data-stu-id="c5ee5-244">Multiplication</span></span>  |
    
<span data-ttu-id="c5ee5-245">不支持传统的 IF 语句。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-245">Traditional IF statements are not supported.</span></span> <span data-ttu-id="c5ee5-246">但是，您可以创建语句并验证它们是否正确。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-246">However, you can create statements and validate whether they are true.</span></span>

|  <span data-ttu-id="c5ee5-247">**对账单验证**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-247">**Statement  Validation**</span></span> | <span data-ttu-id="c5ee5-248">**结果**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-248">**Result**</span></span>  |
|---|---|
|  <span data-ttu-id="c5ee5-249">a > b</span><span class="sxs-lookup"><span data-stu-id="c5ee5-249">a > b</span></span>| <span data-ttu-id="c5ee5-250">真</span><span class="sxs-lookup"><span data-stu-id="c5ee5-250">True</span></span>  |
|  <span data-ttu-id="c5ee5-251">a > b</span><span class="sxs-lookup"><span data-stu-id="c5ee5-251">a > b</span></span> |  <span data-ttu-id="c5ee5-252">假</span><span class="sxs-lookup"><span data-stu-id="c5ee5-252">False</span></span> |
    
<span data-ttu-id="c5ee5-253">**间接成本**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-253">**Overhead cost**</span></span>

<span data-ttu-id="c5ee5-254">开销成本是指经营业务的持续支出。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-254">Overhead costs refer to the ongoing expenses of operating a business.</span></span> <span data-ttu-id="c5ee5-255">这些成本无法直接关联到具体的业务活动。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-255">They are the costs that can’t be linked directly to specific business activities.</span></span> <span data-ttu-id="c5ee5-256">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="c5ee5-256">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c5ee5-257">会计费用</span><span class="sxs-lookup"><span data-stu-id="c5ee5-257">Accounting fees</span></span>
-   <span data-ttu-id="c5ee5-258">折旧</span><span class="sxs-lookup"><span data-stu-id="c5ee5-258">Depreciations</span></span>
-   <span data-ttu-id="c5ee5-259">保险</span><span class="sxs-lookup"><span data-stu-id="c5ee5-259">Insurance</span></span>
-   <span data-ttu-id="c5ee5-260">兴趣</span><span class="sxs-lookup"><span data-stu-id="c5ee5-260">Interest</span></span>
-   <span data-ttu-id="c5ee5-261">法律费用</span><span class="sxs-lookup"><span data-stu-id="c5ee5-261">Legal fees</span></span>
-   <span data-ttu-id="c5ee5-262">税金</span><span class="sxs-lookup"><span data-stu-id="c5ee5-262">Taxes</span></span>
-   <span data-ttu-id="c5ee5-263">公共设施费用</span><span class="sxs-lookup"><span data-stu-id="c5ee5-263">Utilities costs</span></span>

<span data-ttu-id="c5ee5-264">**开销比率**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-264">**Overhead rate**</span></span>

<span data-ttu-id="c5ee5-265">比率按成本对象和成本元素定义。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-265">Rates are defined per cost object and cost element.</span></span> <span data-ttu-id="c5ee5-266">比率有两种类型：会计期间和用户指定。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-266">There are two types of rates: fiscal period and user-specified.</span></span> <span data-ttu-id="c5ee5-267">会计期间比率由开销计算进行计算。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-267">Fiscal period rates are calculated by the overhead calculation.</span></span> <span data-ttu-id="c5ee5-268">用户指定的比率由用户定义，可用于以开销计算中预先确定的比率在成本对象之间分配成本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-268">A user-specific rate is user-defined and can be used to allocate cost between cost objects at a predetermined rate in the overhead calculation.</span></span>

<span data-ttu-id="c5ee5-269">**已发布**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-269">**Published**</span></span>

<span data-ttu-id="c5ee5-270">如果您将此字段设置为是，获得以下角色之一的用户可以在成本控制工作区中查看报表。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-270">If you set this field to Yes, a user who is assigned one of the following roles can view the report in the Cost control workspace:</span></span>

-  <span data-ttu-id="c5ee5-271">成本会计经理</span><span class="sxs-lookup"><span data-stu-id="c5ee5-271">Cost accounting manager</span></span>
-  <span data-ttu-id="c5ee5-272">成本核算师</span><span class="sxs-lookup"><span data-stu-id="c5ee5-272">Cost accountant</span></span>
-  <span data-ttu-id="c5ee5-273">成本核算师</span><span class="sxs-lookup"><span data-stu-id="c5ee5-273">Cost accountant clerk</span></span>
-  <span data-ttu-id="c5ee5-274">成本对象控制器</span><span class="sxs-lookup"><span data-stu-id="c5ee5-274">Cost object controller</span></span>

<span data-ttu-id="c5ee5-275">如果您将此字段设置为否，仅获得以下角色之一的用户可以在成本控制工作区中查看报表。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-275">If you set this field to No, only users who are assigned one of the following roles can view the report in the Cost control workspace:</span></span>

-  <span data-ttu-id="c5ee5-276">成本会计经理</span><span class="sxs-lookup"><span data-stu-id="c5ee5-276">Cost accounting manager</span></span>
-  <span data-ttu-id="c5ee5-277">成本核算师</span><span class="sxs-lookup"><span data-stu-id="c5ee5-277">Cost accountant</span></span>
-  <span data-ttu-id="c5ee5-278">成本核算师</span><span class="sxs-lookup"><span data-stu-id="c5ee5-278">Cost accountant clerk</span></span>

<span data-ttu-id="c5ee5-279">**统计维度**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-279">**Statistical dimension**</span></span>

<span data-ttu-id="c5ee5-280">统计维度及其成员用于登记和控制成本核算中的非货币条目。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-280">A statistical dimension and its members are used to register and control non-monetary entries in Cost accounting.</span></span> <span data-ttu-id="c5ee5-281">统计维度成员可用于两个目的：</span><span class="sxs-lookup"><span data-stu-id="c5ee5-281">Statistical dimension members can be used for two purposes:</span></span>

-  <span data-ttu-id="c5ee5-282">成本分配或成本分摊等策略中的分配基础。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-282">As an allocation base in policies such as cost distribution or cost allocation.</span></span>
-  <span data-ttu-id="c5ee5-283">对于报告非货币消耗。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-283">For reporting of non-monetary consumption.</span></span>

<span data-ttu-id="c5ee5-284">统计维度是活动盘点或总和的表达式，可以用作分摊或成本率计算的基础。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-284">A statistical dimension is the expression of a count or sum of an activity that can be used as the basis for allocations or rate calculations.</span></span> <span data-ttu-id="c5ee5-285">它可以手动创建或从源系统中导入。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-285">It's either created manually or imported from source systems.</span></span> <span data-ttu-id="c5ee5-286">统计维度的例子包括员工人数、各设备上的许可软件的数量、每台机器的耗电量或者成本中心的面积。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-286">Examples of statistical dimensions include the number of employees, the count of licensed software on each device, power consumption of each machine, or square meters for a cost center.</span></span>

<span data-ttu-id="c5ee5-287">**语句**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-287">**Statement**</span></span>

<span data-ttu-id="c5ee5-288">报表是为负责控制成本的经理提供的视图。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-288">Statements are views for the managers who are responsible for controlling costs.</span></span> <span data-ttu-id="c5ee5-289">报表由成本控制员定义，它们提供实际成本、预算成本和偏差的快速概览。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-289">Statements are defined by a cost controller, and they provide a quick overview of actual costs, budgeted costs, and deviations.</span></span> <span data-ttu-id="c5ee5-290">如有需要，经理可以进一步向下钻取详细信息。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-290">A manager can drill further into details if required.</span></span> <span data-ttu-id="c5ee5-291">为了帮助保证经理仅查看由他们负责的数据，报表中显示的数据服从访问规则。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-291">To help ensure that managers view only data that they are accountable for, data that appears in the statements is subject to access rules.</span></span>

<span data-ttu-id="c5ee5-292">**版本**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-292">**Version**</span></span>

<span data-ttu-id="c5ee5-293">版本用于模拟、查看和比较不同结果。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-293">Versions are used to simulate, view, and compare various outcomes.</span></span> <span data-ttu-id="c5ee5-294">默认情况下，所有实际成本在一个名为“*实际*”的基础版本中查看。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-294">By default, all actual costs are viewed in one base version that is known as *actual*.</span></span> <span data-ttu-id="c5ee5-295">对于预算和计算，您可以视需要处理任意数量的版本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-295">For budgets and calculations, you can work with as many versions as you require.</span></span> <span data-ttu-id="c5ee5-296">例如，您可以将预算数据导入到原始版本中，然后在修订版本中修订预算。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-296">For example, you can import budget data into an original version and then revise the budget in a revised version.</span></span> <span data-ttu-id="c5ee5-297">对于计算，您可以创建多个版本。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-297">For calculations, you can create multiple versions.</span></span> <span data-ttu-id="c5ee5-298">然后，您可以在这些不同的版本中使用适用于成本分摊的不同计算规则创建计算。</span><span class="sxs-lookup"><span data-stu-id="c5ee5-298">In these various versions, you can then create calculations by using different calculation rules that will be applied for cost allocation.</span></span>



