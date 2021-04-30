---
title: 将库存级别信息从 Supply Chain Management 同步到 Field Service
description: 本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存水平信息同步到 Dynamics 365 Field Service 的模板和基础任务。
author: ChristianRytt
ms.date: 05/07/2019
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
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910267"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>将库存级别信息从 Supply Chain Management 同步到 Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存水平信息同步到 Dynamics 365 Field Service 的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于将库存现有水平从 Supply Chain Management 同步到 Field Service。

**数据集成中的模板**
- 产品库存（Supply Chain Management 到 Field Service）
  
**数据集成项目中的任务**
- 产品库存

在发生库存水平同步前，需要执行以下同步任务：
- 仓库（Supply Chain Management 到 Field Service） 
- 具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales） 

## <a name="entity-set"></a>实体集

| Field Service                      | 供应链管理                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse 现有库存量（按仓库）     |

## <a name="entity-flow"></a>实体流
将所选产品的库存水平信息从 Finance and Operations 发送到 Field Service。 库存水平信息包括： 
- 现有数量（仓库中当前实际记录的数量）
- 在订单数量上（订单上的总记录数量，如销售订单）
- 订购数量（总记录订购数量，如采购订单）

当库存水平更改时，此信息为每个仓库的每个已发放产品捕获，并基于更改跟踪同步。

在 Field Service 中，集成解决方案为增量创建库存日记帐，以使 Field Service 中的水平与 Supply Chain Management 中的水平匹配。

Supply Chain Management 将充当库存水平的主水平。 因此，如果在 Field Service 中使用此功能，以及从 Supply Chain Management 同步库存水平，为 Field Service 到 Supply Chain Management 的工作订单、转移和调整设置集成非常重要。

从 Supply Chain Management 掌握库存水平的产品和仓库可以通过“高级查询和筛选 (Power Query)”进行控制。

> [!NOTE]
> 可以在 Field Services（**外部维护 = 否**）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Supply Chain Management 中的单个仓库。 这用于您希望 Field service 掌握详细的库存水平并仅向 Supply Chain Management 发送更新的情况。 在这种情况下，Field Service 不会收到来自 Supply Chain Management 的库存水平更新。 更多信息，请参阅[将库存调整从 Field Service 同步到 Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Supply Chain Management 中的项目的销售订单](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
**外部产品库存** 实体仅用于集成中的后端。 此实体从集成中的 Supply Chain Management 接收库存水平值，然后将这些值转换为手动库存日记帐，其随后将更改仓库中的库存产品。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

### <a name="data-integration"></a>数据集成
要让该项目工作，需要确保更新 msdynce_externalproductinventories 的集成密钥。
1.  转到 **数据集成 > 连接集**。
2.  选择使用的连接集。
3.  在 **集成密钥** 选项卡中，确保向 msdynce_externalproductinventories 添加以下密钥：
      - msdynce_productnumber（产品编号）
      - msdynce_warehouseid（仓库 ID）
      
### <a name="data-integration-project"></a>数据集成项目
您可以应用“高级查询和筛选”的筛选器，以仅让某些产品和仓库将库存水平信息从 Supply Chain Management 发送到 Field Service。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>产品库存（Supply Chain Management 到 Field Service）：产品库存

[![数据集成中的模板映射](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]