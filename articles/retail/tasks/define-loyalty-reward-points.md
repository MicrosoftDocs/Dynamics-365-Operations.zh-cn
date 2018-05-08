--- 
title: "定义会员奖励分"
description: "此程序会逐步演示如何定义会员奖励积分。"
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 26b5615df427fb01cc4a1764507fbaa11bf0d7a0
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="define-loyalty-reward-points"></a>定义会员奖励分

[!include [task guide banner](../includes/task-guide-banner.md)]

此程序会逐步演示如何定义会员奖励积分。 在设置会员计划之前，您应设置会员奖励积分。 此程序使用 USRT 演示数据公司。

1. 转至“零售和商业”>“客户”>“会员”>“会员奖励积分”。
2. 单击“新建”。
3. 在“奖励积分 ID”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“奖励积分类型”字段中，选择一个选项。
    * 如果您想要将奖励积分舍入到最近的整数，请选择“数量”。 如果您想要根据币种舍入规则对奖励积分进行舍入，请选择“金额”。 如果您选择“数量”，请跳过此程序的下一步。  
6. 在“货币”字段中，键入一个值。
    * 对于金额类型奖励积分，发放的所有积分都将拥有选定的币种。 对于数量类型奖励积分，此字段不适用，跳过此步骤。  
7. 选中或取消选中“可兑换”复选框。
8. 在“兑换排名”字段中，输入一个数字。
    * 在两个或多个可兑换的奖励积分可用于支付产品货款时，使用兑换排名。 如果两个奖励积分拥有相同的兑换排名，则使用需要较少积分数的奖励积分。  
9. 在“到期时间值”字段中，输入一个数字。
    * 奖励积分将在积分发放的指定天数、月数或年数之后过期。 值为“0”意味着会员奖励积分将永不过期。  
10. 在“到期时间单位”字段中，选择一个选项。
11. 单击“保存”。


