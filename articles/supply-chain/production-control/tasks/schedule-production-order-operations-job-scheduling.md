---
title: 使用工序级和作业级计划来计划生产订单
description: 此主题的重点是使用工序级排产和作业级排产计划生产订单。
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a69339bc678de8343dbf2646a4d6fe0ace9964c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210471"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>使用工序级和作业级计划来计划生产订单

[!include [banner](../../includes/banner.md)]

此主题的重点是使用工序级排产和作业级排产计划生产订单。 不使用工序级排产创建作业，而使用作业级排产创建。 创建此任务的演示数据公司是 USMF。 此过程适用于在离散制造环境中工作的生产经理、生产规划员或车间主管。


## <a name="create-a-production-order"></a>创建生产订单
1. 在导航窗格中，转到**模块 > 生产控制 > 生产订单 > 所有生产订单**。
2. 选择**新建生产订单**。
3. 在**物料编号**字段中，输入或选择一个值。 选择物料编号 **D0001**。  
4. 选择**创建**。

## <a name="schedule-operations-for-the-production-order"></a>为生产订单计划工序
1. 标记新建的行。      
2. 在操作窗格上，选择**计划**。
3. 选择**计划工序**。
4. 在**计划的方向**字段中，选择**从计划日期正推**。
5. 在**计划日期**字段中，输入日期。 选择一个将来的日期，例如，今天加上一周。 使用所选的计划的方向，将安排将生产订单从此日期正推。  
6. 选择**确定**。
7. 在列表中，标记所选的行。 请注意，状态更改为**已计划**。 
8. 选择**所有作业**。 请注意，没有使用工序级排产创建作业。  
9. 关闭该页面。

## <a name="schedule-jobs-for-the-production-order"></a>为生产订单计划作业
1. 在操作窗格上，选择**计划**。
2. 选择**计划作业**。
3. 在**计划的方向**字段中，选择**从计划日期正推**。
4. 在**计划日期**字段中，输入日期。 选择一个将来的日期，例如，今天加上一周。 使用所选的计划的方向，将安排将生产订单从此日期正推。  
5. 选择**确定**。
6. 在操作窗格中，选择**生产订单**。
7. 选择**所有作业**。 请注意，根据有效的工艺路线，通过作业级排产创建 5 个作业。  

