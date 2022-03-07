---
title: 开始生产订单
description: 该过程显示如何在作业车间启动生产订单。
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9822dd66876ef8ed6bbcd5846a39d69d2446d7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981061"
---
# <a name="start-a-production-order"></a>开始生产订单

[!include [banner](../../includes/banner.md)]

该过程显示如何在作业车间启动生产订单。 此流程会报告时间和物料消耗量。 创建此程序的演示数据公司是 USMF。 这是解释生产订单周期的七个步骤中的第五步。


## <a name="start-a-production-order"></a>开始生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
    * 选择一个状态为“已发布”的生产订单。  
2. 在操作窗格上单击“生产订单”。
3. 单击“开始”。
    * 在此页，可以确认生产订单的开始时间。  
4. 单击“常规”选项卡。
5. 在“开始工序 编号 字段中，输入“10”。
6. 在“自动工艺路线消耗量”字段中，选择“始终”。
7. 单击“现在过帐工艺卡”复选框。
8. 在“自动 BOM 消耗量”字段中，选择“始终”。
9. 单击“过帐领料单”复选框。
10. 单击“打印过帐领料单”复选框。
11. 单击“确定”。
    * 这是一个已打印的显示生产订单所使用的物料的领料单。  
12. 关闭该页面。

## <a name="validate-the-picking-list"></a>验证领料单
1. 在操作窗格上，单击“查看”。
2. 单击“领料单”。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 单击“编辑”。
6. 在“消耗”字段中，输入一个数字。
7. 单击“过帐”。
8. 单击“确定”。
    * 在领料单日记帐中，过帐生产订单的物料消耗量。 在过帐日记帐之前，如果在估计数量和实际消耗的数量之间存在差异，可以进行调整。  
9. 单击“网格面板”选项卡。
10. 关闭该页面。

## <a name="verify-the-route-card-journal"></a>核实工艺卡日记帐
1. 在操作窗格上，单击“查看”。
2. 单击“工艺卡”。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 单击“编辑”。
6. 在“小时”字段，输入一个数字。
7. 单击“过帐”。
8. 单击“确定”。
    * 在“工艺卡日记帐”，记录各工序所用的时间。 还可以报告完好和残次数量。  
