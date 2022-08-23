---
title: 使用连续性计划
description: 此过程逐步演示如何销售连续性计划和如何处理相关销售订单。
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267396"
---
# <a name="using-continuity-program"></a>使用连续性计划

[!include [banner](../includes/banner.md)]

此过程逐步演示如何销售连续性计划和如何处理相关销售订单。 若要完成此过程，必须将用户设置为呼叫中心用户。 此程序使用 USRT 演示数据公司。

1. 转至“Retail 和 Commerce”>“客户”>“客户服务”。
2. 在“SearchText”字段中，键入“Karen”，然后按 Tab 键。
    * 应弹出高级搜索对话框。 如果不弹出，请单击此字段右侧的“搜索”。  
3. 在列表中，标记所选的行。
    * 应该只有一行在显示 Karen Berg。 通过单击网格最左侧的复选标记列选中行。  
4. 单击“选择”。
5. 单击“新建销售订单”。
    * 最好记下销售订单编号。 此过程的后面需要该编号。  
6. 在“物料编号”字段中，键入“88000”，然后按 Tab 键。
    * 这是 USRT 演示数据中的一个连续性物料。  
7. 单击“完成”。
8. 在“付款方式”字段中，输入“Visa”。
9. 单击“添加信用卡”。
    * 在此页中输入所需信用卡信息。  
10. 单击“确定”。
11. 展开付款窗口。
    * 若要提交呼叫中心订单，必须为该订单输入付款。  
12. 单击“确定”。
13. 单击“提交”。
    * 您已创建完了新连续性订单。 接下来，您将运行两个批处理流程，用于处理这些连续性订单。  
14. 关闭该页面。
15. 转至“Retail 和 Commerce”>“连续性”>“处理连续性付款”。
16. 在“连续性物料”字段中，键入“88000”，然后按 Tab 键。
17. 单击“确定”。
18. 转至“Retail 和 Commerce”>“连续性”>“创建连续性子订单”。
    * 此流程将基于您的连续性计划的设置创建新销售订单。  
19. 在“连续性物料”字段中，键入“88000”，然后按 Tab 键。
    * 物料“88000”是 USRT 演示数据中的一个连续性物料。  
20. 在“销售订单”字段中，输入或选择一个值。
    * 输入您在此过程中前面记下的销售订单编号。 这将让此过程的处理时间降到最低。 “销售订单”字段为可选字段，您可以处理任一计划的所有订单。  
21. 单击“确定”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
