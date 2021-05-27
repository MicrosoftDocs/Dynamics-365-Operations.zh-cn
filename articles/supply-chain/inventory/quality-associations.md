---
title: 质量关联
description: 本主题介绍如何使用 Microsoft Dynamics 365 Supply Chain Management 中的质量关联来自动生成与您的销售、采购和生产流程相关的质检订单。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022316"
---
# <a name="quality-associations"></a><span data-ttu-id="49d9d-103">质量关联</span><span class="sxs-lookup"><span data-stu-id="49d9d-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49d9d-104">本主题介绍如何使用 Microsoft Dynamics 365 Supply Chain Management 中的质量关联来自动生成与您的销售、采购和生产流程相关的质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="49d9d-105">质量关联定义生成的质检订单的所有以下信息：</span><span class="sxs-lookup"><span data-stu-id="49d9d-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="49d9d-106">交易记录事件</span><span class="sxs-lookup"><span data-stu-id="49d9d-106">The transaction event</span></span>
- <span data-ttu-id="49d9d-107">必须在物料上执行的测试组</span><span class="sxs-lookup"><span data-stu-id="49d9d-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="49d9d-108">可接受质量级别 (AQL)</span><span class="sxs-lookup"><span data-stu-id="49d9d-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="49d9d-109">抽样计划</span><span class="sxs-lookup"><span data-stu-id="49d9d-109">The sampling plan</span></span>

<span data-ttu-id="49d9d-110">您必须为业务流程中要求自动生成质检订单的每种变化定义质量关联。</span><span class="sxs-lookup"><span data-stu-id="49d9d-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="49d9d-111">例如，可以在业务流程中为采购订单、检验单、销售订单和生产订单生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="49d9d-112">使用质量关联</span><span class="sxs-lookup"><span data-stu-id="49d9d-112">Working with quality associations</span></span>

