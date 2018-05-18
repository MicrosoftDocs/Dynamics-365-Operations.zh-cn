--- 
title: "处理付款返利"
description: "该过程说明如何将已批准和处理的客户返利转换到贷方通知单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a>处理付款返利

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程说明如何将已批准和处理的客户返利转换到贷方通知单。 您可以使用 USMF 公司演示运行此指南。 本指南中的先决条件是拥有一个或多个状态为“标记”的要求。 如果您正在使用 USMF，在开始本指南之前，您应该运行“生成和处理客户返利”指南。


## <a name="convert-rebate-claims-to-credit-note"></a>将返利要求转换为贷方通知单
1. 转到“所有客户”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 在“操作窗格”上，单击“收款”。
5. 单击“结算交易记录”。
6. 单击“功能”。
7. 单击“返利计划”。
    * “返利”页面会列示您已在客户返利工作台中处理，且状态为标记的返利要求。    
8. 单击“编辑”。
    * 根据您想要包括在贷方通知单中的要求，设置“标记”字段中的核取标志。   
9. 单击“功能”。
10. 单击“创建贷方通知单”。
    * 一条消息会显示，以通知您某一日记帐已过帐（这是“应收账款参数”页中明确指出的“应收账款耗损日记帐”)。 这会导致实际负债（贷方）金额被移到客户余额。 这意味着，客户的帐户已被记入贷方，“返利”应计项目帐户已被记入借方。  
11. 关闭该页面。
12. 单击“取消”。
    * 这会刷新页面，以便您可以查看更新。  
13. 在“操作窗格”上，单击“收款”。
14. 单击“结算交易记录”。
    * 请注意，负数金额的交易记录（表示总返利金额，而无发票参考编号）已被添加到客户余额。   
15. 单击“取消”。


