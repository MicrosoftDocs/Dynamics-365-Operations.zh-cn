---
title: 结算客户的远期支票
description: 该支票由银行清算后，您可以结算过期支票。
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780007"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>结算客户的远期支票

[!include [banner](../../includes/banner.md)]

该支票由银行清算后，您可以结算过期支票。 此财务交易记录也清算了过期支票的过桥科目交易记录。 

在开始此任务之前，必须完成以下任务：

1) 设置远期支票

2) 为客户登记和过帐远期支票 



此任务指南的角色是出纳员。



该程序适用于 USMF 演示公司。

1. 转到 **信用和收款 > 查询和报表 > 付款 > 客户远期支票**。
2. 单击 **结算**。
3. 单击 **结算清算条目**。
    * 结算用于支票交易记录的客户帐户。  
4. 关闭该页面。
5. 转到 **总帐 > 日记帐条目 > 普通日记帐**。
6. 在 **显示** 字段中，选择一个选项。
7. 选择或清除 **仅显示用户创建项** 复选框。
8. 在列表中，找到并选择所需记录。
9. 单击 **行**。
10. 单击 **凭证**。
11. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