<span data-ttu-id="49d9d-113">使用质量关联的业务流程可与许多源文档相关，例如采购订单、销售订单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="49d9d-114">每个质量关联记录定义了测试组、AQL 和应用于生成的质检订单的抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="49d9d-115">您必须为业务流程中每个变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="49d9d-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="49d9d-116">例如，当更新采购订单产品收据时，您可以设置生成质检订单的质量关联。</span><span class="sxs-lookup"><span data-stu-id="49d9d-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="49d9d-117">根据执行计划的设置，在存在未结质检订单的情况下，可以锁定触发流程本身。</span><span class="sxs-lookup"><span data-stu-id="49d9d-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="49d9d-118">或者，可以锁定后续流程，如采购订单开票。</span><span class="sxs-lookup"><span data-stu-id="49d9d-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="49d9d-119">在有未结质检订单时，会自动锁定库存数量使其不发放。</span><span class="sxs-lookup"><span data-stu-id="49d9d-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="49d9d-120">根据 **物料抽样** 页上的 **完全锁定** 字段的设置，该数量是质检订单上的数量或源文档行上的数量。</span><span class="sxs-lookup"><span data-stu-id="49d9d-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="49d9d-121">有关详细信息，请参阅[质量管理物料抽样](quality-item-sampling.md)。</span><span class="sxs-lookup"><span data-stu-id="49d9d-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="49d9d-122">对于给定业务流程，质量关联记录标识用于生成质检订单的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="49d9d-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="49d9d-123">条件可以特定于站点或法人。</span><span class="sxs-lookup"><span data-stu-id="49d9d-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="49d9d-124">只有对于事件存在现有库存时，才能生成涉及破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="49d9d-125">要使用质量关联，转到 **库存管理 \> 设置 \> 质量控制 \> 质量关联**。</span><span class="sxs-lookup"><span data-stu-id="49d9d-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="49d9d-126">以下示例演示如何为各个业务流程中的变化形式定义质量关联记录。</span><span class="sxs-lookup"><span data-stu-id="49d9d-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="49d9d-127">对于每个示例，下表总结了质量关联记录定义的事件和条件。</span><span class="sxs-lookup"><span data-stu-id="49d9d-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="49d9d-128">引用类型</span><span class="sxs-lookup"><span data-stu-id="49d9d-128">Reference type</span></span></th>
<th><span data-ttu-id="49d9d-129">事件类型</span><span class="sxs-lookup"><span data-stu-id="49d9d-129">Event type</span></span></th>
<th><span data-ttu-id="49d9d-130">执行</span><span class="sxs-lookup"><span data-stu-id="49d9d-130">Execution</span></span></th>
<th><span data-ttu-id="49d9d-131">事件锁定</span><span class="sxs-lookup"><span data-stu-id="49d9d-131">Event blocking</span></span></th>
<th><span data-ttu-id="49d9d-132">文档引用</span><span class="sxs-lookup"><span data-stu-id="49d9d-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49d9d-133">库存</span><span class="sxs-lookup"><span data-stu-id="49d9d-133">Inventory</span></span></td>
<td><span data-ttu-id="49d9d-134">不适用</span><span class="sxs-lookup"><span data-stu-id="49d9d-134">Not applicable</span></span></td>
<td><span data-ttu-id="49d9d-135">不适用</span><span class="sxs-lookup"><span data-stu-id="49d9d-135">Not applicable</span></span></td>
<td><span data-ttu-id="49d9d-136">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-136">None</span></span></td>
<td><span data-ttu-id="49d9d-137">全部</span><span class="sxs-lookup"><span data-stu-id="49d9d-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="49d9d-138">销售额</span><span class="sxs-lookup"><span data-stu-id="49d9d-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="49d9d-139">已计划领料流程</span><span class="sxs-lookup"><span data-stu-id="49d9d-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="49d9d-140">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-140">Before</span></span></td>
<td><span data-ttu-id="49d9d-141">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="49d9d-142">仅特定 ID、组或全部</span><span class="sxs-lookup"><span data-stu-id="49d9d-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-143">领料流程</span><span class="sxs-lookup"><span data-stu-id="49d9d-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-144">装箱单</span><span class="sxs-lookup"><span data-stu-id="49d9d-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-145">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49d9d-146">装箱单</span><span class="sxs-lookup"><span data-stu-id="49d9d-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-147">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-147">Before</span></span></td>
<td><span data-ttu-id="49d9d-148">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-149">装箱单</span><span class="sxs-lookup"><span data-stu-id="49d9d-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-150">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="49d9d-151">采购</span><span class="sxs-lookup"><span data-stu-id="49d9d-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="49d9d-152">收货清单</span><span class="sxs-lookup"><span data-stu-id="49d9d-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="49d9d-153">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-153">Before</span></span></td>
<td><span data-ttu-id="49d9d-154">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-155">收货清单</span><span class="sxs-lookup"><span data-stu-id="49d9d-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-156">物料收货</span><span class="sxs-lookup"><span data-stu-id="49d9d-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-157">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49d9d-158">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-158">After</span></span></td>
<td><span data-ttu-id="49d9d-159">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-160">物料收货</span><span class="sxs-lookup"><span data-stu-id="49d9d-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-161">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49d9d-162">注册</span><span class="sxs-lookup"><span data-stu-id="49d9d-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-163">不适用</span><span class="sxs-lookup"><span data-stu-id="49d9d-163">Not applicable</span></span></td>
<td><span data-ttu-id="49d9d-164">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-165">物料收货</span><span class="sxs-lookup"><span data-stu-id="49d9d-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-166">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="49d9d-167">物料收货</span><span class="sxs-lookup"><span data-stu-id="49d9d-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-168">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-168">Before</span></span></td>
<td><span data-ttu-id="49d9d-169">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-170">物料收货</span><span class="sxs-lookup"><span data-stu-id="49d9d-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-171">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49d9d-172">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-172">After</span></span></td>
<td><span data-ttu-id="49d9d-173">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-174">开票</span><span class="sxs-lookup"><span data-stu-id="49d9d-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="49d9d-175">生产</span><span class="sxs-lookup"><span data-stu-id="49d9d-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-176">注册</span><span class="sxs-lookup"><span data-stu-id="49d9d-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-177">不适用</span><span class="sxs-lookup"><span data-stu-id="49d9d-177">Not applicable</span></span></td>
<td><span data-ttu-id="49d9d-178">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="49d9d-179">全部</span><span class="sxs-lookup"><span data-stu-id="49d9d-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-180">完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-181">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="49d9d-182">完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-183">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-183">Before</span></span></td>
<td><span data-ttu-id="49d9d-184">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-185">完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-186">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49d9d-187">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-187">After</span></span></td>
<td><span data-ttu-id="49d9d-188">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-189">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="49d9d-190">检验</span><span class="sxs-lookup"><span data-stu-id="49d9d-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-191">完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="49d9d-192">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-192">Before</span></span></td>
<td><span data-ttu-id="49d9d-193">完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-194">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-195">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-195">After</span></span></td>
<td><span data-ttu-id="49d9d-196">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-197">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-197">End</span></span></td>
<td><span data-ttu-id="49d9d-198">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-198">Before</span></span></td>
<td><span data-ttu-id="49d9d-199">结束</span><span class="sxs-lookup"><span data-stu-id="49d9d-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49d9d-200">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="49d9d-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-201">报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="49d9d-202">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-202">Before</span></span></td>
<td><span data-ttu-id="49d9d-203">否</span><span class="sxs-lookup"><span data-stu-id="49d9d-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-204">特定 ID、组或全部，以及特定资源、组或全部</span><span class="sxs-lookup"><span data-stu-id="49d9d-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-205">报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-206">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-206">After</span></span></td>
<td><span data-ttu-id="49d9d-207">否</span><span class="sxs-lookup"><span data-stu-id="49d9d-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49d9d-208">联产品生产</span><span class="sxs-lookup"><span data-stu-id="49d9d-208">Co-product production</span></span></td>
<td><span data-ttu-id="49d9d-209">注册</span><span class="sxs-lookup"><span data-stu-id="49d9d-209">Registration</span></span></td>
<td><span data-ttu-id="49d9d-210">不适用</span><span class="sxs-lookup"><span data-stu-id="49d9d-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-211">否</span><span class="sxs-lookup"><span data-stu-id="49d9d-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="49d9d-212">所有</span><span class="sxs-lookup"><span data-stu-id="49d9d-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49d9d-213">报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="49d9d-213">Report as finished</span></span></td>
<td><span data-ttu-id="49d9d-214">之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-215">之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="49d9d-216">*仓库流程质量管理* 功能添加了将 **事件类型** 字段设置为 *报告为完工入库* 并将 **执行** 字段设置为 *以后* 的生产的质检订单处理能力，以及将 **事件类型** 字段设置为 *登记* 的采购的质检订单处理能力。</span><span class="sxs-lookup"><span data-stu-id="49d9d-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="49d9d-217">有关详细信息，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)。</span><span class="sxs-lookup"><span data-stu-id="49d9d-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="49d9d-218">下表提供有关可以如何为特定类型的流程生成质检订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="49d9d-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="49d9d-219">流程的类型</span><span class="sxs-lookup"><span data-stu-id="49d9d-219">Type of process</span></span></th>
<th><span data-ttu-id="49d9d-220">可以自动生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="49d9d-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="49d9d-221">需要破坏性测试的情况下可以生成质检订单时</span><span class="sxs-lookup"><span data-stu-id="49d9d-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="49d9d-222">条件信息</span><span class="sxs-lookup"><span data-stu-id="49d9d-222">Condition information</span></span></th>
<th><span data-ttu-id="49d9d-223">手动生成信息</span><span class="sxs-lookup"><span data-stu-id="49d9d-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49d9d-224">采购订单</span><span class="sxs-lookup"><span data-stu-id="49d9d-224">Purchase order</span></span></td>
<td><span data-ttu-id="49d9d-225">过帐收到的物料的收据清单或产品收据之前或之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="49d9d-226">过帐收到的物料的产品收据之后，因为物料必须可用于破坏性测试</span><span class="sxs-lookup"><span data-stu-id="49d9d-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="49d9d-227">质检订单的要求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="49d9d-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="49d9d-228">引用某一采购订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-229">检验单</span><span class="sxs-lookup"><span data-stu-id="49d9d-229">Quarantine order</span></span></td>
<td><span data-ttu-id="49d9d-230">在检验单报告为已完工入库或已结束之前或之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="49d9d-231">无法生成需要破坏性测试的质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="49d9d-232">假定检验单功能处理损坏物料的处置。</span><span class="sxs-lookup"><span data-stu-id="49d9d-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="49d9d-233">质检订单的要求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="49d9d-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="49d9d-234">引用某一检验单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-235">销售订单</span><span class="sxs-lookup"><span data-stu-id="49d9d-235">Sales order</span></span></td>
<td><span data-ttu-id="49d9d-236">在要被装运的物料的已计划领料流程或装箱单更新之前</span><span class="sxs-lookup"><span data-stu-id="49d9d-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="49d9d-237">任何步骤中</span><span class="sxs-lookup"><span data-stu-id="49d9d-237">At any step</span></span></td>
<td><span data-ttu-id="49d9d-238">质检订单的要求可以反映特定的站点、物料或客户，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="49d9d-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="49d9d-239">引用某一销售订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-240">生产订单</span><span class="sxs-lookup"><span data-stu-id="49d9d-240">Production order</span></span></td>
<td><span data-ttu-id="49d9d-241">报告生产订单的完工数量之前或之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="49d9d-242">报告生产订单的完工数量之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="49d9d-243">质检订单的要求可以反映特定站点或物料，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="49d9d-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="49d9d-244">引用某一生产订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-245">具有工艺路线工序的生产订单</span><span class="sxs-lookup"><span data-stu-id="49d9d-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="49d9d-246">在报告为已完成工序之前或之后</span><span class="sxs-lookup"><span data-stu-id="49d9d-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="49d9d-247">在报告生产最后一道工序完成后</span><span class="sxs-lookup"><span data-stu-id="49d9d-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="49d9d-248">质检订单的要求可以反映特定的站点、物料或运营资源，或者反映这些条件的组合。</span><span class="sxs-lookup"><span data-stu-id="49d9d-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="49d9d-249">引用某一工艺路线工序的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</span><span class="sxs-lookup"><span data-stu-id="49d9d-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-250">库存</span><span class="sxs-lookup"><span data-stu-id="49d9d-250">Inventory</span></span></td>
<td><span data-ttu-id="49d9d-251">无法为库存日志中的交易记录或为转移单交易记录自动生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="49d9d-252">必须为物料的库存数量手动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="49d9d-253">实际现有库存量是必需的。</span><span class="sxs-lookup"><span data-stu-id="49d9d-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="49d9d-254">自动生成质检订单示例</span><span class="sxs-lookup"><span data-stu-id="49d9d-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="49d9d-255">采购</span><span class="sxs-lookup"><span data-stu-id="49d9d-255">Purchasing</span></span>

