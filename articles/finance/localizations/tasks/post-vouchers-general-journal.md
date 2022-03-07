---
title: 过帐普通日记帐的凭证
description: 此过程逐步演示如何使用普通日记帐过帐中国式凭证。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransDimension, DimensionLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 104d3a33c4710a911b679e7821c5fe8f0fcfe52839f77d277376e76932e1eaf4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770494"
---
# <a name="post-vouchers-from-the-general-journal"></a>过帐普通日记帐的凭证

[!include [banner](../../includes/banner.md)]

此过程逐步演示如何使用普通日记帐过帐中国式凭证。  必须确保已创建所有必需的会计日历，才能完成此过程。 

本流程是用演示公司 CNMF 数据生成的。 对于 CNMF 演示数据，必须在会计年度“Fiscal_CN”中创建当年整年的会计年度。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="post-vouchers-from-general-ledger-journals"></a>从总帐日记帐过帐凭证
1. 转到“总帐”>“日记帐条目”>“普通日记帐”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“名称”字段中，输入或选择一个值。
5. 在列表中，单击所选行中的链接。
6. 在“凭证类型”字段中，输入或选择一个值。
7. 在“帐户”字段中，指定所需值。
8. 在“描述”字段中，输入或选择一个值。
9. 在“描述”字段中，键入一个值。
10. 在“借方”字段中，输入一个数值。
11. 在“抵销帐户类型”字段中，选择一个选项。
12. 在“抵销帐户”字段中，指定所需值。
13. 单击“财务维度”。
14. 单击“对方科目”。
15. 在“Cashflow_CN”字段中，输入或选择一个值。
16. 单击“确定”。
17. 单击“验证”。
    * 对于此示例，必须满足凭证类型“付款”的条件。 这意味着一个借方和贷方帐户必须为属于现金帐户的银行帐户，否则不能通过验证。  
18. 单击“验证”。
19. 单击“过帐”。
20. 单击“打印”。
21. 单击“凭证”。
22. 在“打印布局代码”字段中，输入或选择一个值。
23. 选中“打印科目维度”复选框。
24. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]