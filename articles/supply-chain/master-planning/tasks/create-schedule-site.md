---
title: 创建站点计划
description: 此过程显示如何计划没有为站点开始的生产订单。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0db5095020bc14d56ae3680e7d0caa68789180e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469273"
---
# <a name="create-a-schedule-for-a-site"></a>创建站点计划

[!include [banner](../../includes/banner.md)]

此过程显示如何计划没有为站点开始的生产订单。  演示数据公司 USMF 用于完成此过程。


## <a name="identify-production-orders-that-are-not-started"></a>确定未开始的生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
2. 使用“快速筛选器”以查找记录。 例如，使用值“1”在“站点”字段中进行筛选。
    * 1 表示 USMF 中的站点。 如果您不使用 USMF，请选择您公司的站点。  
3. 打开状态列筛选器。
4. 使用“正好是”筛选器运算符将筛选器应用于值为“已计划”的“状态”字段。

## <a name="create-a-schedule"></a>创建计划
1. 在列表中，标记或取消标记所有行。
2. 在“操作窗格”上，单击“计划” 。
3. 单击“计划作业”。
4. 在“计划的方向”字段中，选择“从交货日期倒推”。
5. 在“有限产能”字段中选择“否”。
6. 在“有限物料”字段中，选择“否”。
7. 单击“确定”。
    * 这可能需要花费一段时间。  

## <a name="view-the-result-of-scheduled-production-orders"></a>查看已计划生产订单的结果
1. 在列表中，标记所选的行。
    * 您可以标记任何行。  
2. 在操作窗格上单击“生产订单”。
3. 单击“所有作业”。
    * 在此页，您可以查看工作列表。 在”计划“选项卡上，您可以查看作业的开始日期和结束日期。  
4. 单击“物料”。
    * 在此页，您可以查看生产订单中操作的估计物料消耗量和当前可用库存。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]