<span data-ttu-id="49d9d-256">在采购中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 *物料收货*，并将 **执行** 字段设置为 *之后*，您将得到以下结果：</span><span class="sxs-lookup"><span data-stu-id="49d9d-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="49d9d-257">如果将 **按照更新的数量** 选项设置为 *是*，则会根据物料抽样中收到的数量和设置，根据采购订单为每个收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="49d9d-258">每次根据采购订单接收数量时，都会根据新接收的数量生成新的质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="49d9d-259">如果将 **按照更新的数量** 选项设置为 *否*，则会根据收到的数量，根据采购订单为第一个收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="49d9d-260">此外，根据跟踪维度，将基于剩余数量创建一个或多个质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="49d9d-261">不会根据采购订单为后续收货生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="49d9d-262">生产</span><span class="sxs-lookup"><span data-stu-id="49d9d-262">Production</span></span>

<span data-ttu-id="49d9d-263">在生产中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 *完工入库*，并将 **执行** 字段设置为 *之后*，您将得到以下结果：</span><span class="sxs-lookup"><span data-stu-id="49d9d-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="49d9d-264">如果将 **按照更新的数量** 选项设置为 *是*，则会根据物料抽样中每个完成的数量和设置生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="49d9d-265">每次根据生产订单将数量完工入库时，都会根据新完成的数量生成新的质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="49d9d-266">此生成逻辑与采购一致。</span><span class="sxs-lookup"><span data-stu-id="49d9d-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="49d9d-267">如果将 **按照更新的数量** 选项设置为 *否*，则会根据完成的数量，在数量第一次完工入库时生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="49d9d-268">此外，根据物料抽样的跟踪维度，将基于剩余数量创建一个或多个质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="49d9d-269">后续的完成数量不会生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="49d9d-270">质量规范</span><span class="sxs-lookup"><span data-stu-id="49d9d-270">Quality specification</span></span></th>
<th><span data-ttu-id="49d9d-271">按照更新的数量</span><span class="sxs-lookup"><span data-stu-id="49d9d-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="49d9d-272">按照跟踪维度</span><span class="sxs-lookup"><span data-stu-id="49d9d-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="49d9d-273">结果</span><span class="sxs-lookup"><span data-stu-id="49d9d-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49d9d-274">百分比：10%</span><span class="sxs-lookup"><span data-stu-id="49d9d-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="49d9d-275">是</span><span class="sxs-lookup"><span data-stu-id="49d9d-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="49d9d-276">批处理号：否</span><span class="sxs-lookup"><span data-stu-id="49d9d-276">Batch number: No</span></span></p>
<p><span data-ttu-id="49d9d-277">序列号：否</span><span class="sxs-lookup"><span data-stu-id="49d9d-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="49d9d-278">订单数量：100</span><span class="sxs-lookup"><span data-stu-id="49d9d-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="49d9d-279">30 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="49d9d-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="49d9d-280">3 的质检订单 1（30 的 10%）</span><span class="sxs-lookup"><span data-stu-id="49d9d-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="49d9d-281">70 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="49d9d-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="49d9d-282">7 的质检订单 2（剩余订单数量的 10%，该数量在此例中为 70）</span><span class="sxs-lookup"><span data-stu-id="49d9d-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-283">固定数量：1</span><span class="sxs-lookup"><span data-stu-id="49d9d-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="49d9d-284">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-284">No</span></span></td>
<td>
<p><span data-ttu-id="49d9d-285">批处理号：否</span><span class="sxs-lookup"><span data-stu-id="49d9d-285">Batch number: No</span></span></p>
<p><span data-ttu-id="49d9d-286">序列号：否</span><span class="sxs-lookup"><span data-stu-id="49d9d-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="49d9d-287">订单数量：100</span><span class="sxs-lookup"><span data-stu-id="49d9d-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="49d9d-288">30 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="49d9d-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="49d9d-289">1 的质检订单 1（对于第一个完工入库数量，其固定值为 1）</span><span class="sxs-lookup"><span data-stu-id="49d9d-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="49d9d-290">1 的质检订单 2（对于剩余数量，其固定值仍为 1）</span><span class="sxs-lookup"><span data-stu-id="49d9d-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="49d9d-291">10 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="49d9d-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="49d9d-292">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="49d9d-293">60 的完工入库量</span><span class="sxs-lookup"><span data-stu-id="49d9d-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="49d9d-294">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-295">固定数量：1</span><span class="sxs-lookup"><span data-stu-id="49d9d-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="49d9d-296">是</span><span class="sxs-lookup"><span data-stu-id="49d9d-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="49d9d-297">批处理号：是</span><span class="sxs-lookup"><span data-stu-id="49d9d-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="49d9d-298">序列号：是</span><span class="sxs-lookup"><span data-stu-id="49d9d-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="49d9d-299">订单数量：10</span><span class="sxs-lookup"><span data-stu-id="49d9d-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="49d9d-300">3 的完工入库量：批处理号 b1、序列号 s1 为 1；批处理号 b2、序列号 s2 为 1；批处理号 b3、序列号 s3 为 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="49d9d-301">批处理号 b1、序列号 s1 为 1 的质检订单 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="49d9d-302">批处理号 b2、序列号 s2 为 1 的质检订单 2</span><span class="sxs-lookup"><span data-stu-id="49d9d-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="49d9d-303">批处理号 b3、序列号 s3 为 1 的质检订单 3</span><span class="sxs-lookup"><span data-stu-id="49d9d-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="49d9d-304">2 的完工入库量：批处理号 b4、序列号 s4 为 1；批处理号 b5、序列号 s5 为 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="49d9d-305">批处理号 b4、序列号 s4 为 1 的质检订单 4</span><span class="sxs-lookup"><span data-stu-id="49d9d-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="49d9d-306">批处理号 b5、序列号 s5 为 1 的质检订单 5</span><span class="sxs-lookup"><span data-stu-id="49d9d-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="49d9d-307"><strong>注意：</strong>批次可以重复使用。</span><span class="sxs-lookup"><span data-stu-id="49d9d-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="49d9d-308">固定数量：2</span><span class="sxs-lookup"><span data-stu-id="49d9d-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="49d9d-309">无</span><span class="sxs-lookup"><span data-stu-id="49d9d-309">No</span></span></td>
<td>
<p><span data-ttu-id="49d9d-310">批处理号：是</span><span class="sxs-lookup"><span data-stu-id="49d9d-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="49d9d-311">序列号：是</span><span class="sxs-lookup"><span data-stu-id="49d9d-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="49d9d-312">订单数量：10</span><span class="sxs-lookup"><span data-stu-id="49d9d-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="49d9d-313">4 的完工入库量：批处理号 b1、序列号 s1 为 1；批处理号 b2、序列号 s2 为 1；批处理号 b3、序列号 s3 为 1；批处理号 b4、序列号 s4 为 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="49d9d-314">批处理号 b1、序列号 s1 为 1 的质检订单 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="49d9d-315">批处理号 b2、序列号 s2 为 1 的质检订单 2</span><span class="sxs-lookup"><span data-stu-id="49d9d-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="49d9d-316">批处理号 b3、序列号 s3 为 1 的质检订单 3</span><span class="sxs-lookup"><span data-stu-id="49d9d-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="49d9d-317">批处理号 b4、序列号 s4 为 1 的质检订单 4</span><span class="sxs-lookup"><span data-stu-id="49d9d-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="49d9d-318">2 的质检订单 5，没有批处理号和序列号的引用</span><span class="sxs-lookup"><span data-stu-id="49d9d-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="49d9d-319">6 的完工入库量：批处理号 b5、序列号 s5 为 1；批处理号 b6、序列号 s6 为 1；批处理号 b7、序列号 s7 为 1；批处理号 b8、序列号 s8 为 1；批处理号 b9、序列号 s9 为 1；批处理号 b10、序列号 s10 为 1</span><span class="sxs-lookup"><span data-stu-id="49d9d-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="49d9d-320">未创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="49d9d-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="49d9d-321">其他资源</span><span class="sxs-lookup"><span data-stu-id="49d9d-321">Additional resources</span></span>

- [<span data-ttu-id="49d9d-322">质量管理流程</span><span class="sxs-lookup"><span data-stu-id="49d9d-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="49d9d-323">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="49d9d-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="49d9d-324">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="49d9d-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
