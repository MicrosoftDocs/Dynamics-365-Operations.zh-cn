--- 
title: "向看板规则中添加看板数量计算策略"
description: "此过程重点是创建看板数量计算策略，并将其添加到看板规则，以优化看板大小和数量。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>向看板规则中添加看板数量计算策略

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程重点是创建看板数量计算策略，并将其添加到看板规则，以优化看板大小和数量。 创建此程序的演示数据公司是 USMF。 此程序是专为价值流经理设计的。 此过程是创建“计算看板数量建议”这一过程的先决条件。 


## <a name="create-a-kanban-quantity-calculation-policy"></a>创建看板数量计算策略
1. 转到“生产控制”>“定期任务”>“看板数量计算”>“看板数量计算策略”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
    * 例如，键入“Speaker2016”。  
4. 在“主计划”字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
    * 选择静态计划 (StaticPlan) 以计算需求。  
6. 在列表中，单击所选行中的链接。
7. 单击“保存”。
8. 在“最小看板数量”字段中，输入“1”。
    * 此为看板数量计算中包括的额外看板数。  
9. 设置安全系数为“1”。
    * 此为用于计算安全库存的额外数量的系数。  
10. 在“提前天数”字段中，输入“30”。
    * 此为在看板数量计算日前之前，包括在需求计算中的天数。  
11. 在“滞后天数”字段中，输入“30”。
    * 这是从包括在需求计算中的看板数量计算日期正推的天数。  用于此计算的公式与实际值一起显示。 例如，看板数量 = ((平均每日需求量 x 提前期 x 2.00) / 每物料处理单元的产品数量 + 1  
12. 关闭该页面。

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>向看板规则中添加看板数量计算策略
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 在列表中，找到并选择所需记录。
    * 为此过程选择看板规则 000020。  
3. 在列表中，单击所选行中的链接。
4. 切换“看板数量计算策略”部分的展开项。
5. 单击“添加”。
    * 添加您刚刚在先前的子任务中创建的看板数量计算策略。  
6. 在列表中，标记所选的行。
7. 在“名称”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
    * 选择您刚刚在先前的子任务中创建的策略“Speaker2016”。  


