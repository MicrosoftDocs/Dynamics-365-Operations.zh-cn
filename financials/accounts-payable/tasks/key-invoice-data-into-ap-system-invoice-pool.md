--- 
title: "使用发票池将发票数据键入 AP 系统"
description: "此任务向导将向您展示如何使用发票登记簿创建发票。"
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 08f66db0f62d5d985177b1d4ec0161df0b9961b3
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>使用发票池将发票数据键入 AP 系统

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务向导将向您展示如何使用发票登记簿创建发票。  然后使用发票池对发票与采购订单进行匹配，并在“供应商发票”页对费用进行关帐。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 转到“应付帐款”>“采购订单”>“采购订单”。
2. 单击“新建”以创建新的采购订单。
3. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
4. 从列表中选择供应商。 例如，供应商 1001。
5. 单击“确定”。
6. 在“物料编号”字段中，单击下拉按钮以打开查找。
7. 在该列表中查找服务物料编号。 例如，选择 S0001。
8. 单击物料编号并选择它。
    * 净额为 75.00。  这是我们预期的发票金额。  
9. 在操作窗格上，单击“采购”。
10. 单击“确认”。

## <a name="create-and-post-and-invoice"></a>创建并过帐发票
1. 转到“应付帐款”>“发票”>“发票登记簿”。
2. 单击“新建”。
3. 打开查找以选择您想使用的发票登记簿的名称。
4. 选择您想要使用的发票登记簿名称。
5. 单击“行”，以打开登记簿和输入费用行。
6. 在查找中，选择供应商。 例如，单击供应商 1001 。
7. 在“发票”字段中，输入发票编号。
8. 在“描述”字段中，键入一个值。
9. 在“信用”字段中，输入一个数字。
10. 在“采购订单”字段中，单击下拉按钮以打开查找。
11. 选择您之前创建的采购订单。
12. 在“审核人”字段中，单击下拉按钮以打开查找。
13. 突出显示一个审核人，然后单击“选择”以选择该审核人。
14. 单击“过帐”。
15. 关闭窗体。
16. 关闭窗体。

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>从发票池中打开发票并与采购订单进行匹配以此完成发票流程
1. 转到“应付帐款”>“发票”>“发票池”。
2. 单击“采购订单”以从发票池中的发票中创建供应商发票。
3. 选择您想要查看的发票。
4. 单击“更新匹配状态”以完成匹配。
5. 在操作窗格上，单击“选项”。
6. 单击“更改”视图。
7. 单击“网格”视图。
8. 单击“过帐”。
9. 关闭窗体。
10. 转到“应付帐款”>“供应商”>“供应商”。
11. 选择采购订单上的供应商。 例如，选择供应商 1001。
12. 在列表中，单击所选行中的链接。
13. 在操作窗格上，单击“供应商”。
14. 单击“交易记录”。
15. 选择您创建的发票。
    * 发票登记簿应计项目被冲销并被过帐到相应的费用帐户。  


