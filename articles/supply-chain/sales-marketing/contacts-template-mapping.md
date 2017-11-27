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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。 

本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的联系人（联系人）实体和联系人（客户）同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的模板和基础任务。

## <a name="templates-and-tasks"></a>模板和任务

以下模板和基础任务用于将 Sales 中的联系人（联系人）同步到 Finance and Operations 中的联系人（客户）：

- **模板的名称：**

    - 联系人（从 Sales 到 Fin and Ops）
    - 从联系人到客户（从 Sales 到 Fin and Ops）

- **项目中的任务名称：**

    - 联系人
    - ContactToCustomer

在联系人同步之前必须执行以下同步任务：帐户（从 Sales 到 Fin and Ops）

## <a name="entity-sets"></a>实体集

| 销售    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| 联系人 | 联系人 | CDS 联系人           |
| 联系人 | 科目 | 客户 V2           |

## <a name="entity-flow"></a>实体流

联系人在 Sales 中进行托管，并同步到 Common Data Service (CDS) 和 Finance and Operations。

Sales 中的联系人可以成为 CDS 和 Finance and Operations 中的联系人。 或者，它可以成为 CDS 中的帐户和 Finance and Operations 中的客户。 若要确定是否应该提取 Sales 中的联系人用于同步到 CDS 和 Finance and Operations（例如，Sales 中的联系人 &gt; CDS 中的联系人 &gt; Finance and Operations 中的联系人），系统会检查 Sales 中的联系人的以下属性：

- **同步到 CDS 中的帐户和 Finance and Operations 中的客户：**联系人的**是可用客户**设置为**是**
- **同步到 CDS 中的联系人和 Finance and Operations 中的联系人：**联系人的**是可用客户**设置为**否**且**公司**（上级单位/联系人）指向帐户（不是联系人）

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案 

新的**是可用客户**字段已添加到联系人。 此字段用于区分具有销售活动的联系人和没有销售活动的联系人。 **是可用客户**仅对具有相关报价单、订单或发票的联系人设置为**是**。 仅这些联系人作为客户同步到 Finance and Operations。

新的 **IsCompanyAnAccount** 字段已添加到联系人。 此字段用于指示联系人是否已链接到**帐户**类型的公司（上级单位/联系人）。 此信息用于确定应该作为联系人同步到 Finance and Operations 的联系人。

新的**联系人号码**字段已添加到联系人以帮助保证一个用于集成的自然和唯一参数。 在创建新的联系人时，将使用编号规则自动创建**联系人号码**值。 该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**CON-01000-BVRCPS**

将用于 Sales 的集成解决方案添加到 Sales 后，一个升级脚本使用前面讨论的编号规则设置现有联系人的**联系人号码**字段。 升级脚本还可以对任何具有销售活动的联系人将**是可用客户**字段设置为**是**。

## <a name="in-finance-and-operations"></a>在 Finance and Operations 中 

使用 **IsContactPersonExternallyMaintained** 属性标记联系人。 此属性指示特定联系人由外部维护。 在这种情况下，外部维护的联系人在 Sales 中进行维护。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

### <a name="contact-to-contact"></a>从联系人到联系人

- 在**源 &gt; CDS** 映射中更新 **CDS 组织 ID**。

    - **Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。
    - **PrimaryAccount_Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。

- **地址国家/地区代码** 在 Finance and Operations 中必填。 若要避免同步错误，你可以在 **CDS &gt; Operations** 映射中指定默认值。 如果该字段在 Sales 中为空，则使用该默认值。 **PrimaryAddressCountryRegionISOCode** 的默认模板值是 **USA**。
- 确保以下字段的值在 Finance and Operations 中存在。 如果此信息在 Finance and Operations 中不需要，你可以从 **CDS &gt; 目标**映射中删除映射。

    - **Finance and Operations 中的字段名称：**决策
    - **映射：**PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>从联系人到客户

- 在**源 &gt; CDS** 映射中更新 **CDS 组织 ID**。 **Organization_OrganizationId [组织 ID]** 的默认模板值是 **ORG001**。
- **地址国家/地区代码** 在 Finance and Operations 中必填。 若要避免同步错误，你可以在 **CDS &gt; 目标**映射中指定默认值。 如果该字段在 Sales 中为空，则使用该默认值。 **PrimaryAddressCountryRegionISOCode** 的默认模板值是 **USA**。
- **CustomerGroup** 在 Finance and Operations 中必填。 若要避免同步错误，你可以在 **CDS &gt; 目标**映射中指定默认值。 如果该字段在 Sales 中为空，则使用该默认值。 **CustomerGroupId** 的默认模板值是 **10**。
- 添加来自 **CDS &gt; 目标**的以下映射有助于减少在 Finance and Operations 中手动更新的次数。 你可以使用默认值或来自**国家/地区**或**城市**等的值映射。

    - **SiteId** - 还可以对 Finance and Operations 中的产品定义默认站点。 在 Finance and Operations 中生成报价单和销售订单所需的站点。 **SiteId** 模板值未定义。
    - **WarehouseId** - 还可以对 Finance and Operations 中的产品定义默认仓库。 在 Finance and Operations 中生成报价单和销售订单所需的仓库。 **WarehouseId** 模板值未定义。
    - **LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。 **LanguageId** 的默认模板值是 **en-us**。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

下图显示了数据集成器中的模板映射的一个示例。

### <a name="contact-to-contact"></a>从联系人到联系人

![数据集成器中的模板映射](./media/contacts-template-mapping-data-integrator-1.png)

![数据集成器中的联系人的模板映射](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>从联系人到客户

![数据集成器中的模板映射](./media/contacts-template-mapping-data-integrator-3.png)

![数据集成器中的联系人的模板映射](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>相关主题

[将来自 Finance and Operations 的产品同步到 Sales 中的产品](products-template-mapping.md)

[将来自 Sales 的帐户同步到 Finance and Operations 中的客户](accounts-template-mapping.md)

[将 Sales 的销售报价单标题和行同步到 Finance and Operations](sales-quotation-template-mapping.md)

[将 Finance and Operations 的销售订单标题和行同步到 Sales](sales-order-template-mapping.md)

[将 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping.md)

