---
title: "定义支出策略"
description: "您可以通过在 Microsoft Dynamics 365 for Finance and Operations 中输入和提交费用报表和出差申请来定义工作人员必须遵守的支出策略。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a>支出策略

[!include[banner](../includes/banner.md)]

您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的政策。         
实施支出策略可以帮助您更有效地管理支出。         

例如，您可为纽约城设置一个酒店费用政策，规定每晚酒店费用不能超过 250 美元。       
如果员工提交的支出报表或出差申请中的房费超过了此金额，系统将通知        
该员工，指出超出了针对支出的政策金额。 在您定义该政策时，可以配置员工        
将收到的消息。      
        
您可以定义策略的三种类型：         
        
- 警告 – 允许工作人员提交费用报表或出差申请，但将为所有审核人和最新报表        
标记该费用。        

- 错误 – 在提交支出报表或出差申请前，要求工作人员修改该费用以符合该政策。       
 
 - 调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出政策金额的调整。        
 
 您还可以为支出政策具有效力的设置日期范围。 例如，在节假日旅行旺季，丹麦      
 和纽约市之间航线的飞机票的价格可能很贵。 您可以定义一个飞行支出规则，      
 将飞往纽约城的成本限制在最高 DKK 5000，并且可以指定此规则在 3 月 15 日      
 和 9 月 15 日之间具有效力。

