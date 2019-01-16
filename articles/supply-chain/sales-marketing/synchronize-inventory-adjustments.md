---
title: "将库存转移和调整从 Field Service 同步到 Finance and Operations"
description: "本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>将库存调整从 Field Service 同步到 Finance and Operations

[!include[banner](../includes/banner.md)]

本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于运行 Microsoft Dynamics 365 for Field Service 到 Microsoft Dynamics 365 for Finance and Operations 的库存调整和转移的同步。

**数据集成中的模板名称：**
- 库存调整（Field Service 到 Finance and Operations）
- 库存转移（Field Service 到 Finance and Operations）

**数据集成项目中的任务名称：**
- 库存调整
- 库存转移

## <a name="entity-set"></a>实体集
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS 库存调整日记帐标头和行 |
| msdyn_inventoryadjustmentproducts | CDS 库存转移日记帐标头和行   |

## <a name="entity-flow"></a>实体流
Field Service 中进行的库存调整和转移将在**过帐状态**从“已创建”更改为“已过帐”后同步到 Finance and Operations。 在发生此情况时，调整或转移单将被锁定并变为只读，因为调整和转移可能在 Finance and Operations 中过帐，因此无法修改。
在 Finance and Operations 中，您可以将批处理作业设置为自动过帐通过集成生成的调整和转移库存日记帐。 请参阅以下先决条件了解有关如何启用批处理作业的详细信息。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案 
“库存单位”字段已添加到“产品”实体。 需要此字段是因为销售和库存单位在 Operations 中不是始终相同，对于工序中的仓库库存，我们需要库存单位。
当您在库存调整产品中同时为库存调整和库存转移设置产品时，将从产品库存产品值提取单位。 如果找到值，单位字段将在库存调整产品中被锁定

“过帐状态”字段已同时添加到库存调整实体和库存转移实体。 在调整或转移被发送到 Operations 时，此字段用作筛选器。 字段默认为“已创建 (1)”，及之后不会发送到 Operations。 在更改为“已过帐 (2)”后，它将被发送到 Operations，但之后您不再能够在“调整”或“转移”中更改任何内容或向其添加任何新行。
“编号规则”字段已添加到“库存调整产品”实体。 此字段帮助集成具有唯一编号，以便集成了解何时执行创建和更新。 在创建第一个库存调整产品时，将在“P2C 自动编号”实体中创建新记录以保持所使用的编号系列和前缀。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

### <a name="in-finance-and-operations"></a>在 Finance and Operations 中
集成生成的集成库存日记帐可以通过批处理作业自动过帐。 这从以下位置启用：库存管理 > 定期任务 > CDS 集成 > 过帐集成库存日记帐

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>库存调整（Field Service 到 Finance and Operations）：库存调整

[![数据集成中的模板映射](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>库存转移（Field Service 到 Finance and Operations）：库存转移

[![数据集成中的模板映射](./media/FSTrans1.png)](./media/FSTrans1.png)

