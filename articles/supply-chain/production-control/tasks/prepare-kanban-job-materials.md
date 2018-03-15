---
title: "在物料对于工作单元可用时准备处理看板作业"
description: "此任务的重点是在所有物料可用于工作单元时准备处理看板作业。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: fdedab1bfccafb4f8592aea8ec421e3ba311a94a
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>在物料对于工作单元可用时准备处理看板作业

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务的重点是在所有物料可用于工作单元时准备处理看板作业。 创建此任务的演示数据公司是 USMF。 此过程是专为机器操作员设计的。

1. 转到“处理作业的看板面板”。
2. 在“工作单元”字段中，单击下拉按钮打开查找。
3. 在列表中，单击所选行中的链接。
    * 选择工作单元 1250，然后单击“确定”。  
4. 在列表中，选择第 4 行 。
    * 在演示公司中，第 4 行的看板 000329 是第一个作业，且未完成。  
5. 切换“领料单”部分的展开项。
    * 验证领料单上的所有物料均可有供应状态。  
    * 如果选中多个作业，领料单将显示所选作业所需的所有物料的总和。  
6. 单击“准备”。
    * 准备流程现在已完成。 物料单中选中所有行的复选框指示供应状态为已领料。  

