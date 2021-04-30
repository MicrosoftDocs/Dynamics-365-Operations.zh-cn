---
title: 将 Sales 的客户直接同步到 Supply Chain Management 中的客户
description: 此主题介绍用于将客户从 Dynamics 365 Sales 同步到 Supply Chain Management 的模板和基础任务。
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
ms.openlocfilehash: fff9171966045e9dad5f2c70087a568cfa075e43
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908124"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="c8586-103">将 Sales 的客户直接同步到 Supply Chain Management 中的客户</span><span class="sxs-lookup"><span data-stu-id="c8586-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="c8586-104">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="c8586-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="c8586-105">此主题介绍用于将客户直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="c8586-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c8586-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="c8586-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c8586-107">“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="c8586-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="c8586-108">提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="c8586-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="c8586-109">下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="c8586-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="c8586-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c8586-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c8586-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="c8586-111">Templates and tasks</span></span>

<span data-ttu-id="c8586-112">若要访问可用模板，打开 [Power Apps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="c8586-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c8586-113">选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="c8586-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c8586-114">以下模板和基础任务用于将客户从 Sales 同步到 Supply Chain Management：</span><span class="sxs-lookup"><span data-stu-id="c8586-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="c8586-115">**数据集成中的模板名称：** 帐户（Sales 到 Fin and Ops）- 直接</span><span class="sxs-lookup"><span data-stu-id="c8586-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="c8586-116">**项目中的任务名称：** 帐户 - 客户</span><span class="sxs-lookup"><span data-stu-id="c8586-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="c8586-117">不需要同步任务即可进行帐户/客户同步。</span><span class="sxs-lookup"><span data-stu-id="c8586-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c8586-118">实体集</span><span class="sxs-lookup"><span data-stu-id="c8586-118">Entity set</span></span>

| <span data-ttu-id="c8586-119">销售额</span><span class="sxs-lookup"><span data-stu-id="c8586-119">Sales</span></span>    | <span data-ttu-id="c8586-120">供应链管理</span><span class="sxs-lookup"><span data-stu-id="c8586-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="c8586-121">科目</span><span class="sxs-lookup"><span data-stu-id="c8586-121">Accounts</span></span> | <span data-ttu-id="c8586-122">客户 V2</span><span class="sxs-lookup"><span data-stu-id="c8586-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="c8586-123">实体流</span><span class="sxs-lookup"><span data-stu-id="c8586-123">Entity flow</span></span>

<span data-ttu-id="c8586-124">客户在 Sales 中托管，并作为客户同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="c8586-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="c8586-125">这些客户的 **外部维护** 属性设置为 **是** 以跟踪源自 Sales 的客户。</span><span class="sxs-lookup"><span data-stu-id="c8586-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="c8586-126">在开票期间，此信息用于筛选将同步到 Sales 的发票。</span><span class="sxs-lookup"><span data-stu-id="c8586-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c8586-127">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="c8586-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c8586-128">**帐号** 列在 **帐户** 页提供。</span><span class="sxs-lookup"><span data-stu-id="c8586-128">The **Account Number** column is available on the **Account** page.</span></span> <span data-ttu-id="c8586-129">它由一个自然和唯一参数组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="c8586-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="c8586-130">客户关系管理 (CRM) 解决方案的自然键特征可能影响已经使用 **帐号** 列，但各帐户不使用唯一 **帐号** 值的客户。</span><span class="sxs-lookup"><span data-stu-id="c8586-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** column, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="c8586-131">目前，集成解决方案不支持此案例。</span><span class="sxs-lookup"><span data-stu-id="c8586-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="c8586-132">当创建新帐户时，如果 **帐号** 值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="c8586-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="c8586-133">该值由 **ACC** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="c8586-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c8586-134">示例：**ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="c8586-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="c8586-135">当对 Sales 应用集成解决方案时，升级脚本为 Sales 中的现有帐户设置 **帐号** 列。</span><span class="sxs-lookup"><span data-stu-id="c8586-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** column for existing accounts in Sales.</span></span> <span data-ttu-id="c8586-136">如果没有 **帐号** 值，可以使用之前提到的编号规则。</span><span class="sxs-lookup"><span data-stu-id="c8586-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c8586-137">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="c8586-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="c8586-138">**CustomerGroupId** 映射在 Supply Chain Management 中必须更新到一个有效值。</span><span class="sxs-lookup"><span data-stu-id="c8586-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="c8586-139">你可以指定一个默认值，或者使用值映射设置该值。</span><span class="sxs-lookup"><span data-stu-id="c8586-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="c8586-140">默认模板值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="c8586-140">The default template value is **10**.</span></span>

- <span data-ttu-id="c8586-141">添加以下映射有助于减少在 Supply Chain Management 中所需的手动更新的次数。</span><span class="sxs-lookup"><span data-stu-id="c8586-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="c8586-142">你可以使用默认值或来自 **国家/地区** 或 **城市** 等的值映射。</span><span class="sxs-lookup"><span data-stu-id="c8586-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="c8586-143">**SiteId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的站点。</span><span class="sxs-lookup"><span data-stu-id="c8586-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="c8586-144">默认站点可以从产品或从订单头的客户提取。</span><span class="sxs-lookup"><span data-stu-id="c8586-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="c8586-145">默认模板值为 **1**。</span><span class="sxs-lookup"><span data-stu-id="c8586-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="c8586-146">**WarehouseId** - 在 Supply Chain Management 中处理报价单和销售订单行所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="c8586-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="c8586-147">默认仓库可以在 Supply Chain Management 中从产品或从订单头的客户提取。</span><span class="sxs-lookup"><span data-stu-id="c8586-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="c8586-148">默认模板值为 **13**。</span><span class="sxs-lookup"><span data-stu-id="c8586-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="c8586-149">**LanguageId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的语言。</span><span class="sxs-lookup"><span data-stu-id="c8586-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="c8586-150">默认情况下，使用来自客户的订单头的语言。</span><span class="sxs-lookup"><span data-stu-id="c8586-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="c8586-151">默认模板值为 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="c8586-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c8586-152">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="c8586-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="c8586-153">**付款期限**、**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 列不包括在默认映射中。</span><span class="sxs-lookup"><span data-stu-id="c8586-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="c8586-154">若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。</span><span class="sxs-lookup"><span data-stu-id="c8586-154">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="c8586-155">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="c8586-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8586-156">此映射显示将从 Sales 同步到 Supply Chain Management 的列信息。</span><span class="sxs-lookup"><span data-stu-id="c8586-156">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

![数据集成中的模板映射](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="c8586-158">相关主题</span><span class="sxs-lookup"><span data-stu-id="c8586-158">Related topics</span></span>


[<span data-ttu-id="c8586-159">现金的目标客户</span><span class="sxs-lookup"><span data-stu-id="c8586-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c8586-160">将 Sales 的客户直接同步到 Supply Chain Management 中的客户</span><span class="sxs-lookup"><span data-stu-id="c8586-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c8586-161">将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="c8586-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="c8586-162">直接在 Sales 和 Supply Chain Management 之间同步销售订单</span><span class="sxs-lookup"><span data-stu-id="c8586-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="c8586-163">将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="c8586-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]