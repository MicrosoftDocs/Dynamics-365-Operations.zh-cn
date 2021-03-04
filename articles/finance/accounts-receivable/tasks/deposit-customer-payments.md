---
title: 存放客户付款
description: 存入客户付款。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440747"
---
# <a name="deposit-customer-payments"></a>存放客户付款

[!include [banner](../../includes/banner.md)]

存入客户付款。 此任务使用 USMF 公司演示。

1. 转到 **导航窗格 > 模块 > 应收帐款 > 付款 > 付款日记帐**。
2. 选择 **新建**。
3. 在 **名称** 字段中，选择下拉菜单中的 **CustPay**。
4. 选择 **行**。
5. 在 **帐户** 字段中，选择记录付款的客户。
6. 在 **信用** 字段，输入付款金额。 您可以选择不填金额，由系统通过选择已经支付的发票计算出金额。  
7. 在 **付款参考** 字段中，键入一个值。 付款参考可以是您输入的付款的支票编号。 填写付款参考是为了在存款单上添加付款。  
8. 标记“使用存款单”框。 如果付款应该包含在存款中，请将此设置更改为“是”。  
9. 选择 **新建**。
10. 在 **帐户** 字段中，选择下一付款的客户。
11. 在 **信用** 字段，输入付款金额。
12. 在 **付款参考** 字段中，键入一个值。
13. 标记 **使用存款单** 框。
14. 选择 **过帐**。 需在存款单生成之前，对付款过帐。 这是为了确保在存款单生成后付款不会发生更改。  
15. 选择 **功能**。
16. 选择 **存款单**。
17. 选择 **确定**。 第一页用于创建存款单。  
18. 选择 **确定**。 第二步为打印存款单，此步骤非必填项。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]