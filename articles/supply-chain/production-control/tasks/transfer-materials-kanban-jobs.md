--- 
title: "转移具有看板作业的物料（仅 2016 年 2 月）"
description: "此过程重点是撤销看板作业，以转移物料。"
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>转移具有看板作业的物料（仅 2016 年 2 月）

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程重点是撤销看板作业，以转移物料。 创建此程序的演示数据公司是 USMF。 此过程是专为仓库工作人员设计的。


## <a name="display-transfer-jobs"></a>显示转移作业。
1. 转到“生产控制”>“看板”>“转移作业的看板面板”。
2. 展开或折叠“筛选器”部分。
    * 在筛选器部分，您可以通过筛选生产流、活动名称、源仓库和位置以及目标仓库和位置指定想看见的作业。  
3. 在“源仓库”字段中，键入“11”。
4. 在“目标位置”字段中，键入“12”。

## <a name="start-a-transfer-job"></a>开始转移作业
1. 在列表中，取消选中的行（若有）。
2. 在列表中，选择第 4 行 。
    * 选择状态为“未计划”的第一个作业。 确保只选中这一作业。  
3. 单击“开始”。
    * 请注意，图标指示作业开始。  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>选择第二个转移作业并更改数量
1. 在列表中，找到并选择所需记录。
    * 您可以选中多个作业，但现在只选中行 5。  
2. 在列表中，找到并选择所需记录。
    * 确保上一步中的作业是唯一选中的作业。 取消选择所有其他作业。  
3. 请注意，“作业数量”字段中的值供稍后参考。
4. 将作业数量设置为“30”。
    * 请注意该警告！ 不允许进行 30 项转移。 根据看板规则的设置，您只能转移原始数量。  
5. 使用以前在“作业数量”字段中记下的值
    * 将作业数量设置为前一个值。  

## <a name="start-the-second-transfer-job"></a>开始第二个转移作业
1. 单击“开始”。
    * 这将开始行 5 中作业的转移。  

## <a name="complete-both-transfer-jobs"></a>完成两个转移作业
1. 在列表中，选择第 4 行 。
    * 现在选中了行 4 和行 5 两个转移作业。  
2. 单击“完成”。
    * 这将完成两个作业的转移。  


