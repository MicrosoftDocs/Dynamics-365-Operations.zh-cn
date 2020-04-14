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
# <a name="integrated-vendor-master"></a>集成的供应商主数据

[!include [banner](../../includes/banner.md)]



术语*供应商*是指为企业提供商品或服务的供应商组织或独立经营者。 尽管*供应商*是 Microsoft Dynamics 365 Supply Chain Management 中的一个熟悉的概念，而 Dynamics 365 中的模型驱动应用中则不存在供应商这个概念。 但是，您可以重载**客户/联系人**实体来存储供应商信息。 集成的供应商主数据在 Dynamics 365 中的模型驱动应用中引入了明确的供应商概念。 您可以使用新的供应商设计，也可以将供应商数据存储在**客户/联系人**实体中。 双写入同时支持这两种方法。

在这两种方法中，供应商数据在 Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service 和 Power Apps 门户之间集成。 在 Supply Chain Management 中，此数据可用于工作流，如采购申请和采购订单。

## <a name="vendor-data-flow"></a>供应商数据流

如果您不希望将供应商数据存储在 Common Data Service 中的**客户/联系人**实体中，您可以使用新的供应商设计。

![供应商数据流](media/dual-write-vendor-data-flow.png)

如果您希望继续将供应商数据存储在**客户/联系人**实体中，您可以使用扩展的供应商设计。 要使用扩展的供应商设计，必须在双写入解决方案包中配置供应商工作流。 有关详细信息，请参阅[在供应商设计之间切换](vendor-switch.md)。

![扩展供应商数据流](media/dual-write-vendor-detail.jpg)

> [!TIP]
> 如果您正在使用自助服务供应商的 Power Apps 门户，供应商信息可以直接流向 Finance and Operations 应用。

## <a name="templates"></a>模板

供应商数据包括有关供应商的所有信息，如供应商组、地址、联系信息、付款配置文件、发票配置文件和会员状态。 供应商数据交互期间，实体映射集合协同工作，如下表中所示。

Finance and Operations 应用 | 其他 Dynamics 365 应用     | 说明
----------------------------|-----------------------------|------------
供应商 V2                   | 科目                     | 使用供应商实体存储供应商信息的企业可以继续按照相同方法使用此实体。 还可以利用 Finance and Operations 应用集成带来的显式供应商功能。
供应商 V2                   | Msdyn\_vendors              | 使用适用于供应商的自定义解决方案的企业可以利用因 Finance and Operations 应用集成而在 Common Data Service 中引入的现成供应商概念。 
供应商组               | msdyn\_vendorgroups         | 此模板同步供应商组信息。
供应商付款方式       | msdyn\_vendorpaymentmethods | 此模板同步供应商付款方式信息。
CDS 联系人 V2             | 联系人                    | [联系人](customer-mapping.md#cds-contacts-v2-to-contacts)模板同步客户和供应商的所有第一、第二和第三联系信息。
付款计划行      | msdyn\_paymentschedulelines | [付款计划行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)模板同步客户和供应商的引用数据。
付款计划            | msdyn\_paymentschedules     | [付款计划](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)模板同步客户和供应商的付款计划引用数据。
付款日行 CDS V2    | msdyn\_paymentdaylines      | [付款日行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)模板同步客户和供应商的付款日行引用数据。
付款日 CDS            | msdyn\_paymentdays          | [付款日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)模板同步客户和供应商的付款日引用数据。
付款期限            | msdyn\_paymentterms         | [付款期限](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)模板同步客户和供应商的付款期限引用数据。
名称词缀                | msdyn\_nameaffixes          | [名称词缀](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)模板同步客户和供应商的名称词缀引用数据。

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
