---
title: 将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户
description: 本主题讨论用于将来自 Dynamics 365 Sales 的联系人（联系人）和联系人（客户）实体同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994036"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="b6de9-103">将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="b6de9-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="b6de9-104">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="b6de9-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="b6de9-105">本主题讨论用于直接将来自 Dynamics 365 Sales 的联系人（联系人）和联系人（客户）表同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="b6de9-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b6de9-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="b6de9-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b6de9-107">“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="b6de9-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="b6de9-108">提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="b6de9-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b6de9-109">下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="b6de9-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b6de9-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b6de9-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b6de9-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="b6de9-111">Templates and tasks</span></span>

<span data-ttu-id="b6de9-112">若要访问可用模板，打开 [PowerApps 管理中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="b6de9-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b6de9-113">选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="b6de9-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b6de9-114">以下模板和基础任务用于将 Sales 中的联系人（联系人）表同步到 Supply Chain Management 中的联系人（客户）表。</span><span class="sxs-lookup"><span data-stu-id="b6de9-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="b6de9-115">**数据集成中的模板名称**</span><span class="sxs-lookup"><span data-stu-id="b6de9-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="b6de9-116">联系人（Sales 到 Supply Chain Management）- 直接</span><span class="sxs-lookup"><span data-stu-id="b6de9-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="b6de9-117">从联系人到客户（Sales 到 Supply Chain Management）- 直接</span><span class="sxs-lookup"><span data-stu-id="b6de9-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="b6de9-118">**数据集成项目中的任务名称**</span><span class="sxs-lookup"><span data-stu-id="b6de9-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="b6de9-119">联系人</span><span class="sxs-lookup"><span data-stu-id="b6de9-119">Contacts</span></span>
    - <span data-ttu-id="b6de9-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="b6de9-120">ContactToCustomer</span></span>

<span data-ttu-id="b6de9-121">必须先执行以下同步任务才能够进行联系人同步：帐户（从 Sales 到 Supply Chain Management）</span><span class="sxs-lookup"><span data-stu-id="b6de9-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="b6de9-122">实体集</span><span class="sxs-lookup"><span data-stu-id="b6de9-122">Entity sets</span></span>

| <span data-ttu-id="b6de9-123">销售额</span><span class="sxs-lookup"><span data-stu-id="b6de9-123">Sales</span></span>    | <span data-ttu-id="b6de9-124">供应链管理</span><span class="sxs-lookup"><span data-stu-id="b6de9-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="b6de9-125">联系人</span><span class="sxs-lookup"><span data-stu-id="b6de9-125">Contacts</span></span> | <span data-ttu-id="b6de9-126">Dataverse 联系人</span><span class="sxs-lookup"><span data-stu-id="b6de9-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="b6de9-127">联系人</span><span class="sxs-lookup"><span data-stu-id="b6de9-127">Contacts</span></span> | <span data-ttu-id="b6de9-128">客户 V2</span><span class="sxs-lookup"><span data-stu-id="b6de9-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b6de9-129">实体流</span><span class="sxs-lookup"><span data-stu-id="b6de9-129">Entity flow</span></span>

<span data-ttu-id="b6de9-130">联系人在 Sales 中托管，并同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="b6de9-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="b6de9-131">Sales 中的联系人可以成为 Supply Chain Management 中的联系人或客户。</span><span class="sxs-lookup"><span data-stu-id="b6de9-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="b6de9-132">为了确定在 Sales 中的联系人是否应该作为联系人或客户同步到 Supply Chain Management，系统将在 Sales 中查看联系人的以下属性：</span><span class="sxs-lookup"><span data-stu-id="b6de9-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="b6de9-133">**同步到 Supply Chain Management 中的客户：** 联系人的 **是可用客户** 设置为 **是**</span><span class="sxs-lookup"><span data-stu-id="b6de9-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="b6de9-134">**同步到 Supply Chain Management 中的联系人：** 联系人的 **是可用客户** 设置为 **否** 且 **公司**（上级单位/联系人）指向帐户（不是联系人）</span><span class="sxs-lookup"><span data-stu-id="b6de9-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b6de9-135">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="b6de9-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b6de9-136">新的 **是可用客户** 列已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="b6de9-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="b6de9-137">此列用于区分具有销售活动的联系人和没有销售活动的联系人。</span><span class="sxs-lookup"><span data-stu-id="b6de9-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="b6de9-138">**是可用客户** 仅对具有相关报价单、订单或发票的联系人设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b6de9-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="b6de9-139">仅这些联系人作为客户同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="b6de9-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="b6de9-140">新的 **IsCompanyAnAccount** 列已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="b6de9-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="b6de9-141">此列指示联系人是否已链接到 **客户** 类型的公司（上级单位/联系人）。</span><span class="sxs-lookup"><span data-stu-id="b6de9-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="b6de9-142">此信息用于确定应该作为联系人同步到 Supply Chain Management 的联系人。</span><span class="sxs-lookup"><span data-stu-id="b6de9-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="b6de9-143">新的 **联系人号码** 列已添加到联系人以帮助保证一个用于集成的自然和唯一参数。</span><span class="sxs-lookup"><span data-stu-id="b6de9-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="b6de9-144">在创建新的联系人时，将使用编号规则自动创建 **联系人号码** 值。</span><span class="sxs-lookup"><span data-stu-id="b6de9-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="b6de9-145">该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="b6de9-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b6de9-146">示例：**CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b6de9-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="b6de9-147">应用用于 Sales 的集成解决方案后，一个升级脚本使用前面提到的编号规则设置现有联系人的 **联系人号码** 列。</span><span class="sxs-lookup"><span data-stu-id="b6de9-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="b6de9-148">升级脚本还可以对任何具有销售活动的联系人将 **是可用客户** 列设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b6de9-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="b6de9-149">在 Supply Chain Management 中</span><span class="sxs-lookup"><span data-stu-id="b6de9-149">In Supply Chain Management</span></span>

<span data-ttu-id="b6de9-150">使用 **IsContactPersonExternallyMaintained** 属性标记联系人。</span><span class="sxs-lookup"><span data-stu-id="b6de9-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="b6de9-151">此属性指示特定联系人由外部维护。</span><span class="sxs-lookup"><span data-stu-id="b6de9-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="b6de9-152">在这种情况下，外部维护的联系人在 Sales 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="b6de9-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b6de9-153">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="b6de9-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="b6de9-154">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="b6de9-154">Contact to customer</span></span>

- <span data-ttu-id="b6de9-155">**CustomerGroup** 在 Supply Chain Management 中是必需的。</span><span class="sxs-lookup"><span data-stu-id="b6de9-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="b6de9-156">若要帮助避免同步错误，你可以在映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="b6de9-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="b6de9-157">如果该列在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="b6de9-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="b6de9-158">默认模板值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="b6de9-158">The default template value is **10**.</span></span>

- <span data-ttu-id="b6de9-159">添加以下映射有助于减少在 Supply Chain Management 中所需的手动更新的次数。</span><span class="sxs-lookup"><span data-stu-id="b6de9-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="b6de9-160">你可以使用默认值或来自 **国家/地区** 或 **城市** 等的值映射。</span><span class="sxs-lookup"><span data-stu-id="b6de9-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b6de9-161">**SiteId** – 还可以对 Supply Chain Management 中的产品定义默认站点。</span><span class="sxs-lookup"><span data-stu-id="b6de9-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="b6de9-162">在 Supply Chain Management 中生成报价单和销售订单必需有站点。</span><span class="sxs-lookup"><span data-stu-id="b6de9-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="b6de9-163">**SiteId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="b6de9-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="b6de9-164">**WarehouseId** – 还可以对 Supply Chain Management 中的产品定义默认仓库。</span><span class="sxs-lookup"><span data-stu-id="b6de9-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="b6de9-165">在 Supply Chain Management 中生成报价单和销售订单必需有仓库。</span><span class="sxs-lookup"><span data-stu-id="b6de9-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="b6de9-166">**WarehouseId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="b6de9-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="b6de9-167">**LanguageId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的语言。</span><span class="sxs-lookup"><span data-stu-id="b6de9-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="b6de9-168">默认模板值为 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="b6de9-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b6de9-169">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="b6de9-169">Template mapping in Data integration</span></span>

<span data-ttu-id="b6de9-170">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="b6de9-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b6de9-171">此映射显示将从 Sales 同步到 Supply Chain Management 的列信息。</span><span class="sxs-lookup"><span data-stu-id="b6de9-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="b6de9-172">从联系人到联系人</span><span class="sxs-lookup"><span data-stu-id="b6de9-172">Contact to contact</span></span>

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="b6de9-174">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="b6de9-174">Contact to customer</span></span>

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="b6de9-176">相关主题</span><span class="sxs-lookup"><span data-stu-id="b6de9-176">Related topics</span></span>

[<span data-ttu-id="b6de9-177">现金的目标客户</span><span class="sxs-lookup"><span data-stu-id="b6de9-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b6de9-178">将 Sales 的客户直接同步到 Supply Chain Management 中的客户</span><span class="sxs-lookup"><span data-stu-id="b6de9-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b6de9-179">将 Supply Chain Management 的产品直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="b6de9-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b6de9-180">直接在 Sales 和 Supply Chain Management 之间同步销售订单</span><span class="sxs-lookup"><span data-stu-id="b6de9-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="b6de9-181">将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="b6de9-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


