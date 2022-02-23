---
title: 使用最小库存事件创建看板规则
description: 此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422719"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>使用最小库存事件创建看板规则

[!include [banner](../../includes/banner.md)]

此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。 创建看板规则，以便在库存水平下降到低于 200 件时将物料转移到该地点。 通过运行需求声明事件处理，创建所需看板。 创建此任务的演示数据公司是 USMF。 该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。


## <a name="create-a-new-kanban-rule"></a>创建新看板规则
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 单击“新建”。
3. 在“类型”字段中选择“提领”。
    * 此类型用于创建转移看板。  
4. 在“补货策略”字段中，选择“事件”。
    * 事件策略用于基于事件创建看板的转移。 在此过程的后面，将通过使用补货触发转移看板。  
5. 在“第一个计划活动”字段中，输入或选择一个值。
    * 输入或选择 ReplenishSpeakerComponents。 此转移活动具有收货（输出）仓库和库位 12，这意味着物料将移到仓库 12 中的库位 12。  
6. 展开“详细信息”部分。
7. 在“产品”字段中，输入或选择一个值。
    * 选择“M0007”。  
8. 展开“事件”部分。
9. 在“补货事件”字段中，选择“批处理”。
    * 这将创建看板，以便满足处理需求声明事件期间相关地点的物料需求。  

## <a name="set-the-minimum-quantity-for-the-item"></a>设置物料的最低数量
1. 单击以访问“产品”字段中的链接。
2. 单击并打开“物料编号”字段中的链接。
3. 展开“产品图像”速见表。
4. 在操作窗格上，单击“计划”。
5. 单击“物料覆盖范围”。
6. 单击“新建”。
7. 在列表中，标记所选的行。
8. 在“仓库”字段中，输入或选择一个值。
    * 将“仓库”设置为 12。  
9. 将“最小值”设置为“200”。

## <a name="run-the-batch-event-creation-job"></a>运行批量事件创建作业。
1. 转到“生产控制”>“定期任务”>“看板作业批处理”>“需求声明事件处理”。
2. 单击“确定”。
3. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
4. 在列表中，单击所选行中的链接。
    * 选择之前所创建的看板规则。  
5. 展开“看板”部分。
    * 请注意，创建了一个看板来将所需物料转移到仓库 12。  

