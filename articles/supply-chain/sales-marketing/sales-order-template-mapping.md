---
title: "将 Finance and Operations 的销售订单标题和行同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="20300-103">将 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="20300-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20300-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="20300-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="20300-105">模板和任务</span><span class="sxs-lookup"><span data-stu-id="20300-105">Template and tasks</span></span>

<span data-ttu-id="20300-106">以下模板和基础任务用于将来自 Finance and Operations 的销售订单标题和行同步到 Sales：</span><span class="sxs-lookup"><span data-stu-id="20300-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="20300-107">**数据集成中的模板名称**</span><span class="sxs-lookup"><span data-stu-id="20300-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="20300-108">销售订单（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="20300-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="20300-109">**数据集成项目中的任务名称**</span><span class="sxs-lookup"><span data-stu-id="20300-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="20300-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="20300-110">OrderHeader</span></span>
    - <span data-ttu-id="20300-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="20300-111">OrderLine</span></span>

<span data-ttu-id="20300-112">在同步销售发票抬头和行之前所需的同步任务：</span><span class="sxs-lookup"><span data-stu-id="20300-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="20300-113">产品（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="20300-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="20300-114">帐户（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="20300-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="20300-115">从联系人到客户（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="20300-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="20300-116">实体集</span><span class="sxs-lookup"><span data-stu-id="20300-116">Entity set</span></span>

| <span data-ttu-id="20300-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20300-117">Finance and Operations</span></span> |    <span data-ttu-id="20300-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="20300-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="20300-119">销售</span><span class="sxs-lookup"><span data-stu-id="20300-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="20300-120">CDS 销售订单标题</span><span class="sxs-lookup"><span data-stu-id="20300-120">CDS sales order headers</span></span>| <span data-ttu-id="20300-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="20300-121">SalesOrder</span></span>     | <span data-ttu-id="20300-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="20300-122">SalesOrders</span></span> |
| <span data-ttu-id="20300-123">CDS 销售订单行</span><span class="sxs-lookup"><span data-stu-id="20300-123">CDS sales order lines</span></span>  | <span data-ttu-id="20300-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="20300-124">SalesOrderLine</span></span> | <span data-ttu-id="20300-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="20300-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="20300-126">实体流</span><span class="sxs-lookup"><span data-stu-id="20300-126">Entity flow</span></span>

