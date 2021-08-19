---
title: 计划看板作业
description: 此程序是为特定工作单元调度处理看板作业而设计的。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d017599d1e9e7c1406a9501b9c8dd5c9e760e124fbb1eebf00ad3ad712f36da6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711559"
---
# <a name="schedule-kanban-jobs"></a>计划看板作业

[!include [banner](../../includes/banner.md)]

此程序是为特定工作单元调度处理看板作业而设计的。 创建该程序的先决条件是该程序为“在材料不可用的情况下特殊处理看板作业备用”。 创建此程序的演示数据公司是 USMF。 此任务用于车间主管与生产计划主任共同使用看板管理。


## <a name="select-kanban-jobs-for-a-work-cell"></a>为工作单元选择看板作业
1. 转到“生产控制”>“看板管理”>“安排看板作业”。
2. 展开“期间产能事实资料箱”
    * 展开“看板事实资料箱”。  
3. 在“工作单元”字段中，单击下拉按钮打开查找。
4. 在列表中，标记所选的行。
    * 选择 1250 号工作单元。 筛选资料之后将只展示 1250 号工作单元的工作情况。  
5. 在列表中，单击所选行中的链接。
6. 单击“选择”。

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>在第一个可用期间内安排一个看板作业
1. 在列表中，标记所选的行。
    * 在“无计划状态”列表中选择第一行。 “作业状态”字段中的可见图标为无计划状态。  
2. 单击“计划”。
    * 在第一个可用期间内安排看板作业。  
    * 请注意该看板作业已转移到列表末尾，因为它已经添加到今天开始的这个期间。  
    * 如果从今天开始的期间已经预订完毕，该作业将转移到第一个可用期间。  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>在具体日期安排两个计划作业
1. 在列表中，选择第一行 。
    * 请查看“作业状态”字段中显示“无计划状态”的第一行。  
2. 在列表中，选择第 2 行。
    * 请查看“作业状态”字段中显示“无计划状态”的第二行。 现在您已经选择了第一行的两个作业。  
3. 单击“日期安排”打开下拉对话框。
4. 选中或取消选中“覆盖产能短缺反应箱”。
    * 此选项允许覆盖默认产能短缺反应。  
5. 在“产能短缺反应”字段中，选择“添加到请求期间”。
    * 此选项确保该作业添加到所请求的期间，无论该工作单元是否出现超负荷状态。  
6. 单击“计划”。
    * 请注意这两个作业都添加到了预期期间。  
    * 在“期间产能”部分中，可查看每个期间的工作量。 “消耗量”字段显示该期间内的预定消耗量。 如果该期间内预定消耗量高于可用消耗量，将选择超负荷消耗量。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]