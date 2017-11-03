---
title: "工作流操作"
description: "本文说明每个工作流审核流程的参与者可以采取的操作。"
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bbaac72d8adb764c4b186b022100248b1c5a3804
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-actions"></a>工作流操作

[!include[banner](../includes/banner.md)]


本文说明每个工作流审核流程的参与者可以采取的操作。

工作流可能涉及若干组人员：发起方、任务受托人、决策者和审核人。 例如，在以下支出报表工作流中，Sam 是发起方，队列的成员是任务受托人，John 是决策者，Frank、Sue 和 Ann 是审核人。   

[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) 

以下部分说明各个组可以执行的工作流操作。

## <a name="actions-that-an-originator-can-perform"></a>发起方可以执行的操作
发起方通过提交文档进行审查来启动工作流实例。 例如，Sam 必须在**“支出报表”**页上单击**“提交”**按钮，才能提交其支出报表。

## <a name="actions-that-a-task-assignee-can-perform"></a>任务受托人可执行的操作
一个任务可分配给多个人员或到由若干人员监控的工作项队列。 不过，只能由一个人来完成任务。 例如，Sam 提交了一份支出报表并将其收据发送到其组织的支出报表部门进行审查。 

Adventure Works 支出报表部门的成员监控该队列。 该部门的成员 Julie 接受了审查 Sam 的支出报表和收据的任务。 她现在可以执行以下操作之一：完成、拒绝、委托、请求更改、重新分配或下达。 

**注释：**可用操作将随软件开发人员设计任务的方式而变化。

### <a name="complete"></a>完成

用户完成某项任务后，提请处理的文档分配给工作流中的下一用户（如果有）。 如果不需要进一步处理，该工作流程即告终止。 

例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。 在 Julie 完成自己的审核后，该单据将分配给 John。

### <a name="reject"></a>拒绝

如果用户拒绝了文档，该工作流程即告终止。 

例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。 如果 Julie 拒绝了该支出报表，该工作流程即告终止。 

然后 Sam 可以重新提交该支出报表。 他可以首先进行更改，或者可以重新提交原始版本。 如果 Sam 重新提交支出报表，则该工作流程将从手动审查任务开始。

### <a name="delegate"></a>委托

如果用户委托某项任务，该任务将分配给其他用户。 

例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。 Julie 将此任务分配给她的助手 Tim。 

然后，Tim 代表 Julie 采取操作。 因此，在 Tim 完成审查后，支出报表分配给 John，就像 Julie 完成了任务一样。

### <a name="request-change"></a>请求更改

如果用户请求对提交的单据进行更改，该单据将发还发起方。 

例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。 Julie 注意到支出报表上的一些错误并请求进行更改。 该支出报表发还给 Sam。 

Sam 可以重新提交该支出报表。 他可以首先进行所请求的更改，或者可以重新提交原始版本。 如果 Sam 重新提交支出报表，则工作项队列的成员必须重新审查支出报告和收据。

### <a name="reassign"></a>重新分配

工作项队列的成员可以将该队列中的文档分配到另一个队列。 

例如，该 Adventure Works 支出报表部门的成员 Julie 正在监控该队列。 为了帮助平衡工作量，她可以将支出报表和其中包含的收据重新分配到另一个队列。

### <a name="release"></a>发布

偶尔，工作项队列的成员可以接受任务，不过，随后确定他或她无法完成任务。 在这种情况下，接受任务的人员可以将文档释放后工作项队列。 

例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。 如果 Julie 确定她不能完成此任务，则她可以下达文档。 支出报表返回到该队列，以便 Adventure Works 支出报表部门的其他成员可以完成任务。

## <a name="actions-that-a-decision-maker-can-perform"></a>决策者可以执行的操作
通常，文档分配给决策者，因为有必须由决策者回答的问题。 该问题的答案通常是“**是**”或“**否**”或者是“**True**”或“**False**”。 如果决策者不选择这些选项之一，他或她可以委托决策。

### <a name="choice-1-or-choice-2"></a>\[选择 1\] 或\[选择 2\]

决策者必须回答与文档相关的问题。 该问题的答案通常是“**是**”或“**否**”或者是“**True**”或“**False**”。 决策者选择的回答确定使用哪个分支处理文档。 

例如，Sam 的支出报表分配给 John。 John 必须确定文档中的信息是否要求致电 Sam 的经理。 如果 John 确定需要呼叫，则支出报表分配给 Aretha，然后 Aretha 必须致电 Sam 的经理。 如果 John 决定不需要通话，则支出报表分配给 Frank 进行审核。

### <a name="delegate"></a>委托

在决策者委托决策时，该文档将分配给必须制定决策的其他用户。 

例如，Sam 的支出报表分配给 John。 John 将决策委托给他的助手 Maria。 

然后，Maria 代表 John 采取操作。 如果 Maria 确定需要致电 Sam 的经理，则支出报表分配给 Aretha，然后 Aretha 必须致电 Sam 的经理。 如果 Maria 决定不需要通话，则支出报表分配给 Frank 进行审核。

## <a name="actions-that-an-approver-can-perform"></a>审核人可以执行的操作
将单据分配给审核人后，审核人必须采取以下操作之一：批准、拒绝、委托或请求更改。

### <a name="approve"></a>审核

审核人审核单据后，该单据将根据需要分配给工作流中的下一用户（如果有）。 如果不需要进一步处理，该工作流程即告终止。 

例如，Sam 提交了一份 6,000 美元的支出报表，而且该文档分配给 Frank。 在 Frank a审核该单据后，该单据将分配给 Sue 进行审核。 一旦 Sue 批准了该支出报表，工作流程即告结束。

### <a name="reject"></a>拒绝

如果审核人拒绝了单据，该工作流程即告终止。 

例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Sue。 如果 Sue 拒绝了该支出报表，该工作流程即告终止。 

Sam 可以重新提交该支出报表。 他可以首先进行更改，或者可以重新提交支出报表的原始版本。 如果 Sam 重新提交了该支出报表，该工作流程将从审核流程开始运行。

### <a name="delegate"></a>委托

如果审核人委托处理单据，该单据将分配给其他用户进行审核。 

例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Frank。 晓辉将该支出报表委托给安然。 

随后，Ann 代表 Frank 执行操作。 因此，在 Ann 审核该单据后，该单据将分配给 Sue 进行审核 - 就如同 Frank 审核的一样。 Sue 批准了文档后，该文档将发送给 Ann 进行审核。

### <a name="request-change"></a>请求更改

如果审核人请求对单据进行更改，该单据将发还发起方。 

例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Sue。 如果 Sue 请求更改，该支出报表将发还 Sam。 

Sam 可以重新提交该支出报表。 他可以首先进行所请求的更改，或者可以重新提交支出报表的原始版本。 如果 Sam 重新提交了该支出报表，该报表将发送给 Frank 审核，因为 Frank 是审核流程中的第一位审核人。




