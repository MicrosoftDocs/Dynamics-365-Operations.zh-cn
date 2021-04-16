---
title: 将 Sales 的销售报价单标题和行直接同步到 Supply Chain Management
description: 本主题讨论用于将销售报价单标题和行直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。
author: ChristianRytt
ms.date: 10/25/2018
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838997"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="4918d-103">将 Sales 的销售报价单标题和行直接同步到 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4918d-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4918d-104">本主题讨论用于将销售报价单标题和行直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="4918d-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="4918d-105">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="4918d-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4918d-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="4918d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4918d-107">“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="4918d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="4918d-108">提供“数据集成”功能的“从目标客户到现金”模板启用 Supply Chain Management 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="4918d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="4918d-109">下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="4918d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="4918d-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4918d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="4918d-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="4918d-111">Template and tasks</span></span>

<span data-ttu-id="4918d-112">以下模板和基础任务用于将来自 Sales 的销售报价单标头和行直接同步到 Supply Chain Management：</span><span class="sxs-lookup"><span data-stu-id="4918d-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="4918d-113">**数据集成中模板的名称：** 销售报价（从 Sales 到 Supply Chain Management）- 直接</span><span class="sxs-lookup"><span data-stu-id="4918d-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="4918d-114">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="4918d-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4918d-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4918d-115">QuoteHeader</span></span>
    - <span data-ttu-id="4918d-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4918d-116">QuoteLine</span></span>

<span data-ttu-id="4918d-117">在发生销售报价单标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="4918d-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="4918d-118">产品（Supply Chain Management 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="4918d-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="4918d-119">科目（Sales 到 Supply Chain Management）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="4918d-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="4918d-120">从联系人到客户（Sales 到 Supply Chain Management）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="4918d-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="4918d-121">实体集</span><span class="sxs-lookup"><span data-stu-id="4918d-121">Entity set</span></span>

| <span data-ttu-id="4918d-122">销售额</span><span class="sxs-lookup"><span data-stu-id="4918d-122">Sales</span></span>        | <span data-ttu-id="4918d-123">供应链管理</span><span class="sxs-lookup"><span data-stu-id="4918d-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="4918d-124">报价</span><span class="sxs-lookup"><span data-stu-id="4918d-124">Quotes</span></span>       | <span data-ttu-id="4918d-125">Dataverse 销售报价单标题</span><span class="sxs-lookup"><span data-stu-id="4918d-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="4918d-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="4918d-126">QuoteDetails</span></span> | <span data-ttu-id="4918d-127">Dataverse 销售报价单行</span><span class="sxs-lookup"><span data-stu-id="4918d-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="4918d-128">实体流</span><span class="sxs-lookup"><span data-stu-id="4918d-128">Entity flow</span></span>

<span data-ttu-id="4918d-129">销售报价单在 Sales 中创建并同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4918d-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="4918d-130">仅当满足以下条件时，来自 Sales 的销售报价单同步：</span><span class="sxs-lookup"><span data-stu-id="4918d-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="4918d-131">销售报价单上的所有报价产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="4918d-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="4918d-132">在您单击 **激活报价** 后，销售报价单是活动的。</span><span class="sxs-lookup"><span data-stu-id="4918d-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4918d-133">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="4918d-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4918d-134">**仅具有外部维护的产品** 字段已添加到 **报价** 实体以一致地跟踪销售报价单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="4918d-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="4918d-135">如果销售报价单只具有外部维护的产品，则产品在 Supply Chain Management 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="4918d-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="4918d-136">此行为有助于保障你不会尝试将具有未知产品的销售报价单行同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4918d-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="4918d-137">销售报价单上的所有报价产品均使用来自销售报价单标头的 **仅具有外部维护的产品** 信息进行更新。</span><span class="sxs-lookup"><span data-stu-id="4918d-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="4918d-138">此信息可在 **QuoteDetails** 实体上的 **报价仅具有外部维护的产品** 字段中找到。</span><span class="sxs-lookup"><span data-stu-id="4918d-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="4918d-139">折扣可以添加到报价产品，并且同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4918d-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="4918d-140">标题上的 **折扣**、**费用** 和 **税金** 字段由 Supply Chain Management 中的设置控制。</span><span class="sxs-lookup"><span data-stu-id="4918d-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="4918d-141">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="4918d-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4918d-142">在当前设计中，**价格**、**折扣**、**费用** 和 **税金** 字段在 Supply Chain Management 中维护和处理。</span><span class="sxs-lookup"><span data-stu-id="4918d-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="4918d-143">在 Sales 中，由于值未同步到 Supply Chain Management，因此该解决方案使以下字段只读：</span><span class="sxs-lookup"><span data-stu-id="4918d-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="4918d-144">销售报价单标题上的只读字段：**折扣 %**、**折扣** 和 **运费**</span><span class="sxs-lookup"><span data-stu-id="4918d-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="4918d-145">报价产品的只读字段：**税**</span><span class="sxs-lookup"><span data-stu-id="4918d-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4918d-146">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="4918d-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="4918d-147">在同步销售报价单前，更新下列设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="4918d-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="4918d-148">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="4918d-148">Setup in Sales</span></span>

