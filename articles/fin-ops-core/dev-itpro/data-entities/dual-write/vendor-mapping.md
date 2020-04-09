---
title: 集成的供应商主数据
description: 本主题介绍 Finance and Operations 应用与 Common Data Service 之间的供应商数据集成。
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
ms.openlocfilehash: 8d531ed4e46d8ee5d2b0937b6efc480e051fe708
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173100"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="a1a4d-103">集成的供应商主数据</span><span class="sxs-lookup"><span data-stu-id="a1a4d-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a1a4d-104">术语*供应商*是指为企业提供商品或服务的供应商组织或独立经营者。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-104">The term *vendor* refers to a supplier organization, or a sole proprietor who supplies goods or services to a business.</span></span> <span data-ttu-id="a1a4d-105">尽管*供应商*是 Microsoft Dynamics 365 Supply Chain Management 中的一个熟悉的概念，而 Dynamics 365 中的模型驱动应用中则不存在供应商这个概念。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-105">Although *vendor* is an established concept in Microsoft Dynamics 365 Supply Chain Management, no vendor concept exists in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a1a4d-106">但是，您可以重载**客户/联系人**实体来存储供应商信息。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-106">However, you can overload the **Account/Contact** entity to store vendor information.</span></span> <span data-ttu-id="a1a4d-107">集成的供应商主数据在 Dynamics 365 中的模型驱动应用中引入了明确的供应商概念。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-107">The integrated vendor master introduces an explicit vendor concept in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a1a4d-108">您可以使用新的供应商设计，也可以将供应商数据存储在**客户/联系人**实体中。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-108">You can either use the new vendor design or store vendor data in the **Account/Contact** entity.</span></span> <span data-ttu-id="a1a4d-109">双写入同时支持这两种方法。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-109">Dual-write supports both approaches.</span></span>

<span data-ttu-id="a1a4d-110">在这两种方法中，供应商数据在 Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service 和 Power Apps 门户之间集成。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-110">In both approaches, the vendor data is integrated between Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, and Power Apps portals.</span></span> <span data-ttu-id="a1a4d-111">在 Supply Chain Management 中，此数据可用于工作流，如采购申请和采购订单。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-111">In Supply Chain Management, the data is available for workflows such as purchase requisitions and purchase orders.</span></span>

## <a name="vendor-data-flow"></a><span data-ttu-id="a1a4d-112">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="a1a4d-112">Vendor data flow</span></span>

<span data-ttu-id="a1a4d-113">如果您不希望将供应商数据存储在 Common Data Service 中的**客户/联系人**实体中，您可以使用新的供应商设计。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-113">If you don't want to store vendor data in the **Account/Contact** entity in Common Data Service, you can use the new vendor design.</span></span>

