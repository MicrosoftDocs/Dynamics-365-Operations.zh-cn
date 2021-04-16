---
title: 在发票日记帐中记录供应商发票
description: 此任务指南将显示如何记录与采购订单无关的供应商发票。
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35862195f3c2c13711157be919956f40fea0989b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820633"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>在发票日记帐中记录供应商发票

[!include [banner](../../includes/banner.md)]

此任务指南将显示如何记录与采购订单无关的供应商发票。 此类型发票的示例包括货物供应或服务的费用。  此记录使用 USMF 公司演示。

1. 找到 **导航窗格 > 模块 > 应付帐款 > 工作区 > 供应商发票条目**。
2. 在 **操作窗格** 中，单击 **新的发票日记帐**。
3. 单击 **新建**。
4. 在 **名称** 字段中，输入日记帐名称或单击下拉按钮以打开查找。
5. 在 **描述** 字段中，键入一个值。
6. 在 **操作窗格** 上，单击 **行**。 在 **日期** 字段中，输入要更新总帐的过帐日期。  
7. 在 **帐户** 字段中，指定 **供应商帐户**。
8. 在 **发票** 字段中，输入发票编号。
9. 在 **描述** 字段中，键入一个值。
10. 在 **信用** 字段中，输入一个数字。
11. 在 **抵销帐户** 字段中，输入科目编号或单击下拉按钮以打开查找
    * **销售税组** 将会根据供应商帐户默认显示。  
    * **物料销售税组** 将默认为 **抵销帐户** 字段中指定的主科目信息。  
    * **到期日期** 将根据“付款期限”计算。  
    * **现金折扣** 将默认为供应商帐户信息。
12. 如果启用了供应商发票日记帐工作流，请单击 **工作流 > 提交**。
    * 如果批准了您的提交，并且交易记录过帐日期在“保留”或“结束”期内，则该日期将提前到下一个启用期间的第一天。
12. 单击 **过帐**。
13. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]