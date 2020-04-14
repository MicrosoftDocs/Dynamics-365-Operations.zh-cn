---
title: 创建替换看板规则
description: 此过程介绍在特定日期将现有看板规则替换为新看板规则。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d507418965f0ebcd657ef6363ec206eb73a722f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146943"
---
# <a name="create-a-replacement-kanban-rule"></a>创建替换看板规则

[!include [banner](../../includes/banner.md)]

此过程介绍在特定日期将现有看板规则替换为新看板规则。 在生产流或补货规则的更改需要协调和计划时这很有用。 用于创建过程的演示数据公司是 USMF。 当他们为更改的生产流或新补货规则准备生产时，该过程面向工艺工程师和价值流经理。 此任务使用新规则替换看板规则 000022，并且将新规则的最大数量从 48 增加到 100。


## <a name="select-a-kanban-rule-to-replace"></a>选择要替换的看板规则
1. 转到“看板规则”。
2. 在列表中，找到并选择所需记录。
    * 选择看板规则 000022。  

## <a name="create-a-replacement-kanban-rule"></a>创建替换看板规则
1. 单击“替换看板规则”。
2. 在“有效日期”字段中输入日期和时间。
    * 选择未来的一个日期，例如从现在起一个星期。 这是新看板规则生效并取代旧看板规则的日期和时间。  
    * 如果看板规则更改生产流的路径，可以选择另一活动。  在此过程中，我们将保持活动不改变。  
3. 单击“确定”。
    * 请注意，将创建新的看板规则来替换看板规则 000022。  
    * 生效日期根据您替换看板规则时选择的日期设置。  
4. 在列表中，找到并选择所需记录。
    * 选择替换的看板规则 000022。  
    * 请注意，替换的看板规则具有与到期日期相同的日期，因为这是它将到期的日期。  
5. 在列表中，选择第一行 。
    * 选择列表顶部的新看板规则。 这是看板规则编号最高的看板规则。  
6. 在列表中，单击所选行中的链接。
    * 单击看板规则编号打开该看板规则。  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>修改替换看板规则的最大数量
1. 设置最大数量为 '100'。
    * 展开“数量”快速选项卡查看“最大数量”字段。 更改最大数量为 100 可以最多处理 100 个看板。    这是该任务的最后一步。  

