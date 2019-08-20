---
title: 从其他模块（如销售发票）过帐凭证
description: 可以从总帐、库存变动日记帐、销售发票和采购发票过帐中国式凭证。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, InventProductDimensionLookup, DimensionLookup, InventTrans, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5a9419688d046fa00915555f889730dd5b34344
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848764"
---
# <a name="post-vouchers-from-other-modules-like-sales-invoices"></a>从其他模块（如销售发票）过帐凭证

[!include [task guide banner](../../includes/task-guide-banner.md)]

可以从总帐、库存变动日记帐、销售发票和采购发票过帐中国式凭证。 . 从这些源过帐时，将为这些财务凭证分配默认中国式凭证类型和中国式凭证号。
此任务逐步演示如何从库存变动日记帐和从销售发票过帐中国式凭证。
必须先向当前会计日历添加当前会计年度，才能完成此任务。 用于创建此任务的演示数据公司是 CNMF。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="post-chinese-vouchers-from-an-inventory-movement-journal"></a>从库存变动日记帐过帐中国式凭证
1. 转到“库存管理”>“日记帐条目”>“物料”>“移动”。
2. 单击“新建”。
3. 在“名称”字段中，输入或选择一个值。
4. 单击“确定”。
5. 单击“新建”。
6. 在列表中，标记所选的行。
7. 在“日期”字段中，输入一个日期。
8. 在“物料编号”字段中，输入或选择一个值。
9. 在“项目编号”字段中，输入一个值。
10. 关闭该页面。
11. 在“数量”字段中，输入一个数字。
12. 在“抵销帐户”字段中，指定所需值。
13. 在“抵销帐户”字段中，指定所需值。
14. 单击“库存维度”选项卡。
15. 在“站点”字段中，输入或选择一个值。
16. 在“仓库”字段中，输入或选择一个值。
17. 在“仓库”字段中，键入一个值。
18. 关闭该页面。
19. 在“尺寸”字段中，输入或选择一个值。
20. 在“大小”字段中，键入一个值。
21. 单击“财务维度”选项卡。
22. 关闭该页面。
23. 在“业务单位”字段中，输入或选择一个值。
24. 在“CostCenter_CN”字段中，输入或选择一个值。
25. 在“Department_CN”字段中，输入或选择一个值。
26. 单击“保存”。
27. 单击“验证”。
28. 单击“确定”。
29. 单击“过帐”。
30. 单击“确定”。
31. 单击“库存”。
32. 单击“交易记录”。
33. 在操作窗格上，单击"分类帐"。
34. 单击“财务凭证”。
    * 例如，为“中国式凭证类型”分配“交易”。  

## <a name="post-chinese-vouchers-from-a-sales-invoice"></a>从销售发票过帐中国式凭证
1. 转到应收帐项目>订单>所有销售订单。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
4. 展开“常规”部分。
5. 展开“管理”部分。
6. 单击“确定”。
7. 在列表中，标记所选的行。
8. 在“物料编号”字段中，输入或选择一个值。
9. 在“项目编号”字段中，输入一个值。
10. 关闭该页面。
11. 展开“行明细”部分。
12. 单击“设置”选项卡。
13. 单击“产品”选项卡。
14. 在“尺寸”字段中，输入或选择一个值。
15. 在“站点”字段中，输入或选择一个值。
16. 在“站点”字段中，输入一个值。
17. 在“仓库”字段中，键入一个值。
18. 在“仓库”字段中，输入或选择一个值。
19. 关闭该页面。
20. 关闭该页面。
21. 单击"价格和折扣"选项卡。
22. 单击“财务维度”选项卡。
23. 在“数量”字段中，输入一个数字。
24. 在“单价”字段中，输入一个数字。
25. 在“当前交货量”字段中，输入一个数字。
26. 在“当前交货量”字段中，输入一个数字。
27. 单击“保存”。
28. 在操作窗格上，单击“发票”。
29. 单击“发票”。
30. 展开“参数”部分。
31. 在数量字段，挑一选项。
32. 单击“确定”。
33. 单击“确定”。
34. 单击“发票”。
35. 单击“交易记录”。
36. 单击“凭证”。
    * 例如，可以看到为“中国式凭证类型”分配了“交易”。  

