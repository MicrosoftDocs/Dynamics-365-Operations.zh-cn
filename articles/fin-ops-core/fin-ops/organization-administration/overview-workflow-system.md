---
title: 工作流系统概览
description: 此主题介绍工作流系统。
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b9fbb47f2ba4601a275423db3c072d61d460ece3204e2f8ee995e1c2febe230
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715931"
---
# <a name="workflow-system-overview"></a>工作流系统概览

[!include [banner](../includes/banner.md)]

此主题介绍工作流系统。

## <a name="what-is-workflow"></a>什么是工作流？

术语 *工作流* 可以通过两种方式定义：作为系统和作为业务流程。

### <a name="workflow-is-a-system"></a>工作流是一个系统

工作流是在应用程序对象服务器 (AOS) 上运行的系统。 使用工作流系统提供的功能，您可以创建单独的工作流或业务流程。

### <a name="workflow-is-a-business-process"></a>工作流是一个业务流程

“工作流”代表业务流程。 它通过显示谁必须完成任务、制定决策或批准文档定义单据如何在系统中流动或移动。 例如，下图显示支出报表的工作流。

![具有分配给用户的元素的工作流。](./media/workflow_user.gif)

为了更好地理解这一工作流，假定 Sam 提交 7,000 美元的支出报表。 在此场景中，Ivan 必须审核 Sam 传送给他的收据。 然后，晓辉和素心必须对该支出报表进行审核。 现在，假定 Sam 提交了一份 11,000 美元的支出报表。 在这种情况下，Ivan 必须复核相关收据，并且 Frank、Sue 和 Ann 必须审核该支出报表。

## <a name="benefits-of-using-the-workflow-system"></a>使用工作流系统的优点

在组织内使用工作流系统具有若干优点：

- **一致的流程** - 您可定义处理特定文档（如采购申请和支出报表）的方法。 通过使用工作流系统，您可以确保以一致且有效的方式来处理和审核文档。
- **流程可见性** - 您可跟踪工作流实例的状态、历史记录和绩效指标。 这帮助您确定是否需要对该工作流做出更改，以提高效率。
- **工作列表集中化** - 用户可以查看集中化的工作列表，该列表显示分配给他们的工作流任务和审核任务。


## <a name="workflow-content"></a>工作流内容

+ [工作流系统体系结构](workflow-system-architecture.md)
+ [工作流元素](workflow-elements.md)
+ [工作流审核流程中的操作](workflow-actions.md)
+ [创建工作流概览](create-workflow.md)
+ [配置工作流属性](configure-workflow-properties.md)
+ [配置工作流中的手动任务](configure-manual-task-workflow.md)
+ [配置工作流中的自动化任务](configure-automated-task-workflow.md)
+ [配置工作流中的审核流程](configure-approval-process-workflow.md)
+ [配置工作流中的审核步骤](configure-approval-step-workflow.md)
+ [配置工作流中的手动决策](configure-manual-decision-workflow.md)
+ [配置工作流中的有条件决策](configure-conditional-decision-workflow.md)
+ [配置工作流中的并行活动](configure-parallel-activity-workflow.md)
+ [配置工作流中的并行分支](configure-parallel-branch-workflow.md)
+ [配置行项工作流](configure-line-item-workflow.md)
+ [工作流常见问题](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]