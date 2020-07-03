---
title: 双写入中的目标客户到现金
description: 此主题提供有关双写入中的目标客户到现金的信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b10e5f0fe97e65ad380e85815c56e88a3ce4e303
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443887"
---
# <a name="prospect-to-cash-in-dual-write"></a>双写入中的目标客户到现金

[!include [banner](../../includes/banner.md)]



大多数业务的一个重要目标是将目标客户转换为客户，然后维护与这些客户之间的当前业务关系。 在 Microsoft Dynamics 365 应用中，通过报价或订单处理工作流进行目标客户到现金流程，并核对和确认财务。 将目标客户到现金与双写入集成将创建一个工作流，该工作流采用源自 Dynamics 365 Sales 或 Dynamics 365 Supply Chain Management 的报价单和订单，并使该报价单和订单在这两个应用中可用。

在这些应用界面中，可以实时访问处理状态和发票信息。 因此，可以在 Supply Chain Management 中更轻松地管理产品库存、库存处理和履行等功能，不必重新创建报价单和订单。

![目标客户到现金中的双写入数据流](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

必须先更新以下设置，然后才能同步销售报价单。

### <a name="setup-in-sales"></a>Sales 中的设置

在 Sales 中，转到**设置 \> 管理 \> 系统设置 \> Sales**，确保使用以下设置：

- **使用系统定价计算**系统选项设置为**是**。
- **折扣计算方法**字段设置为**行项**。

### <a name="sites-and-warehouses"></a>站点和仓库

在 Supply Chain Management 中，**站点**和**仓库**字段是报价单行和订单行的必填字段。 如果设置默认订单设置中的站点和仓库，向报价单行或订单行添加产品时，将自动设置这些字段。 

### <a name="number-sequences-for-quotations-and-orders"></a>报价单和订单的编号规则

在 Sales 和 Supply Chain Management 中创建和同步报价单和订单时，不会连接 Supply Chain Management 和 Sales 的编号规则。 如果 Sales 中创建的销售订单同步到 Supply Chain Management，则其在, Supply Chain Management 中具有相同的销售订单编号。 若要帮助确保销售订单编号不重复，必须在这两个应用中使用不同编号规则系统。

例如，Supply Chain Management 中的编号规则为 **1, 2, 3, 4, 5, ...**，而 Sales 中的编号规则为 **100, 99, 98, ...**。如果在 Sales 中创建 100 个销售订单，则最终生成的一个订单编号已经在 Supply Chain Management 中存在。 换句话说，因为在 Supply Chain Management 和 Sales 中创建销售订单，所以这两个编号规则最终将重合。 不过，可以在 Supply Chain Management 中使用 **F1, F2, F3, ...** 这样的编号规则，在 Sales 中则使用 **C1, C2, C3, ...** 这样的编号规则。 这些编号规则始终不会生成重复的销售订单编号。

## <a name="sales-quotations"></a>销售报价单

销售报价单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。 如果在 Sales 中创建报价单，其将实时同步到 Supply Chain Management。 同样，如果在 Supply Chain Management 中创建报价单，其将实时同步到 Sales。 请注意以下点：

+ 可以向报价单中的产品添加折扣。 在此情况下，折扣将同步到 Supply Chain Management。 标题上的**折扣**、**费用**和**税金**字段由 Supply Chain Management 中的设置控制。 此设置不支持集成映射。 **价格**、**折扣**、**费用**和**税金**字段在 Supply Chain Management 中维护和处理。
+ 销售报价单标题上的**折扣 %**、**折扣**和**运费**字段为只读字段。
+ **货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

如果您还使用 Field Service 解决方案，请确保重新启用**询价行快速创建**参数。 重新启用此参数可使您继续使用快速创建功能创建询价行。
1. 导航到您的 Dynamics 365 Sales 应用程序。
2. 选择顶部导航栏中的设置图标。
3. 选择**高级设置**。
4. 选择**自定义系统**选项。
5. 选择**询价行**菜单项。
6. 转到**数据服务**部分，然后选择**允许快速创建**复选框。

## <a name="sales-orders"></a>销售订单

销售订单既可以在 Sales 中创建，也可以在 Supply Chain Management 中创建。 如果在 Sales 中创建销售订单，其将实时同步到 Supply Chain Management。 同样，如果在 Supply Chain Management 中创建销售订单，其将实时同步到 Sales。 请注意以下点：

+ 仅当订单中的所有产品都来自 Finance and Operations 应用时，才能从 Sales 激活和同步订单。 因此，可能没有目录外产品。
+ 折扣计算和化整：

    - Sales 中的折扣计算模型不同于 Supply Chain Management。 在 Supply Chain Management 中，销售行的最终折扣金额可以是折扣金额和折扣百分比组合的结果。 如果此最终折扣金额除以行中的数量，可能发生化整。 不过，如果化整的每单位折扣金额同步到 Sales，则不考虑此化整。 为了帮助确保 Supply Chain Management 中销售行的完整折扣金额正确同步到 Sales，全部金额都必须同步，而无需再除以行中的数量。 因此，您必须在 Sales 中将折扣计算方法定义为**行项**。
    - 在销售订单行从 Sales 同步到 Supply Chain Management 时，将使用完整行折扣金额。 因为 Supply Chain Management 没有能够存储完整折扣金额的字段，此金额除以数量，并存储在**行折扣**字段中。 在此除法计算期间发生的任何舍入都将存储在销售行的**销售费用**字段中。

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>示例：从 Sales 同步到 Supply Chain Management

您有以下销售订单：

+ **Sales：** 数量 = 3，每行折扣 = 10.00 美元
+ **Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01

如果从 Supply Chain Management 同步到 Sales，则结果如下：

+ **Supply Chain Management：** 数量 = 3，行折扣金额 = $3.33，销售费用 = –$0.01
+ **Sales：** 数量 = 3，每行折扣 = (3 × $3.33) + $0.01 = $10.00

## <a name="dual-write-solution-for-sales"></a>适用于 Sales 的双写入解决方案

新字段已添加到**订单**实体并显示在以下页面。 这些字段中的大多数都在 Sales 中的**集成**选项卡内显示。 有一些特殊字段：

+ **处理状态**字段显示订单在 Supply Chain Management 中的处理状态。 此字段已锁定，并且仅显示来自 Supply Chain Management 的订单的状态。 提供以下值：

    + **活动** – 通过使用**激活**按钮在 Sales 中激活订单后的状态。
    + **已确认**
    + **已交货**
    + **已开票**
    + **已部分交货**
    + **已部分开票**
    + **已领料**
    + **已取消**

    下表显示如何将处理状态映射到 **CRM 状态代码**值。

    | 处理状态           | CRM 状态代码    |
    |-----------------------------|--------------------|
    | 活动                      | 新/待定/暂停 |
    | 已确认/已取货            | 在进行中        |
    | 已部分交货         | 部分            |
    | 已交货                   | 已完成           |
    | 已开票/已部分开票 | 已开票           |
    | 已取消                    | 无钱           |

+ **销售订单**页中的**创建发票**和**取消订单**按钮在 Sales 中已隐藏。
+ **销售订单状态**值将保持**活动**状态，以帮助确保来自 Supply Chain Management 的更改可以流向 Sales 中的销售订单。 若要控制此行为，请将默认的**状态代码 \[Status\]** 值设置为**活动**。

## <a name="invoices"></a>发票

销售发票在 Supply Chain Management 中创建并同步到 Sales。 请注意以下点：

+ **发票编号**字段已添加到**发票**实体中并显示在页面上。
+ **销售订单**页上的**创建发票**按钮被隐藏，因为将在 Supply Chain Management 中创建发票并同步到 Sales。 **发票**页不可编辑，因为发票将从 Supply Chain Management 同步。
+ 当关联的发票从 Supply Chain Management 同步到 Sales 后，**销售订单状态**值自动更改为**已开票**。 而且，创建发票的销售订单的所有者被指定为发票的所有者。 因此，销售订单的所有者可以查看发票。
+ **货运条款**、**交货条款**和**交货方式**字段不包括在默认映射中。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

## <a name="templates"></a>模板

目标客户到现金中包括核心实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| Finance and Operations 应用 | Dynamics 365 中的模型驱动应用 | 说明 |
|-----------------------------|-----------------------------------|-------------|
| 销售发票抬头 V2    | 发票                          |             |
| 销售发票行 V2      | invoicedetails                    |             |
| CDS 销售订单标题     | salesorders                       |             |
| CDS 销售订单行       | salesorderdetails                 |             |
| 销售订单来源代码    | msdyn\_salesorderorigins          |             |
| CDS 销售报价单标题  | 询价                            |             |
| CDS 销售报价单行   | quotedetails                      |             |

下面是目标客户到现金的相关核心实体映射：

+ [客户 V3 到帐户](customer-mapping.md#customers-v3-to-accounts)
+ [CDS 联系人 V2 到联系人](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [客户 V3 到联系人](customer-mapping.md#customers-v3-to-contacts)
+ [发放的产品 V2 到 msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [所有产品到 msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [价目表](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
