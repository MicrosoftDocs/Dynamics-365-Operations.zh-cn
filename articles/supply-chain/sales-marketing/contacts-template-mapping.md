---
title: "将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的联系人（联系人）和联系人（客户）同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本 的模板和基础任务。"
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="0f165-103">将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="0f165-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0f165-104">在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。</span><span class="sxs-lookup"><span data-stu-id="0f165-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0f165-105">本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的联系人（联系人）实体和联系人（客户）同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="0f165-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0f165-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="0f165-106">Templates and tasks</span></span>

<span data-ttu-id="0f165-107">以下模板和基础任务用于将 Sales 中的联系人（联系人）同步到 Finance and Operations 中的联系人（客户）：</span><span class="sxs-lookup"><span data-stu-id="0f165-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="0f165-108">**模板的名称：**</span><span class="sxs-lookup"><span data-stu-id="0f165-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="0f165-109">联系人（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="0f165-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="0f165-110">从联系人到客户（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="0f165-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="0f165-111">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="0f165-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="0f165-112">联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-112">Contacts</span></span>
    - <span data-ttu-id="0f165-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="0f165-113">ContactToCustomer</span></span>

<span data-ttu-id="0f165-114">在联系人同步之前必须执行以下同步任务：帐户（从 Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="0f165-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="0f165-115">实体集</span><span class="sxs-lookup"><span data-stu-id="0f165-115">Entity sets</span></span>

| <span data-ttu-id="0f165-116">销售</span><span class="sxs-lookup"><span data-stu-id="0f165-116">Sales</span></span>    | <span data-ttu-id="0f165-117">CDS</span><span class="sxs-lookup"><span data-stu-id="0f165-117">CDS</span></span>     | <span data-ttu-id="0f165-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f165-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="0f165-119">联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-119">Contacts</span></span> | <span data-ttu-id="0f165-120">联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-120">Contact</span></span> | <span data-ttu-id="0f165-121">CDS 联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-121">CDS Contacts</span></span>           |
| <span data-ttu-id="0f165-122">联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-122">Contacts</span></span> | <span data-ttu-id="0f165-123">科目</span><span class="sxs-lookup"><span data-stu-id="0f165-123">Account</span></span> | <span data-ttu-id="0f165-124">客户 V2</span><span class="sxs-lookup"><span data-stu-id="0f165-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="0f165-125">实体流</span><span class="sxs-lookup"><span data-stu-id="0f165-125">Entity flow</span></span>

<span data-ttu-id="0f165-126">联系人在 Sales 中进行托管，并同步到 Common Data Service (CDS) 和 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="0f165-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="0f165-127">Sales 中的联系人可以成为 CDS 和 Finance and Operations 中的联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="0f165-128">或者，它可以成为 CDS 中的帐户和 Finance and Operations 中的客户。</span><span class="sxs-lookup"><span data-stu-id="0f165-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="0f165-129">若要确定是否应该提取 Sales 中的联系人用于同步到 CDS 和 Finance and Operations（例如，Sales 中的联系人 &gt; CDS 中的联系人 &gt; Finance and Operations 中的联系人），系统会检查 Sales 中的联系人的以下属性：</span><span class="sxs-lookup"><span data-stu-id="0f165-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="0f165-130">**同步到 CDS 中的帐户和 Finance and Operations 中的客户：**联系人的**是可用客户**设置为**是**</span><span class="sxs-lookup"><span data-stu-id="0f165-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="0f165-131">**同步到 CDS 中的联系人和 Finance and Operations 中的联系人：**联系人的**是可用客户**设置为**否**且**公司**（上级单位/联系人）指向帐户（不是联系人）</span><span class="sxs-lookup"><span data-stu-id="0f165-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0f165-132">用于 Sales 的“从目标客户到现金”解决方案</span><span class="sxs-lookup"><span data-stu-id="0f165-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="0f165-133">新的**是可用客户**字段已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="0f165-134">此字段用于区分具有销售活动的联系人和没有销售活动的联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="0f165-135">**是可用客户**仅对具有相关报价单、订单或发票的联系人设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0f165-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="0f165-136">仅这些联系人作为客户同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="0f165-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="0f165-137">新的 **IsCompanyAnAccount** 字段已添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="0f165-138">此字段用于指示联系人是否已链接到**帐户**类型的公司（上级单位/联系人）。</span><span class="sxs-lookup"><span data-stu-id="0f165-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="0f165-139">此信息用于确定应该作为联系人同步到 Finance and Operations 的联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="0f165-140">新的**联系人号码**字段已添加到联系人以帮助保证一个用于集成的自然和唯一参数。</span><span class="sxs-lookup"><span data-stu-id="0f165-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="0f165-141">在创建新的联系人时，将使用编号规则自动创建**联系人号码**值。</span><span class="sxs-lookup"><span data-stu-id="0f165-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="0f165-142">该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="0f165-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="0f165-143">示例：**CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="0f165-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="0f165-144">将用于 Sales 的集成解决方案添加到 Sales 后，一个升级脚本使用前面讨论的编号规则设置现有联系人的**联系人号码**字段。</span><span class="sxs-lookup"><span data-stu-id="0f165-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="0f165-145">升级脚本还可以对任何具有销售活动的联系人将**是可用客户**字段设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0f165-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="0f165-146">在 Finance and Operations 中</span><span class="sxs-lookup"><span data-stu-id="0f165-146">In Finance and Operations</span></span> 