<span data-ttu-id="20300-127">销售订单在 Finance and Operations 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="20300-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="20300-128">模板中的筛选器确保同步中只包括相关销售订单：</span><span class="sxs-lookup"><span data-stu-id="20300-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="20300-129">来自 Sales 的销售订单上的订购和开票客户都将包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="20300-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="20300-130">在 Finance and Operations 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 字段都用于跟踪数据实体中的同步。</span><span class="sxs-lookup"><span data-stu-id="20300-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="20300-131">必须确认 Finance and Operations 中的**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="20300-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="20300-132">仅已确认的销售订单或具有更高处理状态（如已装运或已开票状态）的销售订单同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="20300-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="20300-133">在创建或修改销售订单后，必须在 Finance and Operations 中执行批处理作业**计算销售额总计**。</span><span class="sxs-lookup"><span data-stu-id="20300-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="20300-134">仅计算了销售额总计的销售订单将被同步到 CDS 和 Sales。</span><span class="sxs-lookup"><span data-stu-id="20300-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="20300-135">与**销售订单标题**上的费用关联的税金当前不包括在从 Finance and Operations 到 Sales 的同步中。</span><span class="sxs-lookup"><span data-stu-id="20300-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="20300-136">这是因为 Sales 不支持标题级别的税务信息。</span><span class="sxs-lookup"><span data-stu-id="20300-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="20300-137">与行级别的费用关联的税金包括在内。</span><span class="sxs-lookup"><span data-stu-id="20300-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="20300-138">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="20300-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="20300-139">新字段添加到**订单**实体并显示在以下页面：</span><span class="sxs-lookup"><span data-stu-id="20300-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="20300-140">**外部维护** - 当订单来自 Finance and Operations 时设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="20300-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="20300-141">**处理状态** - 用于显示订单在 Finance and Operations 中的处理状态。</span><span class="sxs-lookup"><span data-stu-id="20300-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="20300-142">值包括：</span><span class="sxs-lookup"><span data-stu-id="20300-142">Values are:</span></span>

    - <span data-ttu-id="20300-143">活动</span><span class="sxs-lookup"><span data-stu-id="20300-143">Active</span></span>
    - <span data-ttu-id="20300-144">已确认</span><span class="sxs-lookup"><span data-stu-id="20300-144">Confirmed</span></span>
    - <span data-ttu-id="20300-145">装箱单</span><span class="sxs-lookup"><span data-stu-id="20300-145">Packing Slip</span></span>
    - <span data-ttu-id="20300-146">已开票</span><span class="sxs-lookup"><span data-stu-id="20300-146">Invoiced</span></span>
    - <span data-ttu-id="20300-147">已领料</span><span class="sxs-lookup"><span data-stu-id="20300-147">Picked</span></span>
    - <span data-ttu-id="20300-148">已部分领料</span><span class="sxs-lookup"><span data-stu-id="20300-148">Partially Picked</span></span>
    - <span data-ttu-id="20300-149">已部分包装</span><span class="sxs-lookup"><span data-stu-id="20300-149">Partially Packed</span></span>
    - <span data-ttu-id="20300-150">已装运</span><span class="sxs-lookup"><span data-stu-id="20300-150">Shipped</span></span>
    - <span data-ttu-id="20300-151">已部分装运</span><span class="sxs-lookup"><span data-stu-id="20300-151">Partially Shipped</span></span>
    - <span data-ttu-id="20300-152">已部分开票</span><span class="sxs-lookup"><span data-stu-id="20300-152">Partially Invoiced</span></span>
    - <span data-ttu-id="20300-153">已取消</span><span class="sxs-lookup"><span data-stu-id="20300-153">Cancelled</span></span>

<span data-ttu-id="20300-154">**仅具有外部维护的产品**设置在其他销售订单方案（从 Sales 到 Finance and Operation 同步）中使用，以一致地跟踪销售订单是否全部由**外部维护的产品**构成，在这种情况下，产品在 Finance and Operations 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="20300-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="20300-155">这确保您不会尝试将具有未知产品的销售订单行同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="20300-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="20300-156">**销售订单**页上的**创建发票**、**取消订单**、**重新计算**、**获取产品**和**查找地址**按钮对外部维护的订单隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="20300-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="20300-157">订单页不可编辑，因为将同步来自 Finance and Operations 的销售订单信息。</span><span class="sxs-lookup"><span data-stu-id="20300-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="20300-158">**销售订单状态**将保持活动状态，以确保来自 Finance and Operations 的更改可以流向 Sales 中的**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="20300-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="20300-159">对其进行控制的方法是在数据集成项目中将默认的**状态代码 [状态]** 设置为**活动**。</span><span class="sxs-lookup"><span data-stu-id="20300-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="20300-160">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="20300-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="20300-161">在同步销售订单前，使用下列设置更新系统十分重要：</span><span class="sxs-lookup"><span data-stu-id="20300-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="20300-162">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="20300-162">Setup in Sales</span></span>

