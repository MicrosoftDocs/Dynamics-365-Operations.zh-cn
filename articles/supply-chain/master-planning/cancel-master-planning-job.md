---
title: 取消主计划作业
description: 本主题说明如何取消使用内置计划功能的活动计划作业。
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947472"
---
# <a name="cancel-a-master-planning-job"></a>取消主计划作业

在 Microsoft Dynamics 365 Supply Chain Management 中，有多个选项可用于取消主计划作业。 例如，如果主计划作业是被错误开始的或运行时间比预期长，您想要结束它，您可能希望取消主计划作业。 取消计划作业的最佳方法是从**未完成的计划流程**页进行。 只有未在几分钟内完成从**未完成的计划流程**页取消主计划作业时，才应使用**批处理作业**和**增强的批处理作业**页面的替代选项。

## <a name="preferred-cancel-option"></a>首选取消选项
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>从**未完成的计划流程**页取消主计划作业
1. 转到**主计划 > 查询和报表 > 主计划 > 未完成的计划流程**。
2. 选择具有您要取消的计划流程的行。
3. 单击**取消**。

## <a name="additional-cancel-options"></a>其他取消选项
仅当未在几分钟内从**未完成的计划流程**页取消主计划作业时，才应使用这些选项。

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>从**批处理作业**页删除主计划作业
1. 转到**系统管理 > 查询 > 批处理作业**。
2. 选择具有您要删除的计划作业的行。
3. 单击**删除**。

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>从**增强的批处理作业**页中止主计划作业任务
1. 转到**系统管理 > 查询 > 批处理作业**。
2. 如果作业 ID 未显示在列表中，请单击**切换到增强窗体**，或继续下一步。
3. 打开批处理作业。 单击具有您要结束的任务的批处理作业的**作业 ID**。
4. 在**批处理任务**中，选择要结束的任务。
5. 在**批处理任务**快速选项卡中，单击**中止**。
