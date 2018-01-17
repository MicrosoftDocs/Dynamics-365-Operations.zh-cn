---
title: "将来自 Finance and Operations 的产品同步到 Sales 中的产品"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的产品同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b949701604d0cbca2728a0055d52f7385106082b
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="0beed-103">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="0beed-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0beed-104">在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="0beed-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0beed-105">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的产品同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="0beed-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="0beed-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="0beed-106">Template and task</span></span>

<span data-ttu-id="0beed-107">以下模板和基础任务用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的产品同步到 Microsoft Dynamics 365 for Sales (Sales)。</span><span class="sxs-lookup"><span data-stu-id="0beed-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="0beed-108">模板名称：产品（从 Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="0beed-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="0beed-109">项目中的任务名称：产品</span><span class="sxs-lookup"><span data-stu-id="0beed-109">Name of task in project: Products</span></span>

<span data-ttu-id="0beed-110">在产品同步之前所需的同步任务：无</span><span class="sxs-lookup"><span data-stu-id="0beed-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="0beed-111">实体集</span><span class="sxs-lookup"><span data-stu-id="0beed-111">Entity set</span></span>

| <span data-ttu-id="0beed-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="0beed-112">**Finance and Operations**</span></span> | <span data-ttu-id="0beed-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="0beed-113">**CDS**</span></span> | <span data-ttu-id="0beed-114">**销售**</span><span class="sxs-lookup"><span data-stu-id="0beed-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="0beed-115">适售的已发布产品</span><span class="sxs-lookup"><span data-stu-id="0beed-115">Sellable released products</span></span> | <span data-ttu-id="0beed-116">产品</span><span class="sxs-lookup"><span data-stu-id="0beed-116">Product</span></span> | <span data-ttu-id="0beed-117">产品</span><span class="sxs-lookup"><span data-stu-id="0beed-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="0beed-118">实体流</span><span class="sxs-lookup"><span data-stu-id="0beed-118">Entity flow</span></span>

