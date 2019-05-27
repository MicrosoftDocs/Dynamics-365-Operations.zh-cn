---
title: 质量管理概述
description: 本主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations 中使用质量管理来帮助改进您的供应链中的产品质量。
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557492"
---
# <a name="quality-management-overview"></a><span data-ttu-id="f6978-103">质量管理概述</span><span class="sxs-lookup"><span data-stu-id="f6978-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6978-104">本主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations 中使用质量管理来帮助改进您的供应链中的产品质量。</span><span class="sxs-lookup"><span data-stu-id="f6978-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="f6978-105">质量管理可帮助您在处理未达标的产品时管理周转时间，而不管其源点如何。</span><span class="sxs-lookup"><span data-stu-id="f6978-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="f6978-106">因为诊断类型链接到更正报表，所以 Microsoft Dynamics 365 for Finance and Operations 可以计划任务以更正问题并防止重复执行它们。</span><span class="sxs-lookup"><span data-stu-id="f6978-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="f6978-107">除了管理不符合项的功能外，质量管理还包括按问题类型（甚至内部问题）跟踪问题以及将解决方案标识为短期或长期的功能。 </span><span class="sxs-lookup"><span data-stu-id="f6978-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="f6978-108">有关关键绩效指标 (KPI) 的统计能让您了解以前的不符合项问题以及用于更正它们的解决方案的历史记录。</span><span class="sxs-lookup"><span data-stu-id="f6978-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="f6978-109">您可以使用历史数据检查以前质量度量的效果并确定相应的度量以备将来使用。</span><span class="sxs-lookup"><span data-stu-id="f6978-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="f6978-110">在您设置质量关联时，Finance and Operations 可以为各种业务流程、事件和条件生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="f6978-111">质量关联可以包含特定物料、特定物料组或所有物料。</span><span class="sxs-lookup"><span data-stu-id="f6978-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="f6978-112">质量管理的使用示例</span><span class="sxs-lookup"><span data-stu-id="f6978-112">Examples of the use of quality management</span></span>
<span data-ttu-id="f6978-113">质量管理是可变的，并且可以以多种方式实施来满足特定级别供应链操作的要求。</span><span class="sxs-lookup"><span data-stu-id="f6978-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="f6978-114">以下示例说明对这些功能的可能用途：</span><span class="sxs-lookup"><span data-stu-id="f6978-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="f6978-115">根据预定义的标准自动启动质量控制流程（特定供应商的某一采购订单的仓库登记）。</span><span class="sxs-lookup"><span data-stu-id="f6978-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="f6978-116">在检查时锁定库存以防止使用未审核的库存（采购订单数量的完全锁定）。</span><span class="sxs-lookup"><span data-stu-id="f6978-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="f6978-117">使用物料抽样作为质量关联的一部分来定义必须检查的当前实际库存的金额。</span><span class="sxs-lookup"><span data-stu-id="f6978-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="f6978-118">抽样可以基于固定数量或百分比。</span><span class="sxs-lookup"><span data-stu-id="f6978-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="f6978-119">为部分收货创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="f6978-120">若要创建基于某订单已实际接收的数量的质检订单，必须在**物料抽样**窗体上选择**按照更新的数量**复选框。</span><span class="sxs-lookup"><span data-stu-id="f6978-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="f6978-121">创建测试包括最小值、最大值和目标测试值在内的类型，然后执行具有预定义验证结果的定性与定量测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="f6978-122">指定一个可接受质量级别 (AQL) 来控制质量度量容差。</span><span class="sxs-lookup"><span data-stu-id="f6978-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="f6978-123">指定检查操作所需的资源，如测试区域和测试仪器。</span><span class="sxs-lookup"><span data-stu-id="f6978-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="f6978-124">使用质量关联</span><span class="sxs-lookup"><span data-stu-id="f6978-124">Working with quality associations</span></span>
<span data-ttu-id="f6978-125">使用质量关联的业务流程可与许多源文档相关，例如采购订单、销售订单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="f6978-126">每个质量关联记录定义了测试组、AQL 和应用于生成的质检订单的抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="f6978-127">您必须为业务流程中每个变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="f6978-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="f6978-128">例如，当更新采购订单产品收据时，您可以设置生成质检订单的质量关联。</span><span class="sxs-lookup"><span data-stu-id="f6978-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="f6978-129">根据执行计划的设置，在有未结质检订单或者下一流程（例如采购订单开票）时，可以将触发流程自身锁定。</span><span class="sxs-lookup"><span data-stu-id="f6978-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="f6978-130">**注释：** 在有未结质检订单时，会自动锁定库存数量使其不签发。</span><span class="sxs-lookup"><span data-stu-id="f6978-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="f6978-131">根据**物料抽样**页上的**完全锁定**设置，该数量是质检订单上的数量或源文档行上的数量。</span><span class="sxs-lookup"><span data-stu-id="f6978-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="f6978-132">对于给定业务流程，质量关联记录标识用于生成质检订单的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="f6978-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="f6978-133">条件可以特定于站点或法人。</span><span class="sxs-lookup"><span data-stu-id="f6978-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="f6978-134">只有对于事件存在现有库存时，才能生成涉及破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="f6978-135">以下示例说明如何为各个业务流程中的变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="f6978-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="f6978-136">对于每个示例，下表总结了质量关联记录定义的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="f6978-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="f6978-137">引用类型</span><span class="sxs-lookup"><span data-stu-id="f6978-137">Reference type</span></span></th>
<th><span data-ttu-id="f6978-138">事件类型</span><span class="sxs-lookup"><span data-stu-id="f6978-138">Event type</span></span></th>
<th><span data-ttu-id="f6978-139">执行</span><span class="sxs-lookup"><span data-stu-id="f6978-139">Execution</span></span></th>
<th><span data-ttu-id="f6978-140">事件锁定</span><span class="sxs-lookup"><span data-stu-id="f6978-140">Event blocking</span></span></th>
<th><span data-ttu-id="f6978-141">文档引用</span><span class="sxs-lookup"><span data-stu-id="f6978-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="f6978-142">库存</span><span class="sxs-lookup"><span data-stu-id="f6978-142">Inventory</span></span></td>
<td><span data-ttu-id="f6978-143">不适用</span><span class="sxs-lookup"><span data-stu-id="f6978-143">Not applicable</span></span></td>
<td><span data-ttu-id="f6978-144">不适用</span><span class="sxs-lookup"><span data-stu-id="f6978-144">Not applicable</span></span></td>
<td><span data-ttu-id="f6978-145">无</span><span class="sxs-lookup"><span data-stu-id="f6978-145">None</span></span></td>
<td><span data-ttu-id="f6978-146">全部</span><span class="sxs-lookup"><span data-stu-id="f6978-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="f6978-147">销售额</span><span class="sxs-lookup"><span data-stu-id="f6978-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="f6978-148">已计划领料流程</span><span class="sxs-lookup"><span data-stu-id="f6978-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="f6978-149">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-149">Before</span></span></td>
<td><span data-ttu-id="f6978-150">无</span><span class="sxs-lookup"><span data-stu-id="f6978-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="f6978-151">仅特定 ID、组或全部</span><span class="sxs-lookup"><span data-stu-id="f6978-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-152">领料流程</span><span class="sxs-lookup"><span data-stu-id="f6978-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-153">装箱单</span><span class="sxs-lookup"><span data-stu-id="f6978-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-154">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6978-155">装箱单</span><span class="sxs-lookup"><span data-stu-id="f6978-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-156">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-156">Before</span></span></td>
<td><span data-ttu-id="f6978-157">无</span><span class="sxs-lookup"><span data-stu-id="f6978-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-158">装箱单</span><span class="sxs-lookup"><span data-stu-id="f6978-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-159">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="f6978-160">采购</span><span class="sxs-lookup"><span data-stu-id="f6978-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="f6978-161">收货清单</span><span class="sxs-lookup"><span data-stu-id="f6978-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="f6978-162">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-162">Before</span></span></td>
<td><span data-ttu-id="f6978-163">无</span><span class="sxs-lookup"><span data-stu-id="f6978-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-164">收货清单</span><span class="sxs-lookup"><span data-stu-id="f6978-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-165">物料收货</span><span class="sxs-lookup"><span data-stu-id="f6978-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-166">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6978-167">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-167">After</span></span></td>
<td><span data-ttu-id="f6978-168">无</span><span class="sxs-lookup"><span data-stu-id="f6978-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-169">物料收货</span><span class="sxs-lookup"><span data-stu-id="f6978-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-170">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6978-171">注册</span><span class="sxs-lookup"><span data-stu-id="f6978-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-172">不适用</span><span class="sxs-lookup"><span data-stu-id="f6978-172">Not applicable</span></span></td>
<td><span data-ttu-id="f6978-173">无</span><span class="sxs-lookup"><span data-stu-id="f6978-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-174">物料收货</span><span class="sxs-lookup"><span data-stu-id="f6978-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-175">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f6978-176">物料收货</span><span class="sxs-lookup"><span data-stu-id="f6978-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-177">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-177">Before</span></span></td>
<td><span data-ttu-id="f6978-178">无</span><span class="sxs-lookup"><span data-stu-id="f6978-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-179">物料收货</span><span class="sxs-lookup"><span data-stu-id="f6978-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-180">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6978-181">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-181">After</span></span></td>
<td><span data-ttu-id="f6978-182">无</span><span class="sxs-lookup"><span data-stu-id="f6978-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-183">开票</span><span class="sxs-lookup"><span data-stu-id="f6978-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="f6978-184">生产</span><span class="sxs-lookup"><span data-stu-id="f6978-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-185">注册</span><span class="sxs-lookup"><span data-stu-id="f6978-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-186">不适用</span><span class="sxs-lookup"><span data-stu-id="f6978-186">Not applicable</span></span></td>
<td><span data-ttu-id="f6978-187">无</span><span class="sxs-lookup"><span data-stu-id="f6978-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="f6978-188">全部</span><span class="sxs-lookup"><span data-stu-id="f6978-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-189">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-190">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f6978-191">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-192">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-192">Before</span></span></td>
<td><span data-ttu-id="f6978-193">无</span><span class="sxs-lookup"><span data-stu-id="f6978-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-194">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-195">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6978-196">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-196">After</span></span></td>
<td><span data-ttu-id="f6978-197">无</span><span class="sxs-lookup"><span data-stu-id="f6978-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-198">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f6978-199">检验</span><span class="sxs-lookup"><span data-stu-id="f6978-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-200">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="f6978-201">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-201">Before</span></span></td>
<td><span data-ttu-id="f6978-202">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-203">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-204">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-204">After</span></span></td>
<td><span data-ttu-id="f6978-205">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-206">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-206">End</span></span></td>
<td><span data-ttu-id="f6978-207">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-207">Before</span></span></td>
<td><span data-ttu-id="f6978-208">结束</span><span class="sxs-lookup"><span data-stu-id="f6978-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6978-209">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="f6978-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-210">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="f6978-211">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-211">Before</span></span></td>
<td><span data-ttu-id="f6978-212">无</span><span class="sxs-lookup"><span data-stu-id="f6978-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-213">特定 ID、组或全部，以及资源特定、组或全部</span><span class="sxs-lookup"><span data-stu-id="f6978-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-214">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-215">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-215">After</span></span></td>
<td><span data-ttu-id="f6978-216">无</span><span class="sxs-lookup"><span data-stu-id="f6978-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6978-217">联产品生产</span><span class="sxs-lookup"><span data-stu-id="f6978-217">Co-product production</span></span></td>
<td><span data-ttu-id="f6978-218">注册</span><span class="sxs-lookup"><span data-stu-id="f6978-218">Registration</span></span></td>
<td><span data-ttu-id="f6978-219">不适用</span><span class="sxs-lookup"><span data-stu-id="f6978-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-220">无</span><span class="sxs-lookup"><span data-stu-id="f6978-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="f6978-221">全部</span><span class="sxs-lookup"><span data-stu-id="f6978-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6978-222">完工入库</span><span class="sxs-lookup"><span data-stu-id="f6978-222">Report as finished</span></span></td>
<td><span data-ttu-id="f6978-223">之前</span><span class="sxs-lookup"><span data-stu-id="f6978-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-224">之后</span><span class="sxs-lookup"><span data-stu-id="f6978-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6978-225">下表提供有关可以如何为特定类型的流程生成质检订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f6978-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="f6978-226">流程的类型</span><span class="sxs-lookup"><span data-stu-id="f6978-226">Type of process</span></span></th>
<th><span data-ttu-id="f6978-227">可以自动生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="f6978-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="f6978-228">需要破坏性测试的情况下可以生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="f6978-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="f6978-229">条件信息</span><span class="sxs-lookup"><span data-stu-id="f6978-229">Condition information</span></span></th>
<th><span data-ttu-id="f6978-230">手动生成信息</span><span class="sxs-lookup"><span data-stu-id="f6978-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="f6978-231">采购订单</span><span class="sxs-lookup"><span data-stu-id="f6978-231">Purchase order</span></span></td>
<td><span data-ttu-id="f6978-232">过帐收到的物料的收据清单或产品收据之前或之后</span><span class="sxs-lookup"><span data-stu-id="f6978-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="f6978-233">过帐收到的物料的产品收据之后，因为物料必须可用于破坏性测试</span><span class="sxs-lookup"><span data-stu-id="f6978-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="f6978-234">质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="f6978-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="f6978-235">引用某一采购订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-236">检验单</span><span class="sxs-lookup"><span data-stu-id="f6978-236">Quarantine order</span></span></td>
<td><span data-ttu-id="f6978-237">在检验单报告为已完工入库或已结束之前或之后</span><span class="sxs-lookup"><span data-stu-id="f6978-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="f6978-238">无法生成需要破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="f6978-239">假定检验单功能处理损坏物料的处置。</span><span class="sxs-lookup"><span data-stu-id="f6978-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="f6978-240">质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="f6978-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="f6978-241">引用某一检验单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-242">销售订单</span><span class="sxs-lookup"><span data-stu-id="f6978-242">Sales order</span></span></td>
<td><span data-ttu-id="f6978-243">在要被装运的物料的已计划领料流程或装箱单更新之前</span><span class="sxs-lookup"><span data-stu-id="f6978-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="f6978-244">任何步骤中</span><span class="sxs-lookup"><span data-stu-id="f6978-244">At any step</span></span></td>
<td><span data-ttu-id="f6978-245">质检订单的需求可以反映特定的站点、物料或客户，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="f6978-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="f6978-246">引用某一销售订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-247">生产订单</span><span class="sxs-lookup"><span data-stu-id="f6978-247">Production order</span></span></td>
<td><span data-ttu-id="f6978-248">报告生产订单的完工数量之前或之后</span><span class="sxs-lookup"><span data-stu-id="f6978-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="f6978-249">报告生产订单的完工数量之后</span><span class="sxs-lookup"><span data-stu-id="f6978-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="f6978-250">质检订单的需求可以反映特定的站点或物料，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="f6978-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="f6978-251">引用某一生产订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-252">具有工艺路线工序的生产订单</span><span class="sxs-lookup"><span data-stu-id="f6978-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="f6978-253">在报告为已完成工序之前或之后</span><span class="sxs-lookup"><span data-stu-id="f6978-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="f6978-254">在报告生产最后一道工序完成后</span><span class="sxs-lookup"><span data-stu-id="f6978-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="f6978-255">质检订单的需求可以反映特定的站点、物料或运营资源，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="f6978-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="f6978-256">引用某一工艺路线工序的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="f6978-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6978-257">库存</span><span class="sxs-lookup"><span data-stu-id="f6978-257">Inventory</span></span></td>
<td><span data-ttu-id="f6978-258">无法为库存日志中的交易记录或为转移单交易记录自动生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6978-259">必须为物料的库存数量手动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="f6978-260">实际现有库存量是必需的。</span><span class="sxs-lookup"><span data-stu-id="f6978-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="f6978-261">质量管理页</span><span class="sxs-lookup"><span data-stu-id="f6978-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6978-262">页面</span><span class="sxs-lookup"><span data-stu-id="f6978-262">Page</span></span></th>
<th><span data-ttu-id="f6978-263">描述</span><span class="sxs-lookup"><span data-stu-id="f6978-263">Description</span></span></th>
<th><span data-ttu-id="f6978-264">示例</span><span class="sxs-lookup"><span data-stu-id="f6978-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6978-265">质量关联</span><span class="sxs-lookup"><span data-stu-id="f6978-265">Quality associations</span></span></td>
<td><span data-ttu-id="f6978-266">请参阅本文的前几部分。</span><span class="sxs-lookup"><span data-stu-id="f6978-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="f6978-267">质量关联定义生成的质检订单的所有以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6978-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="f6978-268">交易记录事件</span><span class="sxs-lookup"><span data-stu-id="f6978-268">The transaction event</span></span></li>
<li><span data-ttu-id="f6978-269">必须在物料上执行的测试组</span><span class="sxs-lookup"><span data-stu-id="f6978-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="f6978-270">AQL</span><span class="sxs-lookup"><span data-stu-id="f6978-270">The AQL</span></span></li>
<li><span data-ttu-id="f6978-271">抽样计划</span><span class="sxs-lookup"><span data-stu-id="f6978-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="f6978-272">您必须为业务流程中要求自动生成质检订单的每种变化定义质量关联。</span><span class="sxs-lookup"><span data-stu-id="f6978-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="f6978-273">例如，可以在业务流程中为采购订单、检验单、销售订单和生产订单生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6978-274">测试</span><span class="sxs-lookup"><span data-stu-id="f6978-274">Tests</span></span></td>
<td><span data-ttu-id="f6978-275">使用此页可以定义和查看用于确定产品是否符合质量规范的各个测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="f6978-276">您可以将一个或多个单独测试分配给测试组。</span><span class="sxs-lookup"><span data-stu-id="f6978-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="f6978-277">在这种情况下，您还可以指定测试特定信息，例如可接受的度量值。</span><span class="sxs-lookup"><span data-stu-id="f6978-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="f6978-278">度量值用于定量测试，测试变量用于定性测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="f6978-279">定量测试具有测试类型<strong>整数</strong>或<strong>分数</strong>，并且具有指定的度量单位。</span><span class="sxs-lookup"><span data-stu-id="f6978-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="f6978-280">质量规范和测试结果表示为数字。</span><span class="sxs-lookup"><span data-stu-id="f6978-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="f6978-281">定性测试具有测试类型<strong>选项</strong>。</span><span class="sxs-lookup"><span data-stu-id="f6978-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="f6978-282">定性测试需要有关要度量的质量变量及其枚举选项的附加信息。</span><span class="sxs-lookup"><span data-stu-id="f6978-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="f6978-283">质量规范和测试结果根据结果表示。</span><span class="sxs-lookup"><span data-stu-id="f6978-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="f6978-284">某个制造公司对采购物料执行两个测试：有关物料质量的定量测试和有关包装损坏的定性测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="f6978-285">该公司定义有关质量测试的附加信息，以确定测试变量（损坏的包装）及其结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="f6978-286">公司使用<strong>测试组</strong>页将两个测试分配给一个测试组并指定测试特定信息。</span><span class="sxs-lookup"><span data-stu-id="f6978-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="f6978-287">将测试组分配给质检订单，以便公司可以报告这两个测试的测试结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6978-288">测试组</span><span class="sxs-lookup"><span data-stu-id="f6978-288">Test groups</span></span></td>
<td><span data-ttu-id="f6978-289">使用此页面可以设置、编辑和查看测试组以及分配给某个测试组的单独测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="f6978-290">上部窗格显示测试组，而下部窗格显示分配给所选测试组的测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="f6978-291">您可以向测试组分配多个策略，例如抽样计划、AQL 以及破坏性测试的要求。</span><span class="sxs-lookup"><span data-stu-id="f6978-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="f6978-292">当您将单个测试分配给测试组时，您需要定义其他信息，如顺序、文档和生效日期。</span><span class="sxs-lookup"><span data-stu-id="f6978-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="f6978-293">对于定量测试，还可以定义的信息包括可接受的度量值。</span><span class="sxs-lookup"><span data-stu-id="f6978-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="f6978-294">对于定性测试，该信息包括测试变量和默认结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="f6978-295">分配给质检订单的测试组定义必须在特定物料上执行默认测试集。</span><span class="sxs-lookup"><span data-stu-id="f6978-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="f6978-296">但您可以添加、删除或更改质检订单上的测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="f6978-297">将针对质检订单上的每个测试报告测试结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="f6978-298">某制造公司为其质量准则的每个变化定义一个测试组。</span><span class="sxs-lookup"><span data-stu-id="f6978-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="f6978-299">多个测试组反映抽样计划中的差异、必须一起执行的测试集、AQL 和其他因素。</span><span class="sxs-lookup"><span data-stu-id="f6978-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="f6978-300">对于定量测试，可接受的度量值中也存在差别。</span><span class="sxs-lookup"><span data-stu-id="f6978-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="f6978-301">为了落实其质量准则，公司在<strong>质量关联</strong>页上将一个测试组分配给用于自动生成质检订单的每个规则，而且还将一个测试组分配给手动创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="f6978-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6978-302">物料质量组</span><span class="sxs-lookup"><span data-stu-id="f6978-302">Item quality groups</span></span></td>
<td><span data-ttu-id="f6978-303">使用此页面可以设置、编辑和查看分配给质量组的物料或分配给物料的质量组。</span><span class="sxs-lookup"><span data-stu-id="f6978-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="f6978-304">质量组表示物料的公共测试要求。</span><span class="sxs-lookup"><span data-stu-id="f6978-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="f6978-305">在<strong>测试组</strong>页上定义测试要求后，您可以定义用于自动生成质检订单的规则。</span><span class="sxs-lookup"><span data-stu-id="f6978-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="f6978-306">为了简化该流程，您不为各个物料定义规则。</span><span class="sxs-lookup"><span data-stu-id="f6978-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="f6978-307">相反，您使用<strong>质量关联</strong>页为质量组定义规则。</span><span class="sxs-lookup"><span data-stu-id="f6978-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="f6978-308">您还可以为所选质量组使用<strong>物料质量组</strong>页来将相关物料分配给该组。</span><span class="sxs-lookup"><span data-stu-id="f6978-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="f6978-309">您还可以为所选物料使用<strong>物料质量组</strong>页来将相关质量组分配给该物料。</span><span class="sxs-lookup"><span data-stu-id="f6978-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="f6978-310">某制造公司采购的多种原材料具有相同的进货检查测试要求。</span><span class="sxs-lookup"><span data-stu-id="f6978-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="f6978-311">公司定义了一个质量组，然后将与原材料关联的物料编号分配给该组。</span><span class="sxs-lookup"><span data-stu-id="f6978-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="f6978-312">之后，公司采购一个新类型的原材料，具有相同的测试要求。</span><span class="sxs-lookup"><span data-stu-id="f6978-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="f6978-313">公司不是为新物料设置新的测试要求，而是将新物料的物料编号添加到现有的质量组。</span><span class="sxs-lookup"><span data-stu-id="f6978-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="f6978-314">此相同制造公司还生产具有相同测试要求的物料，并装运具有相同装运前测试要求的物料。</span><span class="sxs-lookup"><span data-stu-id="f6978-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="f6978-315">公司定义两个附加质量组，然后将相关物料编号分配给每个组。</span><span class="sxs-lookup"><span data-stu-id="f6978-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6978-316">测试变量</span><span class="sxs-lookup"><span data-stu-id="f6978-316">Test variables</span></span></td>
<td><span data-ttu-id="f6978-317">使用此页可以定义和查看与定性测试关联的变量。</span><span class="sxs-lookup"><span data-stu-id="f6978-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="f6978-318">对于每个变量，您定义表示可能选项的枚举结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="f6978-319">您在<strong>测试</strong>页上定义测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="f6978-320">对于定性测试，您必须将测试类型设置为<strong>选项</strong>。</span><span class="sxs-lookup"><span data-stu-id="f6978-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="f6978-321">使用<strong>测试组</strong>页可以将测试变量分配给单个测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="f6978-322">一个生产饼干的制造公司对成品使用检查测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="f6978-323">此检查测试具有多个变量。</span><span class="sxs-lookup"><span data-stu-id="f6978-323">This inspection test has several variables.</span></span> <span data-ttu-id="f6978-324">一个变量是味道，并且此变量的可能结果是好和坏。</span><span class="sxs-lookup"><span data-stu-id="f6978-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="f6978-325">第二个变量是颜色，其可能结果是过暗、过浅和正好。</span><span class="sxs-lookup"><span data-stu-id="f6978-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6978-326">测试变量结果</span><span class="sxs-lookup"><span data-stu-id="f6978-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="f6978-327">使用此页面可以设置、编辑和查看与定性测试关联的测试变量的可能测试结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="f6978-328">对于每个结果，您分配<strong>通过</strong>或<strong>未通过</strong>状态。</span><span class="sxs-lookup"><span data-stu-id="f6978-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="f6978-329">您必须在<strong>测试</strong>页上定义的每个定性测试定义变量及其结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="f6978-330">（对于定性测试，测试类型在<strong>测试</strong>页上设置为<strong>选项</strong>。）使用<strong>测试组</strong>页可以将测试变量和默认结果分配给单独的定性测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="f6978-331">一个生产饼干的制造公司对成品使用检查测试。</span><span class="sxs-lookup"><span data-stu-id="f6978-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="f6978-332">此检查测试具有多个变量。</span><span class="sxs-lookup"><span data-stu-id="f6978-332">This inspection test has of several variables.</span></span> <span data-ttu-id="f6978-333">一个变量是味道，并且此变量的可能结果是好和坏。</span><span class="sxs-lookup"><span data-stu-id="f6978-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="f6978-334">第二个变量是颜色，其可能结果是过暗、过浅和正好。</span><span class="sxs-lookup"><span data-stu-id="f6978-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="f6978-335">会为每个结果分配一个<strong>通过</strong>或<strong>未通过</strong>的状态。</span><span class="sxs-lookup"><span data-stu-id="f6978-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="f6978-336">在各个变量的检查测试期间，检查员将通过选择其中一个结果报告测试结果。</span><span class="sxs-lookup"><span data-stu-id="f6978-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="f6978-337">其他资源</span><span class="sxs-lookup"><span data-stu-id="f6978-337">Additional resources</span></span>
--------

[<span data-ttu-id="f6978-338">质量管理流程</span><span class="sxs-lookup"><span data-stu-id="f6978-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="f6978-339">启用未达标管理</span><span class="sxs-lookup"><span data-stu-id="f6978-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
