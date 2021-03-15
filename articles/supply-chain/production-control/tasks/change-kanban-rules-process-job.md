---
title: 更改处理作业的看板规则
description: 该过程旨在更改一个给定看板的惯用看板规则。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981347"
---
# <a name="change-kanban-rules-for-a-process-job"></a>更改处理作业的看板规则

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]