![供应商数据流](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="a1a4d-115">如果您希望继续将供应商数据存储在**客户/联系人**实体中，您可以使用扩展的供应商设计。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-115">If you want to continue to store vendor data in the **Account/Contact** entity, you can use the extended vendor design.</span></span> <span data-ttu-id="a1a4d-116">要使用扩展的供应商设计，必须在双写入解决方案包中配置供应商工作流。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-116">To use the extended vendor design, you must configure the vendor workflows in the dual-write solution package.</span></span> <span data-ttu-id="a1a4d-117">有关详细信息，请参阅[在供应商设计之间切换](vendor-switch.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-117">For more information, see [Switch between vendor designs](vendor-switch.md).</span></span>

![扩展供应商数据流](media/dual-write-vendor-detail.jpg)

> [!TIP]
> <span data-ttu-id="a1a4d-119">如果您正在使用自助服务供应商的 Power Apps 门户，供应商信息可以直接流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-119">If you're using Power Apps portals for self-service vendors, the vendor information can flow directly to Finance and Operations apps.</span></span>

## <a name="templates"></a><span data-ttu-id="a1a4d-120">模板</span><span class="sxs-lookup"><span data-stu-id="a1a4d-120">Templates</span></span>

<span data-ttu-id="a1a4d-121">供应商数据包括有关供应商的所有信息，如供应商组、地址、联系信息、付款配置文件、发票配置文件和会员状态。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="a1a4d-122">供应商数据交互期间，实体映射集合协同工作，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-122">A collection of entity maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a1a4d-123">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="a1a4d-123">Finance and Operations apps</span></span> | <span data-ttu-id="a1a4d-124">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="a1a4d-124">Other Dynamics 365 apps</span></span>     | <span data-ttu-id="a1a4d-125">说明</span><span class="sxs-lookup"><span data-stu-id="a1a4d-125">Description</span></span>
----------------------------|-----------------------------|------------
<span data-ttu-id="a1a4d-126">供应商 V2</span><span class="sxs-lookup"><span data-stu-id="a1a4d-126">Vendor V2</span></span>                   | <span data-ttu-id="a1a4d-127">科目</span><span class="sxs-lookup"><span data-stu-id="a1a4d-127">Account</span></span>                     | <span data-ttu-id="a1a4d-128">使用供应商实体存储供应商信息的企业可以继续按照相同方法使用此实体。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-128">Businesses that use the Account entity to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="a1a4d-129">还可以利用 Finance and Operations 应用集成带来的显式供应商功能。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="a1a4d-130">供应商 V2</span><span class="sxs-lookup"><span data-stu-id="a1a4d-130">Vendor V2</span></span>                   | <span data-ttu-id="a1a4d-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="a1a4d-131">Msdyn\_vendors</span></span>              | <span data-ttu-id="a1a4d-132">使用适用于供应商的自定义解决方案的企业可以利用因 Finance and Operations 应用集成而在 Common Data Service 中引入的现成供应商概念。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Common Data Service because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="a1a4d-133">供应商组</span><span class="sxs-lookup"><span data-stu-id="a1a4d-133">Vendor groups</span></span>               | <span data-ttu-id="a1a4d-134">msdyn\_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="a1a4d-134">msdyn\_vendorgroups</span></span>         | <span data-ttu-id="a1a4d-135">此模板同步供应商组信息。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="a1a4d-136">供应商付款方式</span><span class="sxs-lookup"><span data-stu-id="a1a4d-136">Vendor payment method</span></span>       | <span data-ttu-id="a1a4d-137">msdyn\_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="a1a4d-137">msdyn\_vendorpaymentmethods</span></span> | <span data-ttu-id="a1a4d-138">此模板同步供应商付款方式信息。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="a1a4d-139">CDS 联系人 V2</span><span class="sxs-lookup"><span data-stu-id="a1a4d-139">CDS Contacts V2</span></span>             | <span data-ttu-id="a1a4d-140">联系人</span><span class="sxs-lookup"><span data-stu-id="a1a4d-140">contacts</span></span>                    | <span data-ttu-id="a1a4d-141">[联系人](customer-mapping.md#cds-contacts-v2-to-contacts)模板同步客户和供应商的所有第一、第二和第三联系信息。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="a1a4d-142">付款计划行</span><span class="sxs-lookup"><span data-stu-id="a1a4d-142">Payment schedule lines</span></span>      | <span data-ttu-id="a1a4d-143">msdyn\_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="a1a4d-143">msdyn\_paymentschedulelines</span></span> | <span data-ttu-id="a1a4d-144">[付款计划行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)模板同步客户和供应商的引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="a1a4d-145">付款计划</span><span class="sxs-lookup"><span data-stu-id="a1a4d-145">Payment schedule</span></span>            | <span data-ttu-id="a1a4d-146">msdyn\_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="a1a4d-146">msdyn\_paymentschedules</span></span>     | <span data-ttu-id="a1a4d-147">[付款计划](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)模板同步客户和供应商的付款计划引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1a4d-148">付款日行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="a1a4d-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="a1a4d-149">msdyn\_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="a1a4d-149">msdyn\_paymentdaylines</span></span>      | <span data-ttu-id="a1a4d-150">[付款日行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)模板同步客户和供应商的付款日行引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="a1a4d-151">付款日 CDS</span><span class="sxs-lookup"><span data-stu-id="a1a4d-151">Payment days CDS</span></span>            | <span data-ttu-id="a1a4d-152">msdyn\_paymentdays</span><span class="sxs-lookup"><span data-stu-id="a1a4d-152">msdyn\_paymentdays</span></span>          | <span data-ttu-id="a1a4d-153">[付款日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)模板同步客户和供应商的付款日引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1a4d-154">付款期限</span><span class="sxs-lookup"><span data-stu-id="a1a4d-154">Terms of payment</span></span>            | <span data-ttu-id="a1a4d-155">msdyn\_paymentterms</span><span class="sxs-lookup"><span data-stu-id="a1a4d-155">msdyn\_paymentterms</span></span>         | <span data-ttu-id="a1a4d-156">[付款期限](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)模板同步客户和供应商的付款期限引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a1a4d-157">名称词缀</span><span class="sxs-lookup"><span data-stu-id="a1a4d-157">Name affixes</span></span>                | <span data-ttu-id="a1a4d-158">msdyn\_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="a1a4d-158">msdyn\_nameaffixes</span></span>          | <span data-ttu-id="a1a4d-159">[名称词缀](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)模板同步客户和供应商的名称词缀引用数据。</span><span class="sxs-lookup"><span data-stu-id="a1a4d-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
