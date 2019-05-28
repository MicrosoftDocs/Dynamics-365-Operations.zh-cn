---
title: 将 Sales 的销售报价单标题和行直接同步到 Finance and Operations
description: 本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标题和行直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。
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
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572573"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>将 Sales 的销售报价单标题和行直接同步到 Finance and Operations

[!include [banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标题和行直接同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，您应该熟悉[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。

## <a name="data-flow-in-prospect-to-cash"></a>“从目标客户到现金”中的数据流

“从目标客户到现金”使用“数据集成”功能来同步 Finance and Operations 与 Sales 之间的示例的数据。 提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 下图显示 Finance and Operations 与 Sales 之间的数据如何同步。

[![“从目标客户到现金”中的数据流](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>模板和任务

以下模板和基础任务用于将来自 Sales 的销售报价单标头和行直接同步到 Finance and Operations：

- **数据集成中模板的名称：** 销售报价（从 Sales 到 Fin and Ops）- 直接
- **数据集成项目中的任务名称：**

    - QuoteHeader
    - QuoteLine

在发生销售报价单标头和行同步前，需要执行以下同步任务：

- 产品（从 Fin and Ops 到 Sales）- 直接
- 帐户（从 Sales 到 Fin and Ops）- 直接（如果使用）
- 从联系人到客户（从 Sales 到 Fin and Ops）- 直接（如果使用）

## <a name="entity-set"></a>实体集

| 销售        | Finance and Operations     |
|--------------|----------------------------|
| 报价       | CDS 销售报价单标题 |
| QuoteDetails | CDS 销售报价单行  |

## <a name="entity-flow"></a>实体流

销售报价单在 Sales 中创建并同步到 Finance and Operations。

仅当满足以下条件时，来自 Sales 的销售报价单同步：

- 销售报价单上的所有报价产品在外部维护。
- 在您单击**激活报价**后，销售报价单是活动的。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

**仅具有外部维护的产品**字段已添加到**报价**实体以一致地跟踪销售报价单是否全部由外部维护的产品构成。 如果销售报价单只具有外部维护的产品，则产品在 Finance and Operations 中进行维护。 此行为有助于保障你不会尝试将具有未知产品的销售报价单行同步到 Finance and Operations。

销售报价单上的所有报价产品均使用来自销售报价单标头的**仅具有外部维护的产品**信息进行更新。 此信息可在 **QuoteDetails** 实体上的**报价仅具有外部维护的产品**字段中找到。

折扣可以添加到报价产品，并且同步到 Finance and Operations。 标题上的**折扣**、**费用**和**税金**字段由 Finance and Operations 中的设置控制。 此设置当前不支持集成映射。 在当前设计中,**价格**、**折扣**、**费用**和**税金**字段在 Finance and Operations 中维护和处理。

在 Sales 中，由于值未同步到 Finance and Operations，因此该解决方案使以下字段只读：

- 销售报价单标题上的只读字段：**折扣 %**、**折扣**和**运费**
- 报价产品的只读字段：**税**

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售报价单前，更新下列设置十分重要。

### <a name="setup-in-sales"></a>Sales 中的设置

- 确保为用户（来自 Sales 中的连接集）分配到的团队设置了权限。 如果正在使用演示数据，用户通常具有管理员访问权限，但团队没有。 如果当您从数据集成运行项目时团队没有管理员访问权限，您将收到错误消息，指示缺少主体团队。

    若要为团队设置权限，转到**设置** &gt; **安全** &gt; **团队**，然后选择相关团队。 选择**管理角色**，然后选择具有所需权限的角色，如**系统管理员**。

- 转到**设置** &gt; **管理** &gt; **系统设置** &gt; **Sales**，确保使用以下设置：

    - **使用系统定价计算系统**选项设置为**是**。
    - **折扣计算方法**字段设置为**行项**。

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="quoteheader"></a>QuoteHeader

- 确保存在 **Shipto\_country** 到 **DeliveryAddressCountryRegionISOCode** 的所需映射。 在值映射中，您可以定义值为空时使用的默认值。 只需让左侧留空，将右侧设置为所需的国家或地区。 这样，您不必为国家订单键入国家或地区。

    模板值是映射了多个国家或地区的值映射，其中的空值为值 **US**。

#### <a name="quoteline"></a>QuoteLine

- 确保所需的 **SalesUnitSymbol** 值映射在 Finance and Operations 中存在。
- 确保所需单位已在 Sales 中定义。

    为 **oumid.name** 到 **SalesUnitSymbol** 定义了具有值映射的模板值。

- 可选：您可以添加以下映射以帮助保障在没有来自客户或产品的默认信息时将销售报价单行导入到 Finance and Operations 中：

    - **SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。 **SiteId** 没有默认模板值。
    - **WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。 **WarehouseId** 没有默认模板值。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

> [!NOTE]
> - **折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。 此设置当前不支持集成映射。 在当前设计中，**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 处理。
> - **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成器中的模板映射的一个示例。

### <a name="quoteheader"></a>QuoteHeader

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![数据集成器中的模板映射](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>相关主题

[从目标客户到现金](prospect-to-cash.md)

