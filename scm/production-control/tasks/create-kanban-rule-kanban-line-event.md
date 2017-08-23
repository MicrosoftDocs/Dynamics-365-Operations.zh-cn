--- 
title: "使用看板行事件创建看板规则"
description: "此过程通过使用看板行事件设置触发从进程活动的提取来创建看板规则。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: cc8c3ff5e98ccce56a7a19b16c1aceac650cdf5a
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>使用看板行事件创建看板规则

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程通过使用看板行事件设置触发从进程活动的提取来创建看板规则。 看板规则由各数量等于或大于 25 的看板进程活动触发。 创建此任务的演示数据公司是 USMF。 该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。


## <a name="create-a-kanban-rule"></a>创建看板规则
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 单击“新建”。
3. 在“补货策略”字段中，选择“事件”。
    * 这将直接从需求生成看板。 它用于设置定义按订单生产方案的规则。  
4. 在“第一个计划活动”字段中，输入或选择一个值。
    * 输入或选择 SpeakerAssemblyAndPolish。 制造看板规则的第一项活动是生产流中的处理活动。 在选择该活动时，该活动的生效日期将复制到看板规则的生效日期。  
5. 展开“详细信息”部分。
6. 在“产品”字段中，键入“L0001”。
7. 展开“事件”部分。
8. 在“看板行事件”字段中，选择“自动”。
    * 这将根据需要生成事件看板。  此字段用于配置补充下游处理活动所需材料的看板规则。 当您选择“自动”时，随需求创建事件看板。 如果要在同一天进行生产，建议采用此设置。  
9. 设置最小的事件数量为“25”。
    * 当需求数量等于或大于此字段时，生成看板事件。 如果一台机器上要生成的订单数量比此字段少，但另一台机器上要生成的订单数量比此字段多，则这很有用。  
10. 单击“保存”。

## <a name="create-sales-order-and-trigger-kanban-chain"></a>创建销售订单和触发看板链
1. 转至“销售和营销”>“销售订单”>“所有销售订单”。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
    * 选择客户帐户 US-003，Forest Wholesales。  
4. 单击“确定”。
5. 在“物料编号”字段中，键入“L0001”。
    * L0001 是您为其创建了看板规则的物料。  
6. 将“数量”设置为“27”。
    * 由于 27 比看板规则中的 25 这一最小数量大，所以将触发事件看板。  
7. 在“站点”字段中，输入“1”。
8. 在“仓库”字段中，输入或选择一个值。
    * 选择“仓库 13”。  
9. 单击“保存”。

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>查看看板规则生成的看板
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 在列表中，找到并选择所需记录。
3. 展开“看板”部分。
    * 请注意，为 27 创建了看板以基于创建的看板规则处理活动。  
    * 这是最后一个步骤。  


