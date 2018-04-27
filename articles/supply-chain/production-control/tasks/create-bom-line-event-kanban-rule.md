--- 
title: "创建物料清单行事件看板规则"
description: "此任务介绍在混合精益和经典生产环境中创建事件看板规则以确保生产物料清单行的供应所需的设置。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>创建物料清单行事件看板规则

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

此任务介绍在混合精益和经典生产环境中创建事件看板规则以确保生产物料清单行的供应所需的设置。 创建此任务的演示数据公司是 USMF。 该任务面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。


## <a name="create-a-new-kanban-rule"></a>创建新看板规则
1. 转到“生产控制”>“定期任务”>“看板数量计算”>“看板规则”。
2. 单击“新建”。
3. 在“类型”字段中选择“提领”。
    * “提领”类型用于创建转移看板。  
4. 在“补货策略”字段中，选择“事件”。
    * 选择事件策略来基于事件创建看板的转移。 稍后在任务指南中，我们将通过估计生产订单触发它。  
5. 在“第一个计划活动”字段中，输入或选择一个值。
    * 输入或选择 ReplenishSpeakerComponents。 此转移活动具有收货（输出）仓库和库位 12，这意味着物料将移到仓库 12 中的库位 12。  
6. 展开“详细信息”部分。
7. 在“产品”字段中，输入或选择 M0001。
8. 展开“事件”部分。
9. 在“物料清单事件”字段中，选择“自动”。
    * 将“物料清单行事件”字段设置为“自动”将创建看板来履行生产订单物料清单行的物料需要。  
10. 关闭该页面。

## <a name="create-and-modify-a-new-production-order"></a>创建和修改新的生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
2. 单击“新建生产订单”。
3. 在“物料编号”字段中，输入或选择一个值。
    * 输入或选择 'L0001'。 因为物料 M0001 包括在物料 L0001 的物料清单中，我们使用物料 L0001。  
4. 单击“创建”。
5. 在列表中，单击 L0001 的行中的链接。
6. 单击“物料清单”。
7. 在列表中，单击所选行中的链接。
8. 单击“编辑”。
9. 在“行类型”字段中选择“限定供应”。
    * 选择限定供应来触发看板的供应创建。  
10. 在“资源消耗量”字段中选择“否”。
    * 清除“资源消耗量”复选框让我们可以更改仓库。  
11. 展开“库存维度”部分。
12. 在“仓库”字段中，键入“12”。
    * 因为这是提领活动的输出仓库，仓库设置为 12。  
13. 在“位置”字段中，键入 '12'。
    * 因为这是提领活动的输出库位，库位设置为 12。  
14. 关闭该页面。
15. 关闭该页面。

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>估计生产订单并查看已创建的看板
1. 单击“估计”。
    * 估计生产订单将触发关联的看板的创建来供应物料 M0001。  
2. 单击“确定”。
3. 关闭该页面。
4. 关闭该页面。
5. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
6. 在列表中，单击所选行中的链接。
    * 选择为物料 M0001 创建的事件看板规则。  
7. 展开“看板”部分。
8. 在列表中，标记所选的行。
    * 请注意创建的用来供应估计生产订单的 M0001 的看板。  
    * 这是最后一个步骤！  


