---
title: 创建制造的固定数量看板规则
description: 该过程的重点是为触发精益环境的工作单元的转换活动创建固定的制造看板规则所需的设置。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0f58d1e265fb001474eb572b9bc325cf08790c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558164"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>创建制造的固定数量看板规则

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程的重点是为触发精益环境的工作单元的转换活动创建固定的制造看板规则所需的设置。 创建此程序的演示数据公司是 USMF。 该过程面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。


## <a name="create-new-kanban-rule"></a>创建新看板规则
1. 转到“看板规则”。
2. 单击“新建”。
    * 请注意，默认类型“制造和补货策略”是固定的。 您不必更改这些参数。  
3. 在“第一个计划活动”字段中，输入或选择一个值。
    * 将会对根据此看板规则创建的看板执行此活动。  选择“扬声器测试和包装”。  
4. 展开“详细信息”部分。
5. 在“产品”字段中，输入或选择一个值。
    * 选择“L0050”。  
6. 在“度量单位”字段中，输入或选择一个值。
    * 选择分钟。  
7. 在“提前期”字段中，输入一个数字。
    * 输入“5”。  

## <a name="set-quantities"></a>设置数量
1. 展开“数量”部分。
2. 设置“默认数量”为“10”。
    * 这是将为每个看板转移的数量。  
3. 选择“产品数量差异”复选框。
    * 这样，所选看板完成的数量可与默认数量不同。  若要允许看板完成数量介于 8 至 12 之间，将差异设为 2。  
4. 将差异设置为小于“2”。
    * 这将允许完成的数量低至 10 - 2 = 8  
5. 将差异设置为大于“2”。
    * 这将允许完成的数量高达 10 + 2 = 12  
6. 在“固定看板数量”字段中，输入一个数字。
    * 此为活动看板的数量。 此时，5 个看板的处理数量分别为 10。  
7. 在“预警边界最小值”字段中，输入“2”。
    * 用于记录为该目标的所有看板的最小金额。 例如，这在看板数量概览中使用。  
8. 在“预警边界最大值”字段中，输入“4”。
    * 用于记录为该目标的所有看板的最大金额。 例如，这在看板数量概览中使用。  
9. 在“自动计划数量”字段中，输入“1”。
    * 将此项设置为 1 表示将自动规划每个看板。   如果我们输入了 3，直到 3 个空看板已准备就绪，可以规划，才会规划看板。 这对分组工作和避免设置过多非常有用。  

## <a name="create-kanbans"></a>创建看板
1. 展开“看板”部分。
2. 单击“保存”。
    * 在创建看板前需要保存看板规则。  
3. 单击“添加”。
    * 请注意，由于建议的“新看板数”为 5，没有活动的看板。 这与“固定的看板数量”相等。  
4. 单击“创建”。
    * 这将创建 5 个看板。  
    * 请注意，将此制造看板规则创建为 5 个看板，每个处理数量为 10。 这是该过程的最后一步。  

