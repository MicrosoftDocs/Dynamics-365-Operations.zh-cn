--- 
title: "定义供应商付款期限"
description: "设置供应商发票的付款条款。"
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>定义供应商付款期限

[!include[task guide banner](../../includes/task-guide-banner.md)]

设置供应商发票的付款条款。 本任务使用 USMF 公司进行演示。

1. 转到“应付帐款”>“支付设置“>“支付条款”。
2. 单击“新建”。
    * “支付条款”页用于定义如何计算到期日。 并非用于定义如何计算现金折扣日期。  
3. 在“付款条款”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“天数”字段中，输入一个数字。
    * 此处输入的数字将会被添加到截止日期，或添加到“付款方式”所规定的结束日期。 例如，如果您选择“净额”，该数字将添加到截止日期。 如果您选择“本月”，将添加到当前月的最后一天来计算截止日期。  
6. 单击“保存”。
7. 关闭该页面。
8. 转到“应付帐款”>“付款设置”>“现金折扣”。
9. 单击“新建”。
10. 在“现金折扣”字段中，输入 ID。
11. 在“描述”字段中，键入一个值。
12. 如果供应商提供了一个分层折扣，请选择当前到期日后的下一个现金折扣。
13. 关闭该页面。
14. 在“天数”字段中，输入一个数字。
    * 在“天数”字段中输入的数量，将根据“净额/本月”字段中的选项，用于计算“现金折扣日期”。 如果选择“净额”，则数量将添加到发票日期以确定现金折扣日期。 如果已选择“本月数”，则该天数将添加到本月的最后日期以确定现金折扣日期。  
15. 在“折扣”字段中，输入现金折扣的百分比。 
16. 输入客户发票的现金折扣主帐户。
17. 输入供应商发票的现金折扣主帐户。
    * 如果将“折扣抵消帐户”设置为“使用供应商折扣的主帐号”，则应使用该“主帐号”。  如果该选项设置为“发票行上的帐号”，现金折扣将过帐到发票行上的资产或支出帐户。  
18. 单击“保存”。


