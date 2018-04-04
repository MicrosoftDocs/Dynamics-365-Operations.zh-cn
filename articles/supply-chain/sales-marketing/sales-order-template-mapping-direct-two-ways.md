---
title: "将 Sales 与 Finance and Operations 的销售订单直接同步"
description: "本主题讨论用于在 Microsoft Dynamics 365 for Sales 与 Microsoft Dynamics 365 for Finance and Operations 之间直接运行销售订单同步的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a><span data-ttu-id="adcaa-103">将 Sales 与 Finance and Operations 的销售订单直接同步</span><span class="sxs-lookup"><span data-stu-id="adcaa-103">Synchronization of sales orders directly between Sales and Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adcaa-104">本主题讨论用于在 Microsoft Dynamics 365 for Sales 与 Microsoft Dynamics 365 for Finance and Operations 之间直接运行销售订单同步的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="adcaa-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Microsoft Dynamics 365 for Sales and Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="adcaa-105">模板和任务</span><span class="sxs-lookup"><span data-stu-id="adcaa-105">Templates and tasks</span></span>

<span data-ttu-id="adcaa-106">若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="adcaa-106">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="adcaa-107">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="adcaa-107">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="adcaa-108">以下模板和基础任务用于在 Sales 与 Finance and Operations 之间直接运行销售订单的同步：</span><span class="sxs-lookup"><span data-stu-id="adcaa-108">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Finance and Operations:</span></span>

