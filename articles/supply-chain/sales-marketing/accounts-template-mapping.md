---
title: "将来自 Sales 的帐户同步到 Finance and Operations 中的客户"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的帐户同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的模板和基础任务。"
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>将来自 Sales 的帐户同步到 Finance and Operations 中的客户

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。 

本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的帐户同步到 Microsoft Dynamics 365 for Finance and Operations 版本 (Finance and Operations) 的模板和基础任务。

## <a name="template-and-task"></a>模板和任务

以下模板和基础任务用于将来自 Sales 的帐户同步到 Finance and Operations：

- **模板名称：**帐户（从 Sales 到 Fin and Ops）
- **项目中的任务名称：**帐户 - 帐户 - 客户

在帐户/客户同步之前所需的同步任务：无

## <a name="entity-set"></a>实体集

| 销售    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| 帐户 | 科目 | 客户              |

## <a name="entity-flow"></a>实体流

帐户在 Sales 中进行托管并作为客户同步到 Finance and Operations。 这些客户的**外部维护**属性设置为**是**以跟踪源自 Sales 的客户。 在开票期间，此信息用于筛选将同步到 Sales 的发票。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

**帐号**字段在**帐户**页提供。 它由一个自然和唯一参数组成以支持集成。 客户关系管理 (CRM) 解决方案的自然键特征可能影响已经使用**帐号**字段，但各帐户不使用唯一**帐号**的客户。 目前，集成解决方案不支持此案例。

当创建新帐户时，如果**帐号**值不存在，则使用编号规则自动生成。 该值由 **ACC** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**ACC-01000-BVRCPS**

当对 Sales 应用集成解决方案时，升级脚本为 Sales 中的现有帐户设置**帐号**字段。 如果没有**帐号**值，可以使用之前描述的编号规则。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

- 来自 **CDS &gt; 目标**的 **CustomerGroupId** 映射在 Finance and Operations 中必须更新到一个有效值。 你可以指定一个默认值，或者使用值映射设置该值。 默认模板值为 **10**。
- **地址国家/地区代码** 在 Finance and Operations 中必填。 若要避免同步错误，您可以在来自 **CDS &gt; 目标**的映射中指定默认值。 如果该字段在 Sales 中为空，则使用该默认值。

    - **AddressCountryRegionISOCode** 的默认模板值是 **USA**。
    - **DeliveryAddressCountryRegionISOCode** 的默认模板值是 **USA**。

- 添加来自 **CDS &gt; 目标**的以下映射有助于减少在 Finance and Operations 中所需的手动更新的次数。 你可以使用默认值或来自**国家/地区**或**城市**等的值映射。

    - **SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。 默认站点可以从产品或从订单头的客户提取。 **SiteId** 的默认模板值是 **1**。
    - **WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。 默认仓库可以在 Finance and Operations 中从产品或从订单头的客户提取。 **WarehouseId** 的默认模板值是 **13**。
    - **LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。 默认情况下，使用来自客户的订单头的语言。 **LanguageId** 的默认模板值是 **en-us**。

- 在**源 &gt; CDS** 映射中更新 CDS 组织 ID (**Organization_OrganizationId**)。 默认模板值为 **ORG001**。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。 若要映射这些字段，则必须设置值映射。 值映射特定于实体在其中进行同步的组织中的数据。

下图显示了数据集成器中的模板映射的一个示例。

![数据集成器中的模板映射](./media/accounts-template-mapping-data-integrator-1.png)

![数据集成器中的帐户的模板映射](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>相关主题

[将来自 Finance and Operations 的产品同步到 Sales 中的产品](products-template-mapping.md)

[将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户](contacts-template-mapping.md)

[将 Sales 的销售报价单标题和行同步到 Finance and Operations](sales-quotation-template-mapping.md)

[将 Finance and Operations 的销售订单标题和行同步到 Sales](sales-order-template-mapping.md)

[将 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping.md)




