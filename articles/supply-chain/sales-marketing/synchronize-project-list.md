---
title: "将项目列表从 Finance and Operations 同步到 Field Service"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的项目同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。"
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>将项目列表从 Finance and Operations 同步到 Field Service

[!include[banner](../includes/banner.md)]

本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的项目同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的项目的同步。

**数据集成中的模板名称：**
- 项目（Finance and Operations 到 Field Service）

**数据集成项目中的任务名称：**
- 项目

在发生项目列表同步前，需要执行以下同步任务：
- 帐户（Sales 到 Finance and Operations） 

## <a name="entity-set"></a>实体集
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | 项目                |

## <a name="entity-flow"></a>实体流
项目在 Finance and Operations 中创建。 具有**项目类型**时间和材料以及进行中的**项目阶段**的产品将同步到 Field Service 中的**外部项目**实体，包括项目编号、项目名称、项目阶段和客户帐户信息。 **外部项目**的列表用于将 Field service 工作订单与 Finance and Operations 项目匹配。
Field Service CRM 解决方案 外部项目是从 Operations 获取所有项目的新实体。
外部项目字段已添加到“工作订单”实体。 此字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Operations 内的一个项目。 “系统状态”将“打开 - 正在进行(690,970,000)”更改为更高状态后，“外部项目”字段将被锁定，您将无法添加、删除或更改值。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置
### <a name="in-finance-and-operations"></a>在 Finance and Operations 中
为数据实体项目启用更改跟踪

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射


### <a name="projects-finance-and-operations-to-field-service-projects"></a>项目（Finance and Operations 到 Field Service）：项目

[![数据集成中的模板映射](./media/FSProject1.png)](./media/FSProject1.png)

