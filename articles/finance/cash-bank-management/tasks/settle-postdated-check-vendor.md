---
title: 结算供应商的远期支票
description: 在支票过期银行清算之后，如果银行已清算支票交易记录，签发一张远期支票给供应商进行结算。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440816"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>结算供应商的远期支票

[!include [banner](../../includes/banner.md)]

在支票过期银行清算之后，如果银行已清算支票交易记录，签发一张远期支票给供应商进行结算。 

在开始这步之前请完成以下过程。

1) 设置远期支票

2) 为供应商登记和过帐远期支票



本过程由财务主管完成。 该程序适用于 USMF 演示公司。

1. 转到“应付帐款”>“付款”>“供应商远期支票”。
2. 单击“结算”。
3. 单击“结算清算条目”。
    * 结算供应商帐户的支票交易记录。  
4. 关闭该页面。
5. 转到“总帐”>“日记帐条目”>“普通日记帐”。
6. 在“显示”字段中，选择“全部”。
7. 选择或清除“仅显示用户创建的”复选框。
8. 在列表中，标记所选的行。
9. 单击“行”。
10. 单击“凭证”。
11. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]