- <span data-ttu-id="4918d-149">确保为用户（来自 Sales 中的连接集）分配到的团队设置了权限。</span><span class="sxs-lookup"><span data-stu-id="4918d-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="4918d-150">如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="4918d-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="4918d-151">如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。</span><span class="sxs-lookup"><span data-stu-id="4918d-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="4918d-152">若要为团队设置权限，转到 **设置** &gt; **安全** &gt; **团队**，然后选择相关团队。</span><span class="sxs-lookup"><span data-stu-id="4918d-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="4918d-153">选择 **管理角色**，然后选择具有所需权限的角色，如 **系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="4918d-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="4918d-154">转到 **设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="4918d-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="4918d-155">**使用系统定价计算系统** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4918d-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="4918d-156">**折扣计算方法** 字段设置为 **行项**。</span><span class="sxs-lookup"><span data-stu-id="4918d-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="4918d-157">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="4918d-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="4918d-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4918d-158">QuoteHeader</span></span>

- <span data-ttu-id="4918d-159">确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。</span><span class="sxs-lookup"><span data-stu-id="4918d-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="4918d-160">在值映射中，您可以定义值为空时使用的默认值。</span><span class="sxs-lookup"><span data-stu-id="4918d-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="4918d-161">只需让左侧留空，将右侧设置为所需的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="4918d-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="4918d-162">这样，您不必为国家订单键入国家或地区。</span><span class="sxs-lookup"><span data-stu-id="4918d-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="4918d-163">模板值是映射了多个国家或地区的值映射，其中的空值为值 **US**。</span><span class="sxs-lookup"><span data-stu-id="4918d-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="4918d-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4918d-164">QuoteLine</span></span>

- <span data-ttu-id="4918d-165">确保在 Supply Chain Management 中存在所需的 **SalesUnitSymbol** 值映射。</span><span class="sxs-lookup"><span data-stu-id="4918d-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="4918d-166">确保所需单位已在 Sales 中定义。</span><span class="sxs-lookup"><span data-stu-id="4918d-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="4918d-167">为 **oumid.name** 到 **SalesUnitSymbol** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="4918d-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="4918d-168">可选：您可以添加以下映射以帮助保障在没有来自客户或产品的默认信息时将销售报价单行导入到 Supply Chain Management 中：</span><span class="sxs-lookup"><span data-stu-id="4918d-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="4918d-169">**SiteId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的站点。</span><span class="sxs-lookup"><span data-stu-id="4918d-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="4918d-170">**SiteId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="4918d-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="4918d-171">**WarehouseId** - 在 Supply Chain Management 中处理报价单和销售订单行所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="4918d-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="4918d-172">**WarehouseId** 没有默认模板值。</span><span class="sxs-lookup"><span data-stu-id="4918d-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4918d-173">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="4918d-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="4918d-174">**折扣**、**费用** 和 **税金** 字段由 Supply Chain Management 中的复杂设置控制。</span><span class="sxs-lookup"><span data-stu-id="4918d-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="4918d-175">此设置当前不支持集成映射。</span><span class="sxs-lookup"><span data-stu-id="4918d-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="4918d-176">在当前设计中，**价格**、**折扣**、**费用** 和 **税金** 字段由 Supply Chain Management 处理。</span><span class="sxs-lookup"><span data-stu-id="4918d-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="4918d-177">**付款期限**、**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 字段不是默认映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="4918d-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="4918d-178">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="4918d-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="4918d-179">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="4918d-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="4918d-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="4918d-180">QuoteHeader</span></span>

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="4918d-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="4918d-182">QuoteLine</span></span>

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4918d-184">相关主题</span><span class="sxs-lookup"><span data-stu-id="4918d-184">Related topics</span></span>

[<span data-ttu-id="4918d-185">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="4918d-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]