--- 
title: "创建按预算管理的采购订单"
description: "使用此过程可以创建为可用预算检查的采购订单。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc024caa54db6629a1e573df295fe8333996647
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>创建按预算管理的采购订单

[!include[task guide banner](../../includes/task-guide-banner.md)]

使用此过程可以创建为可用预算检查的采购订单。 此录制使用 USMF 演示数据公司。


## <a name="review-the-budget-control-configuration"></a>检查预算控制配置
1. 转至“预算”>“设置”>“预算控制”>“预算控制配置”。
2. 单击“可用的预算资金”选项卡。
3. 单击“单据和日记帐”选项卡。
4. 单击“定义预算控制规则”选项卡。
5. 单击“定义预算组”选项卡。
6. 关闭该页面。

## <a name="create-the-purchase-order-header"></a>创建采购订单头
1. 转到“采购”>“采购订单”>“所有采购订单”。
2. 单击“新建”。
3. 在“供应商帐户”字段中，输入或选择一个值。
4. 展开“常规”部分。
5. 在“会计日期”字段中，将日期设置为“2016-01-01”。
6. 单击“确定”。

## <a name="add-a-purchase-order-line"></a>添加采购订单行
1. 在“采购类别”字段中，输入或选择一个值。
2. 将“数量”设置为“2”。
3. 在“单位”字段中，输入或选择一个值。
4. 将“单价”设置为“10000”。
5. 单击“财务”。
6. 单击“分配金额”。
7. 在“会计科目”字段中，指定值“601300-001-023--”。
8. 关闭该页面。

## <a name="perform-budget-checking"></a>执行预算检查
1. 单击“财务”。
2. 单击“执行预算检查”。
3. 单击“财务”。
4. 单击“预算检查错误或警告”。
5. 单击“关闭”。


