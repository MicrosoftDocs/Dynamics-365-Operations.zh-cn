---
title: 创建和处理符合项
description: 此主题介绍如何执行不符合项管理，基于现有的质检订单。
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383611"
---
# <a name="create-and-process-a-conformance"></a>创建和处理符合项

[!include [banner](../../includes/banner.md)]

此主题介绍如何执行不符合项管理，基于现有的质检订单。 您可以在 USMF 演示公司运行此录制并可以使用建议的值。 此过程通常由质检员执行。  作为先决条件，按照[检查货物质量](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)中的说明完成操作。 若要处理不符合项的审核，运行任务录制的用户必须有在用户页分配的“名称”值。 若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。


## <a name="select-a-quality-order"></a>选择质检订单。
1. 在导航窗格中，转到**模块 > 库存管理 > 定期任务 > 质量管理 > 质检订单**。
2. 在列表中，选择在[检查货物质量](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)中创建的质检订单。  

## <a name="create-a-nonconformance"></a>创建一个不符合项
1. 在操作窗格中，选择**查询**。
2. 选择**不符合项**。
3. 选择**新建**。
4. 在**问题类型**字段的下拉菜单中，选择质检过程中找到的问题。  
5. 选择**确定**。

## <a name="approvereject-a-nonconformance"></a>批准/拒绝不符合项
1. 选择**功能**。
2. 选择**审核不符合项**。 对于本示例，批准不符合项。 批准的不符合项可以与相关操作关联，以记录在不符合项处理期间完成的工作，如本主题中所示，处理更正处理。  
3. 选择**是**。

## <a name="create-a-correction-action"></a>创建更正操作
1. 选择**更正**。
2. 选择**新建**。
3. 在新行的**人员编号**字段中，从下拉菜单选择所需记录。
4. 单击**选择**。
5. 选择**附加**。 创建关于更正的附注。 对于本示例，操作是联系供应商，以讨论不符合项情况。  
6. 选择**新建**。
7. 选择**单据**。 可以打印与不符合项管理有关的报告上的不同文档类型，具体取决于报告设置。  
8. 在**描述**字段中，键入一个值。
9. 关闭该页面。

## <a name="maintain-a-correction"></a>维护更正
1. 选择**标记完成**。
2. 选择**确定**。
3. 关闭该页面。

## <a name="close-a-nonconformance"></a>关闭不符合项
1. 选择**功能**。
2. 选择**关闭不符合项**。
3. 选择**是**。
4. 关闭页面。
