---
title: 在发票日记帐中记录供应商发票
description: 此任务指南将显示如何记录与采购订单无关的供应商发票。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556319"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>在发票日记帐中记录供应商发票

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南将显示如何记录与采购订单无关的供应商发票。 此类型发票的示例包括货物供应或服务的费用。  此记录使用 USMF 公司演示。

1. 转到“应付账款”>“工作区”>“供应商发票条目”。
2. 单击“新发票日记帐”。
3. 单击“新建”。
4. 在“名称”字段中，输入日记帐名称或单击下拉按钮以打开查找。
5. 在“描述”字段中，键入一个值。
6. 单击“行”。
    * 在“日期”字段中，输入要更新总帐的过帐日期。  
7. 在“帐户”字段中，指定供应商帐户。
8. 在“发票”字段中，输入发票编号。
9. 在“描述”字段中，键入一个值。
10. 在“信用”字段中，输入一个数字。
11. 在“抵销帐户”字段中，输入科目编号或单击下拉按钮以打开查找
    * 销售税组将会根据供应商帐户默认显示。  
    * 物料销售税组将默认为“抵销帐户”字段中指定的主科目信息。  
    * “到期日期”将根据“付款期限”计算。  
    * 现金折扣将默认为供应商帐户信息。  
12. 单击“过帐”。
13. 关闭该页面。

