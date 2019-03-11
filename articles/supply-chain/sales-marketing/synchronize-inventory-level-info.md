---
title: 将库存级别信息从 Finance and Operations 同步到 Field Service
description: 本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "356775"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>将库存级别信息从 Finance and Operations 同步到 Field Service 

[!include[banner](../includes/banner.md)]

本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于同步 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的库存现有水平。

**数据集成中的模板**
- 产品库存（Finance and Operations 到 Field Service）
  
**数据集成项目中的任务**
- 产品库存

在发生库存水平同步前，需要执行以下同步任务：
- 仓库（Finance and Operations 到 Field Service） 
- 具有库存单位的 Field Service 产品（Finance and Operations 到 Sales） 

## <a name="entity-set"></a>实体集

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS 现有库存(按仓库分类)     |

## <a name="entity-flow"></a>实体流
将所选产品的库存水平信息从 Finance and Operations 发送到 Field Service。 库存水平信息包括： 
- 现有数量（仓库中当前实际记录的数量）
- 在订单数量上（订单上的总记录数量，如销售订单）
- 订购数量（总记录订购数量，如采购订单）

当库存水平更改时，此信息为每个仓库的每个已发放产品捕获，并基于更改跟踪同步。

在 Field Service 中，集成解决方案为增量创建库存日记帐，以使 Field Service 中的水平与 Finance and Operations 中的水平匹配。

Finance and Operations 将充当库存水平的主水平。 因此，如果在 Field Service 中使用此功能，以及从 Finance and Operations 同步库存水平，为 Field Service 到 Finance and Operations 的工作订单、转移和调整设置集成非常重要。

从 Finance and Operations 掌握库存水平的产品和仓库可以通过“高级查询和筛选 (Power Query)”进行控制。

> [!NOTE]
> 可以在 Field Services（**外部维护 = 否**）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Finance and Operations 中的单个仓库。 这用于您希望 Field service 掌握详细的库存水平并仅向 Finance and Operations 发送更新的情况。 在这种情况下，Field Service 不会收到来自 Finance and Operations 的库存水平更新。 更多信息，请参阅[将库存调整从 Field Service 同步到 Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Finance and Operations 中的项目的销售订单](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
**外部产品库存**实体仅用于集成中的后端。 此实体从集成中的 Finance and Operations 接收库存水平值，然后将这些值转换为手动库存日记帐，其随后将更改仓库中的库存产品。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

### <a name="data-integration-project"></a>数据集成项目
您可以应用“高级查询和筛选”的筛选器，以仅让某些产品和仓库将库存水平信息从 Finance and Operations 发送到 Field Service。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>产品库存（Finance and Operations 到 Field Service）：产品库存

[![数据集成中的模板映射](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
