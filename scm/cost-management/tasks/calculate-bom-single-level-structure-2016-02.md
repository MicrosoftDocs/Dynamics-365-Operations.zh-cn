--- 
title: "通过使用单级结构计算 BOM（仅限 2016 年 2 月）"
description: "此过程显示如何通过使用“成本计算单”中的单级分解计算成品的成本。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 36096c9a0c8dde1028728ec257dfa63e7fb669af
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>通过使用单级结构计算 BOM（仅限 2016 年 2 月）

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何通过使用“成本计算单”中的单级分解计算成品的成本。 这是 BOM 计算系列中的第六个任务。 创建此任务的演示数据公司是 USMF。

1. 转至“产品发布”。
2. 在列表中，找到并选择所需记录。
    * 选择产品 BOM_1。  
3. 在“操作窗格”中，单击“管理成本”。
4. 单击“物料价格”。
5. 单击“计算物料成本”。
    * 可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。  
6. 在“成本计算版本”字段中，单击下拉按钮以打开查找。
    * 在这个演示中选择“10”。 这是用于向组件添加成本价的同一个成本计算版本。  
7. 单击“确定”。
8. 单击“查看计算明细”。
    * 可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。    下面是成本的构成：  •    10 源于 ITEM_A，10 源于 ITEM_B，10 源于 BOM_2。 在此示例中，BOM_2 无详细信息，因为它是作为标准成本 10 输入的，未经计算。  •  7 源自设置时间，这是固定成本，7 源自运行时操作（流程）。  •   还有其他一些与间接成本对应的金额。  
9. @SysTaskRecorder:_RequestClose


