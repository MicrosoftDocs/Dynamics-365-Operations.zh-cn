---
title: "将 Sales 的销售报价单标题和行直接同步到 Finance and Operations"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标头和行直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 77b15a51073bf923f09a4a0e83ee5b2642eec4af
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="e4618-103">将 Sales 的销售报价单标题和行直接同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4618-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4618-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标头和行直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="e4618-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e4618-105">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="e4618-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="e4618-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="e4618-106">Template and tasks</span></span>

<span data-ttu-id="e4618-107">以下模板和基础任务用于将来自 Sales 的销售报价单标头和行直接同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="e4618-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="e4618-108">**“数据集成”中模板的名称：** 销售报价（从 Sales 到 Fin and Ops）- 直接</span><span class="sxs-lookup"><span data-stu-id="e4618-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="e4618-109">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="e4618-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e4618-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e4618-110">QuoteHeader</span></span>
    - <span data-ttu-id="e4618-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e4618-111">QuoteLine</span></span>

<span data-ttu-id="e4618-112">在发生销售报价单标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="e4618-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e4618-113">产品（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="e4618-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e4618-114">帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="e4618-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e4618-115">从联系人到客户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="e4618-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e4618-116">实体集</span><span class="sxs-lookup"><span data-stu-id="e4618-116">Entity set</span></span>

| <span data-ttu-id="e4618-117">销售</span><span class="sxs-lookup"><span data-stu-id="e4618-117">Sales</span></span>        | <span data-ttu-id="e4618-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4618-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="e4618-119">报价</span><span class="sxs-lookup"><span data-stu-id="e4618-119">Quotes</span></span>       | <span data-ttu-id="e4618-120">CDS 销售报价单标题</span><span class="sxs-lookup"><span data-stu-id="e4618-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="e4618-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e4618-121">QuoteDetails</span></span> | <span data-ttu-id="e4618-122">CDS 销售报价单行</span><span class="sxs-lookup"><span data-stu-id="e4618-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="e4618-123">实体流</span><span class="sxs-lookup"><span data-stu-id="e4618-123">Entity flow</span></span>

<span data-ttu-id="e4618-124">销售报价单在 Sales 中创建并同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="e4618-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="e4618-125">仅当满足以下条件时，来自 Sales 的销售报价单同步：</span><span class="sxs-lookup"><span data-stu-id="e4618-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e4618-126">销售报价单上的所有报价产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="e4618-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="e4618-127">在您单击**激活报价**后，销售报价单是活动的。</span><span class="sxs-lookup"><span data-stu-id="e4618-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e4618-128">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="e4618-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e4618-129">**仅具有外部维护的产品**字段已添加到**报价**实体以一致地跟踪销售报价单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="e4618-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e4618-130">如果销售报价单只具有外部维护的产品，则产品在 Finance and Operations 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="e4618-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e4618-131">此行为有助于保障你不会尝试将具有未知产品的销售报价单行同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="e4618-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e4618-132">销售报价单上的所有报价产品均使用来自销售报价单标头的**仅具有外部维护的产品**信息进行更新。</span><span class="sxs-lookup"><span data-stu-id="e4618-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="e4618-133">此信息可在 **QuoteDetails** 实体上的**报价仅具有外部维护的产品**字段中找到。</span><span class="sxs-lookup"><span data-stu-id="e4618-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="e4618-134">折扣可以添加到报价产品，并且同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="e4618-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="e4618-135">标题上的**折扣**、**费用**和**税金**字段由 Finance and Operations 中的设置控制。</span><span class="sxs-lookup"><span data-stu-id="e4618-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="e4618-136">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="e4618-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e4618-137">在当前设计中,**价格**、**折扣**、**费用**和**税金**字段在 Finance and Operations 中维护和处理。</span><span class="sxs-lookup"><span data-stu-id="e4618-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="e4618-138">在 Sales 中，由于值未同步到 Finance and Operations，因此该解决方案使以下字段只读：</span><span class="sxs-lookup"><span data-stu-id="e4618-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="e4618-139">销售报价单标题上的只读字段：**折扣 %**、**折扣**和**运费**</span><span class="sxs-lookup"><span data-stu-id="e4618-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="e4618-140">报价产品的只读字段：**税**</span><span class="sxs-lookup"><span data-stu-id="e4618-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e4618-141">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="e4618-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="e4618-142">在同步销售报价单前，更新下列设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="e4618-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e4618-143">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="e4618-143">Setup in Sales</span></span>

- <span data-ttu-id="e4618-144">确保为用户（来自 Sales 中的连接集）分配到的团队设置了权限。</span><span class="sxs-lookup"><span data-stu-id="e4618-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="e4618-145">如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="e4618-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e4618-146">如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。</span><span class="sxs-lookup"><span data-stu-id="e4618-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e4618-147">若要为团队设置权限，转到**设置** &gt; **安全** &gt; **团队**，然后选择相关团队。</span><span class="sxs-lookup"><span data-stu-id="e4618-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="e4618-148">选择**管理角色**，然后选择具有所需权限的角色，如**系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="e4618-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e4618-149">转到**设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="e4618-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e4618-150">**使用系统定价计算系统**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e4618-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e4618-151">**折扣计算方法**字段设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="e4618-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e4618-152">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="e4618-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e4618-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e4618-153">QuoteHeader</span></span>

- <span data-ttu-id="e4618-154">确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。</span><span class="sxs-lookup"><span data-stu-id="e4618-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e4618-155">在值映射中，您可以定义值为空时使用的默认值。</span><span class="sxs-lookup"><span data-stu-id="e4618-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="e4618-156">只需让左侧留空，将右侧设置为所需的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="e4618-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="e4618-157">这样，您不必为国家订单键入国家或地区。</span><span class="sxs-lookup"><span data-stu-id="e4618-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="e4618-158">模板值是映射了多个国家或地区的值映射，其中的空值为值 **US**。</span><span class="sxs-lookup"><span data-stu-id="e4618-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e4618-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e4618-159">QuoteLine</span></span>

- <span data-ttu-id="e4618-160">确保所需的 **SalesUnitSymbol** 值映射在 Finance and Operations 中存在。</span><span class="sxs-lookup"><span data-stu-id="e4618-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="e4618-161">确保所需单位已在 Sales 中定义。</span><span class="sxs-lookup"><span data-stu-id="e4618-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e4618-162">为 **oumid.name** 到 **SalesUnitSymbol** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="e4618-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="e4618-163">可选：您可以添加以下映射以帮助保障在没有来自客户或产品的默认信息时将销售报价单行导入到 Finance and Operations 中：</span><span class="sxs-lookup"><span data-stu-id="e4618-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e4618-164">**SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。</span><span class="sxs-lookup"><span data-stu-id="e4618-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e4618-165">**SiteId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="e4618-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e4618-166">**WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="e4618-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e4618-167">**WarehouseId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="e4618-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e4618-168">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="e4618-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e4618-169">**折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。</span><span class="sxs-lookup"><span data-stu-id="e4618-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e4618-170">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="e4618-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e4618-171">在当前设计中，**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 处理。</span><span class="sxs-lookup"><span data-stu-id="e4618-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="e4618-172">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="e4618-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e4618-173">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="e4618-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e4618-174">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="e4618-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e4618-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e4618-175">QuoteHeader</span></span>

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="e4618-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e4618-177">QuoteLine</span></span>

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e4618-179">相关主题</span><span class="sxs-lookup"><span data-stu-id="e4618-179">Related topics</span></span>

[<span data-ttu-id="e4618-180">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="e4618-180">Prospect to cash</span></span>](prospect-to-cash.md)


