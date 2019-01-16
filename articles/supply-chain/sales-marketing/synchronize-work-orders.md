---
title: "将工作订单从 Finance and Operations 同步到 Field Service"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Field Service 的具有项目编号的工作订单同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>将包含项目的工作订单从 Field Service 同步到 Finance and Operations

[!include[banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Field Service 的具有项目编号的工作订单同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

使用的 **Field Service 产品（Finance and Operations 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Finance and Operations 到Sales）– 直接**模板。 有关详细信息，请参阅[产品（Finance and Operations 到 Sales）– 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。

本主题仅介绍 **Field Service 产品（Finance and Operations 到 Field Service）** 与 **Field Service 产品（Finance and Operations 到Sales）– 直接**模板之间的差异。

主要差别在于此模板包括分配到 Field Service 中的工作订单的项目编号的映射，确保在 Finance and Operations 中创建的销售订单包含项目编号，并可以在相关项目上开票。 除了此模板外，请使用“高级查询和筛选”。

## <a name="templates-and-tasks"></a>模板和任务

**数据集成中的模板名称：**

- 包含项目的工作订单（Field Service 到 Finance and Operations）

**数据集成项目中的任务名称：**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
**外部项目**字段已添加到“工作订单”实体。 此字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Finance and Operations 内的一个项目。 **系统状态**将“打开 - 正在进行(690,970,000)”更改为更高状态后，**外部项目**字段将被锁定，您将无法添加、删除或更改值。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderHeader

[![数据集成中的模板映射](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderHeaderProject

[![数据集成中的模板映射](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderProduct

[![数据集成中的模板映射](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderService

[![数据集成中的模板映射](./media/FSWOP4.png)](./media/FSWOP4.png)

