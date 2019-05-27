---
title: 创建基准预测
description: 生产规划员可通过使用时间序列预测模型或复制历史需求来创建基线预测。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d23e245ed1c084c26554ef3f859fdadaef9990d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552991"
---
# <a name="create-a-baseline-forecast"></a>创建基准预测

[!include [task guide banner](../../includes/task-guide-banner.md)]

生产规划员可通过使用时间序列预测模型或复制历史需求来创建基线预测。 此过程显示如何复制历史需求以使用一个物料分配参数来创建所有产品的基线预测。 


## <a name="set-up-an-item-allocation-key"></a>设置物料分配参数
1. 转到“主计划”>“设置”>“内部公司计划组”。
2. 使用“快速筛选器”以查找记录。 例如，使用值“10”在“名称”字段中进行筛选。
    * 对法人运行需求预测。 因此您需要设置为其生成内部公司计划组预测的所有公司。  
3. 在列表中，找到并选择所需记录。
4. 单击“物料分配参数”。
    * 选择您想要创建预测的所有物料分配参数。  
5. 在列表中，标记所选的行。
    * 选择 D_Aloc 物料分配参数。  
6. 单击 >。
7. 关闭该页面。
8. 关闭该页面。

## <a name="set-up-the-demand-forecasting-paramters"></a>设置需求预测参数
1. 转到“主计划”>“设置”>“需求预测”>“需求预测参数”。
2. 展开“预测算法参数”部分。
3. 在“预测生成策略”字段中，选择“复制历史需求”。
4. 单击“保存”。

## <a name="create-a-baseline-forecast"></a>创建基准预测
1. 转到“主计划”>“预测”>“需求预测”>“生成统计基线预测”。
2. 在“开始日期”字段中输入日期。
    * 如果您有从 2015 年 1 月 1 日开始的销售订单，请输入此日期。 如果没有，则输入您销售订单的最早日期。  
3. 在“结束日期”字段中输入日期。
    * 输入您的销售订单最后日期，例如 '2015-03-31'。  
4. 在“开始日期”字段中输入日期。
    * 输入 '2015-04-01'。 此日期将自动计算，作为下一预测时段的开始日期。  
5. 扩展“要包括的记录”部分。
6. 单击“筛选器”。
7. 在列表中，标记所选的行。
    * 标记字段=内部公司计划组的行。  
8. 在“标准”字段中，输入一个值。
    * 键入内部公司计划组，例如您在第一个任务所使用的 10。  
9. 在列表中，找到并选择所需记录。
    * 选择字段=物料分配参数的行。  
10. 在“标准”字段中，输入一个值。
11. 单击“确定”。
12. 展开“高级参数”部分。
13. 在“预测时段”字段中，选择“月份”。
14. 在“预测区间”字段中，输入“3”。
15. 输入“锁定时限”字段中，输入“1”。
16. 单击“确定”。

## <a name="visualize-the-demand-forecast"></a>使需求预测可视化
1. 转到“主计划”>“预测”>“需求预测”>“调整后的需求预测”。
2. 在聚合视图表中，选择位于第 1 行、第 2 列的单元格。 这是您为其创建预测的第二个月。
3. 设置数量单元格 (QtyCell) 为“400”。
    * 在单元格中，输入不同于预测值的数字，例如 400。  
4. 您已手动调整预测。 请注意在下一步的图形指示。
5. 单击“预测行详细信息”。
    * 在此页面中，您可以查看准确值、历史需求和预测。 您还可以对预测进行更改。  

