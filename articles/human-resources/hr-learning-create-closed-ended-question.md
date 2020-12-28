---
title: 创建封闭式问题
description: 封闭式问题允许您为回答者提供供选择的选项。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417522"
---
# <a name="create-a-closed-ended-question"></a>创建封闭式问题



封闭式问题允许您为回答者提供供选择的选项。 首先，您需要创建有回答的回答组，然后创建使用该回答组的问题。 创建此程序的演示数据公司是 USMF。


## <a name="create-an-answer-group"></a>创建回答组
1. 转到“调查表”>“设计”>“回答组”。
2. 单击“新建”。
3. 在“回答组”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
    * 每次将回答组用于问题时，使用随机功能以随机在不同订单中设置回答。  
5. 单击“回答”。
6. 单击“新建”。
    * 序列号控制回答显示的顺序，除非回答组已选择“随机”。  
    * 可规定回答项分数，以对调查表进行评分。  
7. 在“分数”字段中，输入一个数字。
    * 可以标记正确答案，以指示所选答案正确。 这可用于对调查表进行评分。  
8. 在“回答”字段中，键入一个值。
    * 继续为回答组创建回答选项。  
9. 单击“新建”。
10. 在“分数”字段中，输入一个数字。
11. 在“回答”字段中，键入一个值。
12. 单击“新建”。
13. 在“分数”字段中，输入一个数字。
14. 在“回答”字段中，键入一个值。
15. 单击“新建”。
16. 在“分数”字段中，输入一个数字。
17. 在“回答”字段中，键入一个值。
18. 单击“新建”。
19. 在“分数”字段中，输入一个数字。
20. 在“回答”字段中，键入一个值。
21. 关闭该页面。
22. 关闭该页面。

## <a name="create-the-question"></a>创建问题
1. 转到“调查表”>“设计”>“问题”。
2. 单击“新建”。
3. 使用“类型”字段，以将相关问题分组。
    * 您可以选择输入类型：复选框、备选按钮或封闭式问题的组合框。  
4. 在“输入类型”字段中，选择一个选项。
5. 在“回答组”字段中，输入或选择一个值。
6. 在“文本”字段中，键入一个值。

