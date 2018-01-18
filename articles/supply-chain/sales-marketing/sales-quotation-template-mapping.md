---
title: "将来自 Sales 的销售报价单标头和行同步到 Finance and Operations"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Sales 的销售报价单标头和行同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的模板和基础任务。"
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>将来自 Sales 的销售报价单标头和行同步到 Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](/common-data-service/entity-reference/dynamics-365-integration)。 

本主题讨论用于将来自 Microsoft Dynamics 365 for Sales (Sales) 的销售报价单标头和行同步到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的模板和基础任务。 

## <a name="template-and-tasks"></a>模板和任务

以下模板和基础任务用于将来自 Sales 的销售报价单标头和行同步到 Finance and Operations：

- **模板名称：**销售报价（从 Sales 到 Fin and Ops）
- **项目中的任务名称：**

    - QuoteHeader
    - QuoteLine

在发生销售报价单标头和行同步前，需要执行以下同步任务：

- 产品（从 Fin and Ops 到 Sales）
- 帐户（从 Sales 到 Fin and Ops）（如果使用）
- 从联系人到客户（从 Sales 到 Fin and Ops）（如果使用）

## <a name="entity-set"></a>实体集

| 销售        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| 报价       | 报价     | 销售报价单标头   |
| QuoteDetails | QuotationLine | CDS 销售报价单行 |

## <a name="entity-flow"></a>实体流

销售报价单在 Sales 中创建并同步到 Finance and Operations。

仅当满足以下条件时，来自 Sales 的销售报价单同步：

- 销售报价单行上的所有产品在外部维护。
- 销售报价单有效或已激活。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

**仅具有外部维护的产品**字段已添加到报价实体以一致地跟踪销售报价单是否全部由外部维护的产品构成。 如果销售报价单只具有外部维护的产品，则产品在 Finance and Operations 中进行维护。 此行为有助于保障你不会尝试将具有未知产品的销售报价单行同步到 Finance and Operations。

报价单上的所有产品和行使用来自报价单标头的**仅具有外部维护的产品**信息进行更新。 此信息可在报价单行实体上的**报价仅具有外部维护的产品**字段找到。

**折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。 此设置当前不支持集成映射。 在当前设计中,**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 掌握和处理。

在 Sales 中，由于值未同步到 Finance and Operations，因此该解决方案使以下字段只读：

- **销售报价单标头上的只读字段：**折扣 %、折扣和运费
- **销售报价单行上的只读字段：**税金

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步销售订单前，使用下列设置更新系统十分重要：

### <a name="setup-in-sales"></a>Sales 中的设置

- 转到**设置** &gt; **管理** &gt; **系统设置** &gt; **销售**，并确保**折扣计算方法**字段设置为**每单位**。 此设置有助于保障来自 Sales 的行项折扣与 Finance and Operations 中的设置匹配。 否则，折扣在 Finance and Operations 中不正确，因为 Finance and Operations 会将折扣读取为每单位折扣，即使它在 Sales 中是每行折扣。

### <a name="setup-in-finance-and-operations"></a>Finance and Operations 中的设置

- 转至**应收账款** &gt; **设置** &gt; **应收账款参数**。 在**编号规则**选项卡上，选择销售报价单的编号规则，然后单击**查看详细信息**。 然后，在**一般设置**下，将**手动**字段设置为**是**。
- 转至**应收账款** &gt; **设置** &gt; **应收账款参数**。 然后，在**装运**选项卡上，将**交货日期控制**字段设置为**无**。 此设置帮助防止对销售报价单的同步失败。

### <a name="setup-in-the-data-integration-project"></a>数据集成项目中的设置

#### <a name="quoteheader"></a>QuoteHeader

- **请求交货日期**字段在 Finance and Operations 中必填，如果将该字段保留为空，同步将失败。 为了防止出现该问题，如果将该字段保留为空，则从**源 &gt; CDS** 中提取默认日期。 日期应更新到一个首选值。 目前，不能输入一个值（例如**当天**）表示当天的日期。 必须输入特定日期。 **请求交货日期**的默认模板值是 **1/1/2020**。
- **地址国家/地区代码**字段在 Finance and Operations 中必填。 为了帮助防止同步错误，你可以指定当该字段在 Sales 中保留为空时要使用的默认值。 此默认值也有用，因为你无需在本地地址的**国家/地区**字段中手动输入一个值。 **DeliveryAddressCountryRegionISOCode** 没有默认模板值。
- 在**源 &gt; CDS** 中更新 **CDS 组织 ID** 的映射，使其与组织实体中的 **CDS 组织**匹配：

    - **Organization_OrganizationId** 的默认模板值是 **ORG001**。
    - **Account_Organization_OrganizationId** 的默认模板值是 **ORG001**。
    - **InvoiceAccount_OrganizationId** 的默认模板值是 **ORG001**。

#### <a name="quoteline"></a>QuoteLine

- 在**源 &gt; CDS** 中更新 **CDS 组织 ID** 的映射，使其与组织实体中的 **CDS 组织**匹配：

    - **Organization_OrganizationId** 的默认模板值是 **ORG001**。
    - **Product_Organization_Organization_OrganizationId** 的默认模板值是 **ORG001**。
    - **Quotation_Organization_Organization_OrganizationId** 的默认模板值是 **ORG001**。

- **请求交货日期**字段在 Finance and Operations 中必填，如果将该字段保留为空，同步将失败。 为了防止出现该问题，如果将该字段保留为空，则从**源 &gt; CDS** 中提取默认日期。 日期应更新到一个首选值。 目前，不能输入一个值（例如**当天**）表示当天的日期。 必须输入特定日期。 **请求交货日期**的默认模板值是 **1/1/2020**。
- 你可以从 **CDS &gt; 目标**添加以下映射以帮助保障在没有来自客户或产品的默认信息时将报价单行导入到 Finance and Operations 中：

    - **SiteId** - 在 Finance and Operations 中生成报价单和销售订单行所需的站点。 **SiteId** 没有默认模板值。
    - **WarehouseId** - 在 Finance and Operations 中处理报价单和销售订单行所需的仓库。 **WarehouseId** 没有默认模板值。

- 确保在 Finance and Operations 中所需的用于销售度量单位 (UOM) 的值映射在用于从 **Quantity_UOM** 到 **SALESUNITSYMBOL** 的 **CDS &gt; 目标**映射中存在。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

> [!NOTE]
> - **折扣**、**费用**和**税金**字段由 Finance and Operations 中的复杂设置控制。 此设置当前不支持集成映射。 在当前设计中，**价格**、**折扣**、**费用**和**税金**字段由 Finance and Operations 处理。
> - **付款期限**、**货运条款**、**交货条款**、**装运方法**和**交货方式**字段不是默认映射的一部分。 若要映射这些字段，必须设置特定于在其中同步实体的组织中的数据的值映射。

下图显示了数据集成器中的模板映射的一个示例。

### <a name="quoteheader"></a>QuoteHeader

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-1.png)

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-3.png)

![数据集成器中的模板映射](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>相关主题

[将来自 Finance and Operations 的产品同步到 Sales 中的产品](products-template-mapping.md)

[将 Sales 的客户同步到 Finance and Operations](accounts-template-mapping.md)

[将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户](contacts-template-mapping.md)



