---
title: 转移物料与看板作业
description: 此过程重点是撤销看板作业，以转移物料。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11771bbedc9fe4bdfaaa074c449cd329ce1a1d8f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567983"
---
# <a name="transfer-materials-with-kanban-jobs"></a>转移物料与看板作业

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]