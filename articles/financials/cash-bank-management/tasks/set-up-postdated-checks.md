--- 
title: "设置远期支票"
description: "本主题说明如何指定是否过帐远期支票的日记帐分录，以及选用哪一个过帐日记帐来清算会计条目和供应商付款。"
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d83713f9d54b396a10894995024ac1c8dd47a6f1
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-postdated-checks"></a>设置远期支票

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

本主题说明如何指定是否过帐远期支票的日记帐分录，以及选用哪一个过帐日记帐来清算会计条目和供应商付款。 您还可以指定已签发支票、已收到支票和预缴税金的清算帐户。 签发用于在将来时间进行付款和收款的远期支票。 您可以指定支票是否必须在其到期日期之前反映在会计帐簿中。



本过程由财务主管完成。 该程序适用于 USMF 演示公司。


## <a name="set-up-postdated-checks"></a>设置远期支票
1. 转到“现金和银行管理”>“设置”>“现金和管理银行参数”。
2. 单击“远期支票”选项卡。
3. 选择或清除“启用远期支票”复选框。
4. 选择或清除“过帐远期支票的日记帐条目”复选框。
5. 在“已签发支票的清算帐户”字段中，指定所需的值。
6. 在“已收到支票的清算帐户”字段中，指定所需的值。
7. 在“清算实体的普通日记帐”字段中，键入一个值。
8. 在“将远期支票转移到此供应商付款日记帐”字段中，键入一个值。
9. 在“预缴税金清算帐户”字段中，指定所需的值。
10. 单击“保存”。
11. 关闭该页面。
12. 转至“应付账款”>“付款设置”>“付款方式”。
13. 单击“新建”。
14. 在“付款方式”字段中，输入值。
15. 选择“远期支票清算过帐”选项以指明支票金额被过帐到清算帐户中。
16. 在“帐户类型”字段中，选择“银行”。
    * 付款方法的抵消帐户将是银行。  
17. 在“付款帐户”字段中，指定所需值。
    * 选择用于扣减发票金额的银行帐户。  
18. 关闭该页面。
19. 转到“应付账款”>“付款设置”>“付款方式”。
20. 单击“新建”。
21. 在“付款方式”字段中，输入值。
22. 选择“远期支票清算过帐”选项以指明支票金额被过帐到清算帐户中。
23. 在“帐户类型”字段中，选择“银行”。
    * 付款方法的抵消帐户将是银行。  
24. 在“付款帐户”字段中，指定所需值。
    * 选择用于扣减发票金额的银行帐户。  
25. 关闭该页面。


