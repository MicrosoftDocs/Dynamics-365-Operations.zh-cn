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
# <a name="integrated-vendor-master"></a>集成的供应商主数据

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

*供应商*指的是供应链过程中为企业提供货物的供应商组织或独立经营者。 尽管*供应商*是 Finance and Operations 应用中的一个熟悉的概念，而其他 Dynamics 365 应用中则不存在供应商这个概念。 相反，某些企业会重用客户实体来同时存储客户信息和供应商信息。 其他企业则使用自定义的供应商概念。 Common Data Service 集成同时支持这两种设计。 因此，您可以根据业务场景来启用其中一种设计。

Finance and Operations 应用与其他 Dynamics 365 应用之间的供应商数据集成让您可以对数据实现多主控处理。 无论供应商数据源自何处，都跨越应用程序边界和基础结构差异在后台集成。 

### <a name="vendor-data-flow"></a>供应商数据流

如果要使用其他 Dynamics 365 应用进行供应商主控，并且希望隔离供应商信息与客户信息，可以使用这种新的供应商设计。

![供应商数据流](media/dual-write-vendor-data-flow.png)

如果要使用其他 Dynamics 365 应用进行供应商主控，并且希望继续使用客户实体存储供应商信息，可以使用这种新的扩展供应商设计。 在这种设计中，扩展供应商信息（如供应商组和供应商过帐模板）存储在供应商供应商详细信息中。

![扩展供应商数据流](media/dual-write-vendor-detail.jpg)

供应商联系信息中包含客户联系信息。 在后台，联系人的信息在同一个实体中存储和检索。

## <a name="templates"></a>模板

供应商数据包括有关供应商的所有信息，如供应商组、地址、联系信息、付款配置文件、发票配置文件和会员状态。 供应商数据交互期间，实体映射集合协同工作，如下表中所示。

Finance and Operations 应用 | 其他 Dynamics 365 应用         | 说明
----------------------------|---------------------------------|------------
供应商 V2               | 科目 | 使用供应商实体存储供应商信息的企业可以继续按照相同方法使用此实体。 还可以利用 Finance and Operations 应用集成带来的显式供应商功能。
供应商 V2               | Msdyn\_vendors | 使用适用于供应商的自定义解决方案的企业可以利用因 Finance and Operations 应用集成而在 Common Data Service 中引入的现成供应商概念。 
供应商组 | msdyn_vendorgroups | 此模板同步供应商组信息。
供应商付款方式 | msdyn_vendorpaymentmethods | 此模板同步供应商付款方式信息。
CDS 联系人 V2             | 联系人                        | [联系人](customer-mapping.md#cds-contacts-v2-to-contacts)模板同步客户和供应商的所有第一、第二和第三联系信息。
付款计划行      | msdyn_paymentschedulelines      | [付款计划行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)模板同步客户和供应商的引用数据。
付款计划            | msdyn_paymentschedules          | [付款计划](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)模板同步客户和供应商的付款计划引用数据。
付款日行 CDS V2    | msdyn_paymentdaylines           | [付款日行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)模板同步客户和供应商的付款日行引用数据。
付款日 CDS            | msdyn_paymentdays               | [付款日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)模板同步客户和供应商的付款日引用数据。
付款期限            | msdyn_paymentterms              | [付款期限](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)模板同步客户和供应商的付款期限引用数据。
名称词缀                | msdyn_nameaffixes               | [名称词缀](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)模板同步客户和供应商的名称词缀引用数据。

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
