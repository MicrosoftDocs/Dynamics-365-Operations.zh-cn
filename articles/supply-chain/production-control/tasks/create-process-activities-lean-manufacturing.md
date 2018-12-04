--- 
title: "创建 lean manufacturing 的流程活动"
description: "创建 lean manufacturing 的流程活动。"
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a>创建 lean manufacturing 的流程活动

[!include [task guide banner](../../includes/task-guide-banner.md)]

创建 lean manufacturing 的流程活动。 

先决条件： 

1. 必须创建非活动的生产流和版本。

2. 必须创建工作单元。


## <a name="find-the-production-flow-version"></a>找到生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。

## <a name="create-a-new-activity"></a>创建新的活动
1. 单击“活动”。
    * 确保所选生产流程具有草稿版本，并选中该版本。  
2. 单击“创建新的计划活动”。
3. 单击“下一步”。
4. 在“名称”字段中，键入一个值。
5. 在“名称”字段中，键入一个值。
    * 请注意，特定生产流的所有版本的名称是唯一的。  
6. 在“流程数量”字段中，输入一个数字。
    * 请注意，无论将处理的工作数量是多少，此为每一工作计算人工成本的最小数量。 如果工作数量与此数量有偏差，将会创建人工成本差异。  
7. 单击“下一步”。

## <a name="select-the-work-cell"></a>选择工作单元
1. 在“工作单元”字段中，单击下拉按钮打开查找。
2. 在列表中，单击所选行中的链接。

## <a name="define-the-inventory-updates"></a>定义库存更新
1. 选择或取消选择“更新现有接收量”复选框。
    * 如果“现有更新=无”，您可定义活动，以接收半成品（活动未达到下一物料清单水平）。    您还可以选择消耗量半成品。  

## <a name="define-the-picking-activities"></a>定义领料活动
1. 单击“下一步”。
2. 在列表中，标记所选的行。
    * 为所选工作单元的输入库位创建默认领料活动。  
3. 单击“添加”。
    * 您可以为不暂存于工作单元输入库位的特定产品创建额外的领料活动。  
4. 在列表中，找到并选择所需记录。
5. 在“项目编号”字段中，输入一个值。
6. 在“仓库”字段，单击下拉按钮以打开查找。
    * 根据此定义，活动消耗的所有物料领自默认输入仓库和库位，除非物料在第二各领料活动中有定义。 此物料将从不同的仓库和库位领取。  
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 选择或取消选择“登记废料”复选框。
10. 单击“下一步”。

## <a name="define-the-activity-times"></a>定义活动时间
1. 在列表中，找到并选择所需记录。
    * 需要定义运行时间。 “运行时间”用于计算看板作业的成本和吞吐时间。 运行时间不用于计算产能负荷以及消耗量，两者按周期时间计算，周期根据生产流版本任务确定。  
2. 在“时间”字段中，输入一个数字。
3. 在“单位”字段中，键入一个值。
4. 选择“时间单位”。
5. 在“单位数量”字段中，输入一个数字。
6. 在列表中，找到并选择所需记录。
    * 排队时间为可选项。  
7. 在“时间”字段中，输入一个数字。
8. 在“单位”字段中，键入一个值。
9. 选择“时间单位”。
10. 在“单位数量”字段中，输入一个数字。
11. 单击“下一步”。
12. 单击“完成”。
13. 关闭该页面。


