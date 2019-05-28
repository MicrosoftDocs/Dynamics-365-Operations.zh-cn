---
title: 将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户
description: 本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的联系人（联系人）和联系人（客户）实体同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 5363c64cd1a475f0047c079d9166718ddc765f02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562346"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>将 Sales 的联系人直接同步到 Finance and Operations 的联系人或客户

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。

本主题讨论用于直接将来自 Microsoft Dynamics 365 for Sales 的联系人（联系人）和联系人（客户）实体同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Finance and Operations 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。 选择**项目**，然后在右上角，选择**新项目**以选择公共模板。

以下模板和基础任务用于将 Sales 中的联系人（联系人）实体同步到 Finance and Operations 中的联系人（客户）实体：

- **数据集成中的模板名称：**

    - 联系人（从 Sales 到 Fin and Ops）- 直接
    - 从联系人到客户（从 Sales 到 Fin and Ops）- 直接

- **数据集成项目中的任务名称：**

    - 联系人
    - ContactToCustomer

必须先执行以下同步任务才能够进行联系人同步：帐户（从 Sales 到 Fin and Ops）

## <a name="entity-sets"></a>实体集

| 销售    | Finance and Operations |
|----------|------------------------|
| 联系人 | CDS 联系人           |
| 联系人 | 客户 V2           |

## <a name="entity-flow"></a>实体流

联系人在 Sales 中进行托管并同步到 Finance and Operations。

Sales 中的联系人可以成为 Finance and Operations 中的联系人或客户。 为了确定在 Sales 中的联系人是否应该作为联系人或客户同步到 Finance and Operations，系统将在 Sales 中查看联系人的以下属性：

- **同步到 Finance and Operations 中的客户：** 联系人的**是可用客户**设置为**是**
- **同步到 Finance and Operations 中的联系人：** 联系人的**是可用客户**设置为**否**且**公司**（上级单位/联系人）指向帐户（不是联系人）

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

新的**是可用客户**字段已添加到联系人。 此字段用于区分具有销售活动的联系人和没有销售活动的联系人。 **是可用客户**仅对具有相关报价单、订单或发票的联系人设置为**是**。 仅这些联系人作为客户同步到 Finance and Operations。

新的 **IsCompanyAnAccount** 字段已添加到联系人。 此字段指示联系人是否已链接到**帐户**类型的公司（上级单位/联系人）。 此信息用于确定应该作为联系人同步到 Finance and Operations 的联系人。

新的**联系人号码**字段已添加到联系人以帮助保证一个用于集成的自然和唯一参数。 在创建新的联系人时，将使用编号规则自动创建**联系人号码**值。 该值由 **CON** 以及依次紧跟在后面的一个增加的编号规则和一个由六个字符组成的后缀构成。 示例：**CON-01000-BVRCPS**

应用用于 Sales 的集成解决方案后，一个升级脚本使用前面提到的编号规则设置现有联系人的**联系人号码**字段。 升级脚本还可以对任何具有销售活动的联系人将**是可用客户**字段设置为**是**。

## <a name="in-finance-and-operations"></a>在 Finance and Operations 中

使用 **IsContactPersonExternallyMaintained** 属性标记联系人。 此属性指示特定联系人由外部维护。 在这种情况下，外部维护的联系人在 Sales 中进行维护。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

### <a name="contact-to-customer"></a>从联系人到客户

- **CustomerGroup** 在 Finance and Operations 中必填。 若要帮助避免同步错误，你可以在映射中指定默认值。 如果该字段在 Sales 中为空，则使用该默认值。

    默认模板值为 **10**。

- 添加以下映射有助于减少在 Finance and Operations 中所需的手动更新的次数。 你可以使用默认值或来自**国家/地区**或**城市**等的值映射。

    - **SiteId** – 还可以对 Finance and Operations 中的产品定义默认站点。 在 Finance and Operations 中生成报价单和销售订单所需的站点。

        **SiteId** 模板值未定义。

    - **WarehouseId** – 还可以对 Finance and Operations 中的产品定义默认仓库。 在 Finance and Operations 中生成报价单和销售订单所需的仓库。

        **WarehouseId** 模板值未定义。

    - **LanguageId** - 在 Finance and Operations 中生成报价单和销售订单所需的语言。
    
        默认模板值为 **en-us**。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。

### <a name="contact-to-contact"></a>从联系人到联系人

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>从联系人到客户

![数据集成器中的模板映射](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>相关主题

[从目标客户到现金](prospect-to-cash.md)

[将直接来自 Sales 的客户同步到 Finance and Operations](accounts-template-mapping-direct.md)

[将直接来自 Finance and Operations 的产品同步到 Sales](products-template-mapping-direct.md)

[将直接来自 Finance and Operations 的销售订单标题和行同步到 Sales](sales-order-template-mapping-direct-two-ways.md)

[将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping-direct.md)


