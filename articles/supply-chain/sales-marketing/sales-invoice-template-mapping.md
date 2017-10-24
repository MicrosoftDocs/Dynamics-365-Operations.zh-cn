---
title: "将 Finance and Operations 的销售发票标题和行同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售发票标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="fdda2-103">将 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="fdda2-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fdda2-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售发票标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="fdda2-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="fdda2-105">模板和任务</span><span class="sxs-lookup"><span data-stu-id="fdda2-105">Templates and tasks</span></span>

<span data-ttu-id="fdda2-106">以下模板和基础任务用于将来自 Finance and Operations 的销售发票标题和行同步到 Sales：</span><span class="sxs-lookup"><span data-stu-id="fdda2-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="fdda2-107">**数据集成中的模板名称**</span><span class="sxs-lookup"><span data-stu-id="fdda2-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="fdda2-108">销售发票（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="fdda2-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="fdda2-109">**数据集成项目中的任务名称**</span><span class="sxs-lookup"><span data-stu-id="fdda2-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="fdda2-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="fdda2-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="fdda2-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fdda2-111">SalesInvoiceLine</span></span>

<span data-ttu-id="fdda2-112">在同步销售发票标题和行之前所需的同步任务：</span><span class="sxs-lookup"><span data-stu-id="fdda2-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="fdda2-113">产品（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="fdda2-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="fdda2-114">帐户（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="fdda2-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="fdda2-115">联系人（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="fdda2-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="fdda2-116">销售订单标题和行（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="fdda2-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="fdda2-117">实体集</span><span class="sxs-lookup"><span data-stu-id="fdda2-117">Entity set</span></span>

| <span data-ttu-id="fdda2-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fdda2-118">Finance and Operations</span></span>                               | <span data-ttu-id="fdda2-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="fdda2-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="fdda2-120">销售</span><span class="sxs-lookup"><span data-stu-id="fdda2-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="fdda2-121">外部维护的客户销售发票抬头</span><span class="sxs-lookup"><span data-stu-id="fdda2-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="fdda2-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="fdda2-122">SalesInvoice</span></span>     | <span data-ttu-id="fdda2-123">发票</span><span class="sxs-lookup"><span data-stu-id="fdda2-123">Invoices</span></span>       |
| <span data-ttu-id="fdda2-124">外部维护的客户销售发票行</span><span class="sxs-lookup"><span data-stu-id="fdda2-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="fdda2-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fdda2-125">SalesInvoiceLine</span></span> | <span data-ttu-id="fdda2-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="fdda2-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fdda2-127">实体流</span><span class="sxs-lookup"><span data-stu-id="fdda2-127">Entity flow</span></span>

<span data-ttu-id="fdda2-128">销售发票在 Finance and Operations 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="fdda2-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="fdda2-129">与**销售发票标题**上的费用关联的税金当前不包括在从 Finance and Operations 到 Sales 的同步中。</span><span class="sxs-lookup"><span data-stu-id="fdda2-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="fdda2-130">这是因为 Sales 不支持标题级别的税务信息。</span><span class="sxs-lookup"><span data-stu-id="fdda2-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="fdda2-131">与行级别的费用关联的税金包括在内。</span><span class="sxs-lookup"><span data-stu-id="fdda2-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fdda2-132">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="fdda2-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="fdda2-133">**发票编号字段**添加到**发票**实体中并显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="fdda2-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="fdda2-134">**销售订单**页上的**创建发票**按钮被隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="fdda2-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="fdda2-135">**发票**页不可编辑，因为发票将从 Finance and Operations 同步。</span><span class="sxs-lookup"><span data-stu-id="fdda2-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="fdda2-136">当关联的发票从 Finance and Operations 同步到 Sales 后，**销售订单状态**自动更改为**已开票**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="fdda2-137">而且，创建发票的销售订单的所有者被指定为发票的所有者。</span><span class="sxs-lookup"><span data-stu-id="fdda2-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="fdda2-138">这使得销售订单的所有者能够查看发票。</span><span class="sxs-lookup"><span data-stu-id="fdda2-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fdda2-139">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="fdda2-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="fdda2-140">在同步销售发票前，使用下列设置更新系统十分重要：</span><span class="sxs-lookup"><span data-stu-id="fdda2-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="fdda2-141">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="fdda2-141">Setup in Sales</span></span>