<span data-ttu-id="0beed-119">产品在 Finance and Operations 中进行托管并同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="0beed-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="0beed-120">Finance and Operations 中的数据实体**适售的已发布产品**仅导出适售的产品，意味着产品具有需要在销售订单上使用的信息。</span><span class="sxs-lookup"><span data-stu-id="0beed-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="0beed-121">相同的规则适用于使用**已发布产品**页上的**验证**功能对产品进行验证时。</span><span class="sxs-lookup"><span data-stu-id="0beed-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="0beed-122">**产品编号**用作参数，这意味着产品变型按照每个**产品变型**一个**产品 ID** 同步到 CDS 和 Sales。</span><span class="sxs-lookup"><span data-stu-id="0beed-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0beed-123">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="0beed-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="0beed-124">在 Sales 中，在产品**外部维护**上添加一个新字段以指示特定产品在外部维护。</span><span class="sxs-lookup"><span data-stu-id="0beed-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="0beed-125">该值在导入到 Sales 期间默认设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0beed-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="0beed-126">**外部维护 = 是**：产品源自 Finance and Operations，在 Sales 中不可编辑。</span><span class="sxs-lookup"><span data-stu-id="0beed-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="0beed-127">**外部维护 = 否**：直接在 Sales 中输入产品。</span><span class="sxs-lookup"><span data-stu-id="0beed-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="0beed-128">**外部维护 = 空白**：在启用从目标客户到现金解决方案前在 Sales 中存在产品。</span><span class="sxs-lookup"><span data-stu-id="0beed-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="0beed-129">**外部维护**信息用于确保仅具有**外部维护的产品**的**报价**和**销售订单**将同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="0beed-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="0beed-130">**外部维护的产品**自动添加到具有相同币种的第一个有效的**价目表**。</span><span class="sxs-lookup"><span data-stu-id="0beed-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="0beed-131">请注意，该列表按**名称**的字母顺序排列。</span><span class="sxs-lookup"><span data-stu-id="0beed-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="0beed-132">来自 Finance and Operations 的产品销售价格用作**价目表**价格。</span><span class="sxs-lookup"><span data-stu-id="0beed-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="0beed-133">这意味着要求对于 Finance and Operations 中的每一个**产品销售币种**，在 Sales 中都有一份**价目表**。</span><span class="sxs-lookup"><span data-stu-id="0beed-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="0beed-134">已发布的适售产品上的币种设置为从中导出产品的法人的记帐币种。</span><span class="sxs-lookup"><span data-stu-id="0beed-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="0beed-135">如果没有匹配币种的**价目表**，产品同步不会成功。</span><span class="sxs-lookup"><span data-stu-id="0beed-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0beed-136">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="0beed-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="0beed-137">在首次运行同步前，必须在 Finance and Operations 中为现有产品填充**独特产品表**。</span><span class="sxs-lookup"><span data-stu-id="0beed-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="0beed-138">完成该作业前，现有产品不会同步。</span><span class="sxs-lookup"><span data-stu-id="0beed-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="0beed-139">在 Finance and Operations 中，使用“搜索”搜索**填充独特产品表**。</span><span class="sxs-lookup"><span data-stu-id="0beed-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="0beed-140">单击**填充独特产品表**以运行作业。</span><span class="sxs-lookup"><span data-stu-id="0beed-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="0beed-141">该作业仅需要运行一次。</span><span class="sxs-lookup"><span data-stu-id="0beed-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="0beed-142">确保在 Finance and Operations 中销售**度量单位** (UOM) 所需的 **ValueMap** 在**源 -\> CDS 映射 SalesUnitSymbol / DefaultSellingUnitOfMeasure** 中存在。</span><span class="sxs-lookup"><span data-stu-id="0beed-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="0beed-143">在**源 -\> CDS** 中更新 **CDS 组织 ID Organization_OrganizationId**。</span><span class="sxs-lookup"><span data-stu-id="0beed-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="0beed-144">模板值默认为 ORG001。</span><span class="sxs-lookup"><span data-stu-id="0beed-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="0beed-145">在 **CDS -\> 目标**中更新**单位组** (**defaultuomscheduleid.name**) 的 **ValueMap** 以匹配 Sales 中的**单位组**。</span><span class="sxs-lookup"><span data-stu-id="0beed-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="0beed-146">模板值默认为**默认单位**。</span><span class="sxs-lookup"><span data-stu-id="0beed-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="0beed-147">确保来自 Finance and Operations 的所有产品销售 UOM 在 Sales 中存在 **CDS 选择列表**值。</span><span class="sxs-lookup"><span data-stu-id="0beed-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="0beed-148">确保 Finance and Operations 中的每个产品销售币种在 Sales 中存在**价目表**。</span><span class="sxs-lookup"><span data-stu-id="0beed-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="0beed-149">可以在 Sales 中使用状态**草稿**或**活动**创建产品。</span><span class="sxs-lookup"><span data-stu-id="0beed-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="0beed-150">这在 Sales 的**销售**下的**系统设置**中进行控制。</span><span class="sxs-lookup"><span data-stu-id="0beed-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="0beed-151">使用草稿状态创建的产品需要激活后才能添加到**报价**或**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="0beed-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0beed-152">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="0beed-152">Template mapping in data integrator</span></span>

<span data-ttu-id="0beed-153">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="0beed-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![数据集成器中的模板映射](./media/products-template-mapping-data-integrator-1.png)

![数据集成器中的产品的模板映射](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="0beed-156">相关主题</span><span class="sxs-lookup"><span data-stu-id="0beed-156">Related topics</span></span>

[<span data-ttu-id="0beed-157">将来自 Sales 的帐户同步到 Finance and Operations 中的客户</span><span class="sxs-lookup"><span data-stu-id="0beed-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0beed-158">将 Sales 的联系人同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="0beed-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="0beed-159">将 Sales 的销售报价单标题和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0beed-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="0beed-160">将 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="0beed-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="0beed-161">将 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="0beed-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


