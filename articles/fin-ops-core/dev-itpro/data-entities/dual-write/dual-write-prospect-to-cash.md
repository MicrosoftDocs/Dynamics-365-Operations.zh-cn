---
title: 双写入中的目标客户到现金
description: 此主题提供有关双写入中的目标客户到现金的信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 12a0e07d1c60a359b3ba6c0d20176927ffe89431
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172800"
---
# <a name="prospect-to-cash-in-dual-write"></a><span data-ttu-id="1e394-103">双写入中的目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="1e394-103">Prospect-to-cash in dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1e394-104">大多数业务的一个重要目标是将目标客户转换为客户，然后维护与这些客户之间的当前业务关系。</span><span class="sxs-lookup"><span data-stu-id="1e394-104">An important goal of most businesses is to convert prospects to customers and then maintain an ongoing business relationship with those customers.</span></span> <span data-ttu-id="1e394-105">在 Microsoft Dynamics 365 应用中，通过报价或订单处理工作流进行目标客户到现金流程，并核对和确认财务。</span><span class="sxs-lookup"><span data-stu-id="1e394-105">In Microsoft Dynamics 365 apps, the prospect-to-cash process occurs through quotations or order processing workflows, and the financials are reconciled and recognized.</span></span> <span data-ttu-id="1e394-106">将目标客户到现金与双写入集成将创建一个工作流，该工作流采用源自 Dynamics 365 Sales 或 Dynamics 365 Supply Chain Management 的报价单和订单，并使该报价单和订单在这两个应用中可用。</span><span class="sxs-lookup"><span data-stu-id="1e394-106">Integration of prospect-to-cash with dual-write creates a workflow that takes a quotation and an order that originate in either Dynamics 365 Sales or Dynamics 365 Supply Chain Management, and makes the quotation and order available in both apps.</span></span>

<span data-ttu-id="1e394-107">在这些应用界面中，可以实时访问处理状态和发票信息。</span><span class="sxs-lookup"><span data-stu-id="1e394-107">In the app interfaces, you can access the processing statuses and invoice information in real time.</span></span> <span data-ttu-id="1e394-108">因此，可以在 Supply Chain Management 中更轻松地管理产品库存、库存处理和履行等功能，不必重新创建报价单和订单。</span><span class="sxs-lookup"><span data-stu-id="1e394-108">Therefore, you can more easily manage functions such as product stocking, inventory handling, and fulfillment in Supply Chain Management, without having to re-create the quotations and orders.</span></span>

