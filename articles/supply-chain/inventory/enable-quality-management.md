---
title: 质量管理概述
description: 本主题介绍如何在 Dynamics 365 Supply Chain Management 中使用质量管理来帮助改进您的供应链中的产品质量。
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65858838b0fbb245a9330fab4e3b65b36a9eb944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219357"
---
# <a name="quality-management-overview"></a><span data-ttu-id="44c72-103">质量管理概述</span><span class="sxs-lookup"><span data-stu-id="44c72-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44c72-104">本主题介绍如何在 Dynamics 365 Supply Chain Management 中使用质量管理来帮助改进您的供应链中的产品质量。</span><span class="sxs-lookup"><span data-stu-id="44c72-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="44c72-105">质量管理可帮助您在处理未达标的产品时管理周转时间，而不管其源点如何。</span><span class="sxs-lookup"><span data-stu-id="44c72-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="44c72-106">因为诊断类型链接到更正报表，所以 Supply Chain Management 可以计划任务以更正问题并防止重复执行它们。</span><span class="sxs-lookup"><span data-stu-id="44c72-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="44c72-107">除了管理不符合项的功能外，质量管理还包括按问题类型（甚至内部问题）跟踪问题以及将解决方案标识为短期或长期的功能。 </span><span class="sxs-lookup"><span data-stu-id="44c72-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="44c72-108">有关关键绩效指标 (KPI) 的统计能让您了解以前的不符合项问题以及用于更正它们的解决方案的历史记录。</span><span class="sxs-lookup"><span data-stu-id="44c72-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="44c72-109">您可以使用历史数据检查以前质量度量的效果并确定相应的度量以备将来使用。</span><span class="sxs-lookup"><span data-stu-id="44c72-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="44c72-110">在您设置质量关联时，Supply Chain Management 可以为各种业务流程、事件和条件生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="44c72-111">质量关联可以包含特定物料、特定物料组或所有物料。</span><span class="sxs-lookup"><span data-stu-id="44c72-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="44c72-112">质量管理的使用示例</span><span class="sxs-lookup"><span data-stu-id="44c72-112">Examples of the use of quality management</span></span>
<span data-ttu-id="44c72-113">质量管理是可变的，并且可以以多种方式实施来满足特定级别供应链操作的要求。</span><span class="sxs-lookup"><span data-stu-id="44c72-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="44c72-114">以下示例说明对这些功能的可能用途：</span><span class="sxs-lookup"><span data-stu-id="44c72-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="44c72-115">根据预定义的标准自动启动质量控制流程（特定供应商的某一采购订单的仓库登记）。</span><span class="sxs-lookup"><span data-stu-id="44c72-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="44c72-116">在检查时锁定库存以防止使用未审核的库存（采购订单数量的完全锁定）。</span><span class="sxs-lookup"><span data-stu-id="44c72-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="44c72-117">使用物料抽样作为质量关联的一部分来定义必须检查的当前实际库存的金额。</span><span class="sxs-lookup"><span data-stu-id="44c72-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="44c72-118">抽样可以基于固定数量、百分比或完整牌照。</span><span class="sxs-lookup"><span data-stu-id="44c72-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="44c72-119">_仓库流程质量管理_ 功能扩展了质量管理能力。</span><span class="sxs-lookup"><span data-stu-id="44c72-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="44c72-120">如果您正在使用此功能，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)获取启用此功能时质量管理工作方式的示例。</span><span class="sxs-lookup"><span data-stu-id="44c72-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="44c72-121">为部分收货创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="44c72-122">若要创建基于某订单已实际接收的数量的质检订单，必须在 **物料抽样** 窗体上选择 **按照更新的数量** 复选框。</span><span class="sxs-lookup"><span data-stu-id="44c72-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="44c72-123">创建测试包括最小值、最大值和目标测试值在内的类型，然后执行具有预定义验证结果的定性与定量测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="44c72-124">指定一个可接受质量级别 (AQL) 来控制质量度量容差。</span><span class="sxs-lookup"><span data-stu-id="44c72-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="44c72-125">指定检查操作所需的资源，如测试区域和测试仪器。</span><span class="sxs-lookup"><span data-stu-id="44c72-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="44c72-126">使用质量关联</span><span class="sxs-lookup"><span data-stu-id="44c72-126">Working with quality associations</span></span>
<span data-ttu-id="44c72-127">使用质量关联的业务流程可与许多源文档相关，例如采购订单、销售订单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="44c72-128">每个质量关联记录定义了测试组、AQL 和应用于生成的质检订单的抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="44c72-129">您必须为业务流程中每个变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="44c72-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="44c72-130">例如，当更新采购订单产品收据时，您可以设置生成质检订单的质量关联。</span><span class="sxs-lookup"><span data-stu-id="44c72-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="44c72-131">根据执行计划的设置，在有未结质检订单或者下一流程（例如采购订单开票）时，可以将触发流程自身锁定。</span><span class="sxs-lookup"><span data-stu-id="44c72-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="44c72-132">**注释：** 在有未结质检订单时，会自动锁定库存数量使其不签发。</span><span class="sxs-lookup"><span data-stu-id="44c72-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="44c72-133">根据 **物料抽样** 页上的 **完全锁定** 设置，该数量是质检订单上的数量或源文档行上的数量。</span><span class="sxs-lookup"><span data-stu-id="44c72-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="44c72-134">对于给定业务流程，质量关联记录标识用于生成质检订单的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="44c72-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="44c72-135">条件可以特定于站点或法人。</span><span class="sxs-lookup"><span data-stu-id="44c72-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="44c72-136">只有对于事件存在现有库存时，才能生成涉及破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="44c72-137">以下示例说明如何为各个业务流程中的变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="44c72-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="44c72-138">对于每个示例，下表总结了质量关联记录定义的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="44c72-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="44c72-139">引用类型</span><span class="sxs-lookup"><span data-stu-id="44c72-139">Reference type</span></span></th>
<th><span data-ttu-id="44c72-140">事件类型</span><span class="sxs-lookup"><span data-stu-id="44c72-140">Event type</span></span></th>
<th><span data-ttu-id="44c72-141">执行</span><span class="sxs-lookup"><span data-stu-id="44c72-141">Execution</span></span></th>
<th><span data-ttu-id="44c72-142">事件锁定</span><span class="sxs-lookup"><span data-stu-id="44c72-142">Event blocking</span></span></th>
<th><span data-ttu-id="44c72-143">文档引用</span><span class="sxs-lookup"><span data-stu-id="44c72-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="44c72-144">库存</span><span class="sxs-lookup"><span data-stu-id="44c72-144">Inventory</span></span></td>
<td><span data-ttu-id="44c72-145">不适用</span><span class="sxs-lookup"><span data-stu-id="44c72-145">Not applicable</span></span></td>
<td><span data-ttu-id="44c72-146">不适用</span><span class="sxs-lookup"><span data-stu-id="44c72-146">Not applicable</span></span></td>
<td><span data-ttu-id="44c72-147">无</span><span class="sxs-lookup"><span data-stu-id="44c72-147">None</span></span></td>
<td><span data-ttu-id="44c72-148">全部</span><span class="sxs-lookup"><span data-stu-id="44c72-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="44c72-149">销售额</span><span class="sxs-lookup"><span data-stu-id="44c72-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="44c72-150">已计划领料流程</span><span class="sxs-lookup"><span data-stu-id="44c72-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="44c72-151">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-151">Before</span></span></td>
<td><span data-ttu-id="44c72-152">无</span><span class="sxs-lookup"><span data-stu-id="44c72-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="44c72-153">仅特定 ID、组或全部</span><span class="sxs-lookup"><span data-stu-id="44c72-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-154">领料流程</span><span class="sxs-lookup"><span data-stu-id="44c72-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-155">装箱单</span><span class="sxs-lookup"><span data-stu-id="44c72-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-156">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="44c72-157">装箱单</span><span class="sxs-lookup"><span data-stu-id="44c72-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-158">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-158">Before</span></span></td>
<td><span data-ttu-id="44c72-159">无</span><span class="sxs-lookup"><span data-stu-id="44c72-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-160">装箱单</span><span class="sxs-lookup"><span data-stu-id="44c72-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-161">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="44c72-162">采购</span><span class="sxs-lookup"><span data-stu-id="44c72-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="44c72-163">收货清单</span><span class="sxs-lookup"><span data-stu-id="44c72-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="44c72-164">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-164">Before</span></span></td>
<td><span data-ttu-id="44c72-165">无</span><span class="sxs-lookup"><span data-stu-id="44c72-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-166">收货清单</span><span class="sxs-lookup"><span data-stu-id="44c72-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-167">物料收货</span><span class="sxs-lookup"><span data-stu-id="44c72-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-168">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="44c72-169">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-169">After</span></span></td>
<td><span data-ttu-id="44c72-170">无</span><span class="sxs-lookup"><span data-stu-id="44c72-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-171">物料收货</span><span class="sxs-lookup"><span data-stu-id="44c72-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-172">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="44c72-173">注册</span><span class="sxs-lookup"><span data-stu-id="44c72-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-174">不适用</span><span class="sxs-lookup"><span data-stu-id="44c72-174">Not applicable</span></span></td>
<td><span data-ttu-id="44c72-175">无</span><span class="sxs-lookup"><span data-stu-id="44c72-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-176">物料收货</span><span class="sxs-lookup"><span data-stu-id="44c72-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-177">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="44c72-178">物料收货</span><span class="sxs-lookup"><span data-stu-id="44c72-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-179">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-179">Before</span></span></td>
<td><span data-ttu-id="44c72-180">无</span><span class="sxs-lookup"><span data-stu-id="44c72-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-181">物料收货</span><span class="sxs-lookup"><span data-stu-id="44c72-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-182">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="44c72-183">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-183">After</span></span></td>
<td><span data-ttu-id="44c72-184">无</span><span class="sxs-lookup"><span data-stu-id="44c72-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-185">开票</span><span class="sxs-lookup"><span data-stu-id="44c72-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="44c72-186">生产</span><span class="sxs-lookup"><span data-stu-id="44c72-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-187">注册</span><span class="sxs-lookup"><span data-stu-id="44c72-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-188">不适用</span><span class="sxs-lookup"><span data-stu-id="44c72-188">Not applicable</span></span></td>
<td><span data-ttu-id="44c72-189">无</span><span class="sxs-lookup"><span data-stu-id="44c72-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="44c72-190">全部</span><span class="sxs-lookup"><span data-stu-id="44c72-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-191">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-192">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="44c72-193">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-194">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-194">Before</span></span></td>
<td><span data-ttu-id="44c72-195">无</span><span class="sxs-lookup"><span data-stu-id="44c72-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-196">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-197">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="44c72-198">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-198">After</span></span></td>
<td><span data-ttu-id="44c72-199">无</span><span class="sxs-lookup"><span data-stu-id="44c72-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-200">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="44c72-201">检验</span><span class="sxs-lookup"><span data-stu-id="44c72-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-202">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="44c72-203">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-203">Before</span></span></td>
<td><span data-ttu-id="44c72-204">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-205">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-206">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-206">After</span></span></td>
<td><span data-ttu-id="44c72-207">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-208">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-208">End</span></span></td>
<td><span data-ttu-id="44c72-209">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-209">Before</span></span></td>
<td><span data-ttu-id="44c72-210">结束</span><span class="sxs-lookup"><span data-stu-id="44c72-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="44c72-211">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="44c72-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-212">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="44c72-213">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-213">Before</span></span></td>
<td><span data-ttu-id="44c72-214">无</span><span class="sxs-lookup"><span data-stu-id="44c72-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-215">特定 ID、组或全部，以及资源特定、组或全部</span><span class="sxs-lookup"><span data-stu-id="44c72-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-216">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-217">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-217">After</span></span></td>
<td><span data-ttu-id="44c72-218">无</span><span class="sxs-lookup"><span data-stu-id="44c72-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="44c72-219">联产品生产</span><span class="sxs-lookup"><span data-stu-id="44c72-219">Co-product production</span></span></td>
<td><span data-ttu-id="44c72-220">注册</span><span class="sxs-lookup"><span data-stu-id="44c72-220">Registration</span></span></td>
<td><span data-ttu-id="44c72-221">不适用</span><span class="sxs-lookup"><span data-stu-id="44c72-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-222">无</span><span class="sxs-lookup"><span data-stu-id="44c72-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="44c72-223">全部</span><span class="sxs-lookup"><span data-stu-id="44c72-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="44c72-224">完工入库</span><span class="sxs-lookup"><span data-stu-id="44c72-224">Report as finished</span></span></td>
<td><span data-ttu-id="44c72-225">之前</span><span class="sxs-lookup"><span data-stu-id="44c72-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-226">之后</span><span class="sxs-lookup"><span data-stu-id="44c72-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44c72-227">下表提供有关可以如何为特定类型的流程生成质检订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="44c72-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="44c72-228">流程的类型</span><span class="sxs-lookup"><span data-stu-id="44c72-228">Type of process</span></span></th>
<th><span data-ttu-id="44c72-229">可以自动生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="44c72-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="44c72-230">需要破坏性测试的情况下可以生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="44c72-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="44c72-231">条件信息</span><span class="sxs-lookup"><span data-stu-id="44c72-231">Condition information</span></span></th>
<th><span data-ttu-id="44c72-232">手动生成信息</span><span class="sxs-lookup"><span data-stu-id="44c72-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="44c72-233">采购订单</span><span class="sxs-lookup"><span data-stu-id="44c72-233">Purchase order</span></span></td>
<td><span data-ttu-id="44c72-234">过帐收到的物料的收据清单或产品收据之前或之后</span><span class="sxs-lookup"><span data-stu-id="44c72-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="44c72-235">过帐收到的物料的产品收据之后，因为物料必须可用于破坏性测试</span><span class="sxs-lookup"><span data-stu-id="44c72-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="44c72-236">质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="44c72-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="44c72-237">引用某一采购订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-238">检验单</span><span class="sxs-lookup"><span data-stu-id="44c72-238">Quarantine order</span></span></td>
<td><span data-ttu-id="44c72-239">在检验单报告为已完工入库或已结束之前或之后</span><span class="sxs-lookup"><span data-stu-id="44c72-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="44c72-240">无法生成需要破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="44c72-241">假定检验单功能处理损坏物料的处置。</span><span class="sxs-lookup"><span data-stu-id="44c72-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="44c72-242">质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="44c72-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="44c72-243">引用某一检验单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-244">销售订单</span><span class="sxs-lookup"><span data-stu-id="44c72-244">Sales order</span></span></td>
<td><span data-ttu-id="44c72-245">在要被装运的物料的已计划领料流程或装箱单更新之前</span><span class="sxs-lookup"><span data-stu-id="44c72-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="44c72-246">任何步骤中</span><span class="sxs-lookup"><span data-stu-id="44c72-246">At any step</span></span></td>
<td><span data-ttu-id="44c72-247">质检订单的需求可以反映特定的站点、物料或客户，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="44c72-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="44c72-248">引用某一销售订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-249">生产订单</span><span class="sxs-lookup"><span data-stu-id="44c72-249">Production order</span></span></td>
<td><span data-ttu-id="44c72-250">报告生产订单的完工数量之前或之后</span><span class="sxs-lookup"><span data-stu-id="44c72-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="44c72-251">报告生产订单的完工数量之后</span><span class="sxs-lookup"><span data-stu-id="44c72-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="44c72-252">质检订单的需求可以反映特定的站点或物料，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="44c72-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="44c72-253">引用某一生产订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-254">具有工艺路线工序的生产订单</span><span class="sxs-lookup"><span data-stu-id="44c72-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="44c72-255">在报告为已完成工序之前或之后</span><span class="sxs-lookup"><span data-stu-id="44c72-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="44c72-256">在报告生产最后一道工序完成后</span><span class="sxs-lookup"><span data-stu-id="44c72-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="44c72-257">质检订单的需求可以反映特定的站点、物料或运营资源，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="44c72-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="44c72-258">引用某一工艺路线工序的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="44c72-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44c72-259">库存</span><span class="sxs-lookup"><span data-stu-id="44c72-259">Inventory</span></span></td>
<td><span data-ttu-id="44c72-260">无法为库存日志中的交易记录或为转移单交易记录自动生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="44c72-261">必须为物料的库存数量手动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="44c72-262">实际现有库存量是必需的。</span><span class="sxs-lookup"><span data-stu-id="44c72-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="44c72-263">质检订单自动生成示例</span><span class="sxs-lookup"><span data-stu-id="44c72-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="44c72-264">采购</span><span class="sxs-lookup"><span data-stu-id="44c72-264">Purchasing</span></span>

