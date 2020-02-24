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
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019654"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="d8beb-103">集成的供应商主数据</span><span class="sxs-lookup"><span data-stu-id="d8beb-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d8beb-104">*供应商*指的是供应链过程中为企业提供货物的供应商组织或独立经营者。</span><span class="sxs-lookup"><span data-stu-id="d8beb-104">The term *vendor* refers to a supplier organization or a sole proprietor that is part of the supply chain process, and that supplies goods for the business.</span></span> <span data-ttu-id="d8beb-105">尽管*供应商*是 Finance and Operations 应用中的一个熟悉的概念，而其他 Dynamics 365 应用中则不存在供应商这个概念。</span><span class="sxs-lookup"><span data-stu-id="d8beb-105">Although *vendor* is an established concept in Finance and Operations apps, a vendor concept doesn't exist in other Dynamics 365 apps.</span></span> <span data-ttu-id="d8beb-106">相反，某些企业会重用客户实体来同时存储客户信息和供应商信息。</span><span class="sxs-lookup"><span data-stu-id="d8beb-106">Instead, some businesses overload the Account entity to store both customer information and vendor information.</span></span> <span data-ttu-id="d8beb-107">其他企业则使用自定义的供应商概念。</span><span class="sxs-lookup"><span data-stu-id="d8beb-107">Other businesses use a custom vendor concept.</span></span> <span data-ttu-id="d8beb-108">Common Data Service 集成同时支持这两种设计。</span><span class="sxs-lookup"><span data-stu-id="d8beb-108">Common Data Service integration supports both these designs.</span></span> <span data-ttu-id="d8beb-109">因此，您可以根据业务场景来启用其中一种设计。</span><span class="sxs-lookup"><span data-stu-id="d8beb-109">Therefore, you can enable either of the designs, depending on your business scenario.</span></span>

<span data-ttu-id="d8beb-110">Finance and Operations 应用与其他 Dynamics 365 应用之间的供应商数据集成让您可以对数据实现多主控处理。</span><span class="sxs-lookup"><span data-stu-id="d8beb-110">Integration of vendor data between Finance and Operations apps and other Dynamics 365 apps lets you multi-master the data.</span></span> <span data-ttu-id="d8beb-111">无论供应商数据源自何处，都跨越应用程序边界和基础结构差异在后台集成。</span><span class="sxs-lookup"><span data-stu-id="d8beb-111">Regardless of where the vendor data originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> 

### <a name="vendor-data-flow"></a><span data-ttu-id="d8beb-112">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="d8beb-112">Vendor data flow</span></span>

<span data-ttu-id="d8beb-113">如果要使用其他 Dynamics 365 应用进行供应商主控，并且希望隔离供应商信息与客户信息，可以使用这种新的供应商设计。</span><span class="sxs-lookup"><span data-stu-id="d8beb-113">If you want to use other Dynamics 365 apps for vendor mastering, and you want to isolate vendor information from customer information, you can use the new vendor design.</span></span>

