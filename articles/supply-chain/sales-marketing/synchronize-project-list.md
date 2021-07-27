---
title: 将项目列表从Supply Chain Management 同步到 Field Service
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的项目的模板和基础任务。
author: ChristianRytt
ms.date: 03/13/2019
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
ms.openlocfilehash: eb98f266a217fc16c56c38e2480b85f529fb1862
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359829"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>将项目列表从Supply Chain Management 同步到 Field Service

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的项目的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步。](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于运行项目从 Supply Chain Management 到 Field Service 的同步。

**数据集成中的模板**
- 项目（Supply Chain Management 到 Field Service）

**数据集成项目中的任务**
- 项目

在发生项目列表同步前，需要执行以下同步任务：
- 科目（Sales 到 Supply Chain Management） 

## <a name="entity-set"></a>实体集
| Field Service           | 供应链管理  |
|-------------------------|-------------------------|
|msdynce_externalprojects | 项目                |

## <a name="entity-flow"></a>实体流
项目在 Supply Chain Management 中创建。 将 **项目类型** 设置为 **时间和材料** 并将 **项目阶段** 设置为 **进行中** 的项目将同步到 Field Service 中的 **外部项目** 实体，包括项目编号、项目名称、项目阶段和客户帐户信息。 **外部项目** 列表用于将 Field service 工作订单与 Supply Chain Management 项目匹配。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
**外部项目** 实体从 Supply Chain Management 获取所有项目。 **外部项目** 字段已添加到 **工作订单** 实体。 此备份字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Supply Chain Management 内的一个项目。 **系统状态** 将 **打开 - 正在进行(690,970,000)** 更改为更高状态后，**外部项目** 字段将被锁定，您将无法再添加、删除或更改值。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置
### <a name="supply-chain-management"></a>供应链管理
为数据实体项目启用更改跟踪。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射


### <a name="projects-supply-chain-management-to-field-service-projects"></a>项目（Supply Chain Management 到 Field Service）：项目

[![数据集成中的模板映射。](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]