---
title: "工作流元素"
description: "本主题介绍构成工作流的不同元素。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 15cac09a97305c1b467cbb97da2d4b8a864ccbc7
ms.contentlocale: zh-cn
ms.lasthandoff: 11/14/2017

---

# <a name="workflow-elements"></a>工作流元素

[!include [banner](../includes/banner.md)]

本主题介绍构成工作流的不同元素。

工作流由“元素”构成。 以下各节描述各个元素类型。

## <a name="tasks"></a>任务

*任务*是必须执行的工作单元。 有两种类型的任务可添加到工作流：手动任务或自动化任务。

### <a name="manual-task"></a>手动任务

*手动任务*是必须由用户执行的工作单元。 例如，支出报表工作流中的手动任务可能要求所分配用户完成以下操作：

- 查看随支出报表一起提交的收据。
- 致电员工的经理。

### <a name="automated-task"></a>自动化任务

*自动化任务*是必须由系统执行的工作单元。 不要求人工交互。 例如，销售订单工作流中的自动化任务可能要求系统完成以下操作：

- 执行信用检查。
- 如果记录不存在，为客户创建客户记录。

## <a name="approval-processes"></a>审核流程

“*审核流程*”是由各个独立步骤构成的流程。 在每个审核步骤，用户可以执行以下操作：

- 批准单据。
- 拒绝单据。
- 请求对单据进行更改。
- 将单据分配给其他用户进行审核。

## <a name="line-item-workflow-elements"></a>行项工作流元素

可以创建工作流来处理文档或文档上的行项。 例如，您为工时单创建了审核工作流。 （我们将把此工作流称为*单据工作流*。）您可以向该单据工作流添加*行项工作流*元素。 在运行行项元素时，提交文档上的每个行项进行处理。 您可能想要由同一行项工作流来处理所有行项，或者您可能想要由不同的行项工作流来处理各行项。 假定员工提交了类似于下图的时间表。

![具有行项的工作流](./media/workflow_lineitemworkflow.gif)

在这种情况下，您可能要创建以下行项工作流：

- **行项工作流 1** – 此工作流用于处理项目 ID 是 1111 的行项。
- **行项工作流 2** – 此工作流用于处理项目 ID 是 2222 的行项。
- **行项工作流 3** – 此工作流用于处理项目 ID 是 3333 的行项。

## <a name="flow-control-elements"></a>流量控制元素

以下元素可让您设计具有同时运行的备选分支或分支的工作流。

### <a name="manual-decision"></a>手动决策

*手动决策*是工作流划分为两个分支处的点。 用户必须制定决策，并且此决策确定哪个分支用于处理提交的单据。

### <a name="conditional-decision"></a>有条件决策

*有条件决策*还是工作流划分为两个分支处的点。 但是，系统将决定哪一个分支用于处理提交的单据。 要进行此决定，系统对该单据进行评估以确定是否符合指定的条件。

### <a name="parallel-activity"></a>并行活动

*并行活动*是指包含两个或更多同时运行的工作流分支的工作流元素。

### <a name="subworkflow"></a>子工作流

*子工作流*是在其他工作流的上下文中运行的工作流。

