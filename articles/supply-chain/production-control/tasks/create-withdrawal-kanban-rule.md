---
title: 创建提款看板规则
description: 此过程显示在精益环境中创建转移物料的提领看板规则所需的设置。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1694472e20c28a0b0f94c1ced8544b7258c22b40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007083"
---
# <a name="create-a-withdrawal-kanban-rule"></a>创建提款看板规则

[!include [banner](../../includes/banner.md)]

此过程显示在精益环境中创建转移物料的提领看板规则所需的设置。 创建此程序的演示数据公司是 USMF。 该过程面向工艺工程师和价值流经理，因为他们负责新型或改良物料的补货准备。


## <a name="create-new-kanban-rule"></a>创建新看板规则
1. 转到“看板规则”。
2. 单击“新建”。
3. 在“类型”字段中选择“提领”。
    * “提领”类型由看板规则用来转移物料或货物。  
4. 在“第一个计划活动”字段中，输入或选择一个值。
    * 选择 ReplenishSpeakerComponents。   设置此活动将组件从仓库 11，库位 11 移到仓库 12 和库位 12。  
5. 在“产品”字段中，输入或选择一个值。
    * 选择“M0007”。  
6. 在“提前期”字段中，输入一个数字。
    * 例如，60。  
7. 在“度量单位”字段中，输入或选择一个值。
    * 例如，分钟。  

## <a name="set-quantities-for-kanban"></a>设置看板数量
1. 设置“默认数量”为“5”。
    * 这是将为每个看板转移的数量。  
2. 在“固定看板数量”字段中，输入 '2'。
    * 此为活动看板的数量。 在此情况下，2 个看板的转移数量分别为 5。  
3. 在“预警边界最小值”字段中，输入“1”。
    * 用于记录为该目标的所有看板的最小金额。 例如，这在看板数量概览中使用。  
4. 在“预警边界最大值”字段中，输入“2”。
    * 用于记录为该目标的所有看板的最大金额。 例如，这在看板数量概览中使用。  

## <a name="create-kanbans"></a>创建看板
1. 单击“保存”。
    * 在创建看板前需要保存看板规则。  
2. 单击“添加”。
    * 请注意，由于建议的“新看板数”为 2（与“固定的看板数量”相等），没有有效看板。  
3. 单击“创建”。
    * 这将创建两个看板。  
    * 请注意，将为此提领看板规则创建 2 个看板，每个处理数量为 5。  这是该过程的最后一步。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]