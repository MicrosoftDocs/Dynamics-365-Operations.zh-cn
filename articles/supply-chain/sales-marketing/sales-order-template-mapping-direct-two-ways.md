---
title: 直接在 Sales 和 Supply Chain Management 之间同步销售订单
description: 本主题讨论用于在 Dynamics 365 Sales 与 Dynamics 365 Supply Chain Management 之间直接运行销售订单同步的模板和基础任务。
author: ChristianRytt
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f0e26c63635179dc4c145f8d08e85fd110d9caac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817765"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a><span data-ttu-id="4dee8-103">直接在 Sales 和 Supply Chain Management 之间同步销售订单</span><span class="sxs-lookup"><span data-stu-id="4dee8-103">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4dee8-104">本主题讨论用于在 Dynamics 365 Sales 与 Dynamics 365 Supply Chain Management 之间直接运行销售订单同步的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="4dee8-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Dynamics 365 Sales and Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4dee8-105">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="4dee8-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4dee8-106">“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="4dee8-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="4dee8-107">提供“数据集成”功能的“从目标客户到现金”模板启用 Supply Chain Management 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="4dee8-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="4dee8-108">下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="4dee8-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="4dee8-109">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4dee8-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4dee8-110">模板和任务</span><span class="sxs-lookup"><span data-stu-id="4dee8-110">Templates and tasks</span></span>

