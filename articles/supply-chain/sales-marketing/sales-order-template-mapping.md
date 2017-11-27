---
title: "将 Finance and Operations 的销售订单标题和行同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>将 Finance and Operations 的销售订单标题和行同步到 Sales

[!include[banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售订单标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。 

## <a name="template-and-tasks"></a>模板和任务

以下模板和基础任务用于将来自 Finance and Operations 的销售订单标题和行同步到 Sales：

- **数据集成中的模板名称** 

    - 销售订单（从 Fin and Ops 到 Sales）
    
- **数据集成项目中的任务名称**

    - OrderHeader
    - OrderLine

在同步销售发票抬头和行之前所需的同步任务：

- 产品（从 Fin and Ops 到 Sales）
- 帐户（从 Sales 到 Fin and Ops）（如果使用）
- 从联系人到客户（从 Sales 到 Fin and Ops）（如果使用）

## <a name="entity-set"></a>实体集

| Finance and Operations |    Common Data Service (CDS)         |     销售      |
|------------------------|----------------|----------------|
| CDS 销售订单标题| SalesOrder     | SalesOrders |
| CDS 销售订单行  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>实体流

销售订单在 Finance and Operations 中创建并同步到 Sales。

模板中的筛选器确保同步中只包括相关销售订单：

- 来自 Sales 的销售订单上的订购和开票客户都将包括在同步中。 在 Finance and Operations 中，**OrderingCustomerIsExternallyMaintained** 和 **InvoiceCustomerIsExternallyMaintained** 字段都用于跟踪数据实体中的同步。

- 必须确认 Finance and Operations 中的**销售订单**。 仅已确认的销售订单或具有更高处理状态（如已装运或已开票状态）的销售订单同步到 Sales。

- 在创建或修改销售订单后，必须在 Finance and Operations 中执行批处理作业**计算销售额总计**。 仅计算了销售额总计的销售订单将被同步到 CDS 和 Sales。

> [!NOTE]
> 与**销售订单标题**上的费用关联的税金当前不包括在从 Finance and Operations 到 Sales 的同步中。 这是因为 Sales 不支持标题级别的税务信息。 与行级别的费用关联的税金包括在内。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

新字段添加到**订单**实体并显示在以下页面：

- **外部维护** - 当订单来自 Finance and Operations 时设置为**是**。

- **处理状态** - 用于显示订单在 Finance and Operations 中的处理状态。 值包括：

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

**仅具有外部维护的产品**设置在其他销售订单方案（从 Sales 到 Finance and Operation 同步）中使用，以一致地跟踪销售订单是否全部由**外部维护的产品**构成，在这种情况下，产品在 Finance and Operations 中进行维护。 这确保您不会尝试将具有未知产品的销售订单行同步到 Finance and Operations。
 
**销售订单**页上的**创建发票**、**取消订单**、**重新计算**、**获取产品**和**查找地址**按钮对外部维护的订单隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。 订单页不可编辑，因为将同步来自 Finance and Operations 的销售订单信息。
 
**销售订单状态**将保持活动状态，以确保来自 Finance and Operations 的更改可以流向 Sales 中的**销售订单**。 对其进行控制的方法是在数据集成项目中将默认的**状态代码 [状态]** 设置为**活动**。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置 

在同步销售订单前，使用下列设置更新系统十分重要：

### <a name="setup-in-sales"></a>Sales 中的设置

- 确保用户（来自 Sales **连接集**）分配到的团队的权限。 如果正在使用演示数据，通常用户具有管理员访问权限，但团队没有。 如果没有，您在运行来自数据集成器的项目时会收到“缺少主体团队”的错误。 

    - 在**设置** > **安全** > **团队**下，选择相关团队，单击**管理角色**并选择具有所需权限的角色，如系统管理员。

- 在**设置** > **管理** > **系统设置** > **Sales** 下，确保**使用系统定价计算系统**设置为**是**。 

- 在**设置** > **管理** > **系统设置** > **Sales** 下，确保**折扣计算方法**设置为**行项**。 

### <a name="setup-in-finance-and-operations"></a>Finance and Operations 中的设置

将**销售和市场营销** > **定期任务** > **计算销售额总计**设置为作为批处理作业运行，并且将**计算销售订单的总计**设置为**是**。 这一点很重要，因为仅计算了销售额总计的销售订单才会被同步到 CDS 和 Sales。 应根据销售订单同步的频率调整批处理作业的频率。

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="salesheader-task"></a>SalesHeader 任务

- 为**源中的 CDS 组织 ID** > **CDS** 更新映射。

    - **Account_Organization_OrganizationId** 的默认模板值是 ORG001。
    - **InvoiceAccount_Organization_OrganizationId** 的默认模板值是 ORG001。
    - **Organization_OrganizationId** 的默认模板值是 ORG001。

- 确保在**源** > **用于从 InvoiceCountryRegionId 到 BillingAddress_Country 的 CDS** 和**从 DeliveryCountryRegionId 到 DeliveryAddress_Country** 的 CDS 中存在所需的映射。

    - 模板值是映射多个国家/地区的 **ValueMap**。

- 在 Sales 中创建订单需要**价目表**。 在 **CDS** > **目标**中将 **pricelevelid.name [价目表名称]** 的 **ValueMap** 按币种更新至 Sales 中使用的**价目表**。 您可以为单个币种使用默认**价目表**，或者如果您具有多个币种的**价目表**，则使用 **ValueMap**。
    
    - **pricelevelid.name [价目表名称]** 的默认模板值是美国 CRM 服务（示例）。 

#### <a name="salesline-task"></a>SalesLine 任务

- 为**源中的 CDS 组织 ID** > **CDS** 更新映射。 
    
    - **SalesOrder_Organization_OrganizationId** 的默认模板值是 ORG001。
    - **Product_Organization_OrganizationId** 的默认模板值是 ORG001。

- 确保在**源** > 从 **DeliveryCountryRegionId** 到 **DeliveryAddress_Country** 的 **CDS** 中存在所需的映射。

    - 模板值是映射多个国家/地区的 **ValueMap**。
    
- 确保 Finance and Operations 中的 **SalesUnitSymbol** 所需的 **ValueMap** 在**源** > **CDS 映射**中存在。

    - 使用 **ValueMap** 为 **SalesUnitSymbol 到数量 UOM** 定义模板值。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成器中的模板映射的一个示例。

### <a name="orderheader"></a>OrderHeader

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>相关主题

[将来自 Finance and Operations 的产品同步到 Sales 中的产品](products-template-mapping.md)

[将 Sales 的客户同步到 Finance and Operations](accounts-template-mapping.md)

[将 Sales 的联系人同步到 Finance and Operations 的联系人或客户](contacts-template-mapping.md)

[将 Sales 的销售报价单标题和行同步到 Finance and Operations](sales-quotation-template-mapping.md)

[将 Finance and Operations 的销售发票标题和行同步到 Sales](sales-invoice-template-mapping.md)


