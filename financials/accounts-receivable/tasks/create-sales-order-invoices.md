--- 
title: "创建销售订单发票"
description: "此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 50c0ee41220461e282aace85f10a0e734a2ab688
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-order-invoices"></a>创建销售订单发票

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务指南介绍如何给销售订单开票，包括合并发票以及成批处理。 该程序适用于 USMF 演示公司。


## <a name="create-an-invoice-from-a-sales-order"></a>为一个销售订单创建一张发票
1. 转到“应收帐款”>“订单”>“已装运但未开票采购订单”。
2. 从列表中选择一个销售订单。 
3. 在操作窗格上，单击“发票”。
4. 单击“发票”。
    * 请注意此销售订单具有多个相关的装箱单。 它将只显示单词“<multiple>”，不会显示装箱单编号。  
5. 展开“参数”部分。
    * 若要过帐发票，请设定为“是”。 也可以关闭过帐功能只打印发票。 但是您还可以通过创建形式发票代替发票，效果一样。  
    * 此选项用于批处理作业。 运行批处理作业，查询将会运行。    
6. 在“打印”字段中，选择“以后”。
7. 选择“是”以“打印发票”。
    * “打印管理”可打印多个发票副本并通过电子邮件以 PDF 文档的形式发送发票。  
8. 在“打印费用”字段中，选择“汇总”。
9. 在“检查信用额度”字段中，选择“余额”。
10. 单击“取消”。

## <a name="combine-orders-into-a-single-invoice"></a>合并订单为一张发票
1. 转到应收帐项目>订单>所有销售订单。
2. 选定一个拥有多个发票的客户。
3. 选择一个开放销售订单。
4. 再选择同一个客户的另一个未结销售订单。
5. 在操作窗格上，单击“发票”。
6. 单击“发票”。
7. 展开“参数”部分。
8. 在“数量”字段中，选择“所有”。
    * 请注意在概述部分列出的两张发票。 现在将两张合并为一张发票。  
9. 在“汇总更新”字段中，选择“发票帐目”。
10. 单击“整理”合并这两个销售订单为一张发票。
    * 两个销售订单现在合并为一张发票。   
11. 单击“取消”。
12. 单击“是”。

## <a name="post-invoices-in-a-batch"></a>成批过帐发票
1. 转到“应收帐款“>”发票“>”批处理发票“>”发票“。
2. 单击“选择”。
3. 单击“确定”。
4. 单击“批处理”。
5. 单击“是”打开批处理程序。
6. 单击“重复执行”。
7. 选择“天数”
8. 单击“确定”。
9. 单击“确定”。
10. 单击“取消”。
11. 单击“是”。


