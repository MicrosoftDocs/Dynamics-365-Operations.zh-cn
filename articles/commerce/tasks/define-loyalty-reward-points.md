---
title: 定义会员奖励分
description: 此程序会逐步演示如何定义会员奖励积分。
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
ms.search.form: RetailLoyaltyRewardPoints
ms.openlocfilehash: 9acd1429d17393f19a5e059b90a48b0b103535d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268884"
---
# <a name="define-loyalty-reward-points"></a>定义会员奖励分

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何定义会员奖励积分。 在设置会员计划之前，您应设置会员奖励积分。 此程序使用 USRT 演示数据公司。

1. 转至“Retail 和 Commerce”>“客户”>“会员”>“会员奖励积分”。
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