<span data-ttu-id="4dee8-111">若要访问可用模板，打开 [Power Apps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="4dee8-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="4dee8-112">选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="4dee8-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4dee8-113">以下模板和基础任务用于在 Sales 与 Supply Chain Management 之间直接运行销售订单的同步。</span><span class="sxs-lookup"><span data-stu-id="4dee8-113">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Supply Chain Management.</span></span>

- <span data-ttu-id="4dee8-114">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="4dee8-114">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="4dee8-115">销售订单（Sales 到 Supply Chain Management）- 直接</span><span class="sxs-lookup"><span data-stu-id="4dee8-115">Sales Orders (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="4dee8-116">销售订单（Supply Chain Management 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="4dee8-116">Sales Orders (Supply Chain Management to Sales) - Direct</span></span>

- <span data-ttu-id="4dee8-117">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="4dee8-117">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4dee8-118">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="4dee8-118">OrderHeader</span></span>
    - <span data-ttu-id="4dee8-119">OrderLine</span><span class="sxs-lookup"><span data-stu-id="4dee8-119">OrderLine</span></span>

<span data-ttu-id="4dee8-120">在发生销售发票标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="4dee8-120">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="4dee8-121">产品（Supply Chain Management 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="4dee8-121">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="4dee8-122">科目（Sales 到 Supply Chain Management）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="4dee8-122">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="4dee8-123">从联系人到客户（Sales 到 Supply Chain Management）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="4dee8-123">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="4dee8-124">实体集</span><span class="sxs-lookup"><span data-stu-id="4dee8-124">Entity set</span></span>

| <span data-ttu-id="4dee8-125">供应链管理</span><span class="sxs-lookup"><span data-stu-id="4dee8-125">Supply Chain Management</span></span>  | <span data-ttu-id="4dee8-126">销售额</span><span class="sxs-lookup"><span data-stu-id="4dee8-126">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="4dee8-127">Dataverse 销售订单标头</span><span class="sxs-lookup"><span data-stu-id="4dee8-127">Dataverse sales order headers</span></span> | <span data-ttu-id="4dee8-128">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="4dee8-128">SalesOrders</span></span>       |
| <span data-ttu-id="4dee8-129">Dataverse 销售订单行</span><span class="sxs-lookup"><span data-stu-id="4dee8-129">Dataverse sales order lines</span></span>   | <span data-ttu-id="4dee8-130">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="4dee8-130">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="4dee8-131">实体流</span><span class="sxs-lookup"><span data-stu-id="4dee8-131">Entity flow</span></span>

<span data-ttu-id="4dee8-132">在为基于 **销售订单（Sales 到 Supply Chain Management）-直接** 模板的项目触发 **运行项目** 后，销售订单在 Sales 中创建，然后同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4dee8-132">Sales orders are created in Sales and synchronized to Supply Chain Management when **Run project** is triggered for a project based on the **Sales Orders (Sales to Supply Chain Management) - Direct** template.</span></span> <span data-ttu-id="4dee8-133">只有当所有 **订单产品** 全部是外部维护产品时，您才能够激活和同步来自 Sales 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-133">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="4dee8-134">因此，可能没有目录外产品。</span><span class="sxs-lookup"><span data-stu-id="4dee8-134">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="4dee8-135">在订单启用后，销售订单将在用户界面 (UI) 变为只读。</span><span class="sxs-lookup"><span data-stu-id="4dee8-135">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="4dee8-136">此时，从 Supply Chain Management 进行更新。</span><span class="sxs-lookup"><span data-stu-id="4dee8-136">At that point, the updates are made from Supply Chain Management.</span></span> <span data-ttu-id="4dee8-137">在销售订单具有状态 **已确认** 后，基于 **销售订单（Supply Chain Management 到 Sales）- 直接** 模板的项目可用于将 Supply Chain Management 的更新或履行状态全部同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-137">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Supply Chain Management to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Supply Chain Management to Sales.</span></span>

<span data-ttu-id="4dee8-138">您不必在 Sales 中创建订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-138">You don't have to create orders in Sales.</span></span> <span data-ttu-id="4dee8-139">而可以在 Supply Chain Management 中创建新销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-139">You can create new sales orders in Supply Chain Management instead.</span></span> <span data-ttu-id="4dee8-140">在销售订单具有状态 **已确认** 后，其将被同步到 Sales，如前面段落中所述。</span><span class="sxs-lookup"><span data-stu-id="4dee8-140">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="4dee8-141">在 Supply Chain Management 中，模板中的筛选器帮助确保同步中只包括相关销售订单：</span><span class="sxs-lookup"><span data-stu-id="4dee8-141">In Supply Chain Management, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="4dee8-142">在销售订单上，订购客户和开票客户都必须来自 Sales 以被包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="4dee8-142">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="4dee8-143">在 Supply Chain Management 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 列用于筛选来自数据表的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-143">In Supply Chain Management, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** columns are used to filter sales orders from the data tables.</span></span>
- <span data-ttu-id="4dee8-144">必须确认 Supply Chain Management 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-144">The sales order in Supply Chain Management must be confirmed.</span></span> <span data-ttu-id="4dee8-145">仅已确认的销售订单或具有更高处理状态（如 **已装运** 或 **已开票**）的销售订单同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-145">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="4dee8-146">在创建或修改销售订单后，必须运行 Supply Chain Management 中的 **计算销售额总计** 批处理作业。</span><span class="sxs-lookup"><span data-stu-id="4dee8-146">After a sales order is created or modified, the **Calculate sales totals** batch job in Supply Chain Management must be run.</span></span> <span data-ttu-id="4dee8-147">仅计算了销售总额的销售订单将被同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-147">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="4dee8-148">货运税</span><span class="sxs-lookup"><span data-stu-id="4dee8-148">Freight tax</span></span>

<span data-ttu-id="4dee8-149">因为税存储在行级别，因此 Sales 不在订单头级别支持税务信息。</span><span class="sxs-lookup"><span data-stu-id="4dee8-149">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="4dee8-150">为了在 Supply Chain Management 的订单头级别支持税务信息（如货运税），系统会将税作为名为 **货运税** 以及具有来自 Supply Chain Management 的税额的目录外产品同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-150">To support tax at the header level from Supply Chain Management, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Supply Chain Management.</span></span> <span data-ttu-id="4dee8-151">这样，即使在 Supply Chain Management 的订单头级别有税时，Sales 中的标准价格计算也可用于总金额。</span><span class="sxs-lookup"><span data-stu-id="4dee8-151">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Supply Chain Management.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="4dee8-152">折扣计算和化整</span><span class="sxs-lookup"><span data-stu-id="4dee8-152">Discount calculation and rounding</span></span>

<span data-ttu-id="4dee8-153">Sales 中的折扣计算模型不同于 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4dee8-153">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="4dee8-154">在 Supply Chain Management 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。</span><span class="sxs-lookup"><span data-stu-id="4dee8-154">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="4dee8-155">如果此最终折扣金额除以行中的数量，可能发生化整。</span><span class="sxs-lookup"><span data-stu-id="4dee8-155">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="4dee8-156">不过，如果化整的每单位折扣金额同步到 Sales，则不考虑此化整。</span><span class="sxs-lookup"><span data-stu-id="4dee8-156">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="4dee8-157">为了帮助确保 Supply Chain Management 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。</span><span class="sxs-lookup"><span data-stu-id="4dee8-157">To help guarantee that the full discount amount from a sales line in Supply Chain Management is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="4dee8-158">因此，您必须在 Sales 中将 **折扣计算方法** 定义为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-158">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="4dee8-159">在销售订单行从 Sales 同步到 Supply Chain Management 时，将使用完整行折扣金额。</span><span class="sxs-lookup"><span data-stu-id="4dee8-159">When a sales order line is synchronized from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="4dee8-160">因为 Supply Chain Management 没有能够存储完整折扣金额的字段，此金额除以数量，并存储在 **行折扣** 字段中。</span><span class="sxs-lookup"><span data-stu-id="4dee8-160">Because Supply Chain Management has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="4dee8-161">在此除法计算中发生的任何化整都将存储在销售行的 **销售费用** 字段中。</span><span class="sxs-lookup"><span data-stu-id="4dee8-161">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="4dee8-162">示例</span><span class="sxs-lookup"><span data-stu-id="4dee8-162">Example</span></span>

<span data-ttu-id="4dee8-163">**从 Sales 同步到 Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="4dee8-163">**Synchronization from Sales to Supply Chain Management**</span></span>

- <span data-ttu-id="4dee8-164">**Sales：** 数量 = 3，每行折扣 = 10.00 美元</span><span class="sxs-lookup"><span data-stu-id="4dee8-164">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="4dee8-165">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="4dee8-165">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="4dee8-166">**从 Supply Chain Management 同步到 Sales**</span><span class="sxs-lookup"><span data-stu-id="4dee8-166">**Synchronization from Supply Chain Management to Sales**</span></span>

- <span data-ttu-id="4dee8-167">**Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="4dee8-167">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="4dee8-168">**Sales：** 数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00</span><span class="sxs-lookup"><span data-stu-id="4dee8-168">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4dee8-169">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="4dee8-169">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4dee8-170">新列已添加到 **订单** 表并显示在页面上：</span><span class="sxs-lookup"><span data-stu-id="4dee8-170">New columns have been added to the **Order** table and appear on the page:</span></span>

- <span data-ttu-id="4dee8-171">**外部维护** – 当订单来自 Supply Chain Management 时将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-171">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Supply Chain Management.</span></span>
- <span data-ttu-id="4dee8-172">**处理状态** – 此列显示订单在 Supply Chain Management 中的处理状态。</span><span class="sxs-lookup"><span data-stu-id="4dee8-172">**Processing status** – This column shows the processing status of the order in Supply Chain Management.</span></span> <span data-ttu-id="4dee8-173">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="4dee8-173">The following values are available:</span></span>

    - <span data-ttu-id="4dee8-174">**草稿** – 在 Sales 中创建订单时的初始状态。</span><span class="sxs-lookup"><span data-stu-id="4dee8-174">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="4dee8-175">在 Sales 中，仅具有此处理状态的订单可编辑。</span><span class="sxs-lookup"><span data-stu-id="4dee8-175">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="4dee8-176">**活动** – 通过使用 **激活** 按钮在 Sales 中激活订单后的状态。</span><span class="sxs-lookup"><span data-stu-id="4dee8-176">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="4dee8-177">**已确认**</span><span class="sxs-lookup"><span data-stu-id="4dee8-177">**Confirmed**</span></span>
    - <span data-ttu-id="4dee8-178">**装箱单**</span><span class="sxs-lookup"><span data-stu-id="4dee8-178">**Packing Slip**</span></span>
    - <span data-ttu-id="4dee8-179">**已开票**</span><span class="sxs-lookup"><span data-stu-id="4dee8-179">**Invoiced**</span></span>
    - <span data-ttu-id="4dee8-180">**已领料**</span><span class="sxs-lookup"><span data-stu-id="4dee8-180">**Picked**</span></span>
    - <span data-ttu-id="4dee8-181">**已部分领料**</span><span class="sxs-lookup"><span data-stu-id="4dee8-181">**Partially Picked**</span></span>
    - <span data-ttu-id="4dee8-182">**已部分包装**</span><span class="sxs-lookup"><span data-stu-id="4dee8-182">**Partially Packed**</span></span>
    - <span data-ttu-id="4dee8-183">**已装运**</span><span class="sxs-lookup"><span data-stu-id="4dee8-183">**Shipped**</span></span>
    - <span data-ttu-id="4dee8-184">**已部分装运**</span><span class="sxs-lookup"><span data-stu-id="4dee8-184">**Partially Shipped**</span></span>
    - <span data-ttu-id="4dee8-185">**已部分开票**</span><span class="sxs-lookup"><span data-stu-id="4dee8-185">**Partially Invoiced**</span></span>
    - <span data-ttu-id="4dee8-186">**已取消**</span><span class="sxs-lookup"><span data-stu-id="4dee8-186">**Cancelled**</span></span>

<span data-ttu-id="4dee8-187">**仅具有外部维护的产品** 设置用于在订单激活期间一致地跟踪销售订单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="4dee8-187">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="4dee8-188">如果销售订单完全由外部维护的产品构成，则产品在 Supply Chain Management 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="4dee8-188">If a sales order consists entirely of externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="4dee8-189">此设置有助于保障您不会激活并尝试将具有未知产品的销售订单行同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4dee8-189">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="4dee8-190">对于外部维护的订单，**销售订单** 页上的 **创建发票**、**取消订单**、**重新计算**、**获取产品** 和 **查找地址** 按钮将隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-190">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="4dee8-191">这些订单不可编辑，因为将在激活后同步来自 Supply Chain Management 的销售订单信息。</span><span class="sxs-lookup"><span data-stu-id="4dee8-191">These orders can't be edited, because sales order information will be synchronized from Supply Chain Management after activation.</span></span>

<span data-ttu-id="4dee8-192">销售订单状态将保持 **活动** 状态，以帮助确保来自 Supply Chain Management 的更改可以流向 Sales 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-192">The sales order status will remain **Active** to help guarantee that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="4dee8-193">若要控制此行为，在数据集成项目中将默认的 **状态代码 \[Status\]** 值设置为 **活动**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-193">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4dee8-194">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="4dee8-194">Preconditions and mapping setup</span></span>

<span data-ttu-id="4dee8-195">在同步销售订单前，更新系统中的下列设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="4dee8-195">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="4dee8-196">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="4dee8-196">Setup in Sales</span></span>

- <span data-ttu-id="4dee8-197">确保为用户（来自 Sales 连接集）分配到的团队设置了权限。</span><span class="sxs-lookup"><span data-stu-id="4dee8-197">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="4dee8-198">如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="4dee8-198">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="4dee8-199">如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。</span><span class="sxs-lookup"><span data-stu-id="4dee8-199">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="4dee8-200">转到 **设置** &gt; **安全** &gt; **团队**，选择相关团队，选择 **管理角色**，并选择具有所需权限的角色，如 **系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-200">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="4dee8-201">为确保 Sales 和 Supply Chain Management 中的折扣计算均正确无误，必须将 **折扣计算方法** 设置为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-201">To ensure correct calculation of discounts in both Sales and Supply Chain Management **Discount calculation method** must be set to **Line item**.</span></span>
- <span data-ttu-id="4dee8-202">转到 **设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="4dee8-202">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="4dee8-203">**使用系统定价计算系统** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-203">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="4dee8-204">**折扣计算方法** 列设置为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-204">The **Discount calculation method** column is set to **Line item**.</span></span>

### <a name="setup-in-supply-chain-management"></a><span data-ttu-id="4dee8-205">Supply Chain Management 中的设置</span><span class="sxs-lookup"><span data-stu-id="4dee8-205">Setup in Supply Chain Management</span></span>

- <span data-ttu-id="4dee8-206">转到 **销售和市场** &gt; **定期任务** &gt; **计算销售额总计**，将作业设置为作为批处理作业运行。</span><span class="sxs-lookup"><span data-stu-id="4dee8-206">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="4dee8-207">将 **计算销售订单的总计** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-207">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="4dee8-208">此步骤很重要，因为只有计算了销售额总计的销售订单才会同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="4dee8-208">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="4dee8-209">应根据销售订单同步的频率调整批处理作业的频率。</span><span class="sxs-lookup"><span data-stu-id="4dee8-209">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

<span data-ttu-id="4dee8-210">如果也使用工作订单集成，则需设置销售来源。</span><span class="sxs-lookup"><span data-stu-id="4dee8-210">If you also use work order integration, you need to set up the sales origin.</span></span> <span data-ttu-id="4dee8-211">销售订单来源用于分辨 Supply Chain Management 中创建自 Field Service 中的工作订单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-211">The sales origin is used to distinguish sales orders in Supply Chain Management that were created from work orders in Field Service.</span></span> <span data-ttu-id="4dee8-212">如果销售订单的销售订单来源类型为 **工作订单集成**，则销售订单头中将显示 **外部工作订单状态** 字段。</span><span class="sxs-lookup"><span data-stu-id="4dee8-212">When a sales order has a sales origin of the **Work order integration** type, the **External work order status** field appears on the sales order header.</span></span> <span data-ttu-id="4dee8-213">此外，销售订单来源可确保将销售订单从 Supply Chain Management 同步到 Field Service 期间过滤掉创建自 Field Service 中的工作订单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="4dee8-213">Additionally, the sales origin ensures that sales orders that were created from work orders in Field Service are filtered out during sales order synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="4dee8-214">转到 **销售和市场营销** \> **设置** \> **销售订单** \> **销售订单来源**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-214">Go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Sales origin**.</span></span>
2. <span data-ttu-id="4dee8-215">选择 **新建** 创建新的销售订单来源。</span><span class="sxs-lookup"><span data-stu-id="4dee8-215">Select **New** to create a new sales origin.</span></span>
3. <span data-ttu-id="4dee8-216">在 **销售订单来源** 列中，输入销售订单来源的名称，如 **SalesOrder**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-216">In the **Sales origin** column, enter a name for the sales origin, such as **SalesOrder**.</span></span>
4. <span data-ttu-id="4dee8-217">在 **描述** 列中，输入描述，如 **来自 Sales 的销售订单**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-217">In the **Description** column, enter a description, such as **Sales Order from Sales**.</span></span>
5. <span data-ttu-id="4dee8-218">选中 **来源类型分配** 复选框。</span><span class="sxs-lookup"><span data-stu-id="4dee8-218">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="4dee8-219">将 **销售订单来源类型** 列设置为 **销售订单集成**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-219">Set the **Sales origin type** column to **Sales order integration**.</span></span>
7. <span data-ttu-id="4dee8-220">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-220">Select **Save**.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a><span data-ttu-id="4dee8-221">销售订单中的设置（Sales 到 Supply Chain Management）- 直接数据集成项目</span><span class="sxs-lookup"><span data-stu-id="4dee8-221">Setup in the Sales Orders (Sales to Supply Chain Management) - Direct Data integration project</span></span>

- <span data-ttu-id="4dee8-222">确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。</span><span class="sxs-lookup"><span data-stu-id="4dee8-222">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="4dee8-223">您可以将值映射中的默认值留空，以避免必须为国家订单键入国家/地区。</span><span class="sxs-lookup"><span data-stu-id="4dee8-223">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="4dee8-224">将左侧设置为“空白”，将右侧设置为所需的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="4dee8-224">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="4dee8-225">模板值是映射了多个国家或地区的值映射，其中“空白”= US。</span><span class="sxs-lookup"><span data-stu-id="4dee8-225">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a><span data-ttu-id="4dee8-226">销售订单中的设置（Supply Chain Management 到 Sales）- 直接数据集成项目</span><span class="sxs-lookup"><span data-stu-id="4dee8-226">Setup in the Sales Orders (Supply Chain Management to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="4dee8-227">SalesHeader 任务</span><span class="sxs-lookup"><span data-stu-id="4dee8-227">SalesHeader task</span></span>

- <span data-ttu-id="4dee8-228">在 Sales 中创建订单需要价目表。</span><span class="sxs-lookup"><span data-stu-id="4dee8-228">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="4dee8-229">将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。</span><span class="sxs-lookup"><span data-stu-id="4dee8-229">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="4dee8-230">您可以为单个币种使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="4dee8-230">You can use the default price list for a single currency.</span></span> <span data-ttu-id="4dee8-231">或者，如果您的价目表有多个币种，则可以使用值映射。</span><span class="sxs-lookup"><span data-stu-id="4dee8-231">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="4dee8-232">**pricelevelid.name \[价目表名称\]** 的默认模板值是 **美国 CRM 服务（示例）**。</span><span class="sxs-lookup"><span data-stu-id="4dee8-232">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="4dee8-233">SalesLine 任务</span><span class="sxs-lookup"><span data-stu-id="4dee8-233">SalesLine task</span></span>

- <span data-ttu-id="4dee8-234">确保在 Supply Chain Management 中存在所需的 **SalesUnitSymbol** 值映射。</span><span class="sxs-lookup"><span data-stu-id="4dee8-234">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>
- <span data-ttu-id="4dee8-235">确保所需单位已在 Sales 中定义。</span><span class="sxs-lookup"><span data-stu-id="4dee8-235">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="4dee8-236">为 **SalesUnitSymbol** 到 **oumid.name** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="4dee8-236">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4dee8-237">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="4dee8-237">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="4dee8-238">**付款期限**、**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 列不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="4dee8-238">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't part of the default mappings.</span></span> <span data-ttu-id="4dee8-239">若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="4dee8-239">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="4dee8-240">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="4dee8-240">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="4dee8-241">此映射显示将从 Sales 同步到 Supply Chain Management 或从 Supply Chain Management 同步到 Sales 的列信息。</span><span class="sxs-lookup"><span data-stu-id="4dee8-241">The mapping shows which column information will be synchronized from Sales to Supply Chain Management, or from Supply Chain Management to Sales.</span></span>

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a><span data-ttu-id="4dee8-242">销售订单（Supply Chain Management 到 Sales）- 直接：OrderHeader</span><span class="sxs-lookup"><span data-stu-id="4dee8-242">Sales Orders (Supply Chain Management to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="4dee8-243">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="4dee8-243">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a><span data-ttu-id="4dee8-244">销售订单（Supply Chain Management 到 Sales）- 直接：OrderLine</span><span class="sxs-lookup"><span data-stu-id="4dee8-244">Sales Orders (Supply Chain Management to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="4dee8-245">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="4dee8-245">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a><span data-ttu-id="4dee8-246">销售订单（Sales 到 Supply Chain Management）- 直接：OrderHeader</span><span class="sxs-lookup"><span data-stu-id="4dee8-246">Sales Orders (Sales to Supply Chain Management) - Direct: OrderHeader</span></span>

<span data-ttu-id="4dee8-247">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="4dee8-247">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a><span data-ttu-id="4dee8-248">销售订单（Sales 到 Supply Chain Management）- 直接：OrderLine</span><span class="sxs-lookup"><span data-stu-id="4dee8-248">Sales Orders (Sales to Supply Chain Management) - Direct: OrderLine</span></span>

<span data-ttu-id="4dee8-249">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="4dee8-249">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dee8-250">相关主题</span><span class="sxs-lookup"><span data-stu-id="4dee8-250">Related topics</span></span>

[<span data-ttu-id="4dee8-251">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="4dee8-251">Prospect to cash</span></span>](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]