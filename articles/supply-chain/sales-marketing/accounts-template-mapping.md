---
title: "将来自 Sales 的帐户同步到 Finance and Operations 中的客户"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的帐户同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的模板和基础任务。"
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
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="9d429-103">将来自 Sales 的帐户同步到 Finance and Operations 中的客户</span><span class="sxs-lookup"><span data-stu-id="9d429-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9d429-104">在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="9d429-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="9d429-105">本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的帐户同步到 Microsoft Dynamics 365 for Finance and Operations 版本 (Finance and Operations) 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="9d429-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="9d429-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="9d429-106">Template and task</span></span>

<span data-ttu-id="9d429-107">以下模板和基础任务用于将来自 Sales 的帐户同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="9d429-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="9d429-108">**模板名称：**帐户（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="9d429-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="9d429-109">**项目中的任务名称：**帐户 - 帐户 - 客户</span><span class="sxs-lookup"><span data-stu-id="9d429-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="9d429-110">在帐户/客户同步之前所需的同步任务：无</span><span class="sxs-lookup"><span data-stu-id="9d429-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="9d429-111">实体集</span><span class="sxs-lookup"><span data-stu-id="9d429-111">Entity set</span></span>

| <span data-ttu-id="9d429-112">销售</span><span class="sxs-lookup"><span data-stu-id="9d429-112">Sales</span></span>    | <span data-ttu-id="9d429-113">CDS</span><span class="sxs-lookup"><span data-stu-id="9d429-113">CDS</span></span>     | <span data-ttu-id="9d429-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9d429-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="9d429-115">帐户</span><span class="sxs-lookup"><span data-stu-id="9d429-115">Accounts</span></span> | <span data-ttu-id="9d429-116">科目</span><span class="sxs-lookup"><span data-stu-id="9d429-116">Account</span></span> | <span data-ttu-id="9d429-117">客户</span><span class="sxs-lookup"><span data-stu-id="9d429-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="9d429-118">实体流</span><span class="sxs-lookup"><span data-stu-id="9d429-118">Entity flow</span></span>

<span data-ttu-id="9d429-119">帐户在 Sales 中进行托管并作为客户同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9d429-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="9d429-120">这些客户的**外部维护**属性设置为**是**以跟踪源自 Sales 的客户。</span><span class="sxs-lookup"><span data-stu-id="9d429-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="9d429-121">在开票期间，此信息用于筛选将同步到 Sales 的发票。</span><span class="sxs-lookup"><span data-stu-id="9d429-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9d429-122">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="9d429-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9d429-123">**帐号**字段在**帐户**页提供。</span><span class="sxs-lookup"><span data-stu-id="9d429-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="9d429-124">它由一个自然和唯一参数组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="9d429-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="9d429-125">客户关系管理 (CRM) 解决方案的自然键特征可能影响已经使用**帐号**字段，但各帐户不使用唯一**帐号**的客户。</span><span class="sxs-lookup"><span data-stu-id="9d429-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="9d429-126">目前，集成解决方案不支持此案例。</span><span class="sxs-lookup"><span data-stu-id="9d429-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="9d429-127">当创建新帐户时，如果**帐号**值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="9d429-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="9d429-128">该值由 **ACC** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="9d429-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="9d429-129">示例：**ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="9d429-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="9d429-130">当对 Sales 应用集成解决方案时，升级脚本为 Sales 中的现有帐户设置**帐号**字段。</span><span class="sxs-lookup"><span data-stu-id="9d429-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="9d429-131">如果没有**帐号**值，可以使用之前描述的编号规则。</span><span class="sxs-lookup"><span data-stu-id="9d429-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9d429-132">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="9d429-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9d429-133">来自 **CDS &gt; 目标**的 **CustomerGroupId** 映射在 Finance and Operations 中必须更新到一个有效值。</span><span class="sxs-lookup"><span data-stu-id="9d429-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="9d429-134">你可以指定一个默认值，或者使用值映射设置该值。</span><span class="sxs-lookup"><span data-stu-id="9d429-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="9d429-135">默认模板值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="9d429-135">The default template value is **10**.</span></span>
- <span data-ttu-id="9d429-136">**地址国家/地区代码** 在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="9d429-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="9d429-137">若要避免同步错误，您可以在来自 **CDS &gt; 目标**的映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="9d429-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="9d429-138">如果该字段在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="9d429-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="9d429-139">**AddressCountryRegionISOCode** 的默认模板值是 **USA**。</span><span class="sxs-lookup"><span data-stu-id="9d429-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="9d429-140">**DeliveryAddressCountryRegionISOCode** 的默认模板值是 **USA**。</span><span class="sxs-lookup"><span data-stu-id="9d429-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="9d429-141">添加来自 **CDS &gt; 目标**的以下映射有助于减少在 Finance and Operations 中所需的手动更新的次数。</span><span class="sxs-lookup"><span data-stu-id="9d429-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="9d429-142">你可以使用默认值或来自**国家/地区**或**城市**等的值映射。</span><span class="sxs-lookup"><span data-stu-id="9d429-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="9d429-143">**SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。</span><span class="sxs-lookup"><span data-stu-id="9d429-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9d429-144">默认站点可以从产品或从订单头的客户提取。</span><span class="sxs-lookup"><span data-stu-id="9d429-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="9d429-145">**SiteId** 的默认模板值是 **1**。</span><span class="sxs-lookup"><span data-stu-id="9d429-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="9d429-146">**WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="9d429-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9d429-147">默认仓库可以在 Finance and Operations 中从产品或从订单头的客户提取。</span><span class="sxs-lookup"><span data-stu-id="9d429-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="9d429-148">**WarehouseId** 的默认模板值是 **13**。</span><span class="sxs-lookup"><span data-stu-id="9d429-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="9d429-149">**LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。</span><span class="sxs-lookup"><span data-stu-id="9d429-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="9d429-150">默认情况下，使用来自客户的订单头的语言。</span><span class="sxs-lookup"><span data-stu-id="9d429-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="9d429-151">**LanguageId** 的默认模板值是 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="9d429-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="9d429-152">在**源 &gt; CDS** 映射中更新 CDS 组织 ID (**Organization_OrganizationId**)。</span><span class="sxs-lookup"><span data-stu-id="9d429-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="9d429-153">默认模板值为 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="9d429-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9d429-154">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="9d429-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="9d429-155">**付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="9d429-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="9d429-156">若要映射这些字段，则必须设置值映射。</span><span class="sxs-lookup"><span data-stu-id="9d429-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="9d429-157">值映射特定于实体在其中进行同步的组织中的数据。</span><span class="sxs-lookup"><span data-stu-id="9d429-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9d429-158">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="9d429-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![数据集成器中的模板映射](./media/accounts-template-mapping-data-integrator-1.png)

![数据集成器中的帐户的模板映射](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="9d429-161">相关主题</span><span class="sxs-lookup"><span data-stu-id="9d429-161">Related topics</span></span>

[<span data-ttu-id="9d429-162">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="9d429-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="9d429-163">将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="9d429-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="9d429-164">将 Sales 的销售报价单标题和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9d429-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="9d429-165">将 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="9d429-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="9d429-166">将 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="9d429-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