- <span data-ttu-id="adcaa-109">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="adcaa-109">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="adcaa-110">销售订单（从 Sales 到 Fin and Ops）- 直接</span><span class="sxs-lookup"><span data-stu-id="adcaa-110">Sales Orders (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="adcaa-111">销售订单（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="adcaa-111">Sales Orders (Fin and Ops to Sales) - Direct</span></span>

- <span data-ttu-id="adcaa-112">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="adcaa-112">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="adcaa-113">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="adcaa-113">OrderHeader</span></span>
    - <span data-ttu-id="adcaa-114">OrderLine</span><span class="sxs-lookup"><span data-stu-id="adcaa-114">OrderLine</span></span>

<span data-ttu-id="adcaa-115">在发生销售发票标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="adcaa-115">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="adcaa-116">产品（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="adcaa-116">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="adcaa-117">帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="adcaa-117">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="adcaa-118">从联系人到客户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="adcaa-118">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="adcaa-119">实体集</span><span class="sxs-lookup"><span data-stu-id="adcaa-119">Entity set</span></span>

| <span data-ttu-id="adcaa-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adcaa-120">Finance and Operations</span></span>  | <span data-ttu-id="adcaa-121">销售</span><span class="sxs-lookup"><span data-stu-id="adcaa-121">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="adcaa-122">CDS 销售订单标题</span><span class="sxs-lookup"><span data-stu-id="adcaa-122">CDS sales order headers</span></span> | <span data-ttu-id="adcaa-123">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="adcaa-123">SalesOrders</span></span>       |
| <span data-ttu-id="adcaa-124">CDS 销售订单行</span><span class="sxs-lookup"><span data-stu-id="adcaa-124">CDS sales order lines</span></span>   | <span data-ttu-id="adcaa-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="adcaa-125">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="adcaa-126">实体流</span><span class="sxs-lookup"><span data-stu-id="adcaa-126">Entity flow</span></span>

<span data-ttu-id="adcaa-127">在为基于**销售订单（Sales 到 Fin and Ops）-直接**模板的项目触发**运行项目**后，销售订单在 Sales 中创建，然后同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="adcaa-127">Sales orders are created in Sales and synchronized to Finance and Operations when **Run project** is triggered for a project based on the **Sales Orders (Sales to Fin and Ops) - Direct** template.</span></span> <span data-ttu-id="adcaa-128">只有当所有**订单产品**全部是外部维护产品时，您才能够激活和同步来自 Sales 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-128">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="adcaa-129">因此，可能没有目录外产品。</span><span class="sxs-lookup"><span data-stu-id="adcaa-129">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="adcaa-130">在订单启用后，销售订单将在用户界面 (UI) 变为只读。</span><span class="sxs-lookup"><span data-stu-id="adcaa-130">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="adcaa-131">此时，从 Finance and Operations 进行更新。</span><span class="sxs-lookup"><span data-stu-id="adcaa-131">At that point, the updates are made from Finance and Operations.</span></span> <span data-ttu-id="adcaa-132">在销售订单具有状态**已确认**后，基于**销售订单（Fin and Ops 到 Sales）- 直接**模板的项目可用于将 Finance and Operations 的更新或履行状态全部同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-132">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Fin and Ops to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Finance and Operations to Sales.</span></span>

<span data-ttu-id="adcaa-133">您不必在 Sales 中创建订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-133">You don't have to create orders in Sales.</span></span> <span data-ttu-id="adcaa-134">而可以在 Finance and Operations 中创建新销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-134">You can create new sales orders in Finance and Operations instead.</span></span> <span data-ttu-id="adcaa-135">在销售订单具有状态**已确认**后，其将被同步到 Sales，如前面段落中所述。</span><span class="sxs-lookup"><span data-stu-id="adcaa-135">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="adcaa-136">在 Finance and Operations 中，模板中的筛选器帮助确保同步中只包括相关销售订单：</span><span class="sxs-lookup"><span data-stu-id="adcaa-136">In Finance and operations, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="adcaa-137">在销售订单上，订购客户和开票客户都必须来自 Sales 以被包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="adcaa-137">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="adcaa-138">在 Finance and Operations 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 字段用于筛选来自数据实体的销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-138">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to filter sales orders from the data entities.</span></span>
- <span data-ttu-id="adcaa-139">必须确认 Finance and Operations 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-139">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="adcaa-140">仅已确认的销售订单或具有更高处理状态（如**已装运**或**已开票**）的销售订单同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-140">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="adcaa-141">在创建或修改销售订单后，必须运行 Finance and Operations 中的**计算销售额总计**批处理作业。</span><span class="sxs-lookup"><span data-stu-id="adcaa-141">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="adcaa-142">仅计算了销售总额的销售订单将被同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-142">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="adcaa-143">货运税</span><span class="sxs-lookup"><span data-stu-id="adcaa-143">Freight tax</span></span>

<span data-ttu-id="adcaa-144">因为税存储在行级别，因此 Sales 不在订单头级别支持税务信息。</span><span class="sxs-lookup"><span data-stu-id="adcaa-144">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="adcaa-145">为了在 Finance and Operations 的订单头级别支持税务信息（如货运税），系统会将税作为名为**货运税**以及具有来自 Finance and Operations 的税额的目录外产品同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-145">To support tax at the header level from Finance and Operations, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Finance and Operations.</span></span> <span data-ttu-id="adcaa-146">这样，即使在 Finance and Operations 的订单头级别有税时，Sales 中的标准价格计算也可用于总金额。</span><span class="sxs-lookup"><span data-stu-id="adcaa-146">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Finance and Operations.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="adcaa-147">折扣计算和舍入</span><span class="sxs-lookup"><span data-stu-id="adcaa-147">Discount calculation and rounding</span></span>

<span data-ttu-id="adcaa-148">Sales 中的折扣计算模型不同于 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="adcaa-148">The discount calculation model in Sales differs from the discount calculation model in Finance and Operations.</span></span> <span data-ttu-id="adcaa-149">在 Finance and Operations 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。</span><span class="sxs-lookup"><span data-stu-id="adcaa-149">In Finance and Operations, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="adcaa-150">如果此最终折扣金额除以行中的数量，可能发生舍入。</span><span class="sxs-lookup"><span data-stu-id="adcaa-150">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="adcaa-151">不过，如果舍入的每单位折扣金额同步到 Sales，则不考虑此舍入。</span><span class="sxs-lookup"><span data-stu-id="adcaa-151">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="adcaa-152">为了帮助确保 Finance and Operations 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。</span><span class="sxs-lookup"><span data-stu-id="adcaa-152">To help guarantee that the full discount amount from a sales line in Finance and Operations is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="adcaa-153">因此，您必须在 Sales 中将**折扣计算方法**定义为**行项**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-153">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="adcaa-154">在销售订单行从 Sales 同步到 Finance and Operations 时，将使用完整行折扣金额。</span><span class="sxs-lookup"><span data-stu-id="adcaa-154">When a sales order line is synchronized from Sales to Finance and Operations, the full line discount amount is used.</span></span> <span data-ttu-id="adcaa-155">因为 Finance and Operations 没有能够存储完整折扣金额的字段，此金额除以数量，并存储在**行折扣**字段中。</span><span class="sxs-lookup"><span data-stu-id="adcaa-155">Because Finance and Operations has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="adcaa-156">在此除法计算中发生的任何舍入都将存储在销售行的**销售费用**字段中。</span><span class="sxs-lookup"><span data-stu-id="adcaa-156">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="adcaa-157">示例</span><span class="sxs-lookup"><span data-stu-id="adcaa-157">Example</span></span>

<span data-ttu-id="adcaa-158">**从 Sales 同步到 Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="adcaa-158">**Synchronization from Sales to Finance and Operations**</span></span>

- <span data-ttu-id="adcaa-159">**Sales：**数量 = 3，每行折扣 = 10.00 美元</span><span class="sxs-lookup"><span data-stu-id="adcaa-159">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="adcaa-160">**Finance and Operations：**数量 = 3，行折扣金额 = 3.33 美元，销售费用 = -0.01 美元</span><span class="sxs-lookup"><span data-stu-id="adcaa-160">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="adcaa-161">**从 Finance and Operations 同步到 Sales**</span><span class="sxs-lookup"><span data-stu-id="adcaa-161">**Synchronization from Finance and Operations to Sales**</span></span>

- <span data-ttu-id="adcaa-162">**Finance and Operations：**数量 = 3，行折扣金额 = 3.33 美元，销售费用 = -0.01 美元</span><span class="sxs-lookup"><span data-stu-id="adcaa-162">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="adcaa-163">**Sales：**数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00</span><span class="sxs-lookup"><span data-stu-id="adcaa-163">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="adcaa-164">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="adcaa-164">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="adcaa-165">新字段已添加到**订单**实体并显示在以下页面：</span><span class="sxs-lookup"><span data-stu-id="adcaa-165">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="adcaa-166">**外部维护** – 当订单来自 Finance and Operations 时将此选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-166">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="adcaa-167">**处理状态** – 此字段显示订单在 Finance and Operations 中的处理状态。</span><span class="sxs-lookup"><span data-stu-id="adcaa-167">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="adcaa-168">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="adcaa-168">The following values are available:</span></span>

    - <span data-ttu-id="adcaa-169">**草稿** – 在 Sales 中创建订单时的初始状态。</span><span class="sxs-lookup"><span data-stu-id="adcaa-169">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="adcaa-170">在 Sales 中，仅具有此处理状态的订单可编辑。</span><span class="sxs-lookup"><span data-stu-id="adcaa-170">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="adcaa-171">**活动** – 通过使用**激活**按钮在 Sales 中激活订单后的状态。</span><span class="sxs-lookup"><span data-stu-id="adcaa-171">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="adcaa-172">**已确认**</span><span class="sxs-lookup"><span data-stu-id="adcaa-172">**Confirmed**</span></span>
    - <span data-ttu-id="adcaa-173">**装箱单**</span><span class="sxs-lookup"><span data-stu-id="adcaa-173">**Packing Slip**</span></span>
    - <span data-ttu-id="adcaa-174">**已开票**</span><span class="sxs-lookup"><span data-stu-id="adcaa-174">**Invoiced**</span></span>
    - <span data-ttu-id="adcaa-175">**已领料**</span><span class="sxs-lookup"><span data-stu-id="adcaa-175">**Picked**</span></span>
    - <span data-ttu-id="adcaa-176">**已部分领料**</span><span class="sxs-lookup"><span data-stu-id="adcaa-176">**Partially Picked**</span></span>
    - <span data-ttu-id="adcaa-177">**已部分包装**</span><span class="sxs-lookup"><span data-stu-id="adcaa-177">**Partially Packed**</span></span>
    - <span data-ttu-id="adcaa-178">**已装运**</span><span class="sxs-lookup"><span data-stu-id="adcaa-178">**Shipped**</span></span>
    - <span data-ttu-id="adcaa-179">**已部分装运**</span><span class="sxs-lookup"><span data-stu-id="adcaa-179">**Partially Shipped**</span></span>
    - <span data-ttu-id="adcaa-180">**已部分开票**</span><span class="sxs-lookup"><span data-stu-id="adcaa-180">**Partially Invoiced**</span></span>
    - <span data-ttu-id="adcaa-181">**已取消**</span><span class="sxs-lookup"><span data-stu-id="adcaa-181">**Cancelled**</span></span>

<span data-ttu-id="adcaa-182">**仅具有外部维护的产品**设置用于在订单激活期间一致地跟踪销售订单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="adcaa-182">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="adcaa-183">如果销售订单完全由外部维护的产品构成，则产品在 Finance and Operations 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="adcaa-183">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="adcaa-184">此设置有助于保障您不会激活并尝试将具有未知产品的销售订单行同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="adcaa-184">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="adcaa-185">对于外部维护的订单，**销售订单**页上的**创建发票**、**取消订单**、**重新计算**、**获取产品**和**查找地址**按钮将隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-185">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="adcaa-186">这些订单不可编辑，因为将在激活后同步来自 Finance and Operations 的销售订单信息。</span><span class="sxs-lookup"><span data-stu-id="adcaa-186">These orders can't be edited, because sales order information will be synchronized from Finance and Operations after activation.</span></span>

<span data-ttu-id="adcaa-187">销售订单状态将保持**活动**状态，以帮助确保来自 Finance and Operations 的更改可以流向 Sales 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcaa-187">The sales order status will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="adcaa-188">若要控制此行为，在数据集成项目中将默认的**状态代码 \[Status\]** 值设置为**活动**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-188">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="adcaa-189">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="adcaa-189">Preconditions and mapping setup</span></span>

<span data-ttu-id="adcaa-190">在同步销售订单前，更新系统中的下列设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="adcaa-190">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="adcaa-191">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="adcaa-191">Setup in Sales</span></span>

- <span data-ttu-id="adcaa-192">确保为用户（来自 Sales 连接集）分配到的团队设置了权限。</span><span class="sxs-lookup"><span data-stu-id="adcaa-192">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="adcaa-193">如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="adcaa-193">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="adcaa-194">如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。</span><span class="sxs-lookup"><span data-stu-id="adcaa-194">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="adcaa-195">转到**设置** &gt; **安全** &gt; **团队**，选择相关团队，选择**管理角色**，并选择具有所需权限的角色，如**系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-195">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="adcaa-196">为确保 Sales 和 Finance and Operations 中的折扣计算均正确无误，必须将**折扣计算方法**设置为**行项**.</span><span class="sxs-lookup"><span data-stu-id="adcaa-196">To ensure correct calculation of discounts in both Sales and Finance and Operations **Discount calculation method** must be set to **Line item**.</span></span>
- <span data-ttu-id="adcaa-197">转到**设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="adcaa-197">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="adcaa-198">**使用系统定价计算系统**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-198">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="adcaa-199">**折扣计算方法**字段设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-199">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="adcaa-200">Finance and Operations 中的设置</span><span class="sxs-lookup"><span data-stu-id="adcaa-200">Setup in Finance and Operations</span></span>

- <span data-ttu-id="adcaa-201">转到**销售和市场** &gt; **定期任务** &gt; **计算销售额总计**，将作业设置为作为批处理作业运行。</span><span class="sxs-lookup"><span data-stu-id="adcaa-201">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="adcaa-202">将**计算销售订单的总计**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-202">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="adcaa-203">此步骤很重要，因为只有计算了销售额总计的销售订单才会同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="adcaa-203">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="adcaa-204">应根据销售订单同步的频率调整批处理作业的频率。</span><span class="sxs-lookup"><span data-stu-id="adcaa-204">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a><span data-ttu-id="adcaa-205">销售订单中的设置（Sales 到 Fin and Ops）- 直接数据集成项目</span><span class="sxs-lookup"><span data-stu-id="adcaa-205">Setup in the Sales Orders (Sales to Fin and Ops) - Direct Data integration project</span></span>

- <span data-ttu-id="adcaa-206">确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。</span><span class="sxs-lookup"><span data-stu-id="adcaa-206">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="adcaa-207">您可以将值映射中的默认值留空，以避免必须为国家订单键入国家/地区。</span><span class="sxs-lookup"><span data-stu-id="adcaa-207">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="adcaa-208">将左侧设置为“空白”，将右侧设置为所需的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="adcaa-208">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="adcaa-209">模板值是映射了多个国家或地区的值映射，其中“空白”= US。</span><span class="sxs-lookup"><span data-stu-id="adcaa-209">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a><span data-ttu-id="adcaa-210">销售订单中的设置（Fin and Ops 到 Sales）- 直接数据集成项目</span><span class="sxs-lookup"><span data-stu-id="adcaa-210">Setup in the Sales Orders (Fin and Ops to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="adcaa-211">SalesHeader 任务</span><span class="sxs-lookup"><span data-stu-id="adcaa-211">SalesHeader task</span></span>

- <span data-ttu-id="adcaa-212">在 Sales 中创建订单需要价目表。</span><span class="sxs-lookup"><span data-stu-id="adcaa-212">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="adcaa-213">将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。</span><span class="sxs-lookup"><span data-stu-id="adcaa-213">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="adcaa-214">您可以为单个币种使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="adcaa-214">You can use the default price list for a single currency.</span></span> <span data-ttu-id="adcaa-215">或者，如果您的价目表有多个币种，则可以使用值映射。</span><span class="sxs-lookup"><span data-stu-id="adcaa-215">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="adcaa-216">**pricelevelid.name \[价目表名称\]** 的默认模板值是**美国 CRM 服务（示例）**。</span><span class="sxs-lookup"><span data-stu-id="adcaa-216">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="adcaa-217">SalesLine 任务</span><span class="sxs-lookup"><span data-stu-id="adcaa-217">SalesLine task</span></span>

- <span data-ttu-id="adcaa-218">确保所需的 **SalesUnitSymbol** 的值映射在 Finance and Operations 中存在。</span><span class="sxs-lookup"><span data-stu-id="adcaa-218">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>
- <span data-ttu-id="adcaa-219">确保所需单位已在 Sales 中定义。</span><span class="sxs-lookup"><span data-stu-id="adcaa-219">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="adcaa-220">为 **SalesUnitSymbol** 到 **oumid.name** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="adcaa-220">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="adcaa-221">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="adcaa-221">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="adcaa-222">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="adcaa-222">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="adcaa-223">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="adcaa-223">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="adcaa-224">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="adcaa-224">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="adcaa-225">此映射显示将从 Sales 同步到 Finance and Operations 或从 Finance and Operations 同步到 Sales 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="adcaa-225">The mapping shows which field information will be synchronized from Sales to Finance and Operations, or from Finance and Operations to Sales.</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a><span data-ttu-id="adcaa-226">销售订单（从 Fin and Ops 到 Sales）- 直接：OrderHeader</span><span class="sxs-lookup"><span data-stu-id="adcaa-226">Sales Orders (Fin and Ops to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="adcaa-227">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="adcaa-227">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a><span data-ttu-id="adcaa-228">销售订单（从 Fin and Ops 到 Sales）- 直接：OrderLine</span><span class="sxs-lookup"><span data-stu-id="adcaa-228">Sales Orders (Fin and Ops to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="adcaa-229">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="adcaa-229">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a><span data-ttu-id="adcaa-230">销售订单（Sales 到 Fin and Ops）- 直接：OrderHeader</span><span class="sxs-lookup"><span data-stu-id="adcaa-230">Sales Orders (Sales to Fin and Ops) - Direct: OrderHeader</span></span>

<span data-ttu-id="adcaa-231">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="adcaa-231">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a><span data-ttu-id="adcaa-232">销售订单（Sales 到 Fin and Ops）- 直接：OrderLine</span><span class="sxs-lookup"><span data-stu-id="adcaa-232">Sales Orders (Sales to Fin and Ops) - Direct: OrderLine</span></span>

<span data-ttu-id="adcaa-233">[![数据集成中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="adcaa-233">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="adcaa-234">相关主题</span><span class="sxs-lookup"><span data-stu-id="adcaa-234">Related topics</span></span>

[<span data-ttu-id="adcaa-235">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="adcaa-235">Prospect to cash</span></span>](prospect-to-cash.md)

