--- 
title: "创建站点计划"
description: "生产规划人员计算特定物料生产的物料和产能需求。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>创建站点计划

[!include[task guide banner](../../includes/task-guide-banner.md)]

生产规划人员计算特定物料生产的物料和产能需求。 在采购建议创建后，他在计划的站点查找订单并确认订单，从最紧急的订单开始。 最紧急的订单是需要在当前日期确定的订单。 使用演示数据公司 USMF 执行这些任务。


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>创建物料的物料和产能计划
1. 单击“主计划”。
    * 您需要导航到默认仪表板。  
2. 单击“运行”。
3. 扩展“要包括的记录”部分。
4. 单击“筛选器”。
5. 在列表中，标记所选的行。
6. 在“标准”字段中，输入一个值。
    * 例子： D0001  
7. 单击“确定”。
8. 单击“确定”。
    * 这可能需要几分钟的时间。  
9. 刷新该页面。

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>确定物料的紧急计划订单
1. 打开“物料编号列”筛选器。
2. 在“物料编号”字段中安装一个筛选器，输入值“D0001”，点击筛选器操作键“开始”。
3. 打开订单日期列筛选器。
4. 在“订单日期”字段中应用筛选器（具有当前日期值），使用“正好是”筛选器运算符。

## <a name="firm-all-the-urgent-orders-for-the-item"></a>确定物料的所有紧急订单
1. 在列表中，标记或取消标记所有行。
2. 单击“确认”。
3. 单击“确定”。