<span data-ttu-id="0f165-147">使用 **IsContactPersonExternallyMaintained** 属性标记联系人。</span><span class="sxs-lookup"><span data-stu-id="0f165-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="0f165-148">此属性指示特定联系人由外部维护。</span><span class="sxs-lookup"><span data-stu-id="0f165-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="0f165-149">在这种情况下，外部维护的联系人在 Sales 中进行维护。</span><span class="sxs-lookup"><span data-stu-id="0f165-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0f165-150">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="0f165-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="0f165-151">从联系人到联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-151">Contact to Contact</span></span>

- <span data-ttu-id="0f165-152">在**源 &gt; CDS** 映射中更新 **CDS 组织 ID**。</span><span class="sxs-lookup"><span data-stu-id="0f165-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="0f165-153">**Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="0f165-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="0f165-154">**PrimaryAccount_Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="0f165-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="0f165-155">**地址国家/地区代码** 在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="0f165-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="0f165-156">若要避免同步错误，你可以在 **CDS &gt; Operations** 映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="0f165-157">如果该字段在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0f165-158">**PrimaryAddressCountryRegionISOCode** 的默认模板值是 **USA**。</span><span class="sxs-lookup"><span data-stu-id="0f165-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="0f165-159">确保以下字段的值在 Finance and Operations 中存在。</span><span class="sxs-lookup"><span data-stu-id="0f165-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="0f165-160">如果此信息在 Finance and Operations 中不需要，你可以从 **CDS &gt; 目标**映射中删除映射。</span><span class="sxs-lookup"><span data-stu-id="0f165-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="0f165-161">**Finance and Operations 中的字段名称：**决策</span><span class="sxs-lookup"><span data-stu-id="0f165-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="0f165-162">**映射：**PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="0f165-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="0f165-163">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="0f165-163">Contact to Customer</span></span>

- <span data-ttu-id="0f165-164">在**源 &gt; CDS** 映射中更新 **CDS 组织 ID**。</span><span class="sxs-lookup"><span data-stu-id="0f165-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="0f165-165">**Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。</span><span class="sxs-lookup"><span data-stu-id="0f165-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="0f165-166">**地址国家/地区代码** 在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="0f165-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="0f165-167">若要避免同步错误，你可以在 **CDS &gt; 目标**映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="0f165-168">如果该字段在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0f165-169">**PrimaryAddressCountryRegionISOCode** 的默认模板值是 **USA**。</span><span class="sxs-lookup"><span data-stu-id="0f165-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="0f165-170">**CustomerGroup** 在 Finance and Operations 中必填。</span><span class="sxs-lookup"><span data-stu-id="0f165-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="0f165-171">若要避免同步错误，你可以在 **CDS &gt; 目标**映射中指定默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="0f165-172">如果该字段在 Sales 中为空，则使用该默认值。</span><span class="sxs-lookup"><span data-stu-id="0f165-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0f165-173">**CustomerGroupId** 的默认模板值是 **10**。</span><span class="sxs-lookup"><span data-stu-id="0f165-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="0f165-174">添加来自 **CDS &gt; 目标**的以下映射有助于减少在 Finance and Operations 中手动更新的次数。</span><span class="sxs-lookup"><span data-stu-id="0f165-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="0f165-175">你可以使用默认值或来自**国家/地区**或**城市**等的值映射。</span><span class="sxs-lookup"><span data-stu-id="0f165-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="0f165-176">**SiteId** - 还可以对 Finance and Operations 中的产品定义默认站点。</span><span class="sxs-lookup"><span data-stu-id="0f165-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="0f165-177">在 Finance and Operations 中生成报价单和销售订单所需的站点。</span><span class="sxs-lookup"><span data-stu-id="0f165-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0f165-178">**SiteId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="0f165-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="0f165-179">**WarehouseId** - 还可以对 Finance and Operations 中的产品定义默认仓库。</span><span class="sxs-lookup"><span data-stu-id="0f165-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="0f165-180">在 Finance and Operations 中生成报价单和销售订单所需的仓库。</span><span class="sxs-lookup"><span data-stu-id="0f165-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0f165-181">**WarehouseId** 模板值未定义。</span><span class="sxs-lookup"><span data-stu-id="0f165-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="0f165-182">**LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。</span><span class="sxs-lookup"><span data-stu-id="0f165-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0f165-183">**LanguageId** 的默认模板值是 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="0f165-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0f165-184">数据集成器中的模板映射</span><span class="sxs-lookup"><span data-stu-id="0f165-184">Template mapping in data integrator</span></span>

<span data-ttu-id="0f165-185">下图显示了数据集成器中的模板映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="0f165-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="0f165-186">从联系人到联系人</span><span class="sxs-lookup"><span data-stu-id="0f165-186">Contact to Contact</span></span>

![数据集成器中的模板映射](./media/contacts-template-mapping-data-integrator-1.png)

![数据集成器中的联系人的模板映射](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="0f165-189">从联系人到客户</span><span class="sxs-lookup"><span data-stu-id="0f165-189">Contact to Customer</span></span>

![数据集成器中的模板映射](./media/contacts-template-mapping-data-integrator-3.png)

![数据集成器中的联系人的模板映射](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="0f165-192">相关主题</span><span class="sxs-lookup"><span data-stu-id="0f165-192">Related topics</span></span>

[<span data-ttu-id="0f165-193">将来自 Finance and Operations 的产品同步到 Sales 中的产品</span><span class="sxs-lookup"><span data-stu-id="0f165-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="0f165-194">将来自 Sales 的帐户同步到 Finance and Operations 中的客户</span><span class="sxs-lookup"><span data-stu-id="0f165-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0f165-195">将 Sales 的销售报价单标题和行同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f165-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="0f165-196">将 Finance and Operations 的销售订单标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="0f165-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="0f165-197">将 Finance and Operations 的销售发票标题和行同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="0f165-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

