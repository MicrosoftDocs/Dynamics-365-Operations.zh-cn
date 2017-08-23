--- 
title: "设置增值税主管机构"
description: "销售税主管机构是收缴需要申报和缴纳的销售税的实体。"
author: twheeloc
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0d8b87e23932ce843791778f65eb77240cc28f4
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-tax-authorities"></a>设置增值税主管机构

[!include[task guide banner](../../includes/task-guide-banner.md)]

销售税主管机构是收缴需要申报和缴纳的销售税的实体。 您可以直接向销售税主管机构支付销售税，也可以通过为销售税主管机构创建的供应商帐户支付。 如果您这样做，公司可以使用其日常付款程序及时向增值税主管机构付款。 如果您没有将增值税主管机构设置为供应商，则某个人必须在相应的到期日期时准备向增值税主管机构手动付款。 本任务使用 USMF 公司进行演示。

1. 转到“纳税”>“间接税”>“销售税”>“销售税主管机构”。
2. 单击“新建”。
3. 在“主管机构”字段中，输入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 为您的国家/地区选择报表版式（如果有）。 如果报表版式不对应于销售税主管机构的要求，请使用默认版式。
9. 在舍入表格和“舍入”字段中输入数字，以指定支付的总税额如何舍入。 所有舍入差额将过帐到总帐中设置的自动交易记录的帐户。
10. 在“舍入”字段中，输入一个数字。
11. 单击“保存”。


