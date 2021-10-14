---
title: 直接在 Sales 和 Supply Chain Management 之间同步销售订单
description: 本主题讨论用于在 Dynamics 365 Sales 与 Dynamics 365 Supply Chain Management 之间直接运行销售订单同步的模板和基础任务。
author: Henrikan
ms.date: 05/09/2019
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
ms.openlocfilehash: ad23190433b2843ec5063b5fa5b30351fcd86390
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566423"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>直接在 Sales 和 Supply Chain Management 之间同步销售订单

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题讨论用于在 Dynamics 365 Sales 与 Dynamics 365 Supply Chain Management 之间直接运行销售订单同步的模板和基础任务。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Supply Chain Management 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用 Supply Chain Management 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Supply Chain Management 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流。](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，打开 [Power Apps 管理员中心](https://preview.admin.powerapps.com/dataintegration)。 选择 **项目**，然后在右上角，选择 **新项目** 以选择公共模板。

以下模板和基础任务用于在 Sales 与 Supply Chain Management 之间直接运行销售订单的同步。

- **数据集成中的模板名称：** 

    - 销售订单（Sales 到 Supply Chain Management）- 直接
    - 销售订单（Supply Chain Management 到 Sales）- 直接

- **数据集成项目中的任务名称：**

    - OrderHeader
    - OrderLine

在发生销售发票标头和行同步前，需要执行以下同步任务：

- 产品（Supply Chain Management 到 Sales）- 直接
- 科目（Sales 到 Supply Chain Management）- 直接（如果使用）
- 从联系人到客户（Sales 到 Supply Chain Management）- 直接（如果使用）

## <a name="entity-set"></a>实体集

| 供应链管理  | 销售额             |
|-------------------------|-------------------|
| Dataverse 销售订单标头 | SalesOrders       |
| Dataverse 销售订单行   | SalesOrderDetails |

## <a name="entity-flow"></a>实体流

在为基于 **销售订单（Sales 到 Supply Chain Management）-直接** 模板的项目触发 **运行项目** 后，销售订单在 Sales 中创建，然后同步到 Supply Chain Management。 只有当所有 **订单产品** 全部是外部维护产品时，您才能够激活和同步来自 Sales 的销售订单。 因此，可能没有目录外产品。 在订单启用后，销售订单将在用户界面 (UI) 变为只读。 此时，从 Supply Chain Management 进行更新。 在销售订单具有状态 **已确认** 后，基于 **销售订单（Supply Chain Management 到 Sales）- 直接** 模板的项目可用于将 Supply Chain Management 的更新或履行状态全部同步到 Sales。

您不必在 Sales 中创建订单。 而可以在 Supply Chain Management 中创建新销售订单。 在销售订单具有状态 **已确认** 后，其将被同步到 Sales，如前面段落中所述。

在 Supply Chain Management 中，模板中的筛选器帮助确保同步中只包括相关销售订单：

- 在销售订单上，订购客户和开票客户都必须来自 Sales 以被包括在同步中。 在 Supply Chain Management 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 列用于筛选来自数据表的销售订单。
- 必须确认 Supply Chain Management 中的销售订单。 仅已确认的销售订单或具有更高处理状态（如 **已装运** 或 **已开票**）的销售订单同步到 Sales。
- 在创建或修改销售订单后，必须运行 Supply Chain Management 中的 **计算销售额总计** 批处理作业。 仅计算了销售总额的销售订单将被同步到 Sales。

## <a name="freight-tax"></a>货运税

因为税存储在行级别，因此 Sales 不在订单头级别支持税务信息。 为了在 Supply Chain Management 的订单头级别支持税务信息（如货运税），系统会将税作为名为 **货运税** 以及具有来自 Supply Chain Management 的税额的目录外产品同步到 Sales。 这样，即使在 Supply Chain Management 的订单头级别有税时，Sales 中的标准价格计算也可用于总金额。

## <a name="discount-calculation-and-rounding"></a>折扣计算和化整

Sales 中的折扣计算模型不同于 Supply Chain Management。 在 Supply Chain Management 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。 如果此最终折扣金额除以行中的数量，可能发生化整。 不过，如果化整的每单位折扣金额同步到 Sales，则不考虑此化整。 为了帮助确保 Supply Chain Management 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。 因此，您必须在 Sales 中将 **折扣计算方法** 定义为 **行项**。

在销售订单行从 Sales 同步到 Supply Chain Management 时，将使用完整行折扣金额。 因为 Supply Chain Management 没有能够存储完整折扣金额的字段，此金额除以数量，并存储在 **行折扣** 字段中。 在此除法计算中发生的任何化整都将存储在销售行的 **销售费用** 字段中。

### <a name="example"></a>示例

**从 Sales 同步到 Supply Chain Management**

- **Sales：** 数量 = 3，每行折扣 = 10.00 美元
- **Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = -$0.01 

**从 Supply Chain Management 同步到 Sales**

- **Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = -$0.01
- **Sales：** 数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

新列已添加到 **订单** 表并显示在页面上：

- **外部维护** – 当订单来自 Supply Chain Management 时将此选项设置为 **是**。
- **处理状态** – 此列显示订单在 Supply Chain Management 中的处理状态。 提供以下值：

    - **草稿** – 在 Sales 中创建订单时的初始状态。 在 Sales 中，仅具有此处理状态的订单可编辑。
    - **活动** – 通过使用 **激活** 按钮在 Sales 中激活订单后的状态。
    - **已确认**
    - **装箱单**
    - **已开票**
    - **已领料**
    - **已部分领料**
    - **已部分包装**
    - **已装运**
    - **已部分装运**
    - **已部分开票**
    - **已取消**

**仅具有外部维护的产品** 设置用于在订单激活期间一致地跟踪销售订单是否全部由外部维护的产品构成。 如果销售订单完全由外部维护的产品构成，则产品在 Supply Chain Management 中进行维护。 此设置有助于保障您不会激活并尝试将具有未知产品的销售订单行同步到 Supply Chain Management。

对于外部维护的订单，**销售订单** 页上的 **创建发票**、**取消订单**、**重新计算**、**获取产品** 和 **查找地址** 按钮将隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。 这些订单不可编辑，因为将在激活后同步来自 Supply Chain Management 的销售订单信息。

销售订单状态将保持 **活动** 状态，以帮助确保来自 Supply Chain Management 的更改可以流向 Sales 中的销售订单。 若要控制此行为，在数据集成项目中将默认的 **状态代码 \[Status\]** 值设置为 **活动**。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售订单前，更新系统中的下列设置十分重要。

### <a name="setup-in-sales"></a>Sales 中的设置

- 确保为用户（来自 Sales 连接集）分配到的团队设置了权限。 如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。 如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。

    转到 **设置** &gt; **安全** &gt; **团队**，选择相关团队，选择 **管理角色**，并选择具有所需权限的角色，如 **系统管理员**。

- 为确保 Sales 和 Supply Chain Management 中的折扣计算均正确无误，必须将 **折扣计算方法** 设置为 **行项**。
- 转到 **设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：

    - **使用系统定价计算系统** 选项设置为 **是**。
    - **折扣计算方法** 列设置为 **行项**。

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management 中的设置

- 转到 **销售和市场** &gt; **定期任务** &gt; **计算销售额总计**，将作业设置为作为批处理作业运行。 将 **计算销售订单的总计** 选项设置为 **是**。 此步骤很重要，因为只有计算了销售额总计的销售订单才会同步到 Sales。 应根据销售订单同步的频率调整批处理作业的频率。

如果也使用工作订单集成，则需设置销售来源。 销售订单来源用于分辨 Supply Chain Management 中创建自 Field Service 中的工作订单的销售订单。 如果销售订单的销售订单来源类型为 **工作订单集成**，则销售订单头中将显示 **外部工作订单状态** 字段。 此外，销售订单来源可确保将销售订单从 Supply Chain Management 同步到 Field Service 期间过滤掉创建自 Field Service 中的工作订单的销售订单。

1. 转到 **销售和市场营销** \> **设置** \> **销售订单** \> **销售订单来源**。
2. 选择 **新建** 创建新的销售订单来源。
3. 在 **销售订单来源** 列中，输入销售订单来源的名称，如 **SalesOrder**。
4. 在 **描述** 列中，输入描述，如 **来自 Sales 的销售订单**。
5. 选中 **来源类型分配** 复选框。
6. 将 **销售订单来源类型** 列设置为 **销售订单集成**。
7. 选择 **保存**。

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>销售订单中的设置（Sales 到 Supply Chain Management）- 直接数据集成项目

- 确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。 您可以将值映射中的默认值留空，以避免必须为国家订单键入国家/地区。 将左侧设置为“空白”，将右侧设置为所需的国家或地区。

    模板值是映射了多个国家或地区的值映射，其中“空白”= US。

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>销售订单中的设置（Supply Chain Management 到 Sales）- 直接数据集成项目

#### <a name="salesheader-task"></a>SalesHeader 任务

- 在 Sales 中创建订单需要价目表。 将 **pricelevelid.name \[价目表名称\]** 的值映射按币种更新至 Sales 中使用的价目表。 您可以为单个币种使用默认价目表。 或者，如果您的价目表有多个币种，则可以使用值映射。

    **pricelevelid.name \[价目表名称\]** 的默认模板值是 **美国 CRM 服务（示例）**。

#### <a name="salesline-task"></a>SalesLine 任务

- 确保在 Supply Chain Management 中存在所需的 **SalesUnitSymbol** 值映射。
- 确保所需单位已在 Sales 中定义。

    为 **SalesUnitSymbol** 到 **oumid.name** 定义了具有值映射的模板值。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法** 和 **交货方式** 列不是默认映射的一部分。 若要映射这些列，必须设置特定于在其中同步表的组织中的数据的值映射。

下图显示了数据集成中的模板映射的一个示例。

> [!NOTE]
> 此映射显示将从 Sales 同步到 Supply Chain Management 或从 Supply Chain Management 同步到 Sales 的列信息。

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>销售订单（Supply Chain Management 到 Sales）- 直接：OrderHeader

[![数据集成中的模板映射，销售订单（Supply Chain Management 到 Sales）- 直接：OrderHeader。](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>销售订单（Supply Chain Management 到 Sales）- 直接：OrderLine

[![数据集成中的模板映射，销售订单（Supply Chain Management 到 Sales）- 直接：OrderLine。](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>销售订单（Sales 到 Supply Chain Management）- 直接：OrderHeader

[![数据集成中的模板映射，销售订单（Sales 到 Supply Chain Management）- 直接：OrderHeader。](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>销售订单（Sales 到 Supply Chain Management）- 直接：OrderLine

[![数据集成中的模板映射，销售订单（Sales 到 Supply Chain Management）- 直接：OrderLine。](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>相关主题

[目标客户到现金](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]