---
title: "将 Sales 的客户直接同步到 Finance and Operations"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的帐户同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>将 Sales 的客户直接同步到 Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。

本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的帐户直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。  提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Finance and Operations 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。 选择**项目**，然后在右上角，选择**新项目**以选择公共模板。

以下模板和基础任务用于将 Sales 的帐户同步到 Finance and Operations：

- **“数据集成”中的模板名称：**帐户（Sales 到 Fin and Ops）- 直接
- **项目中的任务名称：**帐户 - 客户

不需要同步任务即可进行帐户/客户同步。

## <a name="entity-set"></a>实体集

| 销售    | Finance and Operations |
|----------|------------------------|
| 帐户 | 客户 V2           |

## <a name="entity-flow"></a>实体流

帐户在 Sales 中进行托管并作为客户同步到 Finance and Operations。 这些客户的**外部维护**属性设置为**是**以跟踪源自 Sales 的客户。 在开票期间，此信息用于筛选将同步到 Sales 的发票。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

**帐号**字段在**帐户**页提供。 它由一个自然和唯一参数组成以支持集成。 客户关系管理 (CRM) 解决方案的自然键特征可能影响已经使用**帐号**字段，但各帐户不使用唯一**帐号**的客户。 目前，集成解决方案不支持此案例。

当创建新帐户时，如果**帐号**值不存在，则使用编号规则自动生成。 该值由 **ACC** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**ACC-01000-BVRCPS**

当对 Sales 应用集成解决方案时，升级脚本为 Sales 中的现有帐户设置**帐号**字段。 如果没有**帐号**值，可以使用之前提到的编号规则。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

- **CustomerGroupId** 映射在 Finance and Operations 中必须更新到一个有效值。 你可以指定一个默认值，或者使用值映射设置该值。

    默认模板值为 **10**。

- 添加以下映射有助于减少在 Finance and Operations 中所需的手动更新的次数。 你可以使用默认值或来自**国家/地区**或**城市**等的值映射。

    - **SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。 默认站点可以从产品或从订单头的客户提取。

        默认模板值为 **1**。

    - **WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。 默认仓库可以在 Finance and Operations 中从产品或从订单头的客户提取。

        默认模板值为 **13**。

    - **LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。 默认情况下，使用来自客户的订单头的语言。

        默认模板值为 **en-us**。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。

![数据集成中的模板映射](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>相关主题


[从目标客户到现金](prospect-to-cash.md)

[将直接来自 Sales 的客户同步到 Finance and Operations](accounts-template-mapping-direct.md)

[将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户](contacts-template-mapping-direct.md)

[将 Finance and Operations 的销售订单标题和行直接同步到 Sales](sales-order-template-mapping-direct-two-ways.md)

[将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping-direct.md)


