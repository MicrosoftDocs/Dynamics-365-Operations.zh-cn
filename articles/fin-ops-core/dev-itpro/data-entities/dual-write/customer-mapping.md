---
title: 集成客户主控
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的客户数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36716c302d86bc5715798bf4cf4899f666d0872c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997446"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="a363a-103">集成客户主数据</span><span class="sxs-lookup"><span data-stu-id="a363a-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="a363a-104">可以在多个 Dynamics 365 应用程序中掌管客户数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="a363a-105">例如，客户记录可以源自 Dynamics 365 Sales（Dynamics 365 中的模型驱动应用）中的销售活动，或者记录可以源自 Dynamics 365 Commerce（一个 Finance and Operations 应用）中的零售活动。</span><span class="sxs-lookup"><span data-stu-id="a363a-105">For example, a customer record can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a record can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="a363a-106">无论客户数据源自何处，它都在后台集成。</span><span class="sxs-lookup"><span data-stu-id="a363a-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="a363a-107">集成的客户主数据使您可以灵活地在任何 Dynamics 365 应用程序中掌管客户数据，并在整个 Dynamics 365 应用程序套件中提供客户的全面概览。</span><span class="sxs-lookup"><span data-stu-id="a363a-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="a363a-108">客户数据流</span><span class="sxs-lookup"><span data-stu-id="a363a-108">Customer data flow</span></span>

<span data-ttu-id="a363a-109">*客户* 是应用程序中精心定义的概念。</span><span class="sxs-lookup"><span data-stu-id="a363a-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="a363a-110">因此，客户数据的集成包括在这两个应用程序之间协调客户概念。</span><span class="sxs-lookup"><span data-stu-id="a363a-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="a363a-111">下图显示客户数据流。</span><span class="sxs-lookup"><span data-stu-id="a363a-111">The following illustration shows the customer data flow.</span></span>

![客户数据流](media/dual-write-customer-data-flow.png)

<span data-ttu-id="a363a-113">客户可以大致分为两类：商业/组织客户和消费者/最终用户。</span><span class="sxs-lookup"><span data-stu-id="a363a-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="a363a-114">这两种类型的客户存储在 Finance and Operations 和 Common Data Service 中并以不同方式处理。</span><span class="sxs-lookup"><span data-stu-id="a363a-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="a363a-115">在 Finance and Operations 中，商业/组织客户和消费者/最终用户在名为 **CustTable** (CustCustomerV3Entity) 的一个表中主控，并根据 **类型** 属性分类。</span><span class="sxs-lookup"><span data-stu-id="a363a-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="a363a-116">（如果 **类型** 设置为 **组织** ，则客户为商业/组织客户，如果 **类型** 设置为 **个人** ，则客户为消费者/最终用户。）主联系人信息通过 SMMContactPersonEntity 实体处理。</span><span class="sxs-lookup"><span data-stu-id="a363a-116">(If **Type** is set to **Organization** , the customer is a commercial/organizational customer, and if **Type** is set to **Person** , the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="a363a-117">在 Common Data Service 中，商业/组织客户在“客户”实体中主控，并在 **RelationshipType** 属性设置为 **客户** 时标识为客户。</span><span class="sxs-lookup"><span data-stu-id="a363a-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="a363a-118">消费者/最终用户和联系人均通过联系人实体表示。</span><span class="sxs-lookup"><span data-stu-id="a363a-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="a363a-119">为了提供客户/最终用户与联系人之间的清晰界限， **联系人** 实体有一个布尔值标记，名称为 **Sellable** 。</span><span class="sxs-lookup"><span data-stu-id="a363a-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="a363a-120">如果 **Sellable** 为 **True** ，则联系人为消费者/最终用户，可以为该联系人创建报价单和订单。</span><span class="sxs-lookup"><span data-stu-id="a363a-120">When **Sellable** is **True** , the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="a363a-121">如果 **Sellable** 为 **False** ，则联系人只是客户的主要联系人。</span><span class="sxs-lookup"><span data-stu-id="a363a-121">When **Sellable** is **False** , the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="a363a-122">如果非适销联系人参与报价单或订单流程，则 **Sellable** 设置为 **True** 以将该联系人标记为适销联系人。</span><span class="sxs-lookup"><span data-stu-id="a363a-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="a363a-123">已成为适销联系人的联系人仍是适销联系人。</span><span class="sxs-lookup"><span data-stu-id="a363a-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="a363a-124">模板</span><span class="sxs-lookup"><span data-stu-id="a363a-124">Templates</span></span>