![目标客户到现金中的双写入数据流](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1e394-110">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="1e394-110">Prerequisites and mapping setup</span></span>

<span data-ttu-id="1e394-111">必须先更新以下设置，然后才能同步销售报价单。</span><span class="sxs-lookup"><span data-stu-id="1e394-111">Before you can sync sales quotations, you must update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="1e394-112">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="1e394-112">Setup in Sales</span></span>

<span data-ttu-id="1e394-113">在 Sales 中，转到**设置 \> 管理 \> 系统设置 \> Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="1e394-113">In Sales, go to **Settings \> Administration \> System settings \> Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="1e394-114">**使用系统定价计算**系统选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="1e394-114">The **Use system prizing calculation** system option is set to **Yes**.</span></span>
- <span data-ttu-id="1e394-115">**折扣计算方法**字段设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="1e394-115">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="sites-and-warehouses"></a><span data-ttu-id="1e394-116">站点和仓库</span><span class="sxs-lookup"><span data-stu-id="1e394-116">Sites and warehouses</span></span>

<span data-ttu-id="1e394-117">在 Supply Chain Management 中，**站点**和**仓库**字段是报价单行和订单行的必填字段。</span><span class="sxs-lookup"><span data-stu-id="1e394-117">In Supply Chain Management, the **Site** and **warehouse** fields are required for quotation lines and order lines.</span></span> <span data-ttu-id="1e394-118">如果设置默认订单设置中的站点和仓库，向报价单行或订单行添加产品时，将自动设置这些字段。</span><span class="sxs-lookup"><span data-stu-id="1e394-118">If you set the site and warehouse in the default order settings, those fields will automatically be set when you add a product to a quotation line or an order line.</span></span> 

### <a name="number-sequences-for-quotations-and-orders"></a><span data-ttu-id="1e394-119">报价单和订单的编号规则</span><span class="sxs-lookup"><span data-stu-id="1e394-119">Number sequences for quotations and orders</span></span>

<span data-ttu-id="1e394-120">在 Sales 和 Supply Chain Management 中创建和同步报价单和订单时，不会连接 Supply Chain Management 和 Sales 的编号规则。</span><span class="sxs-lookup"><span data-stu-id="1e394-120">The number sequences for Supply Chain Management and Sales aren't connected when quotations and orders are created and synced in Sales and Supply Chain Management.</span></span> <span data-ttu-id="1e394-121">如果 Sales 中创建的销售订单同步到 Supply Chain Management，则其在, Supply Chain Management 中具有相同的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="1e394-121">If a sales order that is created in Sales is synced to Supply Chain Management, it has the same sales order number in Supply Chain Management.</span></span> <span data-ttu-id="1e394-122">若要帮助确保销售订单编号不重复，必须在这两个应用中使用不同编号规则系统。</span><span class="sxs-lookup"><span data-stu-id="1e394-122">To help ensure that the sales order number isn't duplicated, you must use different number sequence systems in the two apps.</span></span>

<span data-ttu-id="1e394-123">例如，Supply Chain Management 中的编号规则为 **1, 2, 3, 4, 5, ...**，而 Sales 中的编号规则为 **100, 99, 98, ...**。如果在 Sales 中创建 100 个销售订单，则最终生成的一个订单编号已经在 Supply Chain Management 中存在。</span><span class="sxs-lookup"><span data-stu-id="1e394-123">For example, the number sequence in Supply Chain Management is **1, 2, 3, 4, 5, ...**, and the number sequence in Sales is **100, 99, 98, ...**. If you create 100 sales orders in Sales, an order number will eventually be generated that already exists in Supply Chain Management.</span></span> <span data-ttu-id="1e394-124">换句话说，因为在 Supply Chain Management 和 Sales 中创建销售订单，所以这两个编号规则最终将重合。</span><span class="sxs-lookup"><span data-stu-id="1e394-124">In other words, the two number sequences will eventually overlap as sales orders are created in Supply Chain Management and Sales.</span></span> <span data-ttu-id="1e394-125">不过，可以在 Supply Chain Management 中使用 **F1, F2, F3, ...** 这样的编号规则，在 Sales 中则使用 **C1, C2, C3, ...** 这样的编号规则。</span><span class="sxs-lookup"><span data-stu-id="1e394-125">Instead, you might use a number sequence such as **F1, F2, F3, ...** in Supply Chain Management and a number sequence such as **C1, C2, C3, ...** in Sales.</span></span> <span data-ttu-id="1e394-126">这些编号规则始终不会生成重复的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="1e394-126">These number sequences will never produce duplicate sales order numbers.</span></span>

## <a name="sales-quotations"></a><span data-ttu-id="1e394-127">销售报价单</span><span class="sxs-lookup"><span data-stu-id="1e394-127">Sales quotations</span></span>

<span data-ttu-id="1e394-128">销售报价单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。</span><span class="sxs-lookup"><span data-stu-id="1e394-128">Sales quotations can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="1e394-129">如果在 Sales 中创建报价单，其将实时同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="1e394-129">If you create a quotation in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="1e394-130">同样，如果在 Supply Chain Management 中创建报价单，其将实时同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="1e394-130">Likewise, if you create a quotation in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="1e394-131">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="1e394-131">Note the following points:</span></span>

+ <span data-ttu-id="1e394-132">可以向报价单中的产品添加折扣。</span><span class="sxs-lookup"><span data-stu-id="1e394-132">You can add a discount to the product on the quotation.</span></span> <span data-ttu-id="1e394-133">在此情况下，折扣将同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="1e394-133">In this case, the discount will be synced to Supply Chain Management.</span></span> <span data-ttu-id="1e394-134">标题上的**折扣**、**费用**和**税金**字段由 Supply Chain Management 中的设置控制。</span><span class="sxs-lookup"><span data-stu-id="1e394-134">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="1e394-135">此设置不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="1e394-135">This setup doesn't support integration mapping.</span></span> <span data-ttu-id="1e394-136">**价格**、**折扣**、**费用**和**税金**字段在 Supply Chain Management 中维护和处理。</span><span class="sxs-lookup"><span data-stu-id="1e394-136">Instead, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Supply Chain Management.</span></span>
+ <span data-ttu-id="1e394-137">销售报价单标题上的**折扣 %**、**折扣**和**运费**字段为只读字段。</span><span class="sxs-lookup"><span data-stu-id="1e394-137">The **Discount %**, **Discount**, and **Freight Amount** fields on the sales quotation header are read-only fields.</span></span>
+ <span data-ttu-id="1e394-138">**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="1e394-138">The **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="1e394-139">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="1e394-139">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synced between.</span></span>

## <a name="sales-orders"></a><span data-ttu-id="1e394-140">销售订单</span><span class="sxs-lookup"><span data-stu-id="1e394-140">Sales orders</span></span>

<span data-ttu-id="1e394-141">销售订单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。</span><span class="sxs-lookup"><span data-stu-id="1e394-141">Sales orders can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="1e394-142">如果在 Sales 中创建销售订单，其将实时同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="1e394-142">If you create a sales order in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="1e394-143">同样，如果在 Supply Chain Management 中创建销售订单，其将实时同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="1e394-143">Likewise, if you create a sales order in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="1e394-144">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="1e394-144">Note the following points:</span></span>

+ <span data-ttu-id="1e394-145">仅当订单中的所有产品都来自 Finance and Operations 应用时，才能从 Sales 激活和同步订单。</span><span class="sxs-lookup"><span data-stu-id="1e394-145">You can activate and sync orders from Sales only if all the products on the order come from Finance and Operations apps.</span></span> <span data-ttu-id="1e394-146">因此，可能没有目录外产品。</span><span class="sxs-lookup"><span data-stu-id="1e394-146">Therefore, there can be no write-in products.</span></span>
+ <span data-ttu-id="1e394-147">折扣计算和化整：</span><span class="sxs-lookup"><span data-stu-id="1e394-147">Discount calculation and rounding:</span></span>

    - <span data-ttu-id="1e394-148">Sales 中的折扣计算模型不同于 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="1e394-148">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="1e394-149">在 Supply Chain Management 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。</span><span class="sxs-lookup"><span data-stu-id="1e394-149">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="1e394-150">如果此最终折扣金额除以行中的数量，可能发生化整。</span><span class="sxs-lookup"><span data-stu-id="1e394-150">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="1e394-151">不过，如果化整的每单位折扣金额同步到 Sales，则不考虑此化整。</span><span class="sxs-lookup"><span data-stu-id="1e394-151">However, this rounding isn't considered if a rounded per-unit discount amount is synced to Sales.</span></span> <span data-ttu-id="1e394-152">为了帮助确保 Supply Chain Management 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。</span><span class="sxs-lookup"><span data-stu-id="1e394-152">To help ensure that the full discount amount from a sales line in Supply Chain Management is correctly synced to Sales, the full amount must be synced without being divided by the line quantity.</span></span> <span data-ttu-id="1e394-153">因此，您必须在 Sales 中将折扣计算方法定义为**行项**。</span><span class="sxs-lookup"><span data-stu-id="1e394-153">Therefore, you must define the discount calculation method as **Line item** in Sales.</span></span>
    - <span data-ttu-id="1e394-154">在销售订单行从 Sales 同步到 Supply Chain Management 时，将使用完整行折扣金额。</span><span class="sxs-lookup"><span data-stu-id="1e394-154">When a sales order line is synced from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="1e394-155">因为 Supply Chain Management 没有能够存储完整折扣金额的字段，此金额除以数量，并存储在**行折扣**字段中。</span><span class="sxs-lookup"><span data-stu-id="1e394-155">Because Supply Chain Management has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="1e394-156">在此除法计算期间发生的任何舍入都将存储在销售行的**销售费用**字段中。</span><span class="sxs-lookup"><span data-stu-id="1e394-156">Any rounding that occurs during this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a><span data-ttu-id="1e394-157">示例：从 Sales 同步到 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1e394-157">Example: Synchronization from Sales to Supply Chain Management</span></span>

<span data-ttu-id="1e394-158">您有以下销售订单：</span><span class="sxs-lookup"><span data-stu-id="1e394-158">You have the following sales order:</span></span>

+ <span data-ttu-id="1e394-159">**Sales：** 数量 = 3，每行折扣 = 10.00 美元</span><span class="sxs-lookup"><span data-stu-id="1e394-159">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
+ <span data-ttu-id="1e394-160">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01</span><span class="sxs-lookup"><span data-stu-id="1e394-160">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>

<span data-ttu-id="1e394-161">如果从 Supply Chain Management 同步到 Sales，则结果如下：</span><span class="sxs-lookup"><span data-stu-id="1e394-161">If you sync from Supply Chain Management to Sales, you get the following result:</span></span>

+ <span data-ttu-id="1e394-162">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01</span><span class="sxs-lookup"><span data-stu-id="1e394-162">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>
+ <span data-ttu-id="1e394-163">**Sales：** 数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00</span><span class="sxs-lookup"><span data-stu-id="1e394-163">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="dual-write-solution-for-sales"></a><span data-ttu-id="1e394-164">适用于 Sales 的双写入解决方案</span><span class="sxs-lookup"><span data-stu-id="1e394-164">Dual-write solution for Sales</span></span>

<span data-ttu-id="1e394-165">新字段已添加到**订单**实体并显示在以下页面。</span><span class="sxs-lookup"><span data-stu-id="1e394-165">New fields have been added to the **Order** entity and appear on the page.</span></span> <span data-ttu-id="1e394-166">这些字段中的大多数都在 Sales 中的**集成**选项卡内显示。</span><span class="sxs-lookup"><span data-stu-id="1e394-166">Most of these fields appear on the **Integration** tab in Sales.</span></span> <span data-ttu-id="1e394-167">有一些特殊字段：</span><span class="sxs-lookup"><span data-stu-id="1e394-167">There are a few special fields:</span></span>

+ <span data-ttu-id="1e394-168">**处理状态**字段显示订单在 Supply Chain Management 中的处理状态。</span><span class="sxs-lookup"><span data-stu-id="1e394-168">The **Processing status** field shows the processing status of the order in Supply Chain Management.</span></span> <span data-ttu-id="1e394-169">此字段已锁定，并且仅显示来自 Supply Chain Management 的订单的状态。</span><span class="sxs-lookup"><span data-stu-id="1e394-169">This field is locked and shows only the status of the order from Supply Chain Management.</span></span> <span data-ttu-id="1e394-170">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="1e394-170">The following values are available:</span></span>

    + <span data-ttu-id="1e394-171">**活动** – 通过使用**激活**按钮在 Sales 中激活订单后的状态。</span><span class="sxs-lookup"><span data-stu-id="1e394-171">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    + <span data-ttu-id="1e394-172">**已确认**</span><span class="sxs-lookup"><span data-stu-id="1e394-172">**Confirmed**</span></span>
    + <span data-ttu-id="1e394-173">**已交货**</span><span class="sxs-lookup"><span data-stu-id="1e394-173">**Delivered**</span></span>
    + <span data-ttu-id="1e394-174">**已开票**</span><span class="sxs-lookup"><span data-stu-id="1e394-174">**Invoiced**</span></span>
    + <span data-ttu-id="1e394-175">**已部分交货**</span><span class="sxs-lookup"><span data-stu-id="1e394-175">**Partially Delivered**</span></span>
    + <span data-ttu-id="1e394-176">**已部分开票**</span><span class="sxs-lookup"><span data-stu-id="1e394-176">**Partially Invoiced**</span></span>
    + <span data-ttu-id="1e394-177">**已领料**</span><span class="sxs-lookup"><span data-stu-id="1e394-177">**Picked**</span></span>
    + <span data-ttu-id="1e394-178">**已取消**</span><span class="sxs-lookup"><span data-stu-id="1e394-178">**Canceled**</span></span>

    <span data-ttu-id="1e394-179">下表显示如何将处理状态映射到 **CRM 状态代码**值。</span><span class="sxs-lookup"><span data-stu-id="1e394-179">The following table shows how the processing status is mapped to the **CRM status code** value.</span></span>

    | <span data-ttu-id="1e394-180">处理状态</span><span class="sxs-lookup"><span data-stu-id="1e394-180">Processing status</span></span>           | <span data-ttu-id="1e394-181">CRM 状态代码</span><span class="sxs-lookup"><span data-stu-id="1e394-181">CRM status code</span></span>    |
    |-----------------------------|--------------------|
    | <span data-ttu-id="1e394-182">活动</span><span class="sxs-lookup"><span data-stu-id="1e394-182">Active</span></span>                      | <span data-ttu-id="1e394-183">新/待定/暂停</span><span class="sxs-lookup"><span data-stu-id="1e394-183">New/Pending/Onhold</span></span> |
    | <span data-ttu-id="1e394-184">已确认/已取货</span><span class="sxs-lookup"><span data-stu-id="1e394-184">Confirmed/Picked</span></span>            | <span data-ttu-id="1e394-185">在进行中</span><span class="sxs-lookup"><span data-stu-id="1e394-185">In Progress</span></span>        |
    | <span data-ttu-id="1e394-186">已部分交货</span><span class="sxs-lookup"><span data-stu-id="1e394-186">Partially Delivered</span></span>         | <span data-ttu-id="1e394-187">部分</span><span class="sxs-lookup"><span data-stu-id="1e394-187">Partial</span></span>            |
    | <span data-ttu-id="1e394-188">已交货</span><span class="sxs-lookup"><span data-stu-id="1e394-188">Delivered</span></span>                   | <span data-ttu-id="1e394-189">已完成</span><span class="sxs-lookup"><span data-stu-id="1e394-189">Complete</span></span>           |
    | <span data-ttu-id="1e394-190">已开票/已部分开票</span><span class="sxs-lookup"><span data-stu-id="1e394-190">Invoiced/Partially Invoiced</span></span> | <span data-ttu-id="1e394-191">已开票</span><span class="sxs-lookup"><span data-stu-id="1e394-191">Invoiced</span></span>           |
    | <span data-ttu-id="1e394-192">已取消</span><span class="sxs-lookup"><span data-stu-id="1e394-192">Canceled</span></span>                    | <span data-ttu-id="1e394-193">无钱</span><span class="sxs-lookup"><span data-stu-id="1e394-193">No Money</span></span>           |

+ <span data-ttu-id="1e394-194">**销售订单**页中的**创建发票**和**取消订单**按钮在 Sales 中已隐藏。</span><span class="sxs-lookup"><span data-stu-id="1e394-194">The **Create Invoice** and **Cancel Order** buttons on the **Sales order** page are hidden in Sales.</span></span>
+ <span data-ttu-id="1e394-195">**销售订单状态**值将保持**活动**状态，以帮助确保来自 Supply Chain Management 的更改可以流向 Sales 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="1e394-195">The **Sales order status** value will remain **Active** to help ensure that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="1e394-196">若要控制此行为，请将默认的**状态代码 \[Status\]** 值设置为**活动**。</span><span class="sxs-lookup"><span data-stu-id="1e394-196">To control this behavior, set the default **Statecode \[Status\]** value to **Active**.</span></span>

## <a name="invoices"></a><span data-ttu-id="1e394-197">发票</span><span class="sxs-lookup"><span data-stu-id="1e394-197">Invoices</span></span>

<span data-ttu-id="1e394-198">销售发票在 Supply Chain Management 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="1e394-198">Sales invoices are created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="1e394-199">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="1e394-199">Note the following points:</span></span>

+ <span data-ttu-id="1e394-200">**发票编号**字段已添加到**发票**实体中并显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="1e394-200">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
+ <span data-ttu-id="1e394-201">**销售订单**页上的**创建发票**按钮被隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="1e394-201">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="1e394-202">**发票**页不可编辑，因为发票将从 Supply Chain Management 同步。</span><span class="sxs-lookup"><span data-stu-id="1e394-202">The **Invoice** page can't be edited, because invoices will be synced from Supply Chain Management.</span></span>
+ <span data-ttu-id="1e394-203">当关联的发票从 Supply Chain Management 同步到 Sales 后，**销售订单状态**值自动更改为**已开票**。</span><span class="sxs-lookup"><span data-stu-id="1e394-203">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synced to Sales.</span></span> <span data-ttu-id="1e394-204">而且，创建发票的销售订单的所有者被指定为发票的所有者。</span><span class="sxs-lookup"><span data-stu-id="1e394-204">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="1e394-205">因此，销售订单的所有者可以查看发票。</span><span class="sxs-lookup"><span data-stu-id="1e394-205">Therefore, the owner of the sales order can view the invoice.</span></span>
+ <span data-ttu-id="1e394-206">**货运条款**、**交货条款**和**交货方式**字段不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="1e394-206">The **Freight terms**, **Delivery terms**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="1e394-207">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="1e394-207">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synced between.</span></span>

## <a name="templates"></a><span data-ttu-id="1e394-208">模板</span><span class="sxs-lookup"><span data-stu-id="1e394-208">Templates</span></span>

<span data-ttu-id="1e394-209">目标客户到现金中包括核心实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="1e394-209">Prospect-to-cash includes a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="1e394-210">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="1e394-210">Finance and Operations apps</span></span> | <span data-ttu-id="1e394-211">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="1e394-211">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="1e394-212">说明</span><span class="sxs-lookup"><span data-stu-id="1e394-212">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="1e394-213">销售发票抬头 V2</span><span class="sxs-lookup"><span data-stu-id="1e394-213">Sales invoice headers V2</span></span>    | <span data-ttu-id="1e394-214">发票</span><span class="sxs-lookup"><span data-stu-id="1e394-214">invoices</span></span>                          |             |
| <span data-ttu-id="1e394-215">销售发票行 V2</span><span class="sxs-lookup"><span data-stu-id="1e394-215">Sales invoice lines V2</span></span>      | <span data-ttu-id="1e394-216">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="1e394-216">invoicedetails</span></span>                    |             |
| <span data-ttu-id="1e394-217">CDS 销售订单标题</span><span class="sxs-lookup"><span data-stu-id="1e394-217">CDS sales order headers</span></span>     | <span data-ttu-id="1e394-218">salesorders</span><span class="sxs-lookup"><span data-stu-id="1e394-218">salesorders</span></span>                       |             |
| <span data-ttu-id="1e394-219">CDS 销售订单行</span><span class="sxs-lookup"><span data-stu-id="1e394-219">CDS sales order lines</span></span>       | <span data-ttu-id="1e394-220">salesorderdetails</span><span class="sxs-lookup"><span data-stu-id="1e394-220">salesorderdetails</span></span>                 |             |
| <span data-ttu-id="1e394-221">销售订单来源代码</span><span class="sxs-lookup"><span data-stu-id="1e394-221">Sales order origin codes</span></span>    | <span data-ttu-id="1e394-222">msdyn\_salesorderorigins</span><span class="sxs-lookup"><span data-stu-id="1e394-222">msdyn\_salesorderorigins</span></span>          |             |
| <span data-ttu-id="1e394-223">CDS 销售报价单标题</span><span class="sxs-lookup"><span data-stu-id="1e394-223">CDS sales quotation header</span></span>  | <span data-ttu-id="1e394-224">询价</span><span class="sxs-lookup"><span data-stu-id="1e394-224">quotes</span></span>                            |             |
| <span data-ttu-id="1e394-225">CDS 销售报价单行</span><span class="sxs-lookup"><span data-stu-id="1e394-225">CDS sales quotation lines</span></span>   | <span data-ttu-id="1e394-226">quotedetails</span><span class="sxs-lookup"><span data-stu-id="1e394-226">quotedetails</span></span>                      |             |

<span data-ttu-id="1e394-227">下面是目标客户到现金的相关核心实体映射：</span><span class="sxs-lookup"><span data-stu-id="1e394-227">Here are the related core entity maps for prospect-to-cash:</span></span>

+ [<span data-ttu-id="1e394-228">客户 V3 到帐户</span><span class="sxs-lookup"><span data-stu-id="1e394-228">Customers V3 to accounts</span></span>](customer-mapping.md#customers-v3-to-accounts)
+ [<span data-ttu-id="1e394-229">CDS 联系人 V2 到联系人</span><span class="sxs-lookup"><span data-stu-id="1e394-229">CDS Contacts V2 to contacts</span></span>](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [<span data-ttu-id="1e394-230">客户 V3 到联系人</span><span class="sxs-lookup"><span data-stu-id="1e394-230">Customers V3 to contacts</span></span>](customer-mapping.md#customers-v3-to-contacts)
+ [<span data-ttu-id="1e394-231">发放的产品 V2 到 msdyn_sharedproductdetails</span><span class="sxs-lookup"><span data-stu-id="1e394-231">Released products V2 to msdyn_sharedproductdetails</span></span>](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [<span data-ttu-id="1e394-232">所有产品到 msdyn_globalproducts</span><span class="sxs-lookup"><span data-stu-id="1e394-232">All products to msdyn_globalproducts</span></span>](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [<span data-ttu-id="1e394-233">价目表</span><span class="sxs-lookup"><span data-stu-id="1e394-233">Pricelist</span></span>](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
