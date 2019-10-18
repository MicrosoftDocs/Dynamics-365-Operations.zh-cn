---
title: 仓库工作策略概览
description: 仓库工作策略控制是否通过仓库流程在制造中基于工作订单类型、库存库位和产品创建仓库工作。
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7476cf797685feb4c50e3cefef4c53ca37b82dff
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251400"
---
# <a name="warehouse-work-policies-overview"></a><span data-ttu-id="04cd9-103">仓库工作策略概览</span><span class="sxs-lookup"><span data-stu-id="04cd9-103">Warehouse work policies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04cd9-104">仓库工作策略控制是否通过仓库流程在制造中基于工作订单类型、库存库位和产品创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-104">Warehouse work policies control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="04cd9-105">此工作策略控制是否为生产中的仓库流程创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="04cd9-106">您可以使用**工作订单类型**、**库存库位**和**产品**组合设置工作策略。</span><span class="sxs-lookup"><span data-stu-id="04cd9-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="04cd9-107">例如，产品 L0101 报告为完工入库到输出库位 001。</span><span class="sxs-lookup"><span data-stu-id="04cd9-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="04cd9-108">成品稍后将在输出库位 001 的另一个生产订单中使用。</span><span class="sxs-lookup"><span data-stu-id="04cd9-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="04cd9-109">在这种情况下，您可以设置工作策略，阻止在您将产品 L0101 报告为完工入库到输出库位 001 时创建产品储存的工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="04cd9-110">工作策略是可以通过以下信息描述的单个实体：</span><span class="sxs-lookup"><span data-stu-id="04cd9-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="04cd9-111">**工作策略名称**（工作策略的唯一标识符）</span><span class="sxs-lookup"><span data-stu-id="04cd9-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="04cd9-112">**工作订单类型**和**工作创建方法**</span><span class="sxs-lookup"><span data-stu-id="04cd9-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="04cd9-113">**库存库位**</span><span class="sxs-lookup"><span data-stu-id="04cd9-113">**Inventory locations**</span></span>
-   <span data-ttu-id="04cd9-114">**产品**</span><span class="sxs-lookup"><span data-stu-id="04cd9-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="04cd9-115">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="04cd9-115">Work order types</span></span>
<span data-ttu-id="04cd9-116">您可以选择以下工作订单类型：</span><span class="sxs-lookup"><span data-stu-id="04cd9-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="04cd9-117">成品储存</span><span class="sxs-lookup"><span data-stu-id="04cd9-117">Finished goods put away</span></span>
-   <span data-ttu-id="04cd9-118">联产品和副产品储存</span><span class="sxs-lookup"><span data-stu-id="04cd9-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="04cd9-119">原材料领取</span><span class="sxs-lookup"><span data-stu-id="04cd9-119">Raw material picking</span></span>

<span data-ttu-id="04cd9-120">**工作创建方法**字段的值为**从不**。</span><span class="sxs-lookup"><span data-stu-id="04cd9-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="04cd9-121">该值表示工作策略将阻止为选定的工作订单类型创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="04cd9-122">库存库位</span><span class="sxs-lookup"><span data-stu-id="04cd9-122">Inventory locations</span></span>
<span data-ttu-id="04cd9-123">您可以选择应用工作策略的位置。</span><span class="sxs-lookup"><span data-stu-id="04cd9-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="04cd9-124">如果工作策略没有关联任何位置，则工作策略不会应用到任何流程。</span><span class="sxs-lookup"><span data-stu-id="04cd9-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="04cd9-125">在**位置**页面，您还可以选择或取消选择特定位置的工作策略。</span><span class="sxs-lookup"><span data-stu-id="04cd9-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="04cd9-126">产品</span><span class="sxs-lookup"><span data-stu-id="04cd9-126">Products</span></span>
<span data-ttu-id="04cd9-127">您可以选择应用工作策略的产品。</span><span class="sxs-lookup"><span data-stu-id="04cd9-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="04cd9-128">您可以将工作策略应用到所有产品或所选的产品。</span><span class="sxs-lookup"><span data-stu-id="04cd9-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="04cd9-129">示例</span><span class="sxs-lookup"><span data-stu-id="04cd9-129">Example</span></span>
<span data-ttu-id="04cd9-130">在以下示例中，有两个生产订单，PRD-001 和 PRD-00*2*。</span><span class="sxs-lookup"><span data-stu-id="04cd9-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="04cd9-131">生产订单 PRD-001 具有名为**装配**的工序，此时产品 SC1 正在报告为完工入库到库位 O1。</span><span class="sxs-lookup"><span data-stu-id="04cd9-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="04cd9-132">生产订单 PRD-002 具有名为**喷涂**的工序，使用来自库位 O1 的产品 SC1。</span><span class="sxs-lookup"><span data-stu-id="04cd9-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="04cd9-133">生产订单 PRD-002 还使用来自库位 O1 的原材料 RM1。</span><span class="sxs-lookup"><span data-stu-id="04cd9-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="04cd9-134">RM1 存储在仓库库位 BULK-001，将通过原材料领料的仓库工作领取到库位 O1。</span><span class="sxs-lookup"><span data-stu-id="04cd9-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="04cd9-135">生产 PRD-002 放行时生成领料工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="04cd9-136">[![仓库工作策略](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="04cd9-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="04cd9-137">当您计划为此场景配置仓库工作策略时，您应该考虑以下信息：</span><span class="sxs-lookup"><span data-stu-id="04cd9-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="04cd9-138">当您报告产品 SC1 从生产订单 PRD-001 完工到库位 O1 时，不要求创建成品储存的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="04cd9-139">这是因为生产订单 PRD-002 的**喷涂**工序使用同一位置的 SC1。</span><span class="sxs-lookup"><span data-stu-id="04cd9-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="04cd9-140">为了将原材料 RM1 从仓库库位 BULK-001 移到库位 O1，要求创建原材料领料的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="04cd9-141">这是您基于这些注意事项可以设置的工作策略示例。</span><span class="sxs-lookup"><span data-stu-id="04cd9-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="04cd9-142"><strong>工作策略名称</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="04cd9-143"><strong>工作订单类型</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="04cd9-144">无储存 01     \`</span><span class="sxs-lookup"><span data-stu-id="04cd9-144">No put away 01     \`</span></span>          |     <span data-ttu-id="04cd9-145">- 成品储存</span><span class="sxs-lookup"><span data-stu-id="04cd9-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="04cd9-146"><strong>位置</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="04cd9-147">- O1</span><span class="sxs-lookup"><span data-stu-id="04cd9-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="04cd9-148"><strong>产品</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="04cd9-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="04cd9-149">- SC1</span></span>                 |

