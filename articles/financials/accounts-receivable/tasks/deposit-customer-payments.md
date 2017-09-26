--- 
title: "存放客户付款"
description: "存入客户付款。"
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a2e5509ec4f763b8fd195f95257bdb085286920b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="deposit-customer-payments"></a>存放客户付款

[!include[task guide banner](../../includes/task-guide-banner.md)]

存入客户付款。 本任务使用 USMF 公司进行演示。

1. 转到“应收帐款”>“付款”>“付款日记帐”。
2. 单击“新建”。
3. 在“名称”字段中，单击下拉按钮以打开查找。
4. 选择付款日记帐。 
5. 单击“行”。
6. 在“帐户”字段中，选择记录付款的“客户”。
7. 在“信用”字段，输入付款金额。
    * 您可以选择不填金额，由系统通过选择已经支付的发票计算出金额。  
8. 在“付款参考”字段中，键入一个值。
    * 付款参考可以是您输入的付款的支票编号。 填写付款参考是为了在存款单上添加付款。  
9. 标记“使用存款单”框。
    * 如果付款应该包含在存款中，请将此设置更改为“是”。  
10. 单击“新建”。
11. 在“帐户”字段中，选择下一付款的“客户”。
12. 在“信用”字段，输入付款金额。
13. 在“付款参考”字段中，键入一个值。
14. 标记“使用存款单”框。
15. 单击“过帐”。
    * 需在存款单生成之前，对付款过帐。 这是为了确保在存款单生成后付款不会发生更改。  
16. 单击“功能”。
17. 单击“存款单”。
18. 单击“确定”。
    * 第一页用于创建存款单。  
19. 单击“确定”。
    * 第二步为打印存款单，此步骤非必填项。  


