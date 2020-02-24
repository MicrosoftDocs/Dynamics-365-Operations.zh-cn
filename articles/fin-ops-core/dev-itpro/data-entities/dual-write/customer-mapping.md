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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019663"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="b8b95-103">集成的客户主数据</span><span class="sxs-lookup"><span data-stu-id="b8b95-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b8b95-104">客户记录通常主控在多个应用程序中。</span><span class="sxs-lookup"><span data-stu-id="b8b95-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="b8b95-105">例如，销售活动可通过 Sales 应用程序获取商业客户记录，而电子商务和零售则可通过 Finance and Operations 应用程序获取客户记录。</span><span class="sxs-lookup"><span data-stu-id="b8b95-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="b8b95-106">无论客户记录源自何处，都跨越应用程序边界和基础结构差异在后台集成。</span><span class="sxs-lookup"><span data-stu-id="b8b95-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="b8b95-107">集成客户主控可以帮助处理多主控场景，并提供客户对 Dynamics 365 应用程序套件丰富的见解。</span><span class="sxs-lookup"><span data-stu-id="b8b95-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="b8b95-108">客户数据流</span><span class="sxs-lookup"><span data-stu-id="b8b95-108">Customer data flow</span></span>

<span data-ttu-id="b8b95-109">*客户*是应用程序中精心定义的概念。</span><span class="sxs-lookup"><span data-stu-id="b8b95-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="b8b95-110">因此，客户数据的集成包括在这两个应用程序之间协调客户概念。</span><span class="sxs-lookup"><span data-stu-id="b8b95-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="b8b95-111">下图显示客户数据流。</span><span class="sxs-lookup"><span data-stu-id="b8b95-111">The following illustration shows the customer data flow.</span></span>

![客户数据流](media/dual-write-customer-data-flow.png)

<span data-ttu-id="b8b95-113">客户可以大致分为两类：商业/组织客户和消费者/最终用户。</span><span class="sxs-lookup"><span data-stu-id="b8b95-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="b8b95-114">这两种类型的客户存储在 Finance and Operations 和 Common Data Service 中并以不同方式处理。</span><span class="sxs-lookup"><span data-stu-id="b8b95-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="b8b95-115">在 Finance and Operations 中，商业/组织客户和消费者/最终用户在名为 **CustTable** (CustomerCustomerV3Entity) 的一个表中主控，并根据**类型**属性分类。</span><span class="sxs-lookup"><span data-stu-id="b8b95-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="b8b95-116">（如果**类型**设置为**组织**，则客户为商业/组织客户，如果**类型**设置为**个人**，则客户为消费者/最终用户。）主联系人信息通过 SMMContactPersonEntity 实体处理。</span><span class="sxs-lookup"><span data-stu-id="b8b95-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="b8b95-117">在 Common Data Service 中，商业/组织客户在“客户”实体中主控，并在 **RelationshipType** 属性设置为**客户**时标识为客户。</span><span class="sxs-lookup"><span data-stu-id="b8b95-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="b8b95-118">消费者/最终用户和联系人均通过联系人实体表示。</span><span class="sxs-lookup"><span data-stu-id="b8b95-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="b8b95-119">为了提供客户/最终用户与联系人之间的清晰界限，**联系人**实体有一个布尔值标记，名称为 **Sellable**。</span><span class="sxs-lookup"><span data-stu-id="b8b95-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="b8b95-120">如果 **Sellable** 为 **True**，则联系人为消费者/最终用户，可以为该联系人创建报价单和订单。</span><span class="sxs-lookup"><span data-stu-id="b8b95-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="b8b95-121">如果 **Sellable** 为 **False**，则联系人只是客户的主要联系人。</span><span class="sxs-lookup"><span data-stu-id="b8b95-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="b8b95-122">如果非适销联系人参与报价单或订单流程，则 **Sellable** 设置为 **True** 以将该联系人标记为适销联系人。</span><span class="sxs-lookup"><span data-stu-id="b8b95-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="b8b95-123">已成为适销联系人的联系人仍是适销联系人。</span><span class="sxs-lookup"><span data-stu-id="b8b95-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="b8b95-124">模板</span><span class="sxs-lookup"><span data-stu-id="b8b95-124">Templates</span></span>

