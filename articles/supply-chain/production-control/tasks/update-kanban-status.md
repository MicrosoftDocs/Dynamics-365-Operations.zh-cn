---
title: 更新看板状态
description: 在看板由错误清空或收到的看板需要清空时，需要更新看板状态。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210333"
---
# <a name="update-kanban-status"></a>更新看板状态

[!include [banner](../../includes/banner.md)]

在看板由错误清空或收到的看板需要清空时，需要更新看板状态。 创建此程序的演示数据公司是 USMF。 此过程专门面向车间主管。


## <a name="find-the-kanban"></a>查找看板。
1. 转到“生产控制”>“看板”>“看板”。
2. 打开处理单元状态列筛选器。
3. 单击“清除”。
    * 这重置筛选器。  
4. 使用“快速筛选器”以查找记录。 例如，在“卡号”字段中筛选值 '000149'。

## <a name="change-emptied-status-to-received-status"></a>将“已清空”状态更改为“已收到”状态
1. 单击“还原空的物料处理单元”。
2. 单击“确定”。
    * 请注意，处理单元状态为“已收到”。  

## <a name="change-received-status-to-emptied-status"></a>将“已收到”状态更改为“已清空”状态
1. 单击“空看板”。
2. 在列表中，标记所选的行。
    * 请注意，处理单元状态为“已清空”。  

