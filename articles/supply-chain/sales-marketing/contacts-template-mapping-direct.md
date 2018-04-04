---
title: "将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的联系人（联系人）和联系人（客户）实体同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 021a43c78cec83b23aff5dcc40db1a4be81aefc3
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="8edc5-103">将 Sales 的联系人直接同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="8edc5-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8edc5-104">在可以使用“从目标客户到现金”解决方案之前，您应该熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="8edc5-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="8edc5-105">本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的联系人（联系人）和联系人（客户）实体直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="8edc5-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="8edc5-106">“从目标客户到现金”中的数据流</span><span class="sxs-lookup"><span data-stu-id="8edc5-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="8edc5-107">“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。</span><span class="sxs-lookup"><span data-stu-id="8edc5-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="8edc5-108">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="8edc5-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8edc5-109">下图显示 Finance and Operations 与 Sales 之间的数据如何同步。</span><span class="sxs-lookup"><span data-stu-id="8edc5-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="8edc5-110">[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="8edc5-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="8edc5-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="8edc5-111">Templates and tasks</span></span>

<span data-ttu-id="8edc5-112">若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。</span><span class="sxs-lookup"><span data-stu-id="8edc5-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="8edc5-113">选择**项目**，然后在右上角，选择**新项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="8edc5-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8edc5-114">以下模板和基础任务用于将 Sales 中的联系人（联系人）实体同步到 Finance and Operations 中的联系人（客户）实体：</span><span class="sxs-lookup"><span data-stu-id="8edc5-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="8edc5-115">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="8edc5-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="8edc5-116">联系人（从 Sales 到 Fin and Ops）- 直接</span><span class="sxs-lookup"><span data-stu-id="8edc5-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="8edc5-117">从联系人到客户（从 Sales 到 Fin and Ops）- 直接</span><span class="sxs-lookup"><span data-stu-id="8edc5-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="8edc5-118">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="8edc5-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="8edc5-119">联系人</span><span class="sxs-lookup"><span data-stu-id="8edc5-119">Contacts</span></span>
    - <span data-ttu-id="8edc5-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="8edc5-120">ContactToCustomer</span></span>

<span data-ttu-id="8edc5-121">必须先执行以下同步任务才能够进行联系人同步：帐户（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="8edc5-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="8edc5-122">实体集</span><span class="sxs-lookup"><span data-stu-id="8edc5-122">Entity sets</span></span>

| <span data-ttu-id="8edc5-123">销售</span><span class="sxs-lookup"><span data-stu-id="8edc5-123">Sales</span></span>    | <span data-ttu-id="8edc5-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8edc5-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="8edc5-125">联系人</span><span class="sxs-lookup"><span data-stu-id="8edc5-125">Contacts</span></span> | <span data-ttu-id="8edc5-126">CDS 联系人</span><span class="sxs-lookup"><span data-stu-id="8edc5-126">CDS Contacts</span></span>           |
| <span data-ttu-id="8edc5-127">联系人</span><span class="sxs-lookup"><span data-stu-id="8edc5-127">Contacts</span></span> | <span data-ttu-id="8edc5-128">客户 V2</span><span class="sxs-lookup"><span data-stu-id="8edc5-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="8edc5-129">实体流</span><span class="sxs-lookup"><span data-stu-id="8edc5-129">Entity flow</span></span>

