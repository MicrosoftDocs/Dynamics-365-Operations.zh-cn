---
title: "将来自 Sales 的销售报价单标头和行同步到 Finance and Operations"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标头和行同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的模板和基础任务。"
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="e2ae4-103">将来自 Sales 的销售报价单标头和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2ae4-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="e2ae4-104">在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="e2ae4-105">本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的销售报价单标头和行同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="e2ae4-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="e2ae4-106">Template and tasks</span></span>

<span data-ttu-id="e2ae4-107">以下模板和基础任务用于将来自 Sales 的销售报价单标头和行同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="e2ae4-108">**模板名称：**销售报价（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="e2ae4-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="e2ae4-109">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="e2ae4-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="e2ae4-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e2ae4-110">QuoteHeader</span></span>
    - <span data-ttu-id="e2ae4-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e2ae4-111">QuoteLine</span></span>

<span data-ttu-id="e2ae4-112">在发生销售报价单标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e2ae4-113">产品（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="e2ae4-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="e2ae4-114">帐户（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="e2ae4-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="e2ae4-115">从联系人到客户（从 Sales 到 Fin and Ops）（如果使用）</span><span class="sxs-lookup"><span data-stu-id="e2ae4-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e2ae4-116">实体集</span><span class="sxs-lookup"><span data-stu-id="e2ae4-116">Entity set</span></span>

| <span data-ttu-id="e2ae4-117">销售</span><span class="sxs-lookup"><span data-stu-id="e2ae4-117">Sales</span></span>        | <span data-ttu-id="e2ae4-118">CDS</span><span class="sxs-lookup"><span data-stu-id="e2ae4-118">CDS</span></span>           | <span data-ttu-id="e2ae4-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2ae4-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="e2ae4-120">报价</span><span class="sxs-lookup"><span data-stu-id="e2ae4-120">Quotes</span></span>       | <span data-ttu-id="e2ae4-121">报价</span><span class="sxs-lookup"><span data-stu-id="e2ae4-121">Quotation</span></span>     | <span data-ttu-id="e2ae4-122">销售报价单标头</span><span class="sxs-lookup"><span data-stu-id="e2ae4-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="e2ae4-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e2ae4-123">QuoteDetails</span></span> | <span data-ttu-id="e2ae4-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="e2ae4-124">QuotationLine</span></span> | <span data-ttu-id="e2ae4-125">CDS 销售报价单行</span><span class="sxs-lookup"><span data-stu-id="e2ae4-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e2ae4-126">实体流</span><span class="sxs-lookup"><span data-stu-id="e2ae4-126">Entity flow</span></span>

<span data-ttu-id="e2ae4-127">销售报价单在 Sales 中创建并同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="e2ae4-128">仅当满足以下条件时，来自 Sales 的销售报价单同步：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e2ae4-129">销售报价单行上的所有产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="e2ae4-130">销售报价单有效或已激活。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e2ae4-131">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="e2ae4-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e2ae4-132">**仅具有外部维护的产品**字段已添加到报价实体以一致地跟踪销售报价单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e2ae4-133">如果销售报价单只具有外部维护的产品，则产品在 Finance and Operations 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-134">此行为有助于保障你不会尝试将具有未知产品的销售报价单行同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e2ae4-135">报价单上的所有产品和行使用来自报价单标头的**仅具有外部维护的产品**信息进行更新。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="e2ae4-136">此信息可在报价单行实体上的**报价仅具有外部维护的产品**字段找到。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="e2ae4-137">**折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-138">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="e2ae4-139">在当前设计中,**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 掌握和处理。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="e2ae4-140">在 Sales 中，由于值未同步到 Finance and Operations，因此该解决方案使以下字段只读：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="e2ae4-141">**销售报价单标头上的只读字段：**折扣 %、折扣和运费</span><span class="sxs-lookup"><span data-stu-id="e2ae4-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="e2ae4-142">**销售报价单行上的只读字段：**税金</span><span class="sxs-lookup"><span data-stu-id="e2ae4-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e2ae4-143">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="e2ae4-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="e2ae4-144">在同步销售订单前，使用下列设置更新系统十分重要：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e2ae4-145">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="e2ae4-145">Setup in Sales</span></span>

