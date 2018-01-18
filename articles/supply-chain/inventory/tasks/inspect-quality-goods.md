---
title: "检查货物质量"
description: "此过程显示如何处理质检订单。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeed7eab750c606ea0009fa7c51baf96e2f9de51
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="inspect-the-quality-of-goods"></a>检查货物质量

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何处理质检订单。 您可以使用 USMF 公司演示数据运行此指南。 在开始此示例过程前，需要确认采购订单为“000016”，并且将产品收据过帐。 这将自动创建质检订单。 质量检查通常由质检员执行。


## <a name="select-a-quality-order"></a>选择质检订单。
1. 转到“库存管理”>“定期任务”>“质量管理”>“质检订单”。
2. 在列表中，标记所选的行。
    * 在开始此过程前，选择已创建的质检订单。  

## <a name="record-test-results"></a>记录测试结果
1. 单击“结果”。
2. 单击“编辑”。
3. 在“结果数量”字段中，输入一个数字。
4. 在列表中，标记所选的行。
5. 在“结果”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
    * 在此示例中，结果将基于预定义的结果。 通常您可以记录更具体的测试结果，例如大小或其他维度。  
7. 在列表中，单击所选行中的链接。
8. 单击“保存”。
9. 关闭该页面。

## <a name="validate-the-quality-order"></a>验证质检订单
1. 单击“验证”。
2. 在“验证人员”字段中，单击下拉按钮以打开查找。
    * 选择执行检查的用户。  
3. 在列表中，单击所选行中的链接。
4. 单击“选择”。
5. 单击“确定”。
6. 关闭该页面。

