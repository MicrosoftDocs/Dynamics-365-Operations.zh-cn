--- 
title: "更改处理作业的看板规则"
description: "该过程旨在更改一个给定看板的惯用看板规则。"
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>更改处理作业的看板规则

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程旨在更改一个给定看板的惯用看板规则。 此适用于水平负荷资源以及万一出现故障的情况。 创建此程序的演示数据公司是 USMF。 该过程是为 lean manufacturing 公司的生产规划人员设计的，为价值流负责。


## <a name="copy-kanban-rule"></a>复制看板规则
1. 转到“看板规则”。
2. 在列表中，找到并选择所需记录。
    * 选择“事件看板规则”000022 至 L0001。  
3. 单击“复制看板规则”。
4. 单击“确定”。

## <a name="change-kanban-rule"></a>更改看板规则
1. 关闭该页面。
2. 转到“看板作业计划”。
3. 在列表中，标记所选的行。
    * 选择看板 000177 行。  
4. 单击“使用备选看板规则”。
5. 单击“下一步”。
6. 在“看板规则”字段中，输入或选择一个值。
    * 选择之前所创建的看板规则。 这是看板规则的最高值。  
7. 单击“完成”。
    * 现在该看板作业正在使用另一种看板规则。 此适用于水平负荷工作单元。  


