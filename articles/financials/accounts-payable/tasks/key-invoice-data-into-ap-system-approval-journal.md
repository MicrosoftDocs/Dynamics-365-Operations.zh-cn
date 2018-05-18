--- 
title: "使用审核日记帐将发票数据键入应付账款"
description: "此任务指南将显示如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>使用审核日记帐将发票数据键入应付账款

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南将显示如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。


## <a name="create-and-post-and-invoice"></a>创建并过帐发票
1. 转到“应付账款”>“发票”>“发票登记簿”。
2. 单击“新建”。
3. 选择您想要使用的发票登记簿名称。
4. 在列表中，单击所选行中的链接。
5. 单击“行”，以打开登记簿和输入费用行。
6. 选择某一供应商。 例如，输入或选择 US-104
7. 在“发票”字段中，输入一个值。
8. 在“描述”字段中，键入一个值。
9. 在“信用”字段中，输入一个数字。
10. 在“审核人”字段中，单击下拉按钮以打开查找。
11. 突出显示一个审核人，然后单击“选择”以选择该审核人。
12. 单击“过帐”。
13. 关闭该页面。
14. 关闭该页面。

## <a name="approve-an-invoice"></a>审核发票
1. 转到“应付账款”>“发票”>“发票审核”。
2. 单击“新建”。
3. 选择您想要使用的发票审核日记帐的名称。
4. 在列表中，单击所选行中的链接。
5. 单击“行”，以显示可以选择要审核发票的页面。
6. 选择“查找凭证”，以显示可供审核的所有发票。
7. 标记您创建的发票。
8. 单击“选择”。
    * 选中后，您选择的以上凭证将移动到此列表中。  
9. 单击“确定”。
10. 单击“帐号”字段，以添加费用帐户到发票中。
11. 输入一个帐号，并关闭该字段。 例如，输入 600120。
12. 单击“过帐”。
13. 单击“凭证”查看已过帐条目。
    * 发票待定审核帐户被冲销，并替换成实际费用帐户。  


