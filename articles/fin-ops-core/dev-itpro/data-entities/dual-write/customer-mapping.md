---
title: 集成客户主控
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的客户数据集成。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0015ca2ccbb0098a5a96bf56ff355fb2f9f8f626
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748915"
---
# <a name="integrated-customer-master"></a>集成客户主数据

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


可以在多个 Dynamics 365 应用程序中掌管客户数据。 例如，客户行可以源自 Dynamics 365 Sales（Dynamics 365 中的模型驱动应用）中的销售活动，或者行可以源自 Dynamics 365 Commerce（一个 Finance and Operations 应用）中的零售活动。 无论客户数据源自何处，它都在后台集成。 集成的客户主数据使您可以灵活地在任何 Dynamics 365 应用程序中掌管客户数据，并在整个 Dynamics 365 应用程序套件中提供客户的全面概览。

## <a name="customer-data-flow"></a>客户数据流

*客户* 是应用程序中精心定义的概念。 因此，客户数据的集成包括在这两个应用程序之间协调客户概念。 下图显示客户数据流。

![客户数据流](media/dual-write-customer-data-flow.png)

客户可以大致分为两类：商业/组织客户和消费者/最终用户。 这两种类型的客户存储在 Finance and Operations 和 Dataverse 中并以不同方式处理。

在 Finance and Operations 中，商业/组织客户和消费者/最终用户在名为 **CustTable** (CustCustomerV3Entity) 的一个表中主控，并根据 **类型** 属性分类。 （如果 **类型** 设置为 **组织**，则客户为商业/组织客户，如果 **类型** 设置为 **个人**，则客户为消费者/最终用户。）主联系人信息通过 SMMContactPersonEntity 表处理。

在 Dataverse 中，商业/组织客户在客户表中主控，并在 **RelationshipType** 属性设置为 **客户** 时标识为客户。 消费者/最终用户和联系人均通过联系人表表示。 为了提供客户/最终用户与联系人之间的清晰界限，**联系人** 表有一个布尔值标记，名称为 **Sellable**。 如果 **Sellable** 为 **True**，则联系人为消费者/最终用户，可以为该联系人创建报价单和订单。 如果 **Sellable** 为 **False**，则联系人只是客户的主要联系人。

如果非适销联系人参与报价单或订单流程，则 **Sellable** 设置为 **True** 以将该联系人标记为适销联系人。 已成为适销联系人的联系人仍是适销联系人。

## <a name="templates"></a>模板

客户数据包括有关客户的所有信息，如客户组、地址、联系信息、付款配置文件、发票配置文件和会员状态。 客户数据交互期间，表映射集合协同工作，如下表中所示。

Finance and Operations 应用 | 其他 Dynamics 365 应用         | 说明
----------------------------|---------------------------------|------------
CDS 联系人 V2             | 联系人                        | 此模板同步客户和供应商的所有第一、第二和第三联系信息。
客户组             | msdyn_customergroups            | 此模板同步客户组信息。
客户付款方式     | msdyn_customerpaymentmethods    | 此模板同步客户付款方式信息。
客户 V3                | 帐户                        | 此模板同步商业客户和组织客户的客户主信息。
客户 V3                | 联系人                        | 此模板同步消费者和最终用户的客户主数据。
名称词缀                | msdyn_nameaffixes               | 此模板同步客户和供应商的名称词缀引用数据。
付款日行 CDS V2    | msdyn_paymentdaylines           | 此模板同步客户和供应商的付款日行引用数据。
付款日 CDS            | msdyn_paymentdays               | 此模板同步客户和供应商的付款日引用数据。
付款计划行      | msdyn_paymentschedulelines      | 同步客户和供应商的付款计划行引用数据。
付款计划            | msdyn_paymentschedules          | 此模板同步客户和供应商的付款计划引用数据。
付款期限            | msdyn_paymentterms              | 此模板同步客户和供应商的付款期限引用数据。

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]