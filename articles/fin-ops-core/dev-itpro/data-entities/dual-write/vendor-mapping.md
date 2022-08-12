---
title: 集成的供应商主数据
description: 本文介绍财务和运营应用与 Dataverse 之间的供应商数据集成。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112185"
---
# <a name="integrated-vendor-master"></a>集成的供应商主数据

[!include [banner](../../includes/banner.md)]



术语 *供应商* 是指为企业提供商品或服务的供应商组织或独立经营者。 尽管 *供应商* 是 Microsoft Dynamics 365 Supply Chain Management 中的一个熟悉的概念，但客户互动应用中不存在供应商这个概念。 但是，您可以重载 **客户/联系人** 表来存储供应商信息。 集成的供应商主数据在客户互动应用中引入了明确的供应商概念。 您可以使用新的供应商设计，也可以将供应商数据存储在 **客户/联系人** 表中。 双写入同时支持这两种方法。

在这两种方法中，供应商数据在 Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service 和 Power Apps 门户之间集成。 在 Supply Chain Management 中，此数据可用于工作流，如采购申请和采购订单。

## <a name="vendor-data-flow"></a>供应商数据流

如果您不希望将供应商数据存储在 Dataverse 中的 **客户/联系人** 表中，您可以使用新的供应商设计。

![供应商数据流。](media/dual-write-vendor-data-flow.png)

如果您希望继续将供应商数据存储在 **客户/联系人** 表中，您可以使用扩展的供应商设计。 要使用扩展的供应商设计，必须在双写入解决方案包中配置供应商工作流。 有关详细信息，请参阅[在供应商设计之间切换](vendor-switch.md)。

![扩展供应商数据流。](media/dual-write-vendor-detail.jpg)

> [!TIP]
> 如果您正在使用自助服务供应商的 Power Apps 门户，供应商信息可以直接流向财务和运营应用。

## <a name="templates"></a>模板

供应商数据包括有关供应商的所有信息，如供应商组、地址、联系信息、付款配置文件、发票配置文件和会员状态。 供应商数据交互期间，表映射集合协同工作，如下表中所示。

财务和运营应用 | 客户互动应用     | 说明
----------------------------|-----------------------------|------------
[CDS 联系人 V2](mapping-reference.md#115) | 联系人 | 此模板同步客户和供应商的所有第一、第二和第三联系信息。
[名称词缀](mapping-reference.md#155) | msdyn_nameaffixes | 此模板同步客户和供应商的名称词缀引用数据。
[付款日行 CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | 此模板同步客户和供应商的付款日行引用数据。
[付款日 CDS](mapping-reference.md#158) | msdyn_paymentdays | 此模板同步客户和供应商的付款日引用数据。
[付款计划行](mapping-reference.md#159) | msdyn_paymentschedulelines | 同步客户和供应商的付款计划行引用数据。
[付款计划](mapping-reference.md#160) | msdyn_paymentschedules | 此模板同步客户和供应商的付款计划引用数据。
[付款期限](mapping-reference.md#161) | msdyn_paymentterms | 此模板同步客户和供应商的付款期限引用数据。
[供应商 V2](mapping-reference.md#202) | msdyn_vendors | 使用适用于供应商的自定义解决方案的企业可以利用因财务和运营应用集成而在 Dataverse 中引入的现成供应商概念。
[供应商组](mapping-reference.md#200) | msdyn_vendorgroups | 此模板同步供应商组信息。
[供应商付款方式](mapping-reference.md#201) | msdyn_vendorpaymentmethods | 此模板同步供应商付款方式信息。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