<span data-ttu-id="04cd9-150">以下步骤提供了关于如何为此场景设置仓库工作策略的详细说明。</span><span class="sxs-lookup"><span data-stu-id="04cd9-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="04cd9-151">还介绍了一个示例设置，显示如何报告生产订单完工入库到非牌照控制的库位。</span><span class="sxs-lookup"><span data-stu-id="04cd9-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="04cd9-152">设置仓库工作策略</span><span class="sxs-lookup"><span data-stu-id="04cd9-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="04cd9-153">仓库流程不是始终包括仓库工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="04cd9-154">通过定义工作策略，您可以防止为原材料领料创建工作，并将一组产品的成品储存在特定位置。</span><span class="sxs-lookup"><span data-stu-id="04cd9-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="04cd9-155">创建此过程时使用的是 USMF 演示数据格式。</span><span class="sxs-lookup"><span data-stu-id="04cd9-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="04cd9-156">步骤 (21)</span><span class="sxs-lookup"><span data-stu-id="04cd9-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="04cd9-157">1</span><span class="sxs-lookup"><span data-stu-id="04cd9-157">1.</span></span>  | <span data-ttu-id="04cd9-158">转到“仓库管理”&gt;“设置”&gt;“工作”&gt;“工作策略”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="04cd9-159">2</span><span class="sxs-lookup"><span data-stu-id="04cd9-159">2.</span></span>  | <span data-ttu-id="04cd9-160">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="04cd9-161">3</span><span class="sxs-lookup"><span data-stu-id="04cd9-161">3.</span></span>  | <span data-ttu-id="04cd9-162">在“工作策略名称”字段中，键入“无储存工作”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="04cd9-163">4</span><span class="sxs-lookup"><span data-stu-id="04cd9-163">4.</span></span>  | <span data-ttu-id="04cd9-164">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="04cd9-165">5</span><span class="sxs-lookup"><span data-stu-id="04cd9-165">5.</span></span>  | <span data-ttu-id="04cd9-166">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="04cd9-167">6</span><span class="sxs-lookup"><span data-stu-id="04cd9-167">6.</span></span>  | <span data-ttu-id="04cd9-168">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="04cd9-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="04cd9-169">7</span><span class="sxs-lookup"><span data-stu-id="04cd9-169">7.</span></span>  | <span data-ttu-id="04cd9-170">在“工作订单类型”字段中，选择“成品储存”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="04cd9-171">8</span><span class="sxs-lookup"><span data-stu-id="04cd9-171">8.</span></span>  | <span data-ttu-id="04cd9-172">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="04cd9-173">9</span><span class="sxs-lookup"><span data-stu-id="04cd9-173">9.</span></span>  | <span data-ttu-id="04cd9-174">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="04cd9-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="04cd9-175">10.</span><span class="sxs-lookup"><span data-stu-id="04cd9-175">10.</span></span> | <span data-ttu-id="04cd9-176">在“工作订单类型”字段中，选择“联产品和副产品储存”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="04cd9-177">11.</span><span class="sxs-lookup"><span data-stu-id="04cd9-177">11.</span></span> | <span data-ttu-id="04cd9-178">展开“库存库位”部分。</span><span class="sxs-lookup"><span data-stu-id="04cd9-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="04cd9-179">12.</span><span class="sxs-lookup"><span data-stu-id="04cd9-179">12.</span></span> | <span data-ttu-id="04cd9-180">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="04cd9-181">13</span><span class="sxs-lookup"><span data-stu-id="04cd9-181">13.</span></span> | <span data-ttu-id="04cd9-182">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="04cd9-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="04cd9-183">14.</span><span class="sxs-lookup"><span data-stu-id="04cd9-183">14.</span></span> | <span data-ttu-id="04cd9-184">在仓库列表中，输入 '51'。</span><span class="sxs-lookup"><span data-stu-id="04cd9-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="04cd9-185">15.</span><span class="sxs-lookup"><span data-stu-id="04cd9-185">15.</span></span> | <span data-ttu-id="04cd9-186">在“位置”字段中，输入或选择 '001'。</span><span class="sxs-lookup"><span data-stu-id="04cd9-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="04cd9-187">16.</span><span class="sxs-lookup"><span data-stu-id="04cd9-187">16.</span></span> | <span data-ttu-id="04cd9-188">展开“产品”部分。</span><span class="sxs-lookup"><span data-stu-id="04cd9-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="04cd9-189">17.</span><span class="sxs-lookup"><span data-stu-id="04cd9-189">17.</span></span> | <span data-ttu-id="04cd9-190">在“产品选择”字段中，选择“已选择”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="04cd9-191">18.</span><span class="sxs-lookup"><span data-stu-id="04cd9-191">18.</span></span> | <span data-ttu-id="04cd9-192">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="04cd9-193">19.</span><span class="sxs-lookup"><span data-stu-id="04cd9-193">19.</span></span> | <span data-ttu-id="04cd9-194">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="04cd9-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="04cd9-195">20.</span><span class="sxs-lookup"><span data-stu-id="04cd9-195">20.</span></span> | <span data-ttu-id="04cd9-196">在“物料编号”字段中，输入或选择 'L0101'。</span><span class="sxs-lookup"><span data-stu-id="04cd9-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="04cd9-197">21.</span><span class="sxs-lookup"><span data-stu-id="04cd9-197">21.</span></span> | <span data-ttu-id="04cd9-198">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="04cd9-199">报告生产订单完工入库到非牌照控制的库位</span><span class="sxs-lookup"><span data-stu-id="04cd9-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="04cd9-200">此过程显示报告为完工入库到非牌照控制的位置的示例。</span><span class="sxs-lookup"><span data-stu-id="04cd9-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="04cd9-201">一个适用的工作策略是此任务的先决条件。</span><span class="sxs-lookup"><span data-stu-id="04cd9-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="04cd9-202">上一个过程显示工作策略的设置。</span><span class="sxs-lookup"><span data-stu-id="04cd9-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="04cd9-203">步骤 (25)</span><span class="sxs-lookup"><span data-stu-id="04cd9-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="04cd9-204"><strong>子任务：设置输出库位。</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="04cd9-205">转到“组织管理”&gt;“资源”&gt;“资源组”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="04cd9-206">在列表中选择资源组 &#39;5102&#39;。</span><span class="sxs-lookup"><span data-stu-id="04cd9-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="04cd9-207">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="04cd9-208">在“输出仓库”字段中，输入 &#39;51&#39;。</span><span class="sxs-lookup"><span data-stu-id="04cd9-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="04cd9-209">在“输出库位”字段中，输入 &#39;001&#39;。</span><span class="sxs-lookup"><span data-stu-id="04cd9-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="04cd9-210">库位 001 不是牌照控制的位置。</span><span class="sxs-lookup"><span data-stu-id="04cd9-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="04cd9-211">只有当库位存在适用的工作策略时，您才可以设置非牌照控制的输出位置。</span><span class="sxs-lookup"><span data-stu-id="04cd9-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="04cd9-212"><strong>子任务：创建生产订单并报告为已完工入库。</strong></span><span class="sxs-lookup"><span data-stu-id="04cd9-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="04cd9-213">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="04cd9-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="04cd9-214">转到“生产控制”&gt;“生产订单”&gt;“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="04cd9-215">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="04cd9-216">在“物料编号”字段中输入 &#39;L0101&#39;。</span><span class="sxs-lookup"><span data-stu-id="04cd9-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="04cd9-217">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="04cd9-218">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="04cd9-219">单击“估计”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="04cd9-220">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="04cd9-221">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="04cd9-222">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="04cd9-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="04cd9-223">在“自动物料清单消耗量”字段中，选择&#39;从不&#39;。</span><span class="sxs-lookup"><span data-stu-id="04cd9-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="04cd9-224">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="04cd9-225">单击“完工入库”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="04cd9-226">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="04cd9-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="04cd9-227">在“接受错误”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="04cd9-228">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="04cd9-229">在“操作窗格”中，单击“仓库”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="04cd9-230">单击“工作详细信息”。</span><span class="sxs-lookup"><span data-stu-id="04cd9-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="04cd9-231">在生产订单报告为完工入库时，尚未为储存生成工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="04cd9-232">发生这种情况是因为将工作策略定义为在产品 L0101 报告为已完工入库到库位 001 时阻止生成工作。</span><span class="sxs-lookup"><span data-stu-id="04cd9-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