<span data-ttu-id="8edc5-130">联系人在 Sales 中进行托管并同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="8edc5-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="8edc5-131">Sales 中的联系人可以成为 Finance and Operations 中的联系人或客户。</span><span class="sxs-lookup"><span data-stu-id="8edc5-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="8edc5-132">为了确定在 Sales 中的联系人是否应该作为联系人或客户同步到 Finance and Operations，系统将在 Sales 中查看联系人的以下属性：</span><span class="sxs-lookup"><span data-stu-id="8edc5-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="8edc5-133">**同步到 Finance and Operations 中的客户：**联系人的**是可用客户**设置为**是**</span><span class="sxs-lookup"><span data-stu-id="8edc5-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="8edc5-134">**同步到 Finance and Operations 中的联系人：**联系人的**是可用客户**设置为**否**且**公司**（上级单位/联系人）指向帐户（不是联系人）</span><span class="sxs-lookup"><span data-stu-id="8edc5-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8edc5-135">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="8edc5-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8edc5-136">新的**是可用客户**字段已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="8edc5-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="8edc5-137">此字段用于区分具有销售活动的联系人和没有销售活动的联系人。</span><span class="sxs-lookup"><span data-stu-id="8edc5-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="8edc5-138">**是可用客户**仅对具有相关报价单、订单或发票的联系人设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="8edc5-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="8edc5-139">仅这些联系人作为客户同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="8edc5-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="8edc5-140">新的 **IsCompanyAnAccount** 字段已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="8edc5-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="8edc5-141">此字段指示联系人是否已链接到**帐户**类型的公司（上级单位/联系人）。</span><span class="sxs-lookup"><span data-stu-id="8edc5-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="8edc5-142">此信息用于确定应该作为联系人同步到 Finance and Operations 的联系人。</span><span class="sxs-lookup"><span data-stu-id="8edc5-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="8edc5-143">新的**联系人号码**字段已添加到联系人以帮助保证一个用于集成的自然和唯一参数。</span><span class="sxs-lookup"><span data-stu-id="8edc5-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="8edc5-144">在创建新的联系人时，将使用编号规则自动创建**联系人号码**值。</span><span class="sxs-lookup"><span data-stu-id="8edc5-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="8edc5-145">该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="8edc5-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="8edc5-146">示例：**CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="8edc5-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="8edc5-147">应用用于 Sales 的集成解决方案后，一个升级脚本使用前面提到的编号规则设置现有联系人的**联系人号码**字段。</span><span class="sxs-lookup"><span data-stu-id="8edc5-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="8edc5-148">升级脚本还可以对任何具有销售活动的联系人将**是可用客户**字段设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="8edc5-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="8edc5-149">在 Finance and Operations 中</span><span class="sxs-lookup"><span data-stu-id="8edc5-149">In Finance and Operations</span></span>

<span data-ttu-id="8edc5-150">使用 **IsContactPersonExternallyMaintained** 属性标记联系人。</span><span class="sxs-lookup"><span data-stu-id="8edc5-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="8edc5-151">此属性指示特定联系人由外部维护。</span><span class="sxs-lookup"><span data-stu-id="8edc5-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="8edc5-152">在这种情况下，外部维护的联系人在 Sales 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="8edc5-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8edc5-153">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="8edc5-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="8edc5-154">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="8edc5-154">Contact to customer</span></span>

- <span data-ttu-id="8edc5-155">**CustomerGroup** 在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="8edc5-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="8edc5-156">若要帮助避免同步错误，你可以在映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="8edc5-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="8edc5-157">如果该字段在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="8edc5-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="8edc5-158">默认模板值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="8edc5-158">The default template value is **10**.</span></span>

- <span data-ttu-id="8edc5-159">添加以下映射有助于减少在 Finance and Operations 中所需的手动更新的次数。</span><span class="sxs-lookup"><span data-stu-id="8edc5-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="8edc5-160">你可以使用默认值或来自**国家/地区**或**城市**等的值映射。</span><span class="sxs-lookup"><span data-stu-id="8edc5-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="8edc5-161">**SiteId** – 还可以对 Finance and Operations 中的产品定义默认站点。</span><span class="sxs-lookup"><span data-stu-id="8edc5-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="8edc5-162">在 Finance and Operations 中生成报价单和销售订单所需的站点。</span><span class="sxs-lookup"><span data-stu-id="8edc5-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="8edc5-163">**SiteId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="8edc5-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="8edc5-164">**WarehouseId** – 还可以对 Finance and Operations 中的产品定义默认仓库。</span><span class="sxs-lookup"><span data-stu-id="8edc5-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="8edc5-165">在 Finance and Operations 中生成报价单和销售订单所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="8edc5-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="8edc5-166">**WarehouseId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="8edc5-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="8edc5-167">**LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。</span><span class="sxs-lookup"><span data-stu-id="8edc5-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="8edc5-168">默认模板值为 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="8edc5-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8edc5-169">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="8edc5-169">Template mapping in Data integration</span></span>

<span data-ttu-id="8edc5-170">下图显示了数据集成中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="8edc5-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="8edc5-171">此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="8edc5-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="8edc5-172">从联系人到联系人</span><span class="sxs-lookup"><span data-stu-id="8edc5-172">Contact to contact</span></span>

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="8edc5-174">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="8edc5-174">Contact to customer</span></span>

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="8edc5-176">相关主题</span><span class="sxs-lookup"><span data-stu-id="8edc5-176">Related topics</span></span>

[<span data-ttu-id="8edc5-177">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="8edc5-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="8edc5-178">将直接来自 Sales 的客户同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8edc5-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="8edc5-179">将直接来自 Finance and Operations 的产品同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="8edc5-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="8edc5-180">将直接来自 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="8edc5-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="8edc5-181">将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="8edc5-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