<span data-ttu-id="44c72-265">在采购中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 **物料收货**，并将 **执行** 字段设置为 **之后**，您将得到以下结果：</span><span class="sxs-lookup"><span data-stu-id="44c72-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="44c72-266">如果将 **按照更新的数量** 选项设置为 **是**，则会根据物料抽样中收到的数量和设置，根据采购订单为每个收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="44c72-267">每次根据采购订单接收数量时，都会根据新接收的数量生成新的质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="44c72-268">如果将 **按照更新的数量** 选项设置为 **否**，则会根据收到的数量，根据采购订单为第一个收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="44c72-269">此外，根据跟踪维度，将基于剩余数量创建一个或多个质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="44c72-270">不会根据采购订单为后续收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="44c72-271">生产</span><span class="sxs-lookup"><span data-stu-id="44c72-271">Production</span></span>

<span data-ttu-id="44c72-272">在生产中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 **完工入库**，并将 **执行** 字段设置为 **之后**，您将得到以下结果：</span><span class="sxs-lookup"><span data-stu-id="44c72-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="44c72-273">如果将 **按照更新的数量** 选项设置为 **是**，则会根据物料抽样中每个完成的数量和设置生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="44c72-274">每次根据生产订单将数量完工入库时，都会根据新完成的数量生成新的质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="44c72-275">此生成逻辑与采购一致。</span><span class="sxs-lookup"><span data-stu-id="44c72-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="44c72-276">如果将 **按照更新的数量** 选项设置为 **否**，则会根据完成的数量，在数量第一次完工入库时生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="44c72-277">此外，根据物料抽样的跟踪维度，将基于剩余数量创建一个或多个质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="44c72-278">后续的完成数量不会生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="44c72-279">质量规范</span><span class="sxs-lookup"><span data-stu-id="44c72-279">Quality specification</span></span></th>
<th><span data-ttu-id="44c72-280">按照更新的数量</span><span class="sxs-lookup"><span data-stu-id="44c72-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="44c72-281">按照跟踪维度</span><span class="sxs-lookup"><span data-stu-id="44c72-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="44c72-282">结果</span><span class="sxs-lookup"><span data-stu-id="44c72-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="44c72-283">百分比：10%</span><span class="sxs-lookup"><span data-stu-id="44c72-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="44c72-284">是</span><span class="sxs-lookup"><span data-stu-id="44c72-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="44c72-285">批处理号：否</span><span class="sxs-lookup"><span data-stu-id="44c72-285">Batch number: No</span></span></p>
<p><span data-ttu-id="44c72-286">序列号：否</span><span class="sxs-lookup"><span data-stu-id="44c72-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="44c72-287">订单数量：100</span><span class="sxs-lookup"><span data-stu-id="44c72-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="44c72-288">30 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="44c72-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="44c72-289">3 的质检订单 #1（30 的 10%）</span><span class="sxs-lookup"><span data-stu-id="44c72-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="44c72-290">70 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="44c72-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="44c72-291">7 的质检订单 #2（剩余订单数量的 10%，该数量在此例中等于 70）</span><span class="sxs-lookup"><span data-stu-id="44c72-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="44c72-292">固定数量：1</span><span class="sxs-lookup"><span data-stu-id="44c72-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="44c72-293">否</span><span class="sxs-lookup"><span data-stu-id="44c72-293">No</span></span></td>
<td>
<p><span data-ttu-id="44c72-294">批处理号：否</span><span class="sxs-lookup"><span data-stu-id="44c72-294">Batch number: No</span></span></p>
<p><span data-ttu-id="44c72-295">序列号：否</span><span class="sxs-lookup"><span data-stu-id="44c72-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="44c72-296">订单数量：100</span><span class="sxs-lookup"><span data-stu-id="44c72-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="44c72-297">30 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="44c72-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="44c72-298">1 的质检订单 #1（对于第一个完工入库数量，其固定值为 1）</span><span class="sxs-lookup"><span data-stu-id="44c72-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="44c72-299">1 的质检订单 #2（对于剩余数量，其固定值仍为 1）</span><span class="sxs-lookup"><span data-stu-id="44c72-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="44c72-300">10 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="44c72-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="44c72-301">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="44c72-302">60 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="44c72-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="44c72-303">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="44c72-304">固定数量：1</span><span class="sxs-lookup"><span data-stu-id="44c72-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="44c72-305">是</span><span class="sxs-lookup"><span data-stu-id="44c72-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="44c72-306">批处理号：是</span><span class="sxs-lookup"><span data-stu-id="44c72-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="44c72-307">序列号：是</span><span class="sxs-lookup"><span data-stu-id="44c72-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="44c72-308">订单数量：10</span><span class="sxs-lookup"><span data-stu-id="44c72-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="44c72-309">3 的完工入库量：#b1、#s1 的 1；#b2、#s2 的 1；#b3、#s3 的 1</span><span class="sxs-lookup"><span data-stu-id="44c72-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="44c72-310">批次 #b1、序列 #s1 的 1 的质检订单 #1</span><span class="sxs-lookup"><span data-stu-id="44c72-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="44c72-311">批次 #b2、序列 #s2 的 1 的质检订单 #2</span><span class="sxs-lookup"><span data-stu-id="44c72-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="44c72-312">批次 #b3、序列 #s3 的 1 的质检订单 #3</span><span class="sxs-lookup"><span data-stu-id="44c72-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="44c72-313">2 的完工入库量：#b4、#s4 的 1；#b5、#s5 的 1</span><span class="sxs-lookup"><span data-stu-id="44c72-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="44c72-314">批次 #b4、序列 #s4 的 1 的质检订单 #4</span><span class="sxs-lookup"><span data-stu-id="44c72-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="44c72-315">批次 #b5、序列 #s5 的 1 的质检订单 #5</span><span class="sxs-lookup"><span data-stu-id="44c72-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="44c72-316"><strong>注意：</strong>批次可以重复使用。</span><span class="sxs-lookup"><span data-stu-id="44c72-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="44c72-317">固定数量：2</span><span class="sxs-lookup"><span data-stu-id="44c72-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="44c72-318">否</span><span class="sxs-lookup"><span data-stu-id="44c72-318">No</span></span></td>
<td>
<p><span data-ttu-id="44c72-319">批处理号：是</span><span class="sxs-lookup"><span data-stu-id="44c72-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="44c72-320">序列号：是</span><span class="sxs-lookup"><span data-stu-id="44c72-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="44c72-321">订单数量：10</span><span class="sxs-lookup"><span data-stu-id="44c72-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="44c72-322">4 的完工入库量：#b1、#s1 的 1；#b2、#s2 的 1；#b3、#s3 的 1；#b4、#s4 的 1</span><span class="sxs-lookup"><span data-stu-id="44c72-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="44c72-323">批次 #b1、序列 #s1 的 1 的质检订单 #1</span><span class="sxs-lookup"><span data-stu-id="44c72-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="44c72-324">批次 #b2、序列 #s2 的 1 的质检订单 #2</span><span class="sxs-lookup"><span data-stu-id="44c72-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="44c72-325">批次 #b3、序列 #s3 的 1 的质检订单 #3</span><span class="sxs-lookup"><span data-stu-id="44c72-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="44c72-326">批次 #b4、序列 #s4 的 1 的质检订单 #4</span><span class="sxs-lookup"><span data-stu-id="44c72-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="44c72-327">2 的质检订单 #5，没有批处理号和序列号的引用</span><span class="sxs-lookup"><span data-stu-id="44c72-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="44c72-328">6 的完工入库量：#b5、#s5 的 1；#b6、#s6 的 1；#b7、#s7 的 1；#b8、#s8 的 1；#b9、#s9 的 1；#b10、#s10 的 1</span><span class="sxs-lookup"><span data-stu-id="44c72-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="44c72-329">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="44c72-330">*仓库流程质量管理* 功能添加了将 **事件类型** 设置为 *报告为完工入库* 并将 **执行** 设置为 *以后* 的生产，以及将 **事件类型** 设置为 *登记* 的采购的质检订单处理能力。</span><span class="sxs-lookup"><span data-stu-id="44c72-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="44c72-331">有关详细信息，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)。</span><span class="sxs-lookup"><span data-stu-id="44c72-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="44c72-332">质量管理页</span><span class="sxs-lookup"><span data-stu-id="44c72-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44c72-333">页</span><span class="sxs-lookup"><span data-stu-id="44c72-333">Page</span></span></th>
<th><span data-ttu-id="44c72-334">说明</span><span class="sxs-lookup"><span data-stu-id="44c72-334">Description</span></span></th>
<th><span data-ttu-id="44c72-335">示例</span><span class="sxs-lookup"><span data-stu-id="44c72-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="44c72-336">质量关联</span><span class="sxs-lookup"><span data-stu-id="44c72-336">Quality associations</span></span></td>
<td><span data-ttu-id="44c72-337">请参阅本文的前几部分。</span><span class="sxs-lookup"><span data-stu-id="44c72-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="44c72-338">质量关联定义生成的质检订单的所有以下信息：</span><span class="sxs-lookup"><span data-stu-id="44c72-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="44c72-339">交易记录事件</span><span class="sxs-lookup"><span data-stu-id="44c72-339">The transaction event</span></span></li>
<li><span data-ttu-id="44c72-340">必须在物料上执行的测试组</span><span class="sxs-lookup"><span data-stu-id="44c72-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="44c72-341">AQL</span><span class="sxs-lookup"><span data-stu-id="44c72-341">The AQL</span></span></li>
<li><span data-ttu-id="44c72-342">抽样计划</span><span class="sxs-lookup"><span data-stu-id="44c72-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="44c72-343">您必须为业务流程中要求自动生成质检订单的每种变化定义质量关联。</span><span class="sxs-lookup"><span data-stu-id="44c72-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="44c72-344">例如，可以在业务流程中为采购订单、检验单、销售订单和生产订单生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44c72-345">测试</span><span class="sxs-lookup"><span data-stu-id="44c72-345">Tests</span></span></td>
<td><span data-ttu-id="44c72-346">使用此页可以定义和查看用于确定产品是否符合质量规范的各个测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="44c72-347">您可以将一个或多个单独测试分配给测试组。</span><span class="sxs-lookup"><span data-stu-id="44c72-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="44c72-348">在这种情况下，您还可以指定测试特定信息，例如可接受的度量值。</span><span class="sxs-lookup"><span data-stu-id="44c72-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="44c72-349">度量值用于定量测试，测试变量用于定性测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="44c72-350">定量测试具有测试类型<strong>整数</strong>或<strong>分数</strong>，并且具有指定的度量单位。</span><span class="sxs-lookup"><span data-stu-id="44c72-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="44c72-351">质量规范和测试结果表示为数字。</span><span class="sxs-lookup"><span data-stu-id="44c72-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="44c72-352">定性测试具有测试类型<strong>选项</strong>。</span><span class="sxs-lookup"><span data-stu-id="44c72-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="44c72-353">定性测试需要有关要度量的质量变量及其枚举选项的附加信息。</span><span class="sxs-lookup"><span data-stu-id="44c72-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="44c72-354">质量规范和测试结果根据结果表示。</span><span class="sxs-lookup"><span data-stu-id="44c72-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="44c72-355">某个制造公司对采购物料执行两个测试：有关物料质量的定量测试和有关包装损坏的定性测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="44c72-356">该公司定义有关质量测试的附加信息，以确定测试变量（损坏的包装）及其结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="44c72-357">公司使用<strong>测试组</strong>页将两个测试分配给一个测试组并指定测试特定信息。</span><span class="sxs-lookup"><span data-stu-id="44c72-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="44c72-358">将测试组分配给质检订单，以便公司可以报告这两个测试的测试结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44c72-359">测试组</span><span class="sxs-lookup"><span data-stu-id="44c72-359">Test groups</span></span></td>
<td><span data-ttu-id="44c72-360">使用此页面可以设置、编辑和查看测试组以及分配给某个测试组的单独测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="44c72-361">上部窗格显示测试组，而下部窗格显示分配给所选测试组的测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="44c72-362">您可以向测试组分配多个策略，例如抽样计划、AQL 以及破坏性测试的要求。</span><span class="sxs-lookup"><span data-stu-id="44c72-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="44c72-363">当您将单个测试分配给测试组时，您需要定义其他信息，如顺序、文档和生效日期。</span><span class="sxs-lookup"><span data-stu-id="44c72-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="44c72-364">对于定量测试，还可以定义的信息包括可接受的度量值。</span><span class="sxs-lookup"><span data-stu-id="44c72-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="44c72-365">对于定性测试，该信息包括测试变量和默认结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="44c72-366">分配给质检订单的测试组定义必须在特定物料上执行默认测试集。</span><span class="sxs-lookup"><span data-stu-id="44c72-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="44c72-367">但您可以添加、删除或更改质检订单上的测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="44c72-368">将针对质检订单上的每个测试报告测试结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="44c72-369">某制造公司为其质量准则的每个变化定义一个测试组。</span><span class="sxs-lookup"><span data-stu-id="44c72-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="44c72-370">多个测试组反映抽样计划中的差异、必须一起执行的测试集、AQL 和其他因素。</span><span class="sxs-lookup"><span data-stu-id="44c72-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="44c72-371">对于定量测试，可接受的度量值中也存在差别。</span><span class="sxs-lookup"><span data-stu-id="44c72-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="44c72-372">为了落实其质量准则，公司在<strong>质量关联</strong>页上将一个测试组分配给用于自动生成质检订单的每个规则，而且还将一个测试组分配给手动创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="44c72-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44c72-373">物料质量组</span><span class="sxs-lookup"><span data-stu-id="44c72-373">Item quality groups</span></span></td>
<td><span data-ttu-id="44c72-374">使用此页面可以设置、编辑和查看分配给质量组的物料或分配给物料的质量组。</span><span class="sxs-lookup"><span data-stu-id="44c72-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="44c72-375">质量组表示物料的公共测试要求。</span><span class="sxs-lookup"><span data-stu-id="44c72-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="44c72-376">在<strong>测试组</strong>页上定义测试要求后，您可以定义用于自动生成质检订单的规则。</span><span class="sxs-lookup"><span data-stu-id="44c72-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="44c72-377">为了简化该流程，您不为各个物料定义规则。</span><span class="sxs-lookup"><span data-stu-id="44c72-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="44c72-378">相反，您使用<strong>质量关联</strong>页为质量组定义规则。</span><span class="sxs-lookup"><span data-stu-id="44c72-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="44c72-379">您还可以为所选质量组使用<strong>物料质量组</strong>页来将相关物料分配给该组。</span><span class="sxs-lookup"><span data-stu-id="44c72-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="44c72-380">您还可以为所选物料使用<strong>物料质量组</strong>页来将相关质量组分配给该物料。</span><span class="sxs-lookup"><span data-stu-id="44c72-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="44c72-381">某制造公司采购的多种原材料具有相同的进货检查测试要求。</span><span class="sxs-lookup"><span data-stu-id="44c72-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="44c72-382">公司定义了一个质量组，然后将与原材料关联的物料编号分配给该组。</span><span class="sxs-lookup"><span data-stu-id="44c72-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="44c72-383">之后，公司采购一个新类型的原材料，具有相同的测试要求。</span><span class="sxs-lookup"><span data-stu-id="44c72-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="44c72-384">公司不是为新物料设置新的测试要求，而是将新物料的物料编号添加到现有的质量组。</span><span class="sxs-lookup"><span data-stu-id="44c72-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="44c72-385">此相同制造公司还生产具有相同测试要求的物料，并装运具有相同装运前测试要求的物料。</span><span class="sxs-lookup"><span data-stu-id="44c72-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="44c72-386">公司定义两个附加质量组，然后将相关物料编号分配给每个组。</span><span class="sxs-lookup"><span data-stu-id="44c72-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44c72-387">测试变量</span><span class="sxs-lookup"><span data-stu-id="44c72-387">Test variables</span></span></td>
<td><span data-ttu-id="44c72-388">使用此页可以定义和查看与定性测试关联的变量。</span><span class="sxs-lookup"><span data-stu-id="44c72-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="44c72-389">对于每个变量，您定义表示可能选项的枚举结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="44c72-390">您在<strong>测试</strong>页上定义测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="44c72-391">对于定性测试，您必须将测试类型设置为<strong>选项</strong>。</span><span class="sxs-lookup"><span data-stu-id="44c72-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="44c72-392">使用<strong>测试组</strong>页可以将测试变量分配给单个测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="44c72-393">一个生产饼干的制造公司对成品使用检查测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="44c72-394">此检查测试具有多个变量。</span><span class="sxs-lookup"><span data-stu-id="44c72-394">This inspection test has several variables.</span></span> <span data-ttu-id="44c72-395">一个变量是味道，并且此变量的可能结果是好和坏。</span><span class="sxs-lookup"><span data-stu-id="44c72-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="44c72-396">第二个变量是颜色，其可能结果是过暗、过浅和正好。</span><span class="sxs-lookup"><span data-stu-id="44c72-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44c72-397">测试变量结果</span><span class="sxs-lookup"><span data-stu-id="44c72-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="44c72-398">使用此页面可以设置、编辑和查看与定性测试关联的测试变量的可能测试结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="44c72-399">对于每个结果，您分配<strong>通过</strong>或<strong>未通过</strong>状态。</span><span class="sxs-lookup"><span data-stu-id="44c72-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="44c72-400">您必须在<strong>测试</strong>页上定义的每个定性测试定义变量及其结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="44c72-401">（对于定性测试，测试类型在<strong>测试</strong>页上设置为<strong>选项</strong>。）使用<strong>测试组</strong>页可以将测试变量和默认结果分配给单独的定性测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="44c72-402">一个生产饼干的制造公司对成品使用检查测试。</span><span class="sxs-lookup"><span data-stu-id="44c72-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="44c72-403">此检查测试具有多个变量。</span><span class="sxs-lookup"><span data-stu-id="44c72-403">This inspection test has of several variables.</span></span> <span data-ttu-id="44c72-404">一个变量是味道，并且此变量的可能结果是好和坏。</span><span class="sxs-lookup"><span data-stu-id="44c72-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="44c72-405">第二个变量是颜色，其可能结果是过暗、过浅和正好。</span><span class="sxs-lookup"><span data-stu-id="44c72-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="44c72-406">会为每个结果分配一个<strong>通过</strong>或<strong>未通过</strong>的状态。</span><span class="sxs-lookup"><span data-stu-id="44c72-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="44c72-407">在各个变量的检查测试期间，检查员将通过选择其中一个结果报告测试结果。</span><span class="sxs-lookup"><span data-stu-id="44c72-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="44c72-408">其他资源</span><span class="sxs-lookup"><span data-stu-id="44c72-408">Additional resources</span></span>
--------

[<span data-ttu-id="44c72-409">质量管理流程</span><span class="sxs-lookup"><span data-stu-id="44c72-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="44c72-410">不符合项管理</span><span class="sxs-lookup"><span data-stu-id="44c72-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="44c72-411">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="44c72-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]