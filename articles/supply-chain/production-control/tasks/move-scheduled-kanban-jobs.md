---
title: 移动计划的看板作业
description: 此程序用于将计划特殊处理的看板作业转移到另一个不同期间。
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb95bab2173cb45300560f59c394cd2d558fe69f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422966"
---
# <a name="move-scheduled-kanban-jobs"></a>移动计划的看板作业

[!include [banner](../../includes/banner.md)]

此程序用于将计划特殊处理的看板作业转移到另一个不同期间。 创建此程序的演示数据公司是 USMF。 此程序用于车间主管与生产计划主任共同使用看板管理。

## <a name="select-scheduled-kanban-jobs"></a>选择计划看板作业。 

1. 转到 **生产控制 > 看板 > 安排看板作业**。 

2. 在 **工作单元** 字段中，单击下拉按钮打开查找。 

3. 在列表中，标记所选的行。 
   - 选择 1250 号工作单元。 
4. 单击 **选择**。 

5. 在 **显示作业状态** 字段中，选择 **预定作业**。 筛选作业列表，仅显示计划看板作业。 

## <a name="move-kanban-jobs-to-a-different-period"></a>将看板作业转移到另一个不同期间。 

1. 在列表中，找到并选择所需记录。 选择一个 **计划作业** 状态的作业，例如，在 **计划期间** 字段中安排于 2012 年 12 月 20 日的作业。 然后将该作业转移到上一个期间。 

2. 单击 **上一期间**。 

3. 单击 **结束** 可将该作业转移到作业列表的末尾，作为上一个期间的最后一个作业。 

4. 在列表中，找到并选择所需记录。 选择一个 **计划作业** 状态的作业，例如，在 **计划期间** 字段中安排于 2012 年 12 月 18 日的作业。 然后将该作业转移到下一个期间。 

5. 单击 **下一期间**。 

6. 单击 **开始** 可将该作业转移到作业列表的开头，作为上一个期间的第一个作业。 

## <a name="move-a-job-within-a-period"></a>将一个作业转移到一个期间内。 

1. 在列表中，找到并选择所需记录。 选择一个“计划作业状态”的作业，例如，在 **计划期间** 字段中安排于 2012 年 12 月 19 日的作业。 然后将该作业转移到计划期间。 

2. 单击 **正推**。 请注意该作业将转移到列表的下一行。 

3. 单击 **后退**。 请注意该作业将转移到列表的上一行。
