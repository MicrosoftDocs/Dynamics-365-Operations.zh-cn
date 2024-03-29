---
title: 执行看板处理作业
description: 此过程介绍看板流程作业的执行。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566571"
---
# <a name="execute-kanban-process-jobs"></a>执行看板处理作业

[!include [banner](../../includes/banner.md)]

此过程介绍看板流程作业的执行。 第一个作业按预期数量完成并没有错误。 第二个作业完成时包含错误。 创建此程序的演示数据公司是 USMF。 此过程是专为机器操作员设计的。


## <a name="select-a-kanban-job"></a>选择看板作业
1. 转到“生产控制”>“看板”>“处理作业的看板面板”。
2. 在“工作单元”字段中，单击下拉按钮打开查找。
3. 单击包含资源组 1250 的行。 这筛选作业列表，将只显示 1250 工作单元的作业。
    * 标记状态为“计划作业”的行。  

## <a name="complete-a-job-with-expected-quantity"></a>按预期数量完成作业
1. 展开或折叠“详细信息”部分。
    * 此部分显示有关卡号、物料编号、已订购数量和活动名称的重要信息。  
2. 展开或折叠“生产说明”部分。
    * 此部分显示活动的生产说明。 说明可以是文本、图片、绘图和其他文档。  
3. 单击“开始”。
    * 选择尚未完成的作业。 使用“作业状态”字段中的状态图标查看作业状态。      
4. 单击“完成”。
    * 作业以预期质量完成。  

## <a name="complete-a-job-with-errors"></a>作业完成时有错误
1. 单击“开始”。
    * 在作业完成后，列表中的下一个作业将被自动选择。 这就是在单击“开始”之前您不需要选择作业的原因。  
2. 在“操作窗格”上单击“制造”。
3. 单击“完成(详细信息)”。
4. 在列表中，标记所选的行。
5. 在“错误数量”字段中，输入一个数字。
6. 在“完好数量”字段中，输入一个数字。
7. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]