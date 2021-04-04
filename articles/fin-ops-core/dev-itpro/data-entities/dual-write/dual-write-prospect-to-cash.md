---
title: 双写入中的目标客户到现金
description: 此主题提供有关双写入中的目标客户到现金的信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 134aeb58db86486195019b4ae6bbbf549542cc07
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561244"
---
# <a name="prospect-to-cash-in-dual-write"></a><span data-ttu-id="6be27-103">双写入中的目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="6be27-103">Prospect-to-cash in dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6be27-104">大多数业务的一个重要目标是将目标客户转换为客户，然后维护与这些客户之间的当前业务关系。</span><span class="sxs-lookup"><span data-stu-id="6be27-104">An important goal of most businesses is to convert prospects to customers and then maintain an ongoing business relationship with those customers.</span></span> <span data-ttu-id="6be27-105">在 Microsoft Dynamics 365 应用中，通过报价或订单处理工作流进行目标客户到现金流程，并核对和确认财务。</span><span class="sxs-lookup"><span data-stu-id="6be27-105">In Microsoft Dynamics 365 apps, the prospect-to-cash process occurs through quotations or order processing workflows, and the financials are reconciled and recognized.</span></span> <span data-ttu-id="6be27-106">将目标客户到现金与双写入集成将创建一个工作流，该工作流采用源自 Dynamics 365 Sales 或 Dynamics 365 Supply Chain Management 的报价单和订单，并使该报价单和订单在这两个应用中可用。</span><span class="sxs-lookup"><span data-stu-id="6be27-106">Integration of prospect-to-cash with dual-write creates a workflow that takes a quotation and an order that originate in either Dynamics 365 Sales or Dynamics 365 Supply Chain Management, and makes the quotation and order available in both apps.</span></span>

<span data-ttu-id="6be27-107">在这些应用界面中，可以实时访问处理状态和发票信息。</span><span class="sxs-lookup"><span data-stu-id="6be27-107">In the app interfaces, you can access the processing statuses and invoice information in real time.</span></span> <span data-ttu-id="6be27-108">因此，可以在 Supply Chain Management 中更轻松地管理产品库存、库存处理和履行等功能，不必重新创建报价单和订单。</span><span class="sxs-lookup"><span data-stu-id="6be27-108">Therefore, you can more easily manage functions such as product stocking, inventory handling, and fulfillment in Supply Chain Management, without having to re-create the quotations and orders.</span></span>

![目标客户到现金中的双写入数据流](../dual-write/media/dual-write-prospect-to-cash[1].png)

