---
title: 将库存转移和调整从 Field Service 同步到 Supply Chain Management
description: 本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存调整和转移同步到 Dynamics 365 Field Service 的模板和基础任务。
author: ChristianRytt
ms.date: 04/30/2019
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
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838973"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>将库存转移和调整从 Field Service 同步到 Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存调整和转移同步到 Dynamics 365 Field Service 的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于将库存调整和转移从 Field Service 同步到 Supply Chain Management。

**数据集成中的模板**
- 库调转移（Field Service 到 Supply Chain Management）
- 库调转移（Field Service 到 Supply Chain Management）

**数据集成项目中的任务**
- 库存调整
- 库存转移

## <a name="table-set"></a>表集
| Field Service                     | 供应链管理                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataverse 库存调整日记帐标头和行 |
| msdyn_inventoryadjustmentproducts | Dataverse 库存转移日记帐标头和行   |

## <a name="table-flow"></a>表流
Field Service 中进行的库存调整和转移将在 **过帐状态** 从 **已创建** 更改为 **已过帐** 后同步到 Supply Chain Management。 在发生此情况时，调整或转移单将锁定并变为只读。 这意味着调整和转移可以在 Supply Chain Management 中过帐，但是无法进行修改。 在 Supply Chain Management 中，您可以将批处理作业设置为自动过帐在集成期间生成的调整和转移库存日记帐。 请参阅以下先决条件了解有关如何启用批处理作业的详细信息。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案 
**库存单位** 列已添加到 **产品** 表。 需要此列是因为销售和库存单位在 Supply Chain Management 中不是始终相同，对于 Supply Chain Management 中的仓库库存，需要库存单位。
当您在库存调整产品中同时为库存调整和库存转移设置产品时，将从产品库存产品值提取单位。 如果找到值，**单位** 列将在库存调整产品中被锁定。

**过帐状态** 列已同时添加到 **库存调整** 表和 **库存转移** 表。 在调整或转移被发送到 Supply Chain Management 时，此列用作筛选器。 此列的默认值为“已创建 (1)”，但是它不发送到 Supply Chain Management。 在将值更新为“已过帐 (2)”后，它将被发送到 Supply Chain Management，但之后您不再能够更改调整或转移或添加新行。

**编号规则** 列已添加到 **库存调整产品** 表。 此列确保集成具有唯一编号，以使集成能够创建和更新调整。 在创建第一个库存调整产品时，将在 **P2C AutoNumber** 表中创建新记录以保持所使用的编号系列和前缀。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

### <a name="supply-chain-management"></a>供应链管理
集成生成的集成库存日记帐可以使用批处理作业自动过帐。 这从 **库存管理 > 定期任务 > Dataverse 集成 > 过帐集成库存日记帐** 启用。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>库存调整（Field Service 到 Supply Chain Management）：库存调整

[![数据集成中的模板映射](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>库存转移（Field Service 到 Supply Chain Management）：库存转移

[![数据集成中的模板映射](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]