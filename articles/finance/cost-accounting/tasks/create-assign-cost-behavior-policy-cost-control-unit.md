---
title: 创建成本行为策略并将其分配到成本控制单元
description: 成本行为是将成本分类为固定或可变。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f52133df2d374d6dc0f1efb33ffc85eb7d11fa9
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759224"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>创建成本行为策略并将其分配到成本控制单元

[!include [banner](../../includes/banner.md)]

成本行为是将成本分类为固定或可变。 必须将政策和相应规则分配给成本控制单元，政策才能生效。 此过程用于创建政策，然后将其分配给成本控制单元。


## <a name="create-a-cost-behavior-hierarchy"></a>创建成本行为层次结构
1. 转到“成本核算”>“维度”>“维度层次结构”。
2. 单击“新建”。
3. 单击“创建”。
4. 在“维度层次结构名称”中，键入“成本行为层次结构”。
5. 在“维度”字段中，输入或选择一个值。
    * 选择“成本元素”。  
6. 单击“保存”。
7. 单击“查看层次结构”。
8. 单击“新建”。
9. 在“节点名称”字段中，键入一个值。
    * 输入固定成本  
10. 在树中，选择“成本行为层次结构”。
11. 单击“新建”。
12. 在“节点名称”字段中，键入一个值。
    * 输入可变成本。  
13. 单击“保存”。
14. 在树中，选择“成本行为层次结构\固定成本”。
15. 单击“新建”。
16. 在列表中，标记所选的行。
17. 在“起始维度成员”字段中，输入或选择一个值。
    * 维度成员的范围中可包含差距，但是这些成员不能重叠。  
18. 在“截止维度成员”字段中，输入或选择一个值。
    * 维度成员的范围中可包含差距，但是这些成员不能重叠。  
19. 在树中，选择“成本行为层次结构\可变成本”。
20. 单击“新建”。
21. 在列表中，标记所选的行。
22. 在“起始维度成员”字段中，输入或选择一个值。
    * 维度成员的范围中可包含差距，但是这些成员不能重叠。  
23. 在“截止维度成员”字段中，输入或选择一个值。
    * 维度成员的范围中可包含差距，但是这些成员不能重叠。  
24. 单击“保存”。

## <a name="create-the-policy-and-rules"></a>创建策略和规则
1. 转到“成本核算”>“政策”>“成本行为政策”。
2. 单击“新建”。
3. 在“政策名称”字段中，键入一个值。
4. 在“成本元素维度层次结构”字段中，输入或选择一个值。
    * 选择刚才创建的政策层次结构。  
5. 在“成本对象维度层次结构”字段中，输入或选择一个值。
    * 选择“组织”。  
6. 单击“保存”。
7. 单击“新建”。
8. 在列表中，标记所选的行。
9. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 展开层次结构以选择“可变成本”。  
10. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 默认情况下，可变百分比为 100%。  
11. 单击“成本控制单元的政策分配”。
12. 单击“新建”。
13. 在列表中，标记所选的行。
14. 在“核算生效日期”字段中输入日期。
    * 规则具有时效性，创建了更新版本时，用户或系统可让规则到期。  
15. 在“成本控制单元”字段中，输入或选择一个值。
16. 单击“保存”。

