---
title: 创建多个活动的看板规则
description: 此过程演示如何创建包含来自生产流的多个活动的看板规则。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5360b7a19a993debd5f50f9df300c7a8862f897920278e712022e1b16052e9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757606"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>创建多个活动的看板规则

[!include [banner](../../includes/banner.md)]

此过程演示如何创建包含来自生产流的多个活动的看板规则。 创建此任务的演示数据公司是 USMF。 该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。


## <a name="create-a-new-kanban-rule"></a>创建新看板规则
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 单击“新建”。
3. 在“补货策略”字段中，选择“已计划”。
4. 在“第一个计划活动”字段中，输入或选择一个值。
    * 选择 SpeakerAssemblyAndPolish。  
5. 选中“多个活动”复选框。
    * 目的是在看板规则中包含多个活动。 当您选择最后一个计划活动时，您就选择了生产流中的一个路径。  
6. 在“最后一个计划活动”字段中，输入或选择一个值。
    * 选择 SpeakerTestAndPackaging。 选择值之后，将自动打开一个页面。 选择看板流 SpeakerAssemblyAndPolish > SpeakerTestAndPackaging。 单击“确定”。  
7. 展开“详细信息”部分。
8. 在“产品”字段中，输入或选择一个值。
    * 选择物料 L0006。  

## <a name="create-kanban-and-view-jobs"></a>创建看板和查看作业
1. 展开“看板”部分。
2. 单击“添加”。
3. 在“新看板数”字段中输入“1”。
    * 这将创建一个看板。  
4. 将产品数量设置为“3”。
    * 看板将处理 3 个产品。  
5. 在“到期日期/时间”字段中输入日期和时间。
    * 可以输入“今天”。  
6. 单击“创建”。
7. 单击“详细信息”。
    * 请注意，此看板有两个来自生产流的处理作业。 第一个是 SpeakerAssemblyAndPolish，第二个是 SpeakerTestAndPackaging。  
    * 这是最后一个步骤！  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]