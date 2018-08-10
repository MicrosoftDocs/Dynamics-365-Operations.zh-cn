--- 
title: "创建 lean manufacturing 的转移活动"
description: "创建 lean manufacturing 的转移活动。"
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 010ac08fa96ead49b6ecbbe083e59fb96427e29e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>创建 lean manufacturing 的转移活动

[!include [task guide banner](../../includes/task-guide-banner.md)]

创建 lean manufacturing 的转移活动。 

先决条件： 

1. 必须创建非活动的生产流和版本。

2. 必须创建源和目标仓库和库位。 （可选）应创建补货或已补货工作单元。


## <a name="find-the-production-flow-version"></a>找到生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
    * 请注意，生产流必须有状态为草稿的版本。  
3. 在列表中，单击所选行中的链接。

## <a name="create-a-new-activity"></a>创建新的活动
1. 单击“活动”。
    * 确保所选生产流程具有草稿版本，并选中该版本。  
2. 单击“创建新的计划活动”。
3. 单击“下一步”。
4. 在“名称”字段中，键入一个值。
5. 在“活动类型”字段中，选择“转移”。
6. 在“流程数量”字段中，输入一个数字。
7. 单击“下一步”。

## <a name="select-the-work-cells"></a>选择“工作单元”
1. 在“补货”字段中，单击下拉按钮以打开查找。
    * 若要将工作单元输出库位作为转移活动的源库位，则选择一个工作单元。 补货工作单位可进行同样操作，此时设置转移活动的目标库位。  
2. 在列表中，单击所选行中的链接。

## <a name="define-the-inventory-updates"></a>定义库存更新
1. 在“产品类型”字段中，选择一个选项。
    * 请注意，转移并不改变产品类型。 您可以转移成品或半成品（在一个生产流以及可能的一个看板流的两个活动之间转移）。      在转移成品时，您可以选择“领取或接收是否产生库存交易记录”。  

## <a name="define-the-transfer-locations"></a>定义转移库位
1. 单击“下一步”。
2. 在“仓库”字段，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 在“地点”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
7. 在“货运服务提供方”字段中，选择“发货人”。
    * 可选项包括：发货人-装运仓库物料的组织、接收人-接收仓库物料的组织、承运人-第三方供应商。 如果运行机构为供应商，转移活动需要转包协议。  
8. 单击“下一步”。

## <a name="define-the-activity-times"></a>定义活动时间
1. 在列表中，找到并选择所需记录。
    * 需要定义运行时间。 “运行时间”用于计算看板作业的成本和吞吐时间。 “运行时间”不用于计算产能负荷以及消耗量，两者按周期时间计算，周期根据生产流版本任务确定。  
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


