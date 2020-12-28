---
title: 查找过时产品变型
description: 此过程显示如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5efd1d471559d320102cd81e4be1ba8c1858f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422852"
---
# <a name="find-obsolete-product-variants"></a>查找过时产品变型 

[!include [banner](../../includes/banner.md)]

此过程显示如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。 先决条件：您需要至少先定义一个对于计划无效的产品生命周期状态，然后才能够播放此任务指南。


## <a name="run-a-simulation"></a>运行模拟
1. 转到“产品信息管理”>“定期任务”>“更改过时产品的生命周期状态”。
2. 在“新产品生命周期状态”字段中，输入或选择一个值。
3. 在“运行没有更新产品数据的模拟”字段中选择“是”。
4. 在“排除在此天数内创建的产品”字段中，输入一个数字。
5. 在“排除交易中使用的产品(以天数为单位)”字段中输入一个数字。
6. 扩展“要包括的记录”部分。
7. 单击“筛选器”。
8. 在列表中，标记所选的行。
9. 在“标准”字段中，输入一个值。
10. 单击“确定”。
11. 单击“确定”。

> [!NOTE]
> 如果您预期搜索大量产品，建议批量运行模拟。 此外，请确保模拟不会在公司大部分的有效工作时间期间运行。  

## <a name="review-the-simulation-results"></a>查看模拟结果
1. 转到“产品信息管理”>“查询和报告”>“产品生命周期状态维护历史记录”。
   
> [!NOTE]
> 在此页上，您可以查看模拟结果并评估在不通过模拟运行更新时有多少产品和产品变型将与新产品生命周期状态关联。  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>运行已过时产品的产品生命周期状态的更新
1. 关闭该页面。
2. 转到“产品信息管理”>“定期任务”>“更改过时产品的生命周期状态”。
3. 扩展“要包括的记录”部分。

> [!NOTE]
> 请注意，上一次选择已保存。  

4. 在“运行没有更新产品数据的模拟”字段中选择“否”。
5. 展开“后台运行”部分。

> [!NOTE]
> 根据受影响的产品和产品变型的数量，考虑批量运行此作业。 请确保不在公司的大部分有效工作时间运行较大的更新作业。  

6. 单击“确定”。
7. 转到“产品信息管理”>“查询和报告”>“产品生命周期状态维护历史记录”。

> [!NOTE]
> 查看更改的已发布产品和产品变型。  

8. 在列表中，找到并选择所需记录。

