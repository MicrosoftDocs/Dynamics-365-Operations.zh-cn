---
title: "将来自 Finance and Operations 的销售订单标题和行直接同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="a9ac9-103">将来自 Finance and Operations 的销售订单标题和行直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="a9ac9-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a9ac9-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a9ac9-105">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="a9ac9-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a9ac9-106">“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="a9ac9-107">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="a9ac9-108">下图显示 Finance and Operations 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="a9ac9-109">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a9ac9-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a9ac9-110">模板和任务</span><span class="sxs-lookup"><span data-stu-id="a9ac9-110">Templates and tasks</span></span>

<span data-ttu-id="a9ac9-111">若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a9ac9-112">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a9ac9-113">以下模板和基础任务用于将来自 Finance and Operations 的销售订单标题和行同步到 Sales：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="a9ac9-114">**“数据集成”中模板的名称：**销售订单（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="a9ac9-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="a9ac9-115">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="a9ac9-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="a9ac9-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="a9ac9-116">OrderHeader</span></span>
    - <span data-ttu-id="a9ac9-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="a9ac9-117">OrderLine</span></span>

<span data-ttu-id="a9ac9-118">在发生销售发票标头和行同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="a9ac9-119">产品（从 Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="a9ac9-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="a9ac9-120">帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="a9ac9-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="a9ac9-121">从联系人到客户（从 Sales 到 Fin and Ops）- 直接（如果使用）</span><span class="sxs-lookup"><span data-stu-id="a9ac9-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="a9ac9-122">实体集</span><span class="sxs-lookup"><span data-stu-id="a9ac9-122">Entity set</span></span>

| <span data-ttu-id="a9ac9-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9ac9-123">Finance and Operations</span></span>  | <span data-ttu-id="a9ac9-124">销售</span><span class="sxs-lookup"><span data-stu-id="a9ac9-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="a9ac9-125">CDS 销售订单标题</span><span class="sxs-lookup"><span data-stu-id="a9ac9-125">CDS sales order headers</span></span> | <span data-ttu-id="a9ac9-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="a9ac9-126">SalesOrders</span></span>       |
| <span data-ttu-id="a9ac9-127">CDS 销售订单行</span><span class="sxs-lookup"><span data-stu-id="a9ac9-127">CDS sales order lines</span></span>   | <span data-ttu-id="a9ac9-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="a9ac9-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a9ac9-129">实体流</span><span class="sxs-lookup"><span data-stu-id="a9ac9-129">Entity flow</span></span>

<span data-ttu-id="a9ac9-130">销售订单在 Finance and Operations 中创建并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="a9ac9-131">模板中的筛选器帮助确保同步中只包括相关销售订单：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="a9ac9-132">在销售订单上，来自 Sales 的订购客户和开票客户都将包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="a9ac9-133">在 Finance and Operations 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 字段都用于跟踪数据实体中的同步。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="a9ac9-134">必须确认 Finance and Operations 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="a9ac9-135">仅已确认的销售订单或具有更高处理状态（如**已装运**或**已开票**）的销售订单同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="a9ac9-136">在创建或修改销售订单后，必须运行 Finance and Operations 中的**计算销售额总计**批处理作业。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="a9ac9-137">仅计算了销售总额的销售订单将被同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="a9ac9-138">目前，与销售订单头上的费用关联的税金不包括在从 Finance and Operations 到 Sales 的同步中。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="a9ac9-139">Sales 不支持标题级别的税务信息。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="a9ac9-140">但是，与行级别的费用相关的税包括在同步中。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a9ac9-141">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="a9ac9-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a9ac9-142">新字段已添加到**订单**实体并显示在以下页面：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="a9ac9-143">**外部维护** – 当订单来自 Finance and Operations 时将此选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="a9ac9-144">**处理状态** – 此字段显示订单在 Finance and Operations 中的处理状态。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="a9ac9-145">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-145">The following values are available:</span></span>

    - <span data-ttu-id="a9ac9-146">活动</span><span class="sxs-lookup"><span data-stu-id="a9ac9-146">Active</span></span>
    - <span data-ttu-id="a9ac9-147">已确认</span><span class="sxs-lookup"><span data-stu-id="a9ac9-147">Confirmed</span></span>
    - <span data-ttu-id="a9ac9-148">装箱单</span><span class="sxs-lookup"><span data-stu-id="a9ac9-148">Packing Slip</span></span>
    - <span data-ttu-id="a9ac9-149">已开票</span><span class="sxs-lookup"><span data-stu-id="a9ac9-149">Invoiced</span></span>
    - <span data-ttu-id="a9ac9-150">已领料</span><span class="sxs-lookup"><span data-stu-id="a9ac9-150">Picked</span></span>
    - <span data-ttu-id="a9ac9-151">已部分领料</span><span class="sxs-lookup"><span data-stu-id="a9ac9-151">Partially Picked</span></span>
    - <span data-ttu-id="a9ac9-152">已部分包装</span><span class="sxs-lookup"><span data-stu-id="a9ac9-152">Partially Packed</span></span>
    - <span data-ttu-id="a9ac9-153">已装运</span><span class="sxs-lookup"><span data-stu-id="a9ac9-153">Shipped</span></span>
    - <span data-ttu-id="a9ac9-154">已部分装运</span><span class="sxs-lookup"><span data-stu-id="a9ac9-154">Partially Shipped</span></span>
    - <span data-ttu-id="a9ac9-155">已部分开票</span><span class="sxs-lookup"><span data-stu-id="a9ac9-155">Partially Invoiced</span></span>
    - <span data-ttu-id="a9ac9-156">已取消</span><span class="sxs-lookup"><span data-stu-id="a9ac9-156">Cancelled</span></span>