- <span data-ttu-id="fdda2-142">在**设置** > **管理** > **系统设置** > **Sales** 下，确保**使用系统定价计算系统**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="fdda2-143">在**设置** > **管理** > **系统设置** > **Sales** 下，确保**折扣计算方法**设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="fdda2-144">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="fdda2-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="fdda2-145">SalesInvoiceHeader 任务</span><span class="sxs-lookup"><span data-stu-id="fdda2-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="fdda2-146">为**源** > **CDS** 中的 **CDS 组织 ID** 更新映射。</span><span class="sxs-lookup"><span data-stu-id="fdda2-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="fdda2-147">**SalesOrder_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="fdda2-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="fdda2-148">**Account_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="fdda2-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="fdda2-149">**Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="fdda2-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="fdda2-150">确保在**源**  >  **InvoiceCountryRegionId 的 CDS** 中存在到 **BillingAddress_Country** 的所需映射。</span><span class="sxs-lookup"><span data-stu-id="fdda2-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="fdda2-151">模板值是映射多个国家/地区的 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="fdda2-152">在 Sales 中创建发票需要**价目表**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="fdda2-153">在 **CDS** > **pricelevelid.name [价目表名称] 目标**中将 **ValueMap** 按币种更新至 Sales 中使用的**价目表**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="fdda2-154">您可以为单个币种使用默认**价目表**，或者如果您具有多个币种的**价目表**，则使用 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="fdda2-155">**pricelevelid.name [价目表名称]** 的模板值是基于**币种**的 **ValueMap**。</span><span class="sxs-lookup"><span data-stu-id="fdda2-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="fdda2-156">美元：美国 CRM 服务（示例）。</span><span class="sxs-lookup"><span data-stu-id="fdda2-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="fdda2-157">SalesInvoiceLine 任务</span><span class="sxs-lookup"><span data-stu-id="fdda2-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="fdda2-158">确保在**源** > **度量单位的 CDS** 中存在所需的映射。</span><span class="sxs-lookup"><span data-stu-id="fdda2-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="fdda2-159">确保 Finance and Operations 中的 **SalesUnitSymbol** 所需的 **ValueMap** 在**源** > **CDS 映射**中存在。</span><span class="sxs-lookup"><span data-stu-id="fdda2-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="fdda2-160">使用 **ValueMap** 为 **SalesUnitSymbol 到数量 UOM** 定义模板值。</span><span class="sxs-lookup"><span data-stu-id="fdda2-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="fdda2-161">为**源中的 CDS 组织 ID** > **CDS** 更新映射。</span><span class="sxs-lookup"><span data-stu-id="fdda2-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="fdda2-162">**SalesInvoicer_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="fdda2-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="fdda2-163">**Product_Organization_OrganizationId** 的默认模板值是 ORG001。</span><span class="sxs-lookup"><span data-stu-id="fdda2-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="fdda2-164">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="fdda2-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="fdda2-165">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="fdda2-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="fdda2-166">映射这些字段必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="fdda2-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="fdda2-167">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="fdda2-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-2.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="fdda2-172">相关主题</span><span class="sxs-lookup"><span data-stu-id="fdda2-172">Related topics</span></span>

[<span data-ttu-id="fdda2-173">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="fdda2-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="fdda2-174">将 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fdda2-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="fdda2-175">将 Sales 的联系人同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="fdda2-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="fdda2-176">将 Sales 的销售报价单标题和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fdda2-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="fdda2-177">将 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="fdda2-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


