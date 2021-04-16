---
title: 将 Supply Chain Management 的产品直接同步到 Sales
description: 此主题介绍用于将产品从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Sales 的模板和基础任务。
author: ChristianRytt
ms.date: 06/10/2019
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
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817813"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>将 Supply Chain Management 的产品直接同步到 Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。

此主题介绍用于将产品直接从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Sales 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用有关 Supply Chain Management 与 Sales 之间的客户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [Power Apps 管理员中心](https://admin.powerapps.com/dataintegration)。 选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。

以下模板和基础任务用于将产品从 Supply Chain Management 同步到 Sales。

- **数据集成中模板的名称：** 产品（Supply Chain Management 到 Sales）- 直接
- **数据集成项目中的任务名称：** 产品

不需要同步任务即可进行产品同步。

## <a name="entity-set"></a>实体集

| 供应链管理    | 销售额    |
|----------------------------|----------|
| 适售的已发布产品 | 产品 |

## <a name="entity-flow"></a>实体流

产品在 Supply Chain Management 中托管，并同步到 Sales。 Supply Chain Management 中的 **适售的已发布产品** 数据实体只导出 *适售* 的产品。 适售产品是具有为用于销售订单而需要具备的信息的产品。 相同的规则适用于使用 **已发布产品** 页上的 **验证** 功能对产品进行验证时。

产品编号用作密钥。 因此，在产品变型同步到 Sales 时，每个产品变型都具有单独的产品 ID。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

在 Sales 中，新 **外部维护** 字段已添加到产品以指示特定产品在外部维护。 默认情况下，该值在导入到 Sales 期间设置为 **是**。 提供以下值：

- **是** – 产品来自 Supply Chain Management，且不可在 Sales 中编辑。
- **否** – 产品直接在 Sales 中输入。
- **(空)** – 在启用“从目标客户到现金”解决方案前，产品存在于 Sales 中。

**外部维护** 字段帮助确保仅具有外部维护的产品的报价单和销售订单将同步到 Supply Chain Management。

外部维护的产品自动添加到具有相同币种的第一个有效的价目表。 价目表按名称的字母顺序排列。 来自 Supply Chain Management 的产品销售价格用作价目表价格。 因此，在 Sales 中必须为 Supply Chain Management 中的每个产品销售币种存在一个价目表。 已发布的适售产品上的币种设置为从中导出产品的法人的记帐币种。

> [!NOTE]
> - 产品同步不会成功，除非存在具有匹配币种的价目表。
> - 您可以通过在数据集成项目中映射 pricelevelid.name [Default Price List (Name)]，使用集成控制所用价目表。 输入必须全部为小写字母。 例如，Sales 中名称为“Standard”的价目表的默认值为：目标字段：pricelevelid.name [Default Price List (Name)]，映射类型：[ { "transformType": "Default", "defaultValue": "standard" } ]。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

- 在首次运行同步前，必须在 Supply Chain Management 中为现有产品填充独特产品表。 完成该作业前，现有产品不会同步。

    1. 在 Supply Chain Management 中，使用“搜索”搜索 **填充独特产品表**。
    2. 选择 **填充独特产品表** 以运行作业。 此作业必须只运行一次。

- 确保在 **SalesUnitSymbol** 到 **DefaultUnit（名称）** 的映射中存在 Supply Chain Management 与 Sales 之间所需的销售度量单位 (UOM) 的值映射。
- 更新 **单位组** (**defaultuomscheduleid.name**) 的值映射以便与 Sales 中的 **单位组** 匹配。

    默认模板值是 **默认单位**。

- 确保来自 Supply Chain Management 的所有产品销售 UOM 均在 Sales 中存在。
- 确保 Supply Chain Management 中的每个产品销售币种在 Sales 中存在价目表。
- 在 Sales 中创建产品时，它们可能具有 **草稿** 或 **活动** 状态。 行为在 Sales 的 **设置** > **管理** > **系统设置** > **Sales** 中进行控制。

    具有 **草稿** 状态的产品在创建后必须激活，才能被添加到报价单或销售订单。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Supply Chain Management 的字段信息。

![数据集成器中的模板映射](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>相关主题

[现金的目标客户](prospect-to-cash.md)

[将 Sales 的客户直接同步到 Supply Chain Management 中的客户](accounts-template-mapping-direct.md)

[将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户](contacts-template-mapping-direct.md)

[直接在 Sales 和 Supply Chain Management 之间同步销售订单](sales-order-template-mapping-direct-two-ways.md)

[将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]