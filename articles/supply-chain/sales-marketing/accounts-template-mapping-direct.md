---
title: 将 Sales 的客户直接同步到 Supply Chain Management 中的客户
description: 此主题介绍用于将客户从 Dynamics 365 Sales 同步到 Supply Chain Management 的模板和基础任务。
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1bf0da5ba5274b61758bc0efdc2f2167327966ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831642"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>将 Sales 的客户直接同步到 Supply Chain Management 中的客户

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。

此主题介绍用于将客户直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。  提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [Power Apps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。 选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。

以下模板和基础任务用于将客户从 Sales 同步到 Supply Chain Management：

- **数据集成中的模板名称：** 帐户（Sales 到 Fin and Ops）- 直接
- **项目中的任务名称：** 帐户 - 客户

不需要同步任务即可进行帐户/客户同步。

## <a name="entity-set"></a>实体集

| 销售额    | 供应链管理 |
|----------|------------------------|
| 科目 | 客户 V2           |

## <a name="entity-flow"></a>实体流

客户在 Sales 中托管，并作为客户同步到 Supply Chain Management。 这些客户的 **外部维护** 属性设置为 **是** 以跟踪源自 Sales 的客户。 在开票期间，此信息用于筛选将同步到 Sales 的发票。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

**帐号** 列在 **帐户** 页提供。 它由一个自然和唯一参数组成以支持集成。 客户关系管理 (CRM) 解决方案的自然键特征可能影响已经使用 **帐号** 列，但各帐户不使用唯一 **帐号** 值的客户。 目前，集成解决方案不支持此案例。

当创建新帐户时，如果 **帐号** 值不存在，则使用编号规则自动生成。 该值由 **ACC** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**ACC-01000-BVRCPS**

当对 Sales 应用集成解决方案时，升级脚本为 Sales 中的现有帐户设置 **帐号** 列。 如果没有 **帐号** 值，可以使用之前提到的编号规则。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

- **CustomerGroupId** 映射在 Supply Chain Management 中必须更新到一个有效值。 你可以指定一个默认值，或者使用值映射设置该值。

    默认模板值为 **10**。

- 添加以下映射有助于减少在 Supply Chain Management 中所需的手动更新的次数。 你可以使用默认值或来自 **国家/地区** 或 **城市** 等的值映射。

    - **SiteId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的站点。 默认站点可以从产品或从订单头的客户提取。

        默认模板值为 **1**。

    - **WarehouseId** - 在 Supply Chain Management 中处理报价单和销售订单行所需的仓库。 默认仓库可以在 Supply Chain Management 中从产品或从订单头的客户提取。

        默认模板值为 **13**。

    - **LanguageId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的语言。 默认情况下，使用来自客户的订单头的语言。

        默认模板值为 **en-us**。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 列不包括在默认映射中。 若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Supply Chain Management 的列信息。

![数据集成中的模板映射](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>相关主题


[现金的目标客户](prospect-to-cash.md)

[将 Sales 的客户直接同步到 Supply Chain Management 中的客户](accounts-template-mapping-direct.md)

[将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户](contacts-template-mapping-direct.md)

[直接在 Sales 和 Supply Chain Management 之间同步销售订单](sales-order-template-mapping-direct-two-ways.md)

[将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]