- <span data-ttu-id="e2ae4-146">转到**设置** &gt; **管理** &gt; **系统设置** &gt; **销售**，并确保**折扣计算方法**字段设置为**每单位**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="e2ae4-147">此设置有助于保障来自 Sales 的行项折扣与 Finance and Operations 中的设置匹配。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-148">否则，折扣在 Finance and Operations 中不正确，因为 Finance and Operations 会将折扣读取为每单位折扣，即使它在 Sales 中是每行折扣。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="e2ae4-149">Finance and Operations 中的设置</span><span class="sxs-lookup"><span data-stu-id="e2ae4-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="e2ae4-150">转至**应收账款** &gt; **设置** &gt; **应收账款参数**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="e2ae4-151">在**编号规则**选项卡上，选择销售报价单的编号规则，然后单击**查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="e2ae4-152">然后，在**一般设置**下，将**手动**字段设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="e2ae4-153">转至**应收账款** &gt; **设置** &gt; **应收账款参数**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="e2ae4-154">然后，在**装运**选项卡上，将**交货日期控制**字段设置为**无**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="e2ae4-155">此设置帮助防止对销售报价单的同步失败。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e2ae4-156">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="e2ae4-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e2ae4-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e2ae4-157">QuoteHeader</span></span>

- <span data-ttu-id="e2ae4-158">**请求交货日期**字段在 Finance and Operations 中必填，如果将该字段保留为空，同步将失败。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="e2ae4-159">为了防止出现该问题，如果将该字段保留为空，则从**源 &gt; CDS** 中提取默认日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="e2ae4-160">日期应更新到一个首选值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="e2ae4-161">目前，不能输入一个值（例如**当天**）表示当天的日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="e2ae4-162">必须输入特定日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-162">You must enter a specific date.</span></span> <span data-ttu-id="e2ae4-163">**请求交货日期**的默认模板值是 **1/1/2020**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="e2ae4-164">**地址国家/地区代码**字段在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-165">为了帮助防止同步错误，你可以指定当该字段在 Sales 中保留为空时要使用的默认值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="e2ae4-166">此默认值也有用，因为你无需在本地地址的**国家/地区**字段中手动输入一个值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="e2ae4-167">**DeliveryAddressCountryRegionISOCode** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="e2ae4-168">在**源 &gt; CDS** 中更新 **CDS 组织 ID** 的映射，使其与组织实体中的 **CDS 组织**匹配：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="e2ae4-169">**Organization_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="e2ae4-170">**Account_Organization_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="e2ae4-171">**InvoiceAccount_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e2ae4-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e2ae4-172">QuoteLine</span></span>

- <span data-ttu-id="e2ae4-173">在**源 &gt; CDS** 中更新 **CDS 组织 ID** 的映射，使其与组织实体中的 **CDS 组织**匹配：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="e2ae4-174">**Organization_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="e2ae4-175">**Product_Organization_Organization_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="e2ae4-176">**Quotation_Organization_Organization_OrganizationId** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="e2ae4-177">**请求交货日期**字段在 Finance and Operations 中必填，如果将该字段保留为空，同步将失败。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="e2ae4-178">为了防止出现该问题，如果将该字段保留为空，则从**源 &gt; CDS** 中提取默认日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="e2ae4-179">日期应更新到一个首选值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="e2ae4-180">目前，不能输入一个值（例如**当天**）表示当天的日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="e2ae4-181">必须输入特定日期。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-181">You must enter a specific date.</span></span> <span data-ttu-id="e2ae4-182">**请求交货日期**的默认模板值是 **1/1/2020**。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="e2ae4-183">你可以从 **CDS &gt; 目标**添加以下映射以帮助保障在没有来自客户或产品的默认信息时将报价单行导入到 Finance and Operations 中：</span><span class="sxs-lookup"><span data-stu-id="e2ae4-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e2ae4-184">**SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-185">**SiteId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e2ae4-186">**WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-187">**WarehouseId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="e2ae4-188">确保在 Finance and Operations 中所需的用于销售度量单位 (UOM) 的值映射在用于从 **Quantity_UOM** 到 **SALESUNITSYMBOL** 的 **CDS &gt; 目标**映射中存在。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e2ae4-189">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="e2ae4-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e2ae4-190">**折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e2ae4-191">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="e2ae4-192">在当前设计中，**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 处理。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="e2ae4-193">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e2ae4-194">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e2ae4-195">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="e2ae4-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e2ae4-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e2ae4-196">QuoteHeader</span></span>

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="e2ae4-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e2ae4-199">QuoteLine</span></span>

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="e2ae4-202">相关主题</span><span class="sxs-lookup"><span data-stu-id="e2ae4-202">Related topics</span></span>

[<span data-ttu-id="e2ae4-203">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="e2ae4-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="e2ae4-204">将 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2ae4-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="e2ae4-205">将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="e2ae4-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



