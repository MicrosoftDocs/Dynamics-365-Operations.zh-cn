--- 
title: "创建、计算和过帐零售商店的报表"
description: "此程序会逐步演示如何手动创建、计算和过帐某一商店的报表。"
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>创建、计算和过帐零售商店的报表

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序会逐步演示如何手动创建、计算和过帐某一商店的报表。 还可以配置相同任务的批处理作业。 配置和运行批处理作业的步骤可以在其他主题中找到。 要完成此程序，您必须在 POS 中有已完成的交易，让后将其拉到 Dynamics AX 中。 此记录使用 USRT 演示数据公司。 此过程可能涉及 Microsoft Dynamics AX。 请注意，Dynamics AX 现在称为 Microsoft Dynamics 365 for Operations。

1. 转至“所有工作区”> >“零售商店财务”。
2. 单击“新建报表”。
3. 在“商店编号”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击所选行中的链接。
5. 单击“确定”。
    * “设置组”中的设置可以控制报表包括哪些交易记录，以及这些交易记录如何分组到报表行。 您可以打开“设置组”并更改这些设置，也可以使用默认设置。  
    * “报表方法”字段定义了报表行如何分组。  
    * 如果您仅想要针对某个职员或收银机计算报表，请选择特定的职员或收银机。  
6. 在“结算方法”字段中，选择一个选项。
7. 单击“计算报表”。
8. 单击“是”。
    * 计算完报表之后，应出现使用所用的每种付款方式和报表方法的总金额创建的行。  
    * 如果需要输入或更新金额，在每一行输入已盘点金额。 使用 POS 中完成的清偿申报金额填充已盘点字段。  
9. 单击“将报表过帐”。
10. 单击“关闭”。
11. 转至“零售和商业”>“渠道”>“零售商店财务”。
12. 单击“已过帐的报表”选项卡。


