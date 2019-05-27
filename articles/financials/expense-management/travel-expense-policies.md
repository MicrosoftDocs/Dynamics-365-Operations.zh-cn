---
title: 定义支出策略
description: 您可以在 Microsoft Dynamics 365 for Finance and Operations 中定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出政策。
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514431"
---
# <a name="expense-policies"></a>支出策略

[!include [banner](../includes/banner.md)]

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

# <a name="policy-tips"></a>政策提示
下面是一些在为费用管理新建政策时可以帮助您的建议。 
* 政策有生效日期，如果创建政策时不为其设置费用产生后的日期，政策不会生效。 例如，如果今天创建新政策以实施最大餐费 50 美元，则不会针对此政策检查截止昨天的任何现有费用。
* 为可明细化的费用类别创建政策时，请考虑为费用行类型添加条件。 某些政策（如索取收据）可能对明细化行无意义，只应该应用于标题行或非明细化行。 

# <a name="when-to-evaluate-policies"></a>何时评估政策

费用管理参数中有一个选项，用于在保存行时或在提交费用报表时评估费用管理政策。 如果选择在保存行时评估，这将确保用户可以查看需要执行哪些操作才能一次性完成所有费用报表。 否则，如果要在结束时向工作流提交期间进行验证，可以推迟政策评估并节约时间。