<span data-ttu-id="a363a-125">客户数据包括有关客户的所有信息，如客户组、地址、联系信息、付款配置文件、发票配置文件和会员状态。</span><span class="sxs-lookup"><span data-stu-id="a363a-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="a363a-126">客户数据交互期间，实体映射集合协同工作，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="a363a-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a363a-127">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="a363a-127">Finance and Operations apps</span></span> | <span data-ttu-id="a363a-128">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="a363a-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="a363a-129">说明</span><span class="sxs-lookup"><span data-stu-id="a363a-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="a363a-130">CDS 联系人 V2</span><span class="sxs-lookup"><span data-stu-id="a363a-130">CDS Contacts V2</span></span>             | <span data-ttu-id="a363a-131">联系人</span><span class="sxs-lookup"><span data-stu-id="a363a-131">contacts</span></span>                        | <span data-ttu-id="a363a-132">此模板同步客户和供应商的所有第一、第二和第三联系信息。</span><span class="sxs-lookup"><span data-stu-id="a363a-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-133">客户组</span><span class="sxs-lookup"><span data-stu-id="a363a-133">Customer groups</span></span>             | <span data-ttu-id="a363a-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="a363a-134">msdyn_customergroups</span></span>            | <span data-ttu-id="a363a-135">此模板同步客户组信息。</span><span class="sxs-lookup"><span data-stu-id="a363a-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="a363a-136">客户付款方式</span><span class="sxs-lookup"><span data-stu-id="a363a-136">Customer payment method</span></span>     | <span data-ttu-id="a363a-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="a363a-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="a363a-138">此模板同步客户付款方式信息。</span><span class="sxs-lookup"><span data-stu-id="a363a-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="a363a-139">客户 V3</span><span class="sxs-lookup"><span data-stu-id="a363a-139">Customers V3</span></span>                | <span data-ttu-id="a363a-140">帐户</span><span class="sxs-lookup"><span data-stu-id="a363a-140">accounts</span></span>                        | <span data-ttu-id="a363a-141">此模板同步商业客户和组织客户的客户主信息。</span><span class="sxs-lookup"><span data-stu-id="a363a-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="a363a-142">客户 V3</span><span class="sxs-lookup"><span data-stu-id="a363a-142">Customers V3</span></span>                | <span data-ttu-id="a363a-143">联系人</span><span class="sxs-lookup"><span data-stu-id="a363a-143">contacts</span></span>                        | <span data-ttu-id="a363a-144">此模板同步消费者和最终用户的客户主数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="a363a-145">名称词缀</span><span class="sxs-lookup"><span data-stu-id="a363a-145">Name affixes</span></span>                | <span data-ttu-id="a363a-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="a363a-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="a363a-147">此模板同步客户和供应商的名称词缀引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-148">付款日行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="a363a-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="a363a-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="a363a-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="a363a-150">此模板同步客户和供应商的付款日行引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-151">付款日 CDS</span><span class="sxs-lookup"><span data-stu-id="a363a-151">Payment days CDS</span></span>            | <span data-ttu-id="a363a-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="a363a-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="a363a-153">此模板同步客户和供应商的付款日引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-154">付款计划行</span><span class="sxs-lookup"><span data-stu-id="a363a-154">Payment schedule lines</span></span>      | <span data-ttu-id="a363a-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="a363a-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="a363a-156">同步客户和供应商的付款计划行引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-157">付款计划</span><span class="sxs-lookup"><span data-stu-id="a363a-157">Payment schedule</span></span>            | <span data-ttu-id="a363a-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="a363a-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="a363a-159">此模板同步客户和供应商的付款计划引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a363a-160">付款期限</span><span class="sxs-lookup"><span data-stu-id="a363a-160">Terms of payment</span></span>            | <span data-ttu-id="a363a-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="a363a-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="a363a-162">此模板同步客户和供应商的付款期限引用数据。</span><span class="sxs-lookup"><span data-stu-id="a363a-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