<span data-ttu-id="b8b95-125">客户数据包括有关客户的所有信息，如客户组、地址、联系信息、付款配置文件、发票配置文件和会员状态。</span><span class="sxs-lookup"><span data-stu-id="b8b95-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="b8b95-126">客户数据交互期间，实体映射集合协同工作，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="b8b95-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b8b95-127">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="b8b95-127">Finance and Operations apps</span></span> | <span data-ttu-id="b8b95-128">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="b8b95-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="b8b95-129">说明</span><span class="sxs-lookup"><span data-stu-id="b8b95-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="b8b95-130">CDS 联系人 V2</span><span class="sxs-lookup"><span data-stu-id="b8b95-130">CDS Contacts V2</span></span>             | <span data-ttu-id="b8b95-131">联系人</span><span class="sxs-lookup"><span data-stu-id="b8b95-131">contacts</span></span>                        | <span data-ttu-id="b8b95-132">此模板同步客户和供应商的所有第一、第二和第三联系信息。</span><span class="sxs-lookup"><span data-stu-id="b8b95-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-133">客户组</span><span class="sxs-lookup"><span data-stu-id="b8b95-133">Customer groups</span></span>             | <span data-ttu-id="b8b95-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="b8b95-134">msdyn_customergroups</span></span>            | <span data-ttu-id="b8b95-135">此模板同步客户组信息。</span><span class="sxs-lookup"><span data-stu-id="b8b95-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="b8b95-136">客户付款方式</span><span class="sxs-lookup"><span data-stu-id="b8b95-136">Customer payment method</span></span>     | <span data-ttu-id="b8b95-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="b8b95-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="b8b95-138">此模板同步客户付款方式信息。</span><span class="sxs-lookup"><span data-stu-id="b8b95-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="b8b95-139">客户 V3</span><span class="sxs-lookup"><span data-stu-id="b8b95-139">Customers V3</span></span>                | <span data-ttu-id="b8b95-140">帐户</span><span class="sxs-lookup"><span data-stu-id="b8b95-140">accounts</span></span>                        | <span data-ttu-id="b8b95-141">此模板同步商业客户和组织客户的客户主信息。</span><span class="sxs-lookup"><span data-stu-id="b8b95-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="b8b95-142">客户 V3</span><span class="sxs-lookup"><span data-stu-id="b8b95-142">Customers V3</span></span>                | <span data-ttu-id="b8b95-143">联系人</span><span class="sxs-lookup"><span data-stu-id="b8b95-143">contacts</span></span>                        | <span data-ttu-id="b8b95-144">此模板同步消费者和最终用户的客户主数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="b8b95-145">会员卡</span><span class="sxs-lookup"><span data-stu-id="b8b95-145">Loyalty card</span></span>                | <span data-ttu-id="b8b95-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="b8b95-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="b8b95-147">此模板同步客户会员卡信息。</span><span class="sxs-lookup"><span data-stu-id="b8b95-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="b8b95-148">名称词缀</span><span class="sxs-lookup"><span data-stu-id="b8b95-148">Name affixes</span></span>                | <span data-ttu-id="b8b95-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="b8b95-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="b8b95-150">此模板同步客户和供应商的名称词缀引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-151">付款日行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="b8b95-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="b8b95-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="b8b95-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="b8b95-153">此模板同步客户和供应商的付款日行引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-154">付款日 CDS</span><span class="sxs-lookup"><span data-stu-id="b8b95-154">Payment days CDS</span></span>            | <span data-ttu-id="b8b95-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="b8b95-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="b8b95-156">此模板同步客户和供应商的付款日引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-157">付款计划行</span><span class="sxs-lookup"><span data-stu-id="b8b95-157">Payment schedule lines</span></span>      | <span data-ttu-id="b8b95-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="b8b95-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="b8b95-159">同步客户和供应商的付款计划行引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-160">付款计划</span><span class="sxs-lookup"><span data-stu-id="b8b95-160">Payment schedule</span></span>            | <span data-ttu-id="b8b95-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="b8b95-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="b8b95-162">此模板同步客户和供应商的付款计划引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b8b95-163">付款期限</span><span class="sxs-lookup"><span data-stu-id="b8b95-163">Terms of payment</span></span>            | <span data-ttu-id="b8b95-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="b8b95-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="b8b95-165">此模板同步客户和供应商的付款期限引用数据。</span><span class="sxs-lookup"><span data-stu-id="b8b95-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
