---
title: 将直接来自 Finance and Operations 的产品同步到 Sales
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Sales 的产品的模板和基础任务。
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
ms.openlocfilehash: ff284585a2eb4c5cf55d2e3a3e0f317d1fb218bb
ms.sourcegitcommit: 51dc11919fcb2324482b48cc4ce4484945ade803
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624327"
---
# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="15bb6-103">将 Finance and Operations 的产品直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="15bb6-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="15bb6-104">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="15bb6-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="15bb6-105">此主题介绍用于直接同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Sales 的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="15bb6-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="15bb6-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="15bb6-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="15bb6-107">“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="15bb6-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="15bb6-108">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="15bb6-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="15bb6-109">下图显示 Finance and Operations 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="15bb6-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="15bb6-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="15bb6-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="15bb6-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="15bb6-111">Templates and tasks</span></span>

<span data-ttu-id="15bb6-112">若要访问可用模板，打开 [PowerApps 管理员中心](https://admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="15bb6-112">To access the available templates, open [PowerApps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="15bb6-113">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="15bb6-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="15bb6-114">以下模板和基础任务用于将来自 Finance and Operations 的产品同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="15bb6-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="15bb6-115">**数据集成中模板的名称：** 产品（Fin and Ops 到 Sales）- 直接</span><span class="sxs-lookup"><span data-stu-id="15bb6-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="15bb6-116">**数据集成项目中的任务名称：** 产品</span><span class="sxs-lookup"><span data-stu-id="15bb6-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="15bb6-117">不需要同步任务即可进行产品同步。</span><span class="sxs-lookup"><span data-stu-id="15bb6-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="15bb6-118">实体集</span><span class="sxs-lookup"><span data-stu-id="15bb6-118">Entity set</span></span>

| <span data-ttu-id="15bb6-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15bb6-119">Finance and Operations</span></span>     | <span data-ttu-id="15bb6-120">销售</span><span class="sxs-lookup"><span data-stu-id="15bb6-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="15bb6-121">适售的已发布产品</span><span class="sxs-lookup"><span data-stu-id="15bb6-121">Sellable released products</span></span> | <span data-ttu-id="15bb6-122">产品</span><span class="sxs-lookup"><span data-stu-id="15bb6-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="15bb6-123">实体流</span><span class="sxs-lookup"><span data-stu-id="15bb6-123">Entity flow</span></span>

<span data-ttu-id="15bb6-124">产品在 Finance and Operations 中进行托管并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="15bb6-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="15bb6-125">Finance and Operations 中的**适售的已发布产品**数据实体只导出*适售*的产品。</span><span class="sxs-lookup"><span data-stu-id="15bb6-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="15bb6-126">适售产品是具有为用于销售订单而需要具备的信息的产品。</span><span class="sxs-lookup"><span data-stu-id="15bb6-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="15bb6-127">相同的规则适用于使用**已发布产品**页上的**验证**功能对产品进行验证时。</span><span class="sxs-lookup"><span data-stu-id="15bb6-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="15bb6-128">产品编号用作密钥。</span><span class="sxs-lookup"><span data-stu-id="15bb6-128">The product number is used as a key.</span></span> <span data-ttu-id="15bb6-129">因此，在产品变型同步到 Sales 时，每个产品变型都具有单独的产品 ID。</span><span class="sxs-lookup"><span data-stu-id="15bb6-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="15bb6-130">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="15bb6-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="15bb6-131">在 Sales 中，新**外部维护**字段已添加到产品以指示特定产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="15bb6-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="15bb6-132">默认情况下，该值在导入到 Sales 期间设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="15bb6-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="15bb6-133">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="15bb6-133">The following values are available:</span></span>

- <span data-ttu-id="15bb6-134">**是** – 产品来自 Finance and Operations，且不可在 Sales 中编辑。</span><span class="sxs-lookup"><span data-stu-id="15bb6-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="15bb6-135">**否** – 产品直接在 Sales 中输入。</span><span class="sxs-lookup"><span data-stu-id="15bb6-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="15bb6-136">**(空)** – 在启用“从目标客户到现金”解决方案前，产品存在于 Sales 中。</span><span class="sxs-lookup"><span data-stu-id="15bb6-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="15bb6-137">**外部维护**字段帮助确保仅具有外部维护的产品的报价单和销售订单将同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="15bb6-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="15bb6-138">外部维护的产品自动添加到具有相同币种的第一个有效的价目表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="15bb6-139">价目表按名称的字母顺序排列。</span><span class="sxs-lookup"><span data-stu-id="15bb6-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="15bb6-140">来自 Finance and Operations 的产品销售价格用作价目表价格。</span><span class="sxs-lookup"><span data-stu-id="15bb6-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="15bb6-141">因此，在 Sales 中必须为 Finance and Operations 中的每个产品销售币种存在一个价目表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="15bb6-142">已发布的适售产品上的币种设置为从中导出产品的法人的记帐币种。</span><span class="sxs-lookup"><span data-stu-id="15bb6-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="15bb6-143">产品同步不会成功，除非存在具有匹配币种的价目表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="15bb6-144">您可以通过在数据集成项目中映射 pricelevelid.name [Default Price List (Name)]，使用集成控制所用价目表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="15bb6-145">输入必须全部为小写字母。</span><span class="sxs-lookup"><span data-stu-id="15bb6-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="15bb6-146">例如，Sales 中名称为“Standard”的价目表的默认值为：目标字段：pricelevelid.name [Default Price List (Name)]，映射类型：[ { "transformType": "Default", "defaultValue": "standard" } ]。</span><span class="sxs-lookup"><span data-stu-id="15bb6-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="15bb6-147">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="15bb6-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="15bb6-148">在首次运行同步前，必须在 Finance and Operations 中为现有产品填充独特产品表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="15bb6-149">完成该作业前，现有产品不会同步。</span><span class="sxs-lookup"><span data-stu-id="15bb6-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="15bb6-150">在 Finance and Operations 中，使用“搜索”搜索**填充独特产品表**。</span><span class="sxs-lookup"><span data-stu-id="15bb6-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="15bb6-151">选择**填充独特产品表**以运行作业。</span><span class="sxs-lookup"><span data-stu-id="15bb6-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="15bb6-152">此作业必须只运行一次。</span><span class="sxs-lookup"><span data-stu-id="15bb6-152">This job must be run only one time.</span></span>

- <span data-ttu-id="15bb6-153">确保在 **SalesUnitSymbol** 到 **DefaultUnit（名称）** 的映射中存在 Finance and Operations 与 Sales 之间所需的销售度量单位 (UOM) 的值映射。</span><span class="sxs-lookup"><span data-stu-id="15bb6-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="15bb6-154">更新**单位组** (**defaultuomscheduleid.name**) 的值映射以便与 Sales 中的**单位组**匹配。</span><span class="sxs-lookup"><span data-stu-id="15bb6-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="15bb6-155">默认模板值是**默认单位**。</span><span class="sxs-lookup"><span data-stu-id="15bb6-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="15bb6-156">确保来自 Finance and Operations 的所有产品销售 UOM 均在 Sales 中存在。</span><span class="sxs-lookup"><span data-stu-id="15bb6-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="15bb6-157">确保 Finance and Operations 中的每个产品销售币种在 Sales 中存在价目表。</span><span class="sxs-lookup"><span data-stu-id="15bb6-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="15bb6-158">在 Sales 中创建产品时，它们可能具有**草稿**或**活动**状态。</span><span class="sxs-lookup"><span data-stu-id="15bb6-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="15bb6-159">行为在 Sales 的**设置** > **管理** > **系统设置** > **Sales** 中进行控制。</span><span class="sxs-lookup"><span data-stu-id="15bb6-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="15bb6-160">具有**草稿**状态的产品在创建后必须激活，才能被添加到报价单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="15bb6-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="15bb6-161">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="15bb6-161">Template mapping in Data integration</span></span>

<span data-ttu-id="15bb6-162">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="15bb6-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="15bb6-163">此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="15bb6-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![数据集成器中的模板映射](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="15bb6-165">相关主题</span><span class="sxs-lookup"><span data-stu-id="15bb6-165">Related topics</span></span>

[<span data-ttu-id="15bb6-166">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="15bb6-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="15bb6-167">将直接来自 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15bb6-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="15bb6-168">将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="15bb6-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="15bb6-169">将 Finance and Operations 的销售订单标题和行直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="15bb6-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="15bb6-170">将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="15bb6-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



