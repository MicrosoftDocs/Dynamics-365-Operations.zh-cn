--- 
title: "为内部库存转移生成转移文档"
description: "此过程显示如何为公司内货物转移创建转移单据。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0fe3d735d6309bf87047a27f9e68c579ca052012
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>为内部库存转移生成转移文档

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何为公司内货物转移创建转移单据。 此过程仅适用于主地址在立陶宛的法人。 此过程所用的演示数据公司为“DEMF“，其主要地址在立陶宛。 必须先完成“为公司内的货物转移设置转移单据”过程，才能完成此过程。 该过程是专为库存会计师设计的。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="create-a-transfer-order"></a>创建转移单
1. 转到“库存管理”>“入站订单”>“转移单”。
2. 单击“新建”。
3. 在“源仓库”字段中，输入或选择一个值。
4. 在“目标仓库”字段中，输入或选择一个值。
5. 单击“添加”。
6. 在列表中，标记所选的行。
7. 在“物料编号”字段中，输入或选择一个值。

## <a name="enter-transportation-details-for-the-transfer-order"></a>输入转移单的运输详细信息
1. 单击“保存”。
2. 在操作窗格上，单击“装运”。
3. 单击“运输详细信息”。
4. 在“打印运输详细信息”字段中选择“是”。
5. 在“货物签发者”字段中，输入或选择一个值。
6. 在“包装”字段中，键入一个值。
7. 在“负荷风险级别”字段中，键入一个值。
8. 在“承运人”字段中，输入或选择一个值。
9. 在“型号”字段中，输入或选择一个值。
10. 在“登记编号”字段中，键入一个值。
11. 在“装运人登记编号”字段中，键入一个值。
12. 在“驾驶员”字段中，输入或选择一个值。
13. 在“驾驶员名称”字段中，键入一个值。
14. 单击“保存”。
15. 关闭该页面。

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>查看未过帐转移单的装箱单
1. 单击“装箱单”。
2. 单击“确定”。
3. 关闭该页面。

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>查看已过帐转移单的装箱单
1. 在操作窗格上单击“转移单”。
2. 在操作窗格上，单击“装运”。
3. 单击“装运转移单”。
4. 单击“常规”选项卡。
5. 在“更新”字段中，选择一个选项。
6. 单击“概览”选项卡。
7. 在“装箱单”字段中，键入一个值。
8. 单击“确定”。
9. 在操作窗格上，单击“装运”。
10. 单击“装箱单”。
11. 单击“确定”。


