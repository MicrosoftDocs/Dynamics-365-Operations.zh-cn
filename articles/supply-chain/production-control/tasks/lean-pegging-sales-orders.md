--- 
title: "销售订单的精益限定标准"
description: "该过程主要为验证看板生产物料的销售行限定标准树形图而设计的。"
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3aa8cd2c0be56875904158f041cf120c466d9e9a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="lean-pegging-from-sales-orders"></a>销售订单的精益限定标准

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程主要为验证看板生产物料的销售行限定标准树形图而设计的。 在验证限定标准树形图后，所有的看板作业为计划作业。 这对订单员需要保证立刻生产的订单方案有用。 创建此程序的演示数据公司是 USMF。 该过程目的在于设计精益公司的高级订单员的工作。


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>创建一个看板管理物料销售订单
1. 转到“所有销售订单”。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
    * 使用 US-001。  
4. 单击“确定”。
5. 在“物料编号”字段中，键入“L0001”。
6. 将“数量”设置为“30”。
    * 数量高于 24 以触发事项看板规则很重要。  

## <a name="open-a-pegging-tree"></a>打开一个限定标准树形图 
1. 单击“产品和供应”。
2. 单击“查看限定标准树”。
    * 请注意，该限定标准树形图显示的销售订单行限定标准所需的所有级别。 在此案例中，有两个级别的看板和所有必需的组件。  

## <a name="plan-the-pegging-tree"></a>计划该限定标准树形图。
1. 在该树形图中，选择“销售管线 000832\看板 000558”
2. 展开“看板”部分。
    * 请注意，该看板作业的作业状态为“未计划”。  
3. 单击“计划整个限定标准树形图”。
    * “作业状态”由“未计划”更改为“已计划”，可以在限定标准树形图中计划所有的看板作业。  
4. 刷新该页面。
    * 请注意，该看板作业的“作业状态”由“未计划”更改为“已计划”。  
5. 在该树形图中，选择“销售管线 000832\看板 000558\装运 L0001\看板 000559”。
    * 第二个看板作业也为计划作业，因为整个限定标准树形图为计划作业。 请注意，该看板作业状态由“未计划”更改为“已计划”。  


