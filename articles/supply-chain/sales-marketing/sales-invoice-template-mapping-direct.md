---
title: 将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales
description: 本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的销售发票标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70fc842463254b02d812447f93970a9da676057d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "319492"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="2561b-103">将 Finance and Operations 的销售发票标题和行直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="2561b-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2561b-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的销售发票标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="2561b-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2561b-105">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="2561b-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2561b-106">“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="2561b-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="2561b-107">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="2561b-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2561b-108">下图显示 Finance and Operations 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="2561b-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2561b-109">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2561b-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2561b-110">模板和任务</span><span class="sxs-lookup"><span data-stu-id="2561b-110">Templates and tasks</span></span>

<span data-ttu-id="2561b-111">若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="2561b-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="2561b-112">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="2561b-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2561b-113">以下模板和基础任务用于将来自 Finance and Operations 的销售发票标题和行同步到 Sales：</span><span class="sxs-lookup"><span data-stu-id="2561b-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="2561b-114">**数据集成中模板的名称：** 销售发票（Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="2561b-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2561b-115">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="2561b-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2561b-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2561b-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="2561b-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2561b-117">SalesInvoiceLine</span></span>

<span data-ttu-id="2561b-118">在发生销售发票标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="2561b-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="2561b-119">产品（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="2561b-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2561b-120">帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="2561b-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2561b-121">联系人（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="2561b-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2561b-122">销售订单标题和行（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="2561b-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="2561b-123">实体集</span><span class="sxs-lookup"><span data-stu-id="2561b-123">Entity set</span></span>

| <span data-ttu-id="2561b-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2561b-124">Finance and Operations</span></span>                               | <span data-ttu-id="2561b-125">销售</span><span class="sxs-lookup"><span data-stu-id="2561b-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="2561b-126">外部维护的客户销售发票抬头</span><span class="sxs-lookup"><span data-stu-id="2561b-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="2561b-127">发票</span><span class="sxs-lookup"><span data-stu-id="2561b-127">Invoices</span></span>       |
| <span data-ttu-id="2561b-128">外部维护的客户销售发票行</span><span class="sxs-lookup"><span data-stu-id="2561b-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="2561b-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="2561b-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="2561b-130">实体流</span><span class="sxs-lookup"><span data-stu-id="2561b-130">Entity flow</span></span>

<span data-ttu-id="2561b-131">销售发票在 Finance and Operations 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="2561b-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="2561b-132">目前，与销售发票标题上的费用关联的税金不包括在从 Finance and Operations 到 Sales 的同步中。</span><span class="sxs-lookup"><span data-stu-id="2561b-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="2561b-133">Sales 不支持标题级别的税务信息。</span><span class="sxs-lookup"><span data-stu-id="2561b-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="2561b-134">但是，与行级别的费用相关的税包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="2561b-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2561b-135">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="2561b-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="2561b-136">**发票编号**字段已添加到**发票**实体中并显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="2561b-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="2561b-137">**销售订单**页上的**创建发票**按钮被隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="2561b-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="2561b-138">**发票**页不可编辑，因为发票将从 Finance and Operations 同步。</span><span class="sxs-lookup"><span data-stu-id="2561b-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="2561b-139">当关联的发票从 Finance and Operations 同步到 Sales 后，**销售订单状态**值自动更改为**已开票**。</span><span class="sxs-lookup"><span data-stu-id="2561b-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="2561b-140">而且，创建发票的销售订单的所有者被指定为发票的所有者。</span><span class="sxs-lookup"><span data-stu-id="2561b-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="2561b-141">因此，销售订单的所有者可以查看发票。</span><span class="sxs-lookup"><span data-stu-id="2561b-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2561b-142">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="2561b-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="2561b-143">在同步销售发票前，在系统中更新以下设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="2561b-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2561b-144">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="2561b-144">Setup in Sales</span></span>

<span data-ttu-id="2561b-145">转到**设置** > **管理** > **系统设置** > **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="2561b-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="2561b-146">**使用系统定价计算系统**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="2561b-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="2561b-147">**折扣计算方法**字段设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="2561b-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2561b-148">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="2561b-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="2561b-149">SalesInvoiceHeader 任务</span><span class="sxs-lookup"><span data-stu-id="2561b-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="2561b-150">确保存在所需的 **InvoiceCountryRegionId** 到 **BillingAddress\_Country** 的映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="2561b-151">模板值是多个国家或地区表在其中映射的值映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="2561b-152">在 Sales 中创建发票需要价目表。</span><span class="sxs-lookup"><span data-stu-id="2561b-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="2561b-153">将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。</span><span class="sxs-lookup"><span data-stu-id="2561b-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="2561b-154">您可以为单个币种使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="2561b-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="2561b-155">或者，如果您的价目表有多个币种，则可以使用值映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="2561b-156">**pricelevelid.name \[价目表名称\]** 的模板值是基于具有“USD = 美国 CRM 服务（示例）”的币种的值映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="2561b-157">SalesInvoiceLine 任务</span><span class="sxs-lookup"><span data-stu-id="2561b-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="2561b-158">确保存在所需的**度量单位**的映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="2561b-159">确保所需的 **SalesUnitSymbol** 的值映射在 Finance and Operations 中存在。</span><span class="sxs-lookup"><span data-stu-id="2561b-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="2561b-160">为 **SalesUnitSymbol** 到 **Quantity\_UOM** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="2561b-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2561b-161">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="2561b-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="2561b-162">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="2561b-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="2561b-163">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="2561b-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2561b-164">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="2561b-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="2561b-165">此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="2561b-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="2561b-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2561b-166">SalesInvoiceHeader</span></span>

![数据集成中的模板映射](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="2561b-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2561b-168">SalesInvoiceLine</span></span>

![数据集成中的模板映射](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="2561b-170">相关主题</span><span class="sxs-lookup"><span data-stu-id="2561b-170">Related topics</span></span>

[<span data-ttu-id="2561b-171">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="2561b-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="2561b-172">将直接来自 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2561b-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="2561b-173">将 Finance and Operations 的产品直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="2561b-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="2561b-174">将 Sales 的联系人直接同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="2561b-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="2561b-175">将直接来自 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="2561b-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)






