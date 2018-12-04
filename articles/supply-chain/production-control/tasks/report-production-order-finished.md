--- 
title: "将生产订单报告为已完工入库"
description: "该过程显示如何报告生产订单为完工入库。"
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: e6f5e7316f89ba7c2b7091eb9df02aa07ea44dbd
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---
# <a name="report-a-production-order-as-finished"></a>将生产订单报告为已完工入库

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程显示如何报告生产订单为完工入库。 创建此程序的演示数据公司是 USMF。 这是解释生产订单周期的七个过程中的第六个过程。


## <a name="report-a-production-order-as-finished"></a>将生产订单报告为已完工入库
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
    * 选择具有“已开始”状态的一个生产订单。  
2. 在操作窗格上单击“生产订单”。
3. 单击“完工入库”。
    * 在此页，您可以确认报告为已完工的成品的数量。  
4. 单击“常规”选项卡。
5. 设置“良品数量”为“18”。
6. 设置“残次数量”为“2”。
7. 在“残次原因”字段中，选择“物料“。
8. 选择或取消选择“结束作业”复选框。
9. 选择或取消选择“接受残次”复选框。
10. 单击“确定”。

## <a name="verify-the-report-as-finished-journal"></a>核实完工入库的日记帐
1. 在操作窗格上，单击“查看”。
2. 单击“完工入库”。
3. 在列表中，标记所选的行。
4. 在列表中，单击所选行中的链接。
    * 过帐“完工入库日记帐”。 如果您想要对日记帐作调整，您可以在可进行更改的位置手动创建新日记帐。  


