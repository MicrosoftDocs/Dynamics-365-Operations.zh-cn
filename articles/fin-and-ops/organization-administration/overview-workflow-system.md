---
title: 工作流系统
description: 此主题介绍了 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统。
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/01/2019
ms.locfileid: "773080"
---
# <a name="workflow-system"></a>工作流系统

[!include [banner](../includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统。

## <a name="what-is-workflow"></a>什么是工作流？

术语*工作流*可以通过两种方式定义：作为系统和作为业务流程。

### <a name="workflow-is-a-system"></a>工作流是一个系统

工作流是随 Finance and Operations 一起安装，并且在应用程序对象服务器 (AOS) 上运行的系统。 使用工作流系统提供的功能，您可以创建单独的工作流或业务流程。

### <a name="workflow-is-a-business-process"></a>工作流是一个业务流程

“工作流”代表业务流程。 它通过显示谁必须完成任务、制定决策或批准文档定义单据如何在系统中流动或移动。 例如，下图显示支出报表的工作流。

![具有分配给用户的元素的工作流](./media/workflow_user.gif)

为了更好地理解这一工作流，假定 Sam 提交 7,000 美元的支出报表。 在此场景中，Ivan 必须审核 Sam 传送给他的收据。 然后，晓辉和素心必须对该支出报表进行审核。 现在，假定 Sam 提交了一份 11,000 美元的支出报表。 在这种情况下，Ivan 必须复核相关收据，并且 Frank、Sue 和 Ann 必须审核该支出报表。

## <a name="benefits-of-using-the-workflow-system"></a>使用工作流系统的优点

在组织内使用工作流系统具有若干优点：

- **一致的流程** - 您可定义处理特定文档（如采购申请和支出报表）的方法。 通过使用工作流系统，您可以确保以一致且有效的方式来处理和审核文档。
- **流程可见性** - 您可跟踪工作流实例的状态、历史记录和绩效指标。 这帮助您确定是否需要对该工作流做出更改，以提高效率。
- **工作列表集中化** - 用户可以查看集中化的工作列表，该列表显示分配给他们的工作流任务和审核任务。


## <a name="workflow-content"></a>工作流内容

+ [工作流架构](workflow-system-architecture.md)
+ [工作流元素](workflow-elements.md)
+ [工作流操作](workflow-actions.md)
+ [创建工作流](create-workflow.md)
+ [配置工作流属性](configure-workflow-properties.md)
+ [在工作流中配置手动任务](configure-manual-task-workflow.md)
+ [在工作流中配置自动化任务](configure-automated-task-workflow.md)
+ [配置工作流中的审核流程](configure-approval-process-workflow.md)
+ [配置工作流中的审核步骤](configure-approval-step-workflow.md)
+ [在工作流中配置手动决策](configure-manual-decision-workflow.md)
+ [在工作流中配置有条件决策](configure-conditional-decision-workflow.md)
+ [配置工作流中的并行活动](configure-parallel-activity-workflow.md)
+ [配置工作流中的并行分支](configure-parallel-branch-workflow.md)
+ [配置行项工作流](configure-line-item-workflow.md)
+ [工作流常见问题](workflow-FAQ.md)
