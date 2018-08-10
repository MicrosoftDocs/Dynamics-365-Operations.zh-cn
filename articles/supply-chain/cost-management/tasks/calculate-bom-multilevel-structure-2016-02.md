--- 
title: "通过使用多级结构计算 BOM（仅限 2016 年 2 月）"
description: "此过程显示如何通过使用“成本计算单”中的多级分解计算成品的成本。"
author: ShylaThompson
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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>通过使用多级结构计算 BOM（仅限 2016 年 2 月）

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何通过使用“成本计算单”中的多级分解计算成品的成本。 这是 BOM 计算系列中的第七个任务。 创建此任务的演示数据公司是 USMF。

1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在列表中，找到并选择所需记录。
    * 选择产品 BOM_1。  
3. 在“操作窗格”中，单击“管理成本”。
4. 单击“物料价格”。
5. 单击“计算物料成本”。
    * 可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。  
6. 在“成本计算版本”字段中，输入或选择一个值。
    * 选择“成本计算版本 20”，因为其“计划成本类型和分解模式”为“多级”。   多级分解模式用于计划成本和模拟。 它不用于标准成本。  
7. 单击“确定”。
8. 单击“查看计算明细”。
    * 可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。  在这种情况下，请注意 BOM_2 的计算考虑了原材料、流程和开销，所以总计为 29,40，而不是此系列中初始任务指南内激活的标准成本 10。  
9. 单击“成本计算单”选项卡。
    * 我们转到“成本计算单”选项卡，这里的单位成本组总计与上一个任务指南中完成的计算相比有所不同。  
10. 在“级别”字段中选择“多”。
    * 如果选择“多”，则成本根据 BOM_2 的构成,归类，其中的 10 源自 M1 成本组 (ITEM_C)，15,60 源自其制造（成本组为 L2 的情况下）。 间接成本也会不同。  
11. 关闭该页面。
12. 关闭该页面。


