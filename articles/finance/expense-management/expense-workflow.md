---
title: 费用工作流
description: 此主题介绍如何使用 Microsoft Dynamics 365 Finance 中的工作流系统在费用管理中设置费用报表审核流程。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52915860709e38013ec06204c52bb06de417eb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187582"
---
# <a name="expense-workflow"></a>费用工作流

[!include [banner](../includes/banner.md)]

可使用工作流系统设置“费用管理”中支出报表的审核流程。 您可以设置使用以下条件确定由谁审核费用报表的工作流：

- 员工报告层次结构和预定义的审核限制
- 支持临时审核人和最终审核人的多级审核
- 财务维度和项目责任
- 给特定用户或用户组的分配

工作流审核可为费用报表、出差申请、预付现金和增值税 (VAT) 还原而创建。

**示例**

以下流程是针对某一支出报表的出差费用管理工作流程示例。

1. 员工创建和保存支出报表。
2. 员工提交支出报表以供审核。 审核人根据工作流设置后定义的规则标识。
3. 审核人接收费用报表可供审核的通知。 审核人审核支出报表并验证是否满足以下条件：

    - 费用不违反任何费用策略。 如果费用违反策略，审核人验证费用报表中是否包括有效的业务理由。
    - 电子收据是否附加到支出报表。

4. 审核人审核整个支出报表。
5. 将费用报表分配给应付账款协调员以供过帐。
6. 发生以下步骤之一，具体取决于是否配置自动过帐：

    - 如果配置自动过帐，则对费用报表进行付款处理，并且更新费用报表的状态。
    - 如果没有配置自动过帐，应付账款协调员验证所有原始收据已提交，并且收货与费用报表上的成本相符。 还必须验证费用报表上的所有税码是否正确。

在验证这些需求后，将支出报表过帐。

在费用报表过帐后，对费用报表授权付款，并且员工获得补偿。
