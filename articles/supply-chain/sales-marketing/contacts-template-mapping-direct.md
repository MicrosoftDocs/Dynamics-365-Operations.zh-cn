---
title: 将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户
description: 本主题讨论用于将来自 Dynamics 365 Sales 的联系人（联系人）和联系人（客户）实体同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 57a9c2a860e99855e841f0f4276ba2f92767c2b1
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062507"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户

[!include [banner](../includes/banner.md)]



> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator)。

本主题讨论用于直接将来自 Dynamics 365 Sales 的联系人（联系人）和联系人（客户）表同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流。](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [PowerApps 管理中心](https://preview.admin.powerapps.com/dataintegration)。 选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。

以下模板和基础任务用于将 Sales 中的联系人（联系人）表同步到 Supply Chain Management 中的联系人（客户）表。

- **数据集成中的模板名称**

    - 联系人（Sales 到 Supply Chain Management）- 直接
    - 从联系人到客户（Sales 到 Supply Chain Management）- 直接

- **数据集成项目中的任务名称**

    - 联系人
    - ContactToCustomer

必须先执行以下同步任务才能够进行联系人同步：帐户（从 Sales 到 Supply Chain Management）

## <a name="entity-sets"></a>实体集

| 销售额    | 供应链管理 |
|----------|------------------------|
| 联系人 | Dataverse 联系人           |
| 联系人 | 客户 V2           |

## <a name="entity-flow"></a>实体流

联系人在 Sales 中托管，并同步到 Supply Chain Management。

Sales 中的联系人可以成为 Supply Chain Management 中的联系人或客户。 为了确定在 Sales 中的联系人是否应该作为联系人或客户同步到 Supply Chain Management，系统将在 Sales 中查看联系人的以下属性：

- **同步到 Supply Chain Management 中的客户：** 联系人的 **是可用客户** 设置为 **是**
- **同步到 Supply Chain Management 中的联系人：** 联系人的 **是可用客户** 设置为 **否** 且 **公司**（上级单位/联系人）指向帐户（不是联系人）

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

新的 **是可用客户** 列已添加到联系人。 此列用于区分具有销售活动的联系人和没有销售活动的联系人。 **是可用客户** 仅对具有相关报价单、订单或发票的联系人设置为 **是**。 仅这些联系人作为客户同步到 Supply Chain Management。

新的 **IsCompanyAnAccount** 列已添加到联系人。 此列指示联系人是否已链接到 **客户** 类型的公司（上级单位/联系人）。 此信息用于确定应该作为联系人同步到 Supply Chain Management 的联系人。

新的 **联系人号码** 列已添加到联系人以帮助保证一个用于集成的自然和唯一参数。 在创建新的联系人时，将使用编号规则自动创建 **联系人号码** 值。 该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**CON-01000-BVRCPS**

应用用于 Sales 的集成解决方案后，一个升级脚本使用前面提到的编号规则设置现有联系人的 **联系人号码** 列。 升级脚本还可以对任何具有销售活动的联系人将 **是可用客户** 列设置为 **是**。

## <a name="in-supply-chain-management"></a>在 Supply Chain Management 中

使用 **IsContactPersonExternallyMaintained** 属性标记联系人。 此属性指示特定联系人由外部维护。 在这种情况下，外部维护的联系人在 Sales 中进行维护。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

### <a name="contact-to-customer"></a>从联系人到客户

- **CustomerGroup** 在 Supply Chain Management 中是必需的。 若要帮助避免同步错误，你可以在映射中指定默认值。 如果该列在 Sales 中为空，则使用该默认值。

    默认模板值为 **10**。

- 添加以下映射有助于减少在 Supply Chain Management 中所需的手动更新的次数。 你可以使用默认值或来自 **国家/地区** 或 **城市** 等的值映射。

    - **SiteId** – 还可以对 Supply Chain Management 中的产品定义默认站点。 在 Supply Chain Management 中生成报价单和销售订单必需有站点。

        **SiteId** 模板值未定义。

    - **WarehouseId** – 还可以对 Supply Chain Management 中的产品定义默认仓库。 在 Supply Chain Management 中生成报价单和销售订单必需有仓库。

        **WarehouseId** 模板值未定义。

    - **LanguageId** – 在 Supply Chain Management 中生成报价单和销售订单行所需的语言。
    
        默认模板值为 **en-us**。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Supply Chain Management 的列信息。

### <a name="contact-to-contact-example"></a>联系人到联系人示例

![数据集成器中的联系人到联系人模板映射。](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer-example"></a>联系人到客户示例

![数据集成器中的联系人到客户模板映射。](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>相关主题

[目标客户到现金](prospect-to-cash.md)

[将 Sales 的客户直接同步到 Supply Chain Management 中的客户](accounts-template-mapping-direct.md)

[将 Supply Chain Management 的产品直接同步到 Sales](products-template-mapping-direct.md)

[直接在 Sales 和 Supply Chain Management 之间同步销售订单](sales-order-template-mapping-direct-two-ways.md)

[将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]