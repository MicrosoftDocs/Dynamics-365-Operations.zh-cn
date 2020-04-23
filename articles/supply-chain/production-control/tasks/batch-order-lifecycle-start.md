---
title: 从创建到开始的批次订单生命周期
description: 该过程向您介绍批次订单生命周期中的第一部分。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16b55726fdb9ab15e74a9f752cac972b80a98de2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210977"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>从创建到开始的批次订单生命周期

[!include [banner](../../includes/banner.md)]

该过程向您介绍批次订单生命周期中的第一部分。

从创建、成本预估和对生产作业计划到批次订单的实际开始。



创建此程序的演示数据公司是 USMF。 



使用其他数据集运行该过程的先决条件是具备有效配方和工艺路线的发布产品。


## <a name="create-a-batch-order"></a>创建批次订单
1. 转至“所有生产订单”。
2. 单击“新批次订单”。
3. 在“物料编号”字段中，输入或选择一个值。
4. 单击“创建”。
5. 使用“快速筛选器”在“生产”字段筛选值“b”。

## <a name="view-production-formula-and-expected-co-products"></a>查看生产配方和预期联产品
1. 在操作窗格上单击“生产订单”。
2. 单击“配方”。
3. 关闭该页面。
4. 单击“联产品”。
5. 关闭该页面。

## <a name="estimate-the-batch-order"></a>估计批次订单
1. 单击“估计”。
2. 单击“确定”。
3. 在“操作窗格”中，单击“管理成本”。
4. 单击“查看计算明细”。
5. 关闭该页面。

## <a name="release-the-batch-order"></a>发布批次订单
1. 在操作窗格上单击“生产订单”。
2. 单击“下达”。
3. 单击“确定”。

## <a name="schedule-production-jobs"></a>计划生产作业
1. 在“操作窗格”上，单击“计划” 。
2. 单击“计划作业”。
3. 在“有限产能”字段中选择“否”。
4. 在“有限物料”字段中，选择“否”。
5. 单击“确定”。
6. 在操作窗格上单击“生产订单”。
7. 单击“所有作业”。
8. 关闭该页面。

## <a name="start-the-batch-order"></a>开始批次订单
1. 单击“开始”。
2. 单击“常规”选项卡。
3. 在“立即将领料单过帐”字段中选择“否”。
4. 单击“确定”。
5. 在操作窗格上，单击“查看”。
6. 单击“领料单”。
7. 在列表中，单击所选行中的链接。
8. 关闭该页面。
9. 关闭该页面。
10. 单击“工艺卡”。
11. 在列表中，单击所选行中的链接。
12. 关闭该页面。
13. 关闭该页面。

