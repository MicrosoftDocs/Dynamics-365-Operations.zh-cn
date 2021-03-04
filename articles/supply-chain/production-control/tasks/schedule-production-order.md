---
title: 计划生产订单
description: 该过程说明安排一个生产订单。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3fe8f6890c7d8ac8835503091642faa773f7f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422958"
---
# <a name="schedule-a-production-order"></a>计划生产订单

[!include [banner](../../includes/banner.md)]

该过程说明安排一个生产订单。 创建此程序的演示数据公司是 USMF。 这是生产订单循环周期七个程序中的第三个。


## <a name="schedule-a-production-order"></a>计划生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
    * 选择具有“预估”状态的一个生产订单。  
2. 在“操作窗格”上，单击“计划” 。
3. 单击“计划作业”。
    * 此页用于设置计划参数。 可以设置为特定用户或所有用户参数。  
4. 在“计划的方向”字段中，选择“从今天开始”。
5. 在“计划日期”字段中，输入日期。
6. 选择或取消选择“有限产能”复选框。
7. 选择或取消选择“有限物料”复选框。
8. 单击“确定”。

## <a name="view-the-scheduling-results"></a>查看计划结果
1. 在操作窗格上单击“生产订单”。
2. 单击“所有作业”。
    * 此页显示的是您刚刚生成的计划作业。  
3. 展开或折叠“计划”部分。
    * 通过“计划”快速选项卡，可以查看计划的日期和时间。  
4. 单击“查询”。
5. 单击“产能负荷”。
    * 该“产能负荷”页显示计划作业的预留产能，当前可用的预留总工时数，以及计划作业仍可用工时数。  
6. 关闭该页面。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]