- <span data-ttu-id="20300-163">确保用户（来自 Sales **连接集**）分配到的团队的权限。</span><span class="sxs-lookup"><span data-stu-id="20300-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="20300-164">如果正在使用演示数据，通常用户具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="20300-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="20300-165">如果没有，您在运行来自数据集成器的项目时会收到“缺少主体团队”的错误。</span><span class="sxs-lookup"><span data-stu-id="20300-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="20300-166">在**设置** > **安全** > **团队**下，选择相关团队，单击**管理角色**并选择具有所需权限的角色，如系统管理员。</span><span class="sxs-lookup"><span data-stu-id="20300-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="20300-167">在**设置** > **管理** > **系统设置** > **Sales** 下，确保**使用系统定价计算系统**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="20300-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="20300-168">在**设置** > **管理** > **系统设置** > **Sales** 下，确保**折扣计算方法**设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="20300-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="20300-169">Finance and Operations 中的设置</span><span class="sxs-lookup"><span data-stu-id="20300-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="20300-170">将**销售和市场营销** > **定期任务** > **计算销售额总计**设置为作为批处理作业运行，并且将**计算销售订单的总计**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="20300-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="20300-171">这一点很重要，因为仅计算了销售额总计的销售订单才会被同步到 CDS 和 Sales。</span><span class="sxs-lookup"><span data-stu-id="20300-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="20300-172">应根据销售订单同步的频率调整批处理作业的频率。</span><span class="sxs-lookup"><span data-stu-id="20300-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="20300-173">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="20300-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="20300-174">SalesHeader 任务</span><span class="sxs-lookup"><span data-stu-id="20300-174">SalesHeader task</span></span>

- <span data-ttu-id="20300-175">为**源中的 CDS 组织 ID** > **CDS** 更新映射。</span><span class="sxs-lookup"><span data-stu-id="20300-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="20300-176">**Account_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="20300-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="20300-177">**InvoiceAccount_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="20300-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="20300-178">**Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="20300-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="20300-179">确保在**源** > **用于从 InvoiceCountryRegionId 到 BillingAddress_Country 的 CDS** 和**从 DeliveryCountryRegionId 到 DeliveryAddress_Country** 的 CDS 中存在所需的映射。</span><span class="sxs-lookup"><span data-stu-id="20300-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="20300-180">模板值是映射多个国家/地区的 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="20300-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="20300-181">在 Sales 中创建订单需要**价目表**。</span><span class="sxs-lookup"><span data-stu-id="20300-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="20300-182">在 **CDS** > **目标**中将 **pricelevelid.name [价目表名称]** 的 **ValueMap** 按币种更新至 Sales 中使用的**价目表**。</span><span class="sxs-lookup"><span data-stu-id="20300-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="20300-183">您可以为单个币种使用默认**价目表**，或者如果您具有多个币种的**价目表**，则使用 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="20300-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="20300-184">**pricelevelid.name [价目表名称]** 的默认模板值是美国 CRM 服务（示例）。</span><span class="sxs-lookup"><span data-stu-id="20300-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="20300-185">SalesLine 任务</span><span class="sxs-lookup"><span data-stu-id="20300-185">SalesLine task</span></span>

- <span data-ttu-id="20300-186">为**源中的 CDS 组织 ID** > **CDS** 更新映射。</span><span class="sxs-lookup"><span data-stu-id="20300-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="20300-187">**SalesOrder_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="20300-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="20300-188">**Product_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="20300-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="20300-189">确保在**源** > 从 **DeliveryCountryRegionId** 到 **DeliveryAddress_Country** 的 **CDS** 中存在所需的映射。</span><span class="sxs-lookup"><span data-stu-id="20300-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="20300-190">模板值是映射多个国家/地区的 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="20300-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="20300-191">确保 Finance and Operations 中的 **SalesUnitSymbol** 所需的 **ValueMap** 在**源** > **CDS 映射**中存在。</span><span class="sxs-lookup"><span data-stu-id="20300-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="20300-192">使用 **ValueMap** 为 **SalesUnitSymbol 到数量 UOM** 定义模板值。</span><span class="sxs-lookup"><span data-stu-id="20300-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="20300-193">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="20300-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="20300-194">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="20300-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="20300-195">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="20300-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="20300-196">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="20300-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="20300-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="20300-197">OrderHeader</span></span>

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="20300-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="20300-200">OrderLine</span></span>

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="20300-203">相关主题</span><span class="sxs-lookup"><span data-stu-id="20300-203">Related topics</span></span>

[<span data-ttu-id="20300-204">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="20300-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="20300-205">将 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20300-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="20300-206">将 Sales 的联系人同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="20300-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="20300-207">将 Sales 的销售报价单标题和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20300-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="20300-208">将 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="20300-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