<span data-ttu-id="6be27-110">有关客户和联系人集成的信息，请参阅[集成客户主数据](customer-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="6be27-110">For information about customer and contact integration, see [Integrated customer master](customer-mapping.md).</span></span> <span data-ttu-id="6be27-111">有关产品集成的信息，请参阅[统一的产品体验](product-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="6be27-111">For information about product integration, see [Unified product experience](product-mapping.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6be27-112">在 Dynamics 365 Sales 中，目标客户和客户都引用 **客户** 表中的记录，表中的 **RelationshipType** 列为 **目标客户** 或 **客户**。</span><span class="sxs-lookup"><span data-stu-id="6be27-112">In Dynamics 365 Sales, both prospect and customer refer to a record in the **Account** table where the **RelationshipType** column is either **Prospect** or **Customer**.</span></span> <span data-ttu-id="6be27-113">如果您的业务逻辑包括 **客户** 资格流程，流程中创建了 **客户** 记录，并首先作为目标客户授予其资格，然后作为客户，那么该记录仅在为客户 (`RelationshipType=Customer`) 时同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="6be27-113">If your business logic includes an **Account** qualification process where the **Account** record is created and qualified as a prospect first and then as a customer, that record synchronizes to the Finance and Operations app only when it is a customer (`RelationshipType=Customer`).</span></span> <span data-ttu-id="6be27-114">如果您希望 **客户** 行作为目标客户同步，那么您需要一个自定义映射来集成目标客户数据。</span><span class="sxs-lookup"><span data-stu-id="6be27-114">If you want the **Account** row to synchronize as a prospect, then you need a custom map to integrate the prospect data.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6be27-115">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="6be27-115">Prerequisites and mapping setup</span></span>

<span data-ttu-id="6be27-116">必须先更新以下设置，然后才能同步销售报价单。</span><span class="sxs-lookup"><span data-stu-id="6be27-116">Before you can sync sales quotations, you must update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6be27-117">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="6be27-117">Setup in Sales</span></span>

<span data-ttu-id="6be27-118">在 Sales 中，转到 **设置 \> 管理 \> 系统设置 \> Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="6be27-118">In Sales, go to **Settings \> Administration \> System settings \> Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="6be27-119">**使用系统定价计算** 系统选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6be27-119">The **Use system prizing calculation** system option is set to **Yes**.</span></span>
- <span data-ttu-id="6be27-120">**折扣计算方法** 列设置为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="6be27-120">The **Discount calculation method** column is set to **Line item**.</span></span>

### <a name="sites-and-warehouses"></a><span data-ttu-id="6be27-121">站点和仓库</span><span class="sxs-lookup"><span data-stu-id="6be27-121">Sites and warehouses</span></span>

<span data-ttu-id="6be27-122">在 Supply Chain Management 中，**站点** 和 **仓库** 列是报价单行和订单行的必需列。</span><span class="sxs-lookup"><span data-stu-id="6be27-122">In Supply Chain Management, the **Site** and **warehouse** columns are required for quotation lines and order lines.</span></span> <span data-ttu-id="6be27-123">如果设置默认订单设置中的站点和仓库，向报价单行或订单行添加产品时，将自动设置这些列。</span><span class="sxs-lookup"><span data-stu-id="6be27-123">If you set the site and warehouse in the default order settings, those columns will automatically be set when you add a product to a quotation line or an order line.</span></span> 

### <a name="number-sequences-for-quotations-and-orders"></a><span data-ttu-id="6be27-124">报价单和订单的编号规则</span><span class="sxs-lookup"><span data-stu-id="6be27-124">Number sequences for quotations and orders</span></span>

<span data-ttu-id="6be27-125">在 Sales 和 Supply Chain Management 中创建和同步报价单和订单时，不会连接 Supply Chain Management 和 Sales 的编号规则。</span><span class="sxs-lookup"><span data-stu-id="6be27-125">The number sequences for Supply Chain Management and Sales aren't connected when quotations and orders are created and synced in Sales and Supply Chain Management.</span></span> <span data-ttu-id="6be27-126">如果 Sales 中创建的销售订单同步到 Supply Chain Management，则其在, Supply Chain Management 中具有相同的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="6be27-126">If a sales order that is created in Sales is synced to Supply Chain Management, it has the same sales order number in Supply Chain Management.</span></span> <span data-ttu-id="6be27-127">若要帮助确保销售订单编号不重复，必须在这两个应用中使用不同编号规则系统。</span><span class="sxs-lookup"><span data-stu-id="6be27-127">To help ensure that the sales order number isn't duplicated, you must use different number sequence systems in the two apps.</span></span>

<span data-ttu-id="6be27-128">例如，Supply Chain Management 中的编号规则为 **1, 2, 3, 4, 5, ...**，而 Sales 中的编号规则为 **100, 99, 98, ...**。如果在 Sales 中创建 100 个销售订单，则最终生成的一个订单编号已经在 Supply Chain Management 中存在。</span><span class="sxs-lookup"><span data-stu-id="6be27-128">For example, the number sequence in Supply Chain Management is **1, 2, 3, 4, 5, ...**, and the number sequence in Sales is **100, 99, 98, ...**. If you create 100 sales orders in Sales, an order number will eventually be generated that already exists in Supply Chain Management.</span></span> <span data-ttu-id="6be27-129">换句话说，因为在 Supply Chain Management 和 Sales 中创建销售订单，所以这两个编号规则最终将重合。</span><span class="sxs-lookup"><span data-stu-id="6be27-129">In other words, the two number sequences will eventually overlap as sales orders are created in Supply Chain Management and Sales.</span></span> <span data-ttu-id="6be27-130">不过，可以在 Supply Chain Management 中使用 **F1, F2, F3, ...** 这样的编号规则，在 Sales 中则使用 **C1, C2, C3, ...** 这样的编号规则。</span><span class="sxs-lookup"><span data-stu-id="6be27-130">Instead, you might use a number sequence such as **F1, F2, F3, ...** in Supply Chain Management and a number sequence such as **C1, C2, C3, ...** in Sales.</span></span> <span data-ttu-id="6be27-131">这些编号规则始终不会生成重复的销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="6be27-131">These number sequences will never produce duplicate sales order numbers.</span></span>

## <a name="sales-quotations"></a><span data-ttu-id="6be27-132">销售报价单</span><span class="sxs-lookup"><span data-stu-id="6be27-132">Sales quotations</span></span>

<span data-ttu-id="6be27-133">销售报价单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。</span><span class="sxs-lookup"><span data-stu-id="6be27-133">Sales quotations can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="6be27-134">如果在 Sales 中创建报价单，其将实时同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="6be27-134">If you create a quotation in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="6be27-135">同样，如果在 Supply Chain Management 中创建报价单，其将实时同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6be27-135">Likewise, if you create a quotation in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="6be27-136">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="6be27-136">Note the following points:</span></span>

+ <span data-ttu-id="6be27-137">可以向报价单中的产品添加折扣。</span><span class="sxs-lookup"><span data-stu-id="6be27-137">You can add a discount to the product on the quotation.</span></span> <span data-ttu-id="6be27-138">在此情况下，折扣将同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="6be27-138">In this case, the discount will be synced to Supply Chain Management.</span></span> <span data-ttu-id="6be27-139">标题上的 **折扣**、**费用** 和 **税金** 列由 Supply Chain Management 中的设置控制。</span><span class="sxs-lookup"><span data-stu-id="6be27-139">The **Discount**, **Charges**, and **Tax** columns on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="6be27-140">此设置不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="6be27-140">This setup doesn't support integration mapping.</span></span> <span data-ttu-id="6be27-141">**价格**、**折扣**、**费用** 和 **税金** 列在 Supply Chain Management 中维护和处理。</span><span class="sxs-lookup"><span data-stu-id="6be27-141">Instead, the **Price**, **Discount**, **Charge**, and **Tax** columns are maintained and handled in Supply Chain Management.</span></span>
+ <span data-ttu-id="6be27-142">销售报价单标题上的 **折扣 %**、**折扣** 和 **运费** 列为只读列。</span><span class="sxs-lookup"><span data-stu-id="6be27-142">The **Discount %**, **Discount**, and **Freight Amount** columns on the sales quotation header are read-only columns.</span></span>
+ <span data-ttu-id="6be27-143">**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 列不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="6be27-143">The **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't part of the default mappings.</span></span> <span data-ttu-id="6be27-144">若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="6be27-144">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synced between.</span></span>

<span data-ttu-id="6be27-145">如果您还使用 Field Service 解决方案，请确保重新启用 **询价行快速创建** 参数。</span><span class="sxs-lookup"><span data-stu-id="6be27-145">If you are also using the Field Service solution, make sure to re-enable the **Quote Line Quick Create** parameter.</span></span> <span data-ttu-id="6be27-146">重新启用此参数可使您继续使用快速创建功能创建询价行。</span><span class="sxs-lookup"><span data-stu-id="6be27-146">Re-enabling the parameter lets you continue creating quote lines using the quick create function.</span></span>
1. <span data-ttu-id="6be27-147">导航到您的 Dynamics 365 Sales 应用程序。</span><span class="sxs-lookup"><span data-stu-id="6be27-147">Navigate to your Dynamics 365 Sales application.</span></span>
2. <span data-ttu-id="6be27-148">选择顶部导航栏中的设置图标。</span><span class="sxs-lookup"><span data-stu-id="6be27-148">Select the settings icon in the top navigation bar.</span></span>
3. <span data-ttu-id="6be27-149">选择 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="6be27-149">Select **Advanced Settings**.</span></span>
4. <span data-ttu-id="6be27-150">选择 **自定义系统** 选项。</span><span class="sxs-lookup"><span data-stu-id="6be27-150">Choose the **Customize the System** option.</span></span>
5. <span data-ttu-id="6be27-151">选择 **询价行** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="6be27-151">Select the **Quote Line** menu item.</span></span>
6. <span data-ttu-id="6be27-152">转到 **数据服务** 部分，然后选择 **允许快速创建** 复选框。</span><span class="sxs-lookup"><span data-stu-id="6be27-152">Go to the **Data Services** section and select the **Allow quick create** checkbox.</span></span>

## <a name="sales-orders"></a><span data-ttu-id="6be27-153">销售订单</span><span class="sxs-lookup"><span data-stu-id="6be27-153">Sales orders</span></span>

<span data-ttu-id="6be27-154">销售订单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。</span><span class="sxs-lookup"><span data-stu-id="6be27-154">Sales orders can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="6be27-155">如果在 Sales 中创建销售订单，其将实时同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="6be27-155">If you create a sales order in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="6be27-156">同样，如果在 Supply Chain Management 中创建销售订单，其将实时同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6be27-156">Likewise, if you create a sales order in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="6be27-157">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="6be27-157">Note the following points:</span></span>

+ <span data-ttu-id="6be27-158">Dynamics 365 Sales 中的目录外产品将在 Dynamics 365 Supply Chain Management 中显示为产品类别。</span><span class="sxs-lookup"><span data-stu-id="6be27-158">Write-in products on Dynamics 365 Sales will appear as product categories in Dynamics 365 Supply Chain Management.</span></span>
+ <span data-ttu-id="6be27-159">折扣计算和化整：</span><span class="sxs-lookup"><span data-stu-id="6be27-159">Discount calculation and rounding:</span></span>

    - <span data-ttu-id="6be27-160">Sales 中的折扣计算模型不同于 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="6be27-160">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="6be27-161">在 Supply Chain Management 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。</span><span class="sxs-lookup"><span data-stu-id="6be27-161">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="6be27-162">如果此最终折扣金额除以行中的数量，可能发生化整。</span><span class="sxs-lookup"><span data-stu-id="6be27-162">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="6be27-163">不过，如果化整的每单位折扣金额同步到 Sales，则不考虑此化整。</span><span class="sxs-lookup"><span data-stu-id="6be27-163">However, this rounding isn't considered if a rounded per-unit discount amount is synced to Sales.</span></span> <span data-ttu-id="6be27-164">为了帮助确保 Supply Chain Management 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。</span><span class="sxs-lookup"><span data-stu-id="6be27-164">To help ensure that the full discount amount from a sales line in Supply Chain Management is correctly synced to Sales, the full amount must be synced without being divided by the line quantity.</span></span> <span data-ttu-id="6be27-165">因此，您必须在 Sales 中将折扣计算方法定义为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="6be27-165">Therefore, you must define the discount calculation method as **Line item** in Sales.</span></span>
    - <span data-ttu-id="6be27-166">在销售订单行从 Sales 同步到 Supply Chain Management 时，将使用完整行折扣金额。</span><span class="sxs-lookup"><span data-stu-id="6be27-166">When a sales order line is synced from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="6be27-167">因为 Supply Chain Management 没有能够存储完整折扣金额的列，此金额除以数量，并存储在 **行折扣** 列中。</span><span class="sxs-lookup"><span data-stu-id="6be27-167">Because Supply Chain Management has no column that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** column.</span></span> <span data-ttu-id="6be27-168">在此除法计算期间发生的任何舍入都将存储在销售行的 **销售费用** 列中。</span><span class="sxs-lookup"><span data-stu-id="6be27-168">Any rounding that occurs during this division is stored in the **Sales charges** column on the sales line.</span></span>

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a><span data-ttu-id="6be27-169">示例：从 Sales 同步到 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6be27-169">Example: Synchronization from Sales to Supply Chain Management</span></span>

<span data-ttu-id="6be27-170">您有以下销售订单：</span><span class="sxs-lookup"><span data-stu-id="6be27-170">You have the following sales order:</span></span>

+ <span data-ttu-id="6be27-171">**Sales：** 数量 = 3，每行折扣 = 10.00 美元</span><span class="sxs-lookup"><span data-stu-id="6be27-171">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
+ <span data-ttu-id="6be27-172">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01</span><span class="sxs-lookup"><span data-stu-id="6be27-172">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>

<span data-ttu-id="6be27-173">如果从 Supply Chain Management 同步到 Sales，则结果如下：</span><span class="sxs-lookup"><span data-stu-id="6be27-173">If you sync from Supply Chain Management to Sales, you get the following result:</span></span>

+ <span data-ttu-id="6be27-174">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01</span><span class="sxs-lookup"><span data-stu-id="6be27-174">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>
+ <span data-ttu-id="6be27-175">**Sales：** 数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00</span><span class="sxs-lookup"><span data-stu-id="6be27-175">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="dual-write-solution-for-sales"></a><span data-ttu-id="6be27-176">适用于 Sales 的双写入解决方案</span><span class="sxs-lookup"><span data-stu-id="6be27-176">Dual-write solution for Sales</span></span>

<span data-ttu-id="6be27-177">新列已添加到 **订单** 表并显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="6be27-177">New columns have been added to the **Order** table and appear on the page.</span></span> <span data-ttu-id="6be27-178">这些列中的大多数都在 Sales 中的 **集成** 选项卡内显示。</span><span class="sxs-lookup"><span data-stu-id="6be27-178">Most of these columns appear on the **Integration** tab in Sales.</span></span> <span data-ttu-id="6be27-179">要了解有关如何映射状态列的详细信息，请参阅[设置销售订单状态列的映射](sales-status-map.md)。</span><span class="sxs-lookup"><span data-stu-id="6be27-179">To learn more about how the status columns are mapped, see [Set up the mapping for sales order status columns](sales-status-map.md).</span></span>

+ <span data-ttu-id="6be27-180">**销售订单** 页中的 **创建发票** 和 **取消订单** 按钮在 Sales 中已隐藏。</span><span class="sxs-lookup"><span data-stu-id="6be27-180">The **Create Invoice** and **Cancel Order** buttons on the **Sales order** page are hidden in Sales.</span></span>
+ <span data-ttu-id="6be27-181">**销售订单状态** 值将保持 **活动** 状态，以帮助确保来自 Supply Chain Management 的更改可以流向 Sales 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="6be27-181">The **Sales order status** value will remain **Active** to help ensure that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="6be27-182">若要控制此行为，请将默认的 **状态代码 \[Status\]** 值设置为 **活动**。</span><span class="sxs-lookup"><span data-stu-id="6be27-182">To control this behavior, set the default **Statecode \[Status\]** value to **Active**.</span></span>

## <a name="invoices"></a><span data-ttu-id="6be27-183">发票</span><span class="sxs-lookup"><span data-stu-id="6be27-183">Invoices</span></span>

<span data-ttu-id="6be27-184">销售发票在 Supply Chain Management 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6be27-184">Sales invoices are created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="6be27-185">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="6be27-185">Note the following points:</span></span>

+ <span data-ttu-id="6be27-186">**发票编号** 列已添加到 **发票** 表中并显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="6be27-186">An **Invoice number** column has been added to the **Invoice** table and appears on the page.</span></span>
+ <span data-ttu-id="6be27-187">**销售订单** 页上的 **创建发票** 按钮被隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6be27-187">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="6be27-188">**发票** 页不可编辑，因为发票将从 Supply Chain Management 同步。</span><span class="sxs-lookup"><span data-stu-id="6be27-188">The **Invoice** page can't be edited, because invoices will be synced from Supply Chain Management.</span></span>
+ <span data-ttu-id="6be27-189">当关联的发票从 Supply Chain Management 同步到 Sales 后，**销售订单状态** 值自动更改为 **已开票**。</span><span class="sxs-lookup"><span data-stu-id="6be27-189">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synced to Sales.</span></span> <span data-ttu-id="6be27-190">而且，创建发票的销售订单的所有者被指定为发票的所有者。</span><span class="sxs-lookup"><span data-stu-id="6be27-190">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="6be27-191">因此，销售订单的所有者可以查看发票。</span><span class="sxs-lookup"><span data-stu-id="6be27-191">Therefore, the owner of the sales order can view the invoice.</span></span>
+ <span data-ttu-id="6be27-192">**货运条款**、**交货条款** 和 **交货方式** 列不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="6be27-192">The **Freight terms**, **Delivery terms**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="6be27-193">若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="6be27-193">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synced between.</span></span>

## <a name="templates"></a><span data-ttu-id="6be27-194">模板</span><span class="sxs-lookup"><span data-stu-id="6be27-194">Templates</span></span>

<span data-ttu-id="6be27-195">目标客户到现金中包括核心表映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="6be27-195">Prospect-to-cash includes a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="6be27-196">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="6be27-196">Finance and Operations apps</span></span> | <span data-ttu-id="6be27-197">客户互动应用</span><span class="sxs-lookup"><span data-stu-id="6be27-197">Customer engagement apps</span></span> | <span data-ttu-id="6be27-198">说明</span><span class="sxs-lookup"><span data-stu-id="6be27-198">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="6be27-199">销售账单抬头 V2</span><span class="sxs-lookup"><span data-stu-id="6be27-199">Sales invoice headers V2</span></span>    | <span data-ttu-id="6be27-200">发票</span><span class="sxs-lookup"><span data-stu-id="6be27-200">invoices</span></span>                          | <span data-ttu-id="6be27-201">Finance and Operations 应用中的“销售发票抬头 V2”表包含销售订单的发票和普通发票。</span><span class="sxs-lookup"><span data-stu-id="6be27-201">The Sales invoice headers V2 table in the Finance and Operations app contains invoices for sales orders and free text invoices.</span></span> <span data-ttu-id="6be27-202">Dataverse 中为双写入应用了筛选器，将筛选出所有普通发票单据。</span><span class="sxs-lookup"><span data-stu-id="6be27-202">A filter is applied in Dataverse for dual-write that will filter out any free text invoice documents.</span></span> |
| <span data-ttu-id="6be27-203">销售账单行 V2</span><span class="sxs-lookup"><span data-stu-id="6be27-203">Sales invoice lines V2</span></span>      | <span data-ttu-id="6be27-204">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="6be27-204">invoicedetails</span></span>                    |             |
| <span data-ttu-id="6be27-205">CDS 销售订单标题</span><span class="sxs-lookup"><span data-stu-id="6be27-205">CDS sales order headers</span></span>     | <span data-ttu-id="6be27-206">salesorders</span><span class="sxs-lookup"><span data-stu-id="6be27-206">salesorders</span></span>                       |             |
| <span data-ttu-id="6be27-207">CDS 销售订单行</span><span class="sxs-lookup"><span data-stu-id="6be27-207">CDS sales order lines</span></span>       | <span data-ttu-id="6be27-208">salesorderdetails</span><span class="sxs-lookup"><span data-stu-id="6be27-208">salesorderdetails</span></span>                 |             |
| <span data-ttu-id="6be27-209">销售订单来源代码</span><span class="sxs-lookup"><span data-stu-id="6be27-209">Sales order origin codes</span></span>    | <span data-ttu-id="6be27-210">msdyn\_salesorderorigins</span><span class="sxs-lookup"><span data-stu-id="6be27-210">msdyn\_salesorderorigins</span></span>          |             |
| <span data-ttu-id="6be27-211">CDS 销售报价单标题</span><span class="sxs-lookup"><span data-stu-id="6be27-211">CDS sales quotation header</span></span>  | <span data-ttu-id="6be27-212">询价</span><span class="sxs-lookup"><span data-stu-id="6be27-212">quotes</span></span>                            |             |
| <span data-ttu-id="6be27-213">CDS 销售报价行</span><span class="sxs-lookup"><span data-stu-id="6be27-213">CDS sales quotation lines</span></span>   | <span data-ttu-id="6be27-214">quotedetails</span><span class="sxs-lookup"><span data-stu-id="6be27-214">quotedetails</span></span>                      |             |

<span data-ttu-id="6be27-215">下面是目标客户到现金的相关核心表映射：</span><span class="sxs-lookup"><span data-stu-id="6be27-215">Here are the related core table maps for prospect-to-cash:</span></span>

+ [<span data-ttu-id="6be27-216">客户 V3 到帐户</span><span class="sxs-lookup"><span data-stu-id="6be27-216">Customers V3 to accounts</span></span>](customer-mapping.md#customers-v3-to-accounts)
+ [<span data-ttu-id="6be27-217">CDS 联系人 V2 到联系人</span><span class="sxs-lookup"><span data-stu-id="6be27-217">CDS Contacts V2 to contacts</span></span>](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [<span data-ttu-id="6be27-218">客户 V3 到联系人</span><span class="sxs-lookup"><span data-stu-id="6be27-218">Customers V3 to contacts</span></span>](customer-mapping.md#customers-v3-to-contacts)
+ [<span data-ttu-id="6be27-219">发放的产品 V2 到 msdyn_sharedproductdetails</span><span class="sxs-lookup"><span data-stu-id="6be27-219">Released products V2 to msdyn_sharedproductdetails</span></span>](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [<span data-ttu-id="6be27-220">所有产品到 msdyn_globalproducts</span><span class="sxs-lookup"><span data-stu-id="6be27-220">All products to msdyn_globalproducts</span></span>](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [<span data-ttu-id="6be27-221">价目表</span><span class="sxs-lookup"><span data-stu-id="6be27-221">Pricelist</span></span>](product-mapping.md)

## <a name="limitations"></a><span data-ttu-id="6be27-222">限制</span><span class="sxs-lookup"><span data-stu-id="6be27-222">Limitations</span></span>
- <span data-ttu-id="6be27-223">不支持退货单。</span><span class="sxs-lookup"><span data-stu-id="6be27-223">Return orders are not supported.</span></span>
- <span data-ttu-id="6be27-224">不支持贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="6be27-224">Credit notes are not supported.</span></span>
- <span data-ttu-id="6be27-225">必须为主数据（例如，客户和供应商）设置财务维度。</span><span class="sxs-lookup"><span data-stu-id="6be27-225">Financial dimensions must be set for the master data, for example, customer and vendor.</span></span> <span data-ttu-id="6be27-226">将客户被添加到报价单或销售订单后，与客户记录关联的财务维度会自动流向订单。</span><span class="sxs-lookup"><span data-stu-id="6be27-226">When a customer is added to a quotation or sales order, the financial dimensions associated with the customer record flow to the order automatically.</span></span> <span data-ttu-id="6be27-227">当前，双写入不包括主数据的财务维度数据。</span><span class="sxs-lookup"><span data-stu-id="6be27-227">Currently dual-write does not include financial dimensions data for master data.</span></span> 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]