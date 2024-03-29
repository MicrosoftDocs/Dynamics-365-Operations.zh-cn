---
title: 为供应商登记和过帐远期支票
description: 在通过使用日记帐凭证给供应商签发支票之前，先注册远期支票的详细信息。
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 312f7c58352e3cb86c22f8c34b1b6c11456c0083
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779414"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a>为供应商登记和过帐远期支票

[!include [banner](../../includes/banner.md)]

在通过使用日记帐凭证给供应商签发支票之前，先注册远期支票的详细信息。 您还可以过帐该远期发票并生成财务交易记录。 在注册并过帐远期支票给供应商之前，请完成以下任务： 

在 **现金和银行管理** 页设置远期支票。 

此任务指南的角色是出纳员。 此任务使用 USMF 公司演示。

1. 转到 **应付帐款 > 付款 > 付款日记帐**。
2. 单击 **新建**。
3. 在 **名称** 字段中，键入“VendPay”。
4. 单击 **行**。
5. 在 **帐户** 字段中，指定所需值。
6. 在列表中，标记所选的行。
7. 在 **借方** 字段中，输入一个数值。
8. 在 **付款方式** 字段中，单击下拉按钮以打开查找。
    * 选择远期支票的付款方式。  
9. 在列表中，找到并选择所需记录。
10. 在列表中，单击所选行中的链接。
11. 单击 **远期支票** 选项卡。
12. 在 **支票编号** 字段中，键入一个值。
    * 输入或更改远期支票的数目。  
13. 在 **开证银行名称** 字段中，键入一个值。
    * 输入签发银行的银行详细资料。  
14. 单击 **列表** 选项卡。
15. 单击 **过帐**。
16. 关闭该页面。
17. 单击“远期支票”选项卡。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
