---
title: 将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales
description: 本主题讨论用于将销售发票头和行直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: 94442eb11aac3faf8a412944617686853a12128d
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251653"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>将 Finance and Operations 的销售发票标题和行直接同步到 Sales

[!include [banner](../includes/banner.md)]

本主题讨论用于将销售发票头和行直接从 Dynamics 365 Sales 同步到 Dynamics 365 Supply Chain Management 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [PowerApps 管理中心](https://preview.admin.powerapps.com/dataintegration)。 选择**项目**，然后在右上角，选择**新项目**以选择公共模板。

以下模板和基础任务用于将来自 Finance and Operations 的销售发票标题和行同步到 Sales：

- **数据集成中模板的名称：** 销售发票（Fin and Ops 到 Sales）- 直接
- **数据集成项目中的任务名称：**

    - SalesInvoiceHeader
    - SalesInvoiceLine

在发生销售发票标头和行同步前，需要执行以下同步任务：

- 产品（Supply Chain Management 到 Sales）- 直接
- 科目（Sales 到 Supply Chain Management）- 直接（如果使用）
- 联系人（Sales 到 Supply Chain Management）- 直接（如果使用）
- 销售订单头和行（Supply Chain Management 到 Sales）- 直接

## <a name="entity-set"></a>实体集

| 供应链管理                              | 销售额          |
|------------------------------------------------------|----------------|
| 外部维护的客户销售发票抬头 | 发票       |
| 外部维护的客户销售发票行   | InvoiceDetails |

## <a name="entity-flow"></a>实体流

销售发票在 Supply Chain Management 中创建并同步到 Sales。

> [!NOTE]
> 目前，与销售发票标题上的费用关联的税金不包括在从 Supply Chain Managements 到 Sales 的同步中。 Sales 不支持标题级别的税务信息。 但是，与行级别的费用相关的税包括在同步中。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

- **发票编号**字段已添加到**发票**实体中并显示在页面上。
- **销售订单**页上的**创建发票**按钮被隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。 **发票**页不可编辑，因为发票将从 Supply Chain Management 同步。
- 当关联的发票从 Supply Chain Management 同步到 Sales 后，**销售订单状态**值自动更改为**已开票**。 而且，创建发票的销售订单的所有者被指定为发票的所有者。 因此，销售订单的所有者可以查看发票。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售发票前，在系统中更新以下设置十分重要。

### <a name="setup-in-sales"></a>Sales 中的设置

转到**设置** > **管理** > **系统设置** > **Sales**，确保使用以下设置：

- **使用系统定价计算系统**选项设置为**是**。
- **折扣计算方法**字段设置为**行项**。

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader 任务

- 确保存在所需的 **InvoiceCountryRegionId** 到 **BillingAddress\_Country** 的映射。

    模板值是多个国家或地区表在其中映射的值映射。

- 在 Sales 中创建发票需要价目表。 将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。 您可以为单个币种使用默认价目表。 或者，如果您的价目表有多个币种，则可以使用值映射。

    **pricelevelid.name \[价目表名称\]** 的模板值是基于具有“USD = 美国 CRM 服务（示例）”的币种的值映射。  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine 任务

- 确保存在所需的**度量单位**的映射。
- 确保在 Supply Chain Management 中存在所需的 **SalesUnitSymbol** 值映射。

    为 **SalesUnitSymbol** 到 **Quantity\_UOM** 定义了具有值映射的模板值。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Supply Chain Management 的字段信息。

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![数据集成中的模板映射](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![数据集成中的模板映射](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>相关主题

[现金的目标客户](prospect-to-cash.md)

[将 Sales 的客户直接同步到 Supply Chain Management 中的客户](accounts-template-mapping-direct.md)

[将 Supply Chain Management 的产品直接同步到 Sales](products-template-mapping-direct.md)

[将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户](contacts-template-mapping-direct.md)

[将 Sales 的销售订单头和行直接从 Supply Chain Management 同步到 Sales](sales-order-template-mapping-direct-two-ways.md)
