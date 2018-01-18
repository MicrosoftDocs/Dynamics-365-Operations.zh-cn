---
title: "将来自 Finance and Operations 的销售订单标题和行直接同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>将来自 Finance and Operations 的销售订单标题和行直接同步到 Sales

[!include[banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行直接同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的有关帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Finance and Operations 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [PowerApps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。 选择**项目**，然后在右上角，选择**新项目**以选择公共模板。

以下模板和基础任务用于将来自 Finance and Operations 的销售订单标题和行同步到 Sales：

- **“数据集成”中模板的名称：**销售订单（从 Fin and Ops 到 Sales）- 直接
- **数据集成项目中的任务名称：**

    - OrderHeader
    - OrderLine

在发生销售发票标头和行同步前，需要执行以下同步任务：

- 产品（从 Fin and Ops 到 Sales）- 直接
- 帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）
- 从联系人到客户（从 Sales 到 Fin and Ops）- 直接（如果使用）

## <a name="entity-set"></a>实体集

| Finance and Operations  | 销售             |
|-------------------------|-------------------|
| CDS 销售订单标题 | SalesOrders       |
| CDS 销售订单行   | SalesOrderDetails |

## <a name="entity-flow"></a>实体流

销售订单在 Finance and Operations 中创建并同步到 Sales。

模板中的筛选器帮助确保同步中只包括相关销售订单：

- 在销售订单上，来自 Sales 的订购客户和开票客户都将包括在同步中。 在 Finance and Operations 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 字段都用于跟踪数据实体中的同步。
- 必须确认 Finance and Operations 中的销售订单。 仅已确认的销售订单或具有更高处理状态（如**已装运**或**已开票**）的销售订单同步到 Sales。
- 在创建或修改销售订单后，必须运行 Finance and Operations 中的**计算销售额总计**批处理作业。 仅计算了销售总额的销售订单将被同步到 Sales。

> [!NOTE]
> 目前，与销售订单头上的费用关联的税金不包括在从 Finance and Operations 到 Sales 的同步中。 Sales 不支持标题级别的税务信息。 但是，与行级别的费用相关的税包括在同步中。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

新字段已添加到**订单**实体并显示在以下页面：

- **外部维护** – 当订单来自 Finance and Operations 时将此选项设置为**是**。
- **处理状态** – 此字段显示订单在 Finance and Operations 中的处理状态。 提供以下值：

    - 活动
    - 已确认
    - 装箱单
    - 已开票
    - 已领料
    - 已部分领料
    - 已部分包装
    - 已装运
    - 已部分装运
    - 已部分开票
    - 已取消

**仅具有外部维护的产品**设置在其他销售订单方案（例如，从 Sales 到 Finance and Operation 的同步）中使用，以一致地跟踪销售订单是否全部由外部维护的产品构成。 如果销售订单完全由外部维护的产品构成，则产品在 Finance and Operations 中进行维护。 此设置有助于保障你不会尝试将具有未知产品的销售订单行同步到 Finance and Operations。

对于外部维护的订单，**销售订单**页上的**创建发票**、**取消订单**、**重新计算**、**获取产品**和**查找地址**按钮将隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。 订单页不可编辑，因为将同步来自 Finance and Operations 的销售订单信息。

销售订单的状态将保持为**活动**，以帮助确保来自 Finance and Operations 的更改可以流向 Sales 中的销售订单。 若要控制此行为，在数据集成项目中将默认的**状态代码 \[Status\]** 值设置为**活动**。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售订单前，更新系统中的下列设置十分重要。

### <a name="setup-in-sales"></a>Sales 中的设置

- 确保为用户（来自 Sales 连接集）分配到的团队设置了权限。 如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。 如果当您从数据集成运行项目时团队还没有管理员访问权限，您将收到错误消息，指示缺少主体团队。

    转到**设置** > **安全** > **团队**，选择相关团队，选择**管理角色**，并选择具有所需权限的角色，如**系统管理员**。

- 转到**设置** > **管理** > **系统设置** > **Sales**，确保使用以下设置：

    - **使用系统定价计算系统**选项设置为**是**。
    - **折扣计算方法**字段设置为**行项**。

### <a name="setup-in-finance-and-operations"></a>Finance and Operations 中的设置

转到**销售和市场** > **定期任务** > **计算销售额总计**，设置作业以作为批处理作业运行。 将**计算销售订单的总计**选项设置为**是**。 此步骤很重要，因为只有计算了销售额总计的销售订单才会同步到 Sales。 应根据销售订单同步的频率调整批处理作业的频率。

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="salesheader-task"></a>SalesHeader 任务

- 确保存在所需的 **InvoiceCountryRegionId** 到 **BillingAddress\_Country** 和 **DeliveryCountryRegionId** 到 **DeliveryAddress\_Country** 的映射。

    模板值是多个国家或地区表在其中映射的值映射。

- 在 Sales 中创建订单需要价目表。 将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。 您可以为单个币种使用默认价目表。 或者，如果您的价目表有多个币种，则可以使用值映射。

    **pricelevelid.name \[价目表名称\]** 的默认模板值是**美国 CRM 服务（示例）**。

#### <a name="salesline-task"></a>SalesLine 任务

- 确保存在所需的 **DeliveryCountryRegionId** 到 **DeliveryAddress\_Country** 的映射。

    模板值是多个国家或地区表在其中映射的值映射。

- 确保所需的 **SalesUnitSymbol** 的值映射在 Finance and Operations 中存在。

    为 **SalesUnitSymbol** 到 **Quantity\_UOM** 定义了具有值映射的模板值。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不包括在默认映射中。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成中的模板映射的一个示例。 

> [!NOTE]
> 此映射显示将从 Sales 同步到 Finance and Operations 的字段信息。

### <a name="orderheader"></a>OrderHeader

![数据集成器中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![数据集成器中的模板映射](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>相关主题

[从目标客户到现金](prospect-to-cash.md)

[将直接来自 Sales 的客户同步到 Finance and Operations](accounts-template-mapping-direct.md)

[将直接来自 Finance and Operations 的产品同步到 Sales](products-template-mapping-direct.md)

[将直接来自 Sales 的联系人同步到 Finance and Operations 的联系人或客户](contacts-template-mapping-direct.md)

[将直接来自 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping-direct.md)