![供应商数据流](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="d8beb-115">如果要使用其他 Dynamics 365 应用进行供应商主控，并且希望继续使用客户实体存储供应商信息，可以使用这种新的扩展供应商设计。</span><span class="sxs-lookup"><span data-stu-id="d8beb-115">If you want to use other Dynamics 365 apps for vendor mastering, and you want to continue to use the Account entity to store vendor information, you can use the new extended vendor design.</span></span> <span data-ttu-id="d8beb-116">在这种设计中，扩展供应商信息（如供应商组和供应商过帐模板）存储在供应商供应商详细信息中。</span><span class="sxs-lookup"><span data-stu-id="d8beb-116">In this design, extended vendor information, such as the vendor group and vendor posting profile, are stored in the vendor detail.</span></span>

![扩展供应商数据流](media/dual-write-vendor-detail.jpg)

<span data-ttu-id="d8beb-118">供应商联系信息中包含客户联系信息。</span><span class="sxs-lookup"><span data-stu-id="d8beb-118">Vendor contact information resembles customer contact information.</span></span> <span data-ttu-id="d8beb-119">在后台，联系人的信息在同一个实体中存储和检索。</span><span class="sxs-lookup"><span data-stu-id="d8beb-119">Behind the scenes, the contact person's information is stored and retrieved from the same entities.</span></span>

## <a name="templates"></a><span data-ttu-id="d8beb-120">模板</span><span class="sxs-lookup"><span data-stu-id="d8beb-120">Templates</span></span>

<span data-ttu-id="d8beb-121">供应商数据包括有关供应商的所有信息，如供应商组、地址、联系信息、付款配置文件、发票配置文件和会员状态。</span><span class="sxs-lookup"><span data-stu-id="d8beb-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="d8beb-122">供应商数据交互期间，实体映射集合协同工作，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="d8beb-122">A collection of entity maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="d8beb-123">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="d8beb-123">Finance and Operations apps</span></span> | <span data-ttu-id="d8beb-124">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="d8beb-124">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="d8beb-125">说明</span><span class="sxs-lookup"><span data-stu-id="d8beb-125">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="d8beb-126">供应商 V2</span><span class="sxs-lookup"><span data-stu-id="d8beb-126">Vendor V2</span></span>               | <span data-ttu-id="d8beb-127">科目</span><span class="sxs-lookup"><span data-stu-id="d8beb-127">Account</span></span> | <span data-ttu-id="d8beb-128">使用供应商实体存储供应商信息的企业可以继续按照相同方法使用此实体。</span><span class="sxs-lookup"><span data-stu-id="d8beb-128">Businesses that use the Account entity to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="d8beb-129">还可以利用 Finance and Operations 应用集成带来的显式供应商功能。</span><span class="sxs-lookup"><span data-stu-id="d8beb-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="d8beb-130">供应商 V2</span><span class="sxs-lookup"><span data-stu-id="d8beb-130">Vendor V2</span></span>               | <span data-ttu-id="d8beb-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="d8beb-131">Msdyn\_vendors</span></span> | <span data-ttu-id="d8beb-132">使用适用于供应商的自定义解决方案的企业可以利用因 Finance and Operations 应用集成而在 Common Data Service 中引入的现成供应商概念。</span><span class="sxs-lookup"><span data-stu-id="d8beb-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Common Data Service because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="d8beb-133">供应商组</span><span class="sxs-lookup"><span data-stu-id="d8beb-133">Vendor groups</span></span> | <span data-ttu-id="d8beb-134">msdyn_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="d8beb-134">msdyn_vendorgroups</span></span> | <span data-ttu-id="d8beb-135">此模板同步供应商组信息。</span><span class="sxs-lookup"><span data-stu-id="d8beb-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="d8beb-136">供应商付款方式</span><span class="sxs-lookup"><span data-stu-id="d8beb-136">Vendor payment method</span></span> | <span data-ttu-id="d8beb-137">msdyn_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="d8beb-137">msdyn_vendorpaymentmethods</span></span> | <span data-ttu-id="d8beb-138">此模板同步供应商付款方式信息。</span><span class="sxs-lookup"><span data-stu-id="d8beb-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="d8beb-139">CDS 联系人 V2</span><span class="sxs-lookup"><span data-stu-id="d8beb-139">CDS Contacts V2</span></span>             | <span data-ttu-id="d8beb-140">联系人</span><span class="sxs-lookup"><span data-stu-id="d8beb-140">contacts</span></span>                        | <span data-ttu-id="d8beb-141">[联系人](customer-mapping.md#cds-contacts-v2-to-contacts)模板同步客户和供应商的所有第一、第二和第三联系信息。</span><span class="sxs-lookup"><span data-stu-id="d8beb-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="d8beb-142">付款计划行</span><span class="sxs-lookup"><span data-stu-id="d8beb-142">Payment schedule lines</span></span>      | <span data-ttu-id="d8beb-143">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="d8beb-143">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="d8beb-144">[付款计划行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)模板同步客户和供应商的引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="d8beb-145">付款计划</span><span class="sxs-lookup"><span data-stu-id="d8beb-145">Payment schedule</span></span>            | <span data-ttu-id="d8beb-146">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="d8beb-146">msdyn_paymentschedules</span></span>          | <span data-ttu-id="d8beb-147">[付款计划](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)模板同步客户和供应商的付款计划引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d8beb-148">付款日行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="d8beb-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="d8beb-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="d8beb-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="d8beb-150">[付款日行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)模板同步客户和供应商的付款日行引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="d8beb-151">付款日 CDS</span><span class="sxs-lookup"><span data-stu-id="d8beb-151">Payment days CDS</span></span>            | <span data-ttu-id="d8beb-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="d8beb-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="d8beb-153">[付款日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)模板同步客户和供应商的付款日引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d8beb-154">付款期限</span><span class="sxs-lookup"><span data-stu-id="d8beb-154">Terms of payment</span></span>            | <span data-ttu-id="d8beb-155">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="d8beb-155">msdyn_paymentterms</span></span>              | <span data-ttu-id="d8beb-156">[付款期限](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)模板同步客户和供应商的付款期限引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d8beb-157">名称词缀</span><span class="sxs-lookup"><span data-stu-id="d8beb-157">Name affixes</span></span>                | <span data-ttu-id="d8beb-158">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="d8beb-158">msdyn_nameaffixes</span></span>               | <span data-ttu-id="d8beb-159">[名称词缀](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)模板同步客户和供应商的名称词缀引用数据。</span><span class="sxs-lookup"><span data-stu-id="d8beb-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
