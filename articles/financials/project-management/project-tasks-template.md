---
title: "从 Project Service Automation 同步项目任务"
description: "本主题介绍用于将项目任务直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>将项目任务从 Project Service Automation 直接同步到 Finance and Operations 中的项目活动

本主题介绍用于将项目任务直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。

> [!NOTE]
> Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation 到 Finance and Operations 的数据传输

Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。 可通过数据集成功能提供的集成模板将有关项目任务的数据从 Project Service Automation 传输到 Finance and Operations。

下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>模板和任务

若要访问此模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目任务从 Project Service Automation 同步到 Finance and Operations：

-**项目中的模板名称：** 项目任务（PSA 到 Fin and Ops）-**项目中的任务名称：** 项目任务

必须先同步项目合同和项目，才能同步项目任务。

## <a name="entity-set"></a>实体集

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| 项目任务                           | 项目任务的集成实体。   |

## <a name="entity-flow"></a>实体流

项目任务在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目活动。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

必须先同步项目合同和项目，才能同步项目任务。

## <a name="power-query"></a>Power Query

如果满足以下条件，则必须使用 Microsoft Power Query：

- 项目任务内有资源特定的记录。

如果必须使用 Power Query，请遵守以下准则：

- “项目任务（PSA 到 Fin and Ops）”模板有一个默认筛选器，通过在 **IsLineTask** 中将该筛选器设置为 **False**，可以从项目任务内排除资源特定的记录。 如果创建自己的模板，则必须添加这个筛选器。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的一个示例。 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


