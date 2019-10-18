---
title: 将 Supply Chain Management 的产品直接同步到 Sales
description: 此主题介绍用于将产品从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Sales 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 06/10/2019
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
ms.openlocfilehash: 38f0db7db0cc4f65d46cd241f75a7274f19f62cf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251377"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="fb0db-103">将 Supply Chain Management 的产品直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="fb0db-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fb0db-104">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="fb0db-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="fb0db-105">此主题介绍用于将产品直接从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="fb0db-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="fb0db-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="fb0db-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="fb0db-107">“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="fb0db-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="fb0db-108">提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="fb0db-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="fb0db-109">下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="fb0db-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="fb0db-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="fb0db-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fb0db-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="fb0db-111">Templates and tasks</span></span>

<span data-ttu-id="fb0db-112">若要访问可用模板，打开 [PowerApps 管理员中心](https://admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="fb0db-112">To access the available templates, open [PowerApps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="fb0db-113">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="fb0db-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fb0db-114">以下模板和基础任务用于将产品从 Supply Chain Management 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="fb0db-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="fb0db-115">**数据集成中模板的名称：** 产品（Supply Chain Management 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="fb0db-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="fb0db-116">**数据集成项目中的任务名称：** 产品</span><span class="sxs-lookup"><span data-stu-id="fb0db-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="fb0db-117">不需要同步任务即可进行产品同步。</span><span class="sxs-lookup"><span data-stu-id="fb0db-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="fb0db-118">实体集</span><span class="sxs-lookup"><span data-stu-id="fb0db-118">Entity set</span></span>

| <span data-ttu-id="fb0db-119">供应链管理</span><span class="sxs-lookup"><span data-stu-id="fb0db-119">Supply Chain Management</span></span>    | <span data-ttu-id="fb0db-120">销售额</span><span class="sxs-lookup"><span data-stu-id="fb0db-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="fb0db-121">适售的已发布产品</span><span class="sxs-lookup"><span data-stu-id="fb0db-121">Sellable released products</span></span> | <span data-ttu-id="fb0db-122">产品</span><span class="sxs-lookup"><span data-stu-id="fb0db-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fb0db-123">实体流</span><span class="sxs-lookup"><span data-stu-id="fb0db-123">Entity flow</span></span>

<span data-ttu-id="fb0db-124">产品在 Supply Chain Management 中托管，并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="fb0db-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="fb0db-125">Supply Chain Management 中的**适售的已发布产品**数据实体只导出*适售*的产品。</span><span class="sxs-lookup"><span data-stu-id="fb0db-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="fb0db-126">适售产品是具有为用于销售订单而需要具备的信息的产品。</span><span class="sxs-lookup"><span data-stu-id="fb0db-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="fb0db-127">相同的规则适用于使用**已发布产品**页上的**验证**功能对产品进行验证时。</span><span class="sxs-lookup"><span data-stu-id="fb0db-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="fb0db-128">产品编号用作密钥。</span><span class="sxs-lookup"><span data-stu-id="fb0db-128">The product number is used as a key.</span></span> <span data-ttu-id="fb0db-129">因此，在产品变型同步到 Sales 时，每个产品变型都具有单独的产品 ID。</span><span class="sxs-lookup"><span data-stu-id="fb0db-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fb0db-130">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="fb0db-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="fb0db-131">在 Sales 中，新**外部维护**字段已添加到产品以指示特定产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="fb0db-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="fb0db-132">默认情况下，该值在导入到 Sales 期间设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="fb0db-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="fb0db-133">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="fb0db-133">The following values are available:</span></span>

- <span data-ttu-id="fb0db-134">**是** – 产品来自 Supply Chain Management，且不可在 Sales 中编辑。</span><span class="sxs-lookup"><span data-stu-id="fb0db-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="fb0db-135">**否** – 产品直接在 Sales 中输入。</span><span class="sxs-lookup"><span data-stu-id="fb0db-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="fb0db-136">**(空)** – 在启用“从目标客户到现金”解决方案前，产品存在于 Sales 中。</span><span class="sxs-lookup"><span data-stu-id="fb0db-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="fb0db-137">**外部维护**字段帮助确保仅具有外部维护的产品的报价单和销售订单将同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="fb0db-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="fb0db-138">外部维护的产品自动添加到具有相同币种的第一个有效的价目表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="fb0db-139">价目表按名称的字母顺序排列。</span><span class="sxs-lookup"><span data-stu-id="fb0db-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="fb0db-140">来自 Supply Chain Management 的产品销售价格用作价目表价格。</span><span class="sxs-lookup"><span data-stu-id="fb0db-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="fb0db-141">因此，在 Sales 中必须为 Supply Chain Management 中的每个产品销售币种存在一个价目表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="fb0db-142">已发布的适售产品上的币种设置为从中导出产品的法人的记帐币种。</span><span class="sxs-lookup"><span data-stu-id="fb0db-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="fb0db-143">产品同步不会成功，除非存在具有匹配币种的价目表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="fb0db-144">您可以通过在数据集成项目中映射 pricelevelid.name [Default Price List (Name)]，使用集成控制所用价目表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="fb0db-145">输入必须全部为小写字母。</span><span class="sxs-lookup"><span data-stu-id="fb0db-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="fb0db-146">例如，Sales 中名称为“Standard”的价目表的默认值为：目标字段：pricelevelid.name [Default Price List (Name)]，映射类型：[ { "transformType": "Default", "defaultValue": "standard" } ]。</span><span class="sxs-lookup"><span data-stu-id="fb0db-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fb0db-147">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="fb0db-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="fb0db-148">在首次运行同步前，必须在 Supply Chain Management 中为现有产品填充独特产品表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="fb0db-149">完成该作业前，现有产品不会同步。</span><span class="sxs-lookup"><span data-stu-id="fb0db-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="fb0db-150">在 Supply Chain Management 中，使用“搜索”搜索**填充独特产品表**。</span><span class="sxs-lookup"><span data-stu-id="fb0db-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="fb0db-151">选择**填充独特产品表**以运行作业。</span><span class="sxs-lookup"><span data-stu-id="fb0db-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="fb0db-152">此作业必须只运行一次。</span><span class="sxs-lookup"><span data-stu-id="fb0db-152">This job must be run only one time.</span></span>

- <span data-ttu-id="fb0db-153">确保在 **SalesUnitSymbol** 到 **DefaultUnit（名称）** 的映射中存在 Supply Chain Management 与 Sales 之间所需的销售度量单位 (UOM) 的值映射。</span><span class="sxs-lookup"><span data-stu-id="fb0db-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="fb0db-154">更新**单位组** (**defaultuomscheduleid.name**) 的值映射以便与 Sales 中的**单位组**匹配。</span><span class="sxs-lookup"><span data-stu-id="fb0db-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="fb0db-155">默认模板值是**默认单位**。</span><span class="sxs-lookup"><span data-stu-id="fb0db-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="fb0db-156">确保来自 Supply Chain Management 的所有产品销售 UOM 均在 Sales 中存在。</span><span class="sxs-lookup"><span data-stu-id="fb0db-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="fb0db-157">确保 Supply Chain Management 中的每个产品销售币种在 Sales 中存在价目表。</span><span class="sxs-lookup"><span data-stu-id="fb0db-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="fb0db-158">在 Sales 中创建产品时，它们可能具有**草稿**或**活动**状态。</span><span class="sxs-lookup"><span data-stu-id="fb0db-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="fb0db-159">行为在 Sales 的**设置** > **管理** > **系统设置** > **Sales** 中进行控制。</span><span class="sxs-lookup"><span data-stu-id="fb0db-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="fb0db-160">具有**草稿**状态的产品在创建后必须激活，才能被添加到报价单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="fb0db-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb0db-161">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="fb0db-161">Template mapping in Data integration</span></span>

<span data-ttu-id="fb0db-162">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="fb0db-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb0db-163">此映射显示将从 Sales 同步到 Supply Chain Management 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="fb0db-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![数据集成器中的模板映射](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="fb0db-165">相关主题</span><span class="sxs-lookup"><span data-stu-id="fb0db-165">Related topics</span></span>

[<span data-ttu-id="fb0db-166">现金的目标客户</span><span class="sxs-lookup"><span data-stu-id="fb0db-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="fb0db-167">将 Sales 的客户直接同步到 Supply Chain Management 中的客户</span><span class="sxs-lookup"><span data-stu-id="fb0db-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="fb0db-168">将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="fb0db-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="fb0db-169">将 Sales 的销售订单头和行直接从 Supply Chain Management 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="fb0db-169">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="fb0db-170">将销售发票头和行直接从 Supply Chain ManagementSupply Chain Management 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="fb0db-170">Synchronize sales invoice headers and lines directly from Supply Chain ManagementSupply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



