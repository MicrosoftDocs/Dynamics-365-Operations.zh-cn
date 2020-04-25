---
title: 在物料对于工作单元可用时准备处理看板作业
description: 此任务的重点是在所有物料可用于工作单元时准备处理看板作业。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd6d5add4d11c917a705e88d10b589e2c43fab89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206925"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>在物料对于工作单元可用时准备处理看板作业

[!include [banner](../../includes/banner.md)]

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

