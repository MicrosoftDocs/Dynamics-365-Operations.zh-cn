---
title: 监控主计划运行
description: 生产规划员想要查看主计划运行是否在进行中。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845105"
---
# <a name="monitor-a-master-planning-run"></a>监控主计划运行

[!include [task guide banner](../../includes/task-guide-banner.md)]

生产规划员想要查看主计划运行是否在进行中。 使用演示数据公司 USMF 来完成此过程。


## <a name="run-master-planning"></a>运行主计划
1. 单击“主计划”。
    * 您将在默认仪表板找到此项。  
2. 在“计划”字段中，输入或选择一个值。
    * 示例：StaticPlan  
3. 单击“运行”。
4. 在“跟踪处理时间”字段中，选择“是”。
    * 如果已选择此字段，则跳过此步骤。  
5. 在“线程数”字段中，输入一个数字。
6. 扩展“要包括的记录”部分。
7. 单击“筛选器”。
8. 在列表中，标记所选的行。
    * 标记“字段=物料编号”的行。  
9. 在“标准”字段中，输入或选择一个值。
    * 例子： T0001  
10. 单击“确定”。
11. 单击“确定”。

## <a name="monitor-the-master-planning-run"></a>监控主计划运行
1. 单击“历史记录”。
2. 单击“查询”。
3. 单击“流程任务持续时间”。
4. 在列表中，找到并选择所需记录。
    * 对于每一物料，您可以获取其花费多长时间完成每个计划步骤的概览。  

