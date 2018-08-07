---
title: "创建和处理符合项"
description: "使用此过程可以执行不符合项管理，基于现有的质检订单。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a>创建和处理符合项

[!include [task guide banner](../../includes/task-guide-banner.md)]

使用此过程可以执行不符合项管理，基于现有的质检订单。 您可以在 USMF 演示公司运行此录制并可以使用建议的值。 此过程通常由质检员执行。  作为先决条件，运行“检查货物质量”任务录制。 若要处理不符合项的审核，运行任务录制的用户必须有在用户页分配的“名称”值。 若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。


## <a name="select-a-quality-order"></a>选择质检订单。
1. 转到“质检订单”。
2. 在列表中，标记所选的行。
    * 选择从“检查货物质量”任务记录创建的质检订单。  

## <a name="create-a-nonconformance"></a>创建一个不符合项
1. 单击“查询”。
2. 单击“不符合项”。
3. 单击“新建”。
4. 在“问题类型”字段中，单击下拉按钮以打开查找。
    * 选择在检查过程中发现的问题。  
5. 在“问题类型”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 单击“确定”。

## <a name="approvereject-a-nonconformance"></a>批准/拒绝不符合项
1. 单击“功能”。
2. 单击“批准不符合项”。
    * 对于本示例，批准不符合项。 批准的不符合项可以与相关操作关联，以记录在不符合项处理期间完成的工作，以及在本工作记录中，处理更正处理。  
3. 单击“是”。

## <a name="create-a-correction-action"></a>创建更正操作
1. 单击“更正”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“人员编号”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
6. 单击“选择”。
7. 单击“附加”。
    * 创建关于更正的附注。 对于本示例，操作是联系供应商，以讨论不符合项情况。  
8. 单击“新建”。
9. 单击“附注”。
    * 请注意，可以打印与不符合项管理有关的报告上的不同文档类型，具体取决于报告设置。  
10. 在“描述”字段中，键入一个值。
11. 关闭该页面。

## <a name="maintain-a-correction"></a>维护更正
1. 单击“完成标记”。
2. 单击“确定”。
3. 关闭该页面。

## <a name="close-a-nonconformance"></a>关闭不符合项
1. 单击“功能”。
2. 单击“关闭此不符合项”。
3. 单击“是”。
4. 关闭该页面。
5. 关闭该页面。

