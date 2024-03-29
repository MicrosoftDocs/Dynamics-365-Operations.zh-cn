---
title: 从计划中删除看板作业
description: 此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 838270189e08065f791c9e58888351025e0a6df8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573625"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>从计划中删除看板作业

[!include [banner](../../includes/banner.md)]

此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。 创建此程序的演示数据公司是 USMF。 此程序是为车间主管或生产计划主任而设计的。


## <a name="find-a-planned-kanban-job"></a>查找一个计划看板作业。
1. 转到“生产控制”>“看板管理”>“安排看板作业”。
2. 在“工作单元”字段中，单击下拉按钮打开查找。
3. 在列表中，单击所选行中的链接。
    * 选择 1250 号工作单元。  
4. 单击“选择”。
5. 在“显示作业状态”字段中，选择“预定作业”。

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>从预定计划中移除该计划看板作业
1. 在列表中，找到并选择所需记录。
    * 选择一个“计划状态”的作业，例如，开始于 2012 年 12 月 19 日的作业。  
2. 在操作窗格上，单击“计划”。
3. 单击“恢复作业原态”。
4. 单击“确定”。
    * 这可以将当前作业状态从“计划”转变为“无计划”，并将其从进程栏上移除。   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]