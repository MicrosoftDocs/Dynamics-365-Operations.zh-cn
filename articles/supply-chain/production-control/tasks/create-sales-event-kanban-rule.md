---
title: 创建销售事件看板规则
description: 该过程的重点是创建在销售订单创建期间触发的看板规则所需的设置。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1759adea6db8120078e2f32bff79178545c2328a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422711"
---
# <a name="create-a-sales-event-kanban-rule"></a>创建销售事件看板规则

[!include [banner](../../includes/banner.md)]

该过程的重点是创建在销售订单创建期间触发的看板规则所需的设置。 事件看板规则源自销售订单行的补货要求。 创建此程序的演示数据公司是 USMF。 这面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。




## <a name="create-a-new-kanban-rule"></a>创建新看板规则
1. 转到“看板规则”。
2. 单击“新建”。
3. 在“补货策略”字段中，选择“事件”。
    * 选择“事件”表示看板规则由事件（如创建销售订单行）触发。   这适用于每个看板应涵盖特定需求的区域。  
4. 在“第一个计划活动”字段中，输入或选择一个值。
    * 选择“最终装配”。  
5. 展开“详细信息”部分。
6. 在“产品”字段中，输入或选择一个值。
    * 选择“L0050”。  

## <a name="define-an-event"></a>定义事件
1. 展开“事件”部分。
2. 在“销售事件”字段中，选择“自动”。
    * 将销售事件选为“自动”后，在销售行匹配产品和收货库位时，将会自动触发此看板规则。 在该过程中，使用的是仓库 13 的 L0050 产品。  
3. 设置最小的事件数量为“50”。
    * 如果最小事件数量为 50，只有事件数量为 50 或以上时才会触发看板规则。  
4. 展开“生产流”部分。
    * 请注意收货库位是仓库 13。 这意味着此库位将会触发看板规则。  
    * 在此示例中，位于仓库 13，数量为 50 或以上的 L0050 产品的销售行将触发此看板规则。  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>创建销售行以触发事件看板规则
1. 转到“所有销售订单”。
    * 在保存看板规则时会显示警告，这意味着在销售订单创建期间将实时创建看板。  
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
    * 例如，选择 US-003。  
4. 单击“确定”。
5. 在“物料编号”字段中，键入“L0050”。
6. 在“站点”字段中，输入“1”。
    * 选择站点 1，因为仓库 13 位于站点 1。  
7. 在“仓库”字段中，输入或选择一个值。
    * 将“仓库”设置为 13。  
8. 将“数量”设置为“75”。
    * 输入 50 或更多数量，以触发已创建的看板规则。  

## <a name="verify-that-kanban-is-created"></a>核实已创建看板。
1. 单击“产品和供应”。
2. 单击“查看限定标准树”。
    * 请注意，创建的看板的数量与销售行数量相同。 您还可以查看生产 L0050 所需的物料领料单。 这是该过程的最后一步。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]