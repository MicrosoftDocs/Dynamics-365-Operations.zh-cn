---
title: 通过使用单级结构计算 BOM（2016 年 2 月）
description: 此过程显示如何通过使用“成本计算单”中的单级分解计算成品的成本。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83a62966e343a9b1c073c2d6ec1c1b69b1daddbb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423076"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>通过使用单级结构计算 BOM（2016 年 2 月）

[!include [banner](../../includes/banner.md)]

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
    * 可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。    下面是成本的构成：  *    10 源于 ITEM_A，10 源于 ITEM_B，10 源于 BOM_2。 在此示例中，BOM_2 无详细信息，因为它是作为标准成本 10 输入的，未经计算。  *    7 源自设置时间，这是固定成本，7 源自运行时操作（流程）。  *    还有其他一些与间接成本对应的金额。  
9. @SysTaskRecorder:_RequestClose

