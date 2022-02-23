---
title: 将项目内的工作订单从 Field Service 同步到 Supply Chain Management
description: 此主题介绍用于同步 Dynamics 365 Field Service 与 Dynamics 365 Supply Chain Management 的具有项目编号的工作订单的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422807"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>将项目内的工作订单从 Field Service 同步到 Supply Chain Management

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Dynamics 365 Field Service 与 Dynamics 365 Supply Chain Management 的具有项目编号的工作订单的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

使用的 **包含项目的工作订单（Field Service 到 Supply Chain Management）** 模板基于 **工作订单（Field Service 到 Supply Chain Management）** 模板。 有关详细信息，请参阅[将 Field Service 的工作订单同步到 Supply Chain Management 的销售订单](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。

本主题仅介绍这两个模板之间的区别：
- **项目内的工作订单（Field Service 到 Supply Chain Management）**
- **工作订单（Field Service 到 Supply Chain Management）**

主要差别在于此模板包括分配到 Field Service 中的工作订单的项目编号的映射，确保在 Supply Chain Management 中创建的销售订单包含项目编号，并可以在相关项目上开票。 除了此模板外，请使用“高级查询和筛选”。

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称：**

- 项目内的工作订单（Field Service 到 Supply Chain Management）

**数据集成项目中的任务名称：**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
**外部项目** 字段已添加到“工作订单”实体。 此字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Supply Chain Management 内的一个项目。 当 **系统状态** 从“打开 - 正在进行(690,970,000)”更改为更高状态时，**外部项目** 字段将被锁定，您将无法添加、删除或更改值。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>项目内的工作订单（Field Service 到 Supply Chain Management）：WorkOrderHeader

[![数据集成中的模板映射](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>项目内的工作订单（Field Service 到 Supply Chain Management）：WorkOrderHeaderProject

[![数据集成中的模板映射](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>项目内的工作订单（Field Service 到 Supply Chain Management）：WorkOrderProduct

[![数据集成中的模板映射](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>项目内的工作订单（Field Service 到 Supply Chain Management）：WorkOrderService

[![数据集成中的模板映射](./media/FSWOP4.png)](./media/FSWOP4.png)
