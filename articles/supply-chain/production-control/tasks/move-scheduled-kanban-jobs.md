--- 
title: "移动计划的看板作业"
description: "此程序用于将计划特殊处理的看板作业转移到另一个不同期间。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>移动计划的看板作业

[!include [task guide banner](../../includes/task-guide-banner.md)]

此程序用于将计划特殊处理的看板作业转移到另一个不同期间。 创建此程序的演示数据公司是 USMF。 此程序用于车间主管与生产计划主任共同使用看板管理。


## <a name="select-scheduled-kanban-jobs"></a>选择计划看板作业
1. 转到“Produktionsstyring”>“看板”>“Tidsplanlægning af 看板作业”。
2. !MtCMR!在“工作单元”字段中，单击下拉按钮打开查找。 áçêìõý!
3. Markér den valgte række på listen.
    * 选择 1250 号工作单元。  
4. 单击“选择”。
5. Vælg 'Planlagt' i feltet 显示作业状态。
    * 筛选作业列表，仅显示计划看板作业。  

## <a name="move-kanban-jobs-to-a-different-period"></a>将看板作业转移到另一个不同期间
1. Find og vælg den ønskede post på listen.
    * 选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 20 日的作业。 然后将该作业转移到上一个期间。  
2. 单击“上一个期间”。
3. 单击“结束”。
    * 如此可将该作业转移到作业列表的末尾，作为上一个期间的最后一个作业。  
4. Find og vælg den ønskede post på listen.
    * 选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 18 日的作业。 然后将该作业转移到下一个期间。  
5. 单击“下一个期间”。
6. 单击“开始”。
    * 如此可将该作业转移到作业列表的开头，作为上一个期间的第一个作业。  

## <a name="task-move-a-job-within-a-period"></a>任务：将一个作业转移到一个期间内
1. Find og vælg den ønskede post på listen.
    * 选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 19 日的作业。 然后将该作业转移到计划期间。  
2. 单击“前进”。
    * 请注意该作业将转移到列表的下一行。  
3. 单击“返回”。
    * 请注意该作业将转移到列表的上一行。  