<span data-ttu-id="a9ac9-157">**仅具有外部维护的产品**设置在其他销售订单方案（例如，从 Sales 到 Finance and Operation 的同步）中使用，以一致地跟踪销售订单是否全部由外部维护的产品构成。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="a9ac9-158">如果销售订单完全由外部维护的产品构成，则产品在 Finance and Operations 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="a9ac9-159">此设置有助于保障你不会尝试将具有未知产品的销售订单行同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="a9ac9-160">对于外部维护的订单，**销售订单**页上的**创建发票**、**取消订单**、**重新计算**、**获取产品**和**查找地址**按钮将隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="a9ac9-161">订单页不可编辑，因为将同步来自 Finance and Operations 的销售订单信息。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="a9ac9-162">销售订单的状态将保持为**活动**，以帮助确保来自 Finance and Operations 的更改可以流向 Sales 中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="a9ac9-163">若要控制此行为，在数据集成项目中将默认的**状态代码 \[Status\]** 值设置为**活动**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a9ac9-164">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="a9ac9-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="a9ac9-165">在同步销售订单前，更新系统中的下列设置十分重要。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="a9ac9-166">Sales 中的设置</span><span class="sxs-lookup"><span data-stu-id="a9ac9-166">Setup in Sales</span></span>

- <span data-ttu-id="a9ac9-167">确保为用户（来自 Sales 连接集）分配到的团队设置了权限。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="a9ac9-168">如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="a9ac9-169">如果当您从数据集成运行项目时团队还没有管理员访问权限，您将收到错误消息，指示缺少主体团队。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="a9ac9-170">转到**设置** > **安全** > **团队**，选择相关团队，选择**管理角色**，并选择具有所需权限的角色，如**系统管理员**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="a9ac9-171">转到**设置** > **管理** > **系统设置** > **Sales**，确保使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="a9ac9-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="a9ac9-172">**使用系统定价计算系统**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="a9ac9-173">**折扣计算方法**字段设置为**行项**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="a9ac9-174">Finance and Operations 中的设置</span><span class="sxs-lookup"><span data-stu-id="a9ac9-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="a9ac9-175">转到**销售和市场** > **定期任务** > **计算销售额总计**，设置作业以作为批处理作业运行。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="a9ac9-176">将**计算销售订单的总计**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="a9ac9-177">此步骤很重要，因为只有计算了销售额总计的销售订单才会同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="a9ac9-178">应根据销售订单同步的频率调整批处理作业的频率。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="a9ac9-179">数据集成项目中的设置</span><span class="sxs-lookup"><span data-stu-id="a9ac9-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="a9ac9-180">SalesHeader 任务</span><span class="sxs-lookup"><span data-stu-id="a9ac9-180">SalesHeader task</span></span>

- <span data-ttu-id="a9ac9-181">确保存在所需的 **InvoiceCountryRegionId** 到 **BillingAddress\_Country** 和 **DeliveryCountryRegionId** 到 **DeliveryAddress\_Country** 的映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="a9ac9-182">模板值是多个国家或地区表在其中映射的值映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="a9ac9-183">在 Sales 中创建订单需要价目表。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="a9ac9-184">将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="a9ac9-185">您可以为单个币种使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="a9ac9-186">或者，如果您的价目表有多个币种，则可以使用值映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="a9ac9-187">**pricelevelid.name \[价目表名称\]** 的默认模板值是**美国 CRM 服务（示例）**。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="a9ac9-188">SalesLine 任务</span><span class="sxs-lookup"><span data-stu-id="a9ac9-188">SalesLine task</span></span>

- <span data-ttu-id="a9ac9-189">确保存在所需的 **DeliveryCountryRegionId** 到 **DeliveryAddress\_Country** 的映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="a9ac9-190">模板值是多个国家或地区表在其中映射的值映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="a9ac9-191">确保所需的 **SalesUnitSymbol** 的值映射在 Finance and Operations 中存在。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="a9ac9-192">为 **SalesUnitSymbol** 到 **Quantity\_UOM** 定义了具有值映射的模板值。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a9ac9-193">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="a9ac9-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="a9ac9-194">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a9ac9-195">若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a9ac9-196">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a9ac9-197">此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="a9ac9-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="a9ac9-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="a9ac9-198">OrderHeader</span></span>

![数据集成器中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="a9ac9-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="a9ac9-200">OrderLine</span></span>

![数据集成器中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="a9ac9-202">相关主题</span><span class="sxs-lookup"><span data-stu-id="a9ac9-202">Related topics</span></span>

[<span data-ttu-id="a9ac9-203">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="a9ac9-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a9ac9-204">将直接来自 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9ac9-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a9ac9-205">将直接来自 Finance and Operations 的产品同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="a9ac9-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="a9ac9-206">将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="a9ac9-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="a9ac9-207">将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="a9ac9-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




