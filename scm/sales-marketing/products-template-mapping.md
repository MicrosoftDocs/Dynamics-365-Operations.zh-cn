---
title: "将来自 Finance and Operations 的产品同步到 Sales 中的产品"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的产品同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>将来自 Finance and Operations 的产品同步到 Sales 中的产品

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 在可以使用“从目标客户到现金”解决方案之前，请先熟悉 [Dynamics 365 数据集成](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration)。 

本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本的产品同步到 Microsoft Dynamics 365 for Sales 的模板和基础任务。

## <a name="template-and-task"></a>模板和任务

以下模板和基础任务用于将来自 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本(Finance and Operations) 的产品同步到 Microsoft Dynamics 365 for Sales (Sales)。

-   模板名称：产品（从 Fin and Ops 到 Sales）

-   项目中的任务名称：产品

在产品同步之前所需的同步任务：无

## <a name="entity-set"></a>实体集

| **Finance and Operations** | **CDS** | **销售**  |
|----------------------------|---------|------------|
| 适售的已发布产品 | 产品 | 产品   |

## <a name="entity-flow"></a>实体流

产品在 Finance and Operations 中进行托管并同步到 Sales。 Finance and Operations 中的数据实体**适售的已发布产品**仅导出适售的产品，意味着产品具有需要在销售订单上使用的信息。 相同的规则适用于使用**已发布产品**页上的**验证**功能对产品进行验证时。

**产品编号**用作参数，这意味着产品变型按照每个**产品变型**一个**产品 ID** 同步到 CDS 和 Sales。

## <a name="prospect-to-cash-solution-for-sales"></a>用于 Sales 的“从目标客户到现金”解决方案

在 Sales 中，在产品**外部维护**上添加一个新字段以指示特定产品在外部维护。 该值在导入到 Sales 期间默认设置为**是**。

-   **外部维护 = 是**：产品源自 Finance and Operations，在 Sales 中不可编辑。

-   **外部维护 = 否**：直接在 Sales 中输入产品。

-   **外部维护 = 空白**：在启用从目标客户到现金解决方案前在 Sales 中存在产品。

**外部维护**信息用于确保仅具有**外部维护的产品**的**报价**和**销售订单**将同步到 Finance and Operations。

**外部维护的产品**自动添加到具有相同币种的第一个有效的**价目表**。 请注意，该列表按**名称**的字母顺序排列。 来自 Finance and Operations 的产品销售价格用作**价目表**价格。 这意味着要求对于 Finance and Operations 中的每一个**产品销售币种**，在 Sales 中都有一份**价目表**。 已发布的适售产品上的币种设置为从中导出产品的法人的记帐币种。

> [!NOTE]
> 如果没有匹配币种的**价目表**，产品同步不会成功。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

-   在首次运行同步前，必须在 Finance and Operations 中为现有产品填充**独特产品表**。 完成该作业前，现有产品不会同步。

    -   在 Finance and Operations 中，使用“搜索”搜索**填充独特产品表**。

    -   单击**填充独特产品表**以运行作业。 该作业仅需要运行一次。

-   确保在 Finance and Operations 中销售**度量单位** (UOM) 所需的 **ValueMap** 在**源 -\> CDS 映射 SalesUnitSymbol / DefaultSellingUnitOfMeasure** 中存在。

-   确保用于 UOM 的**支持小数**与你在 **CDS -\> 目标**中的需求相匹配。 如果你需要对每个度量单位设置不同的值，可以使用来自单位的 **ValueMap** 完成此操作，例如 [件 : 0] & [磅 : 2]。

    -   模板值默认为 0。

-   在**源 -\> CDS** 中更新 **CDS 组织 ID Organization_OrganizationId**。

    -   模板值默认为 ORG001。

-   在 **CDS -\> 目标**中更新**单位组** (**defaultuomscheduleid.name**) 的 **ValueMap** 以匹配 Sales 中的**单位组**。

    -   模板值默认为**默认单位**。

-   确保来自 Finance and Operations 的所有产品销售 UOM 在 Sales 中存在 **CDS 选择列表**值。

-   确保 Finance and Operations 中的每个产品销售币种在 Sales 中存在**价目表**。

-   可以在 Sales 中使用状态**草稿**或**活动**创建产品。 这在 Sales 的**销售**下的**系统设置**中进行控制。

    -   使用草稿状态创建的产品需要激活后才能添加到**报价**或**销售订单**。

## <a name="template-mapping-in-data-integrator"></a>数据集成器中的模板映射

下图显示了数据集成器中的模板映射的一个示例。

![数据集成器中的模板映射](./media/products-template-mapping-data-integrator-1.png)

![数据集成器中的产品的模板映射](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>相关主题

[将来自 Sales 的帐户同步到 Finance and Operations 中的客户](accounts-template-mapping.md)

[将来自 Sales 的联系人同步到 Finance and Operations 中的联系人或客户](contacts-template-mapping.md)

[将来自 Sales 的销售报价单标头和行同步到 Finance and Operations](sales-quotation-template-mapping.md)


