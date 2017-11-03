---
title: "将 Finance and Operations 的销售发票标题和行同步到 Sales"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售发票标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>将 Finance and Operations 的销售发票标题和行同步到 Sales

[!include[banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的销售发票标题和行同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。 

## <a name="templates-and-tasks"></a>模板和任务

以下模板和基础任务用于将来自 Finance and Operations 的销售发票标题和行同步到 Sales：

- **数据集成中的模板名称** 

     - 销售发票（从 Fin and Ops 到 Sales）

- **数据集成项目中的任务名称**

    - SalesInvoiceHeader
    - SalesInvoiceLine

在同步销售发票标题和行之前所需的同步任务：
-   产品（从 Fin and Ops 到 Sales）
-   帐户（从 Sales 到 Fin and Ops）（如果使用）
-   联系人（从 Sales 到 Fin and Ops）（如果使用）
-   销售订单标题和行（从 Fin and Ops 到 Sales）

## <a name="entity-set"></a>实体集

| Finance and Operations                               | Common Data Service (CDS)              | 销售          |
|------------------------------------------------------|------------------|----------------|
| 外部维护的客户销售发票抬头 | SalesInvoice     | 发票       |
| 外部维护的客户销售发票行   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>实体流

销售发票在 Finance and Operations 中创建并同步到 Sales。

> [!NOTE]
> 与**销售发票标题**上的费用关联的税金当前不包括在从 Finance and Operations 到 Sales 的同步中。 这是因为 Sales 不支持标题级别的税务信息。 与行级别的费用关联的税金包括在内。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

-  **发票编号字段**添加到**发票**实体中并显示在页面上。
 
-  **销售订单**页上的**创建发票**按钮被隐藏，因为将在 Finance and Operations 中创建发票并同步到 Sales。 **发票**页不可编辑，因为发票将从 Finance and Operations 同步。
 
-  当关联的发票从 Finance and Operations 同步到 Sales 后，**销售订单状态**自动更改为**已开票**。 而且，创建发票的销售订单的所有者被指定为发票的所有者。 这使得销售订单的所有者能够查看发票。
 
## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售发票前，使用下列设置更新系统十分重要：

### <a name="setup-in-sales"></a>Sales 中的设置

- 在**设置** > **管理** > **系统设置** > **Sales** 下，确保**使用系统定价计算系统**设置为**是**。 

- 在**设置** > **管理** > **系统设置** > **Sales** 下，确保**折扣计算方法**设置为**行项**。 

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader 任务

- 为**源** > **CDS** 中的 **CDS 组织 ID** 更新映射。 

    -  **SalesOrder_Organization_OrganizationId** 的默认模板值是 ORG001。
    -  **Account_Organization_OrganizationId** 的默认模板值是 ORG001。
    -  **Organization_OrganizationId** 的默认模板值是 ORG001。

- 确保在**源**  >  **InvoiceCountryRegionId 的 CDS** 中存在到 **BillingAddress_Country** 的所需映射。

    -  模板值是映射多个国家/地区的 **ValueMap**。

- 在 Sales 中创建发票需要**价目表**。 在 **CDS** > **pricelevelid.name [价目表名称] 目标**中将 **ValueMap** 按币种更新至 Sales 中使用的**价目表**。 您可以为单个币种使用默认**价目表**，或者如果您具有多个币种的**价目表**，则使用 **ValueMap**。

    -  **pricelevelid.name [价目表名称]** 的模板值是基于**币种**的 **ValueMap**。
    -  美元：美国 CRM 服务（示例）。 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine 任务

- 确保在**源** > **度量单位的 CDS** 中存在所需的映射。

- 确保 Finance and Operations 中的 **SalesUnitSymbol** 所需的 **ValueMap** 在**源** > **CDS 映射**中存在。 
    
    - 使用 **ValueMap** 为 **SalesUnitSymbol 到数量 UOM** 定义模板值。
    
-  为**源中的 CDS 组织 ID** > **CDS** 更新映射。 

    -  **SalesInvoicer_Organization_OrganizationId** 的默认模板值是 ORG001。
    -  **Product_Organization_OrganizationId** 的默认模板值是 ORG001。
 
## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

> [!NOTE]
> **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**不是默认映射的一部分。 映射这些字段必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成器中的模板映射的一个示例。

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-2.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>相关主题

[将来自 Finance and Operations 的产品同步到 Sales 中的产品](products-template-mapping.md)

[将 Sales 的客户同步到 Finance and Operations](accounts-template-mapping.md)

[将 Sales 的联系人同步到 Finance and Operations 的联系人或客户](contacts-template-mapping.md)

[将 Sales 的销售报价单标题和行同步到 Finance and Operations](sales-quotation-template-mapping.md)

[将 Finance and Operations 的销售订单标题和行同步到 Sales](sales-order-template-mapping.md)


