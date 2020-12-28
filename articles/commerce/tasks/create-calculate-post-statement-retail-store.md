---
title: 创建、计算和过帐零售商店的对帐单
description: 本主题介绍如何手动创建、计算和过帐某一商店的报表。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f1b0a34205e192957405bc9d298c45c8bb4d25
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410540"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>创建、计算和过帐零售商店的对帐单

[!include [banner](../includes/banner.md)]

本主题介绍如何手动创建、计算和过帐某一商店的报表。 还可以配置相同任务的批处理作业。 配置和运行批处理作业的步骤可以在其他主题中找到。 要完成此过程，您必须在 POS 中有已完成的交易，让后将其拉到 Dynamics 365 Commerce 中。 此记录使用 USRT 演示数据公司。

1. 从主页选择 **商店财务**。
2. 选择 **新建报表**。
3. 在 **商店编号** 字段中，从下拉列表中选择一个选项。
4. 选择 **确定**。
5. **设置** 组中的设置可以控制报表包括哪些交易记录，以及这些交易记录如何分组到报表行。 您可以打开 **设置** 组并更改这些设置，也可以使用默认设置。  
    - **报表方法** 字段定义了报表行如何分组。  
    - 如果您仅想要针对某个职员或收银机计算报表，请在 **职员/收银机** 字段中选择特定的职员或收银机。  
6. 在 **结算方法** 字段中，选择一个选项。
7. 从操作窗格选择 **计算报表**。
8. 选择 **是**。
    - 计算完报表之后，应出现使用所用的每种付款方式和报表方法的总金额创建的行。  
    - 如果需要输入或更新金额，在每一行输入已盘点金额。 使用 POS 中完成的清偿申报金额填充已盘点字段。  
9. 从操作窗格选择 **过帐报表**。
10. 选择 **关闭**。
11. 关闭该窗格。
12. 在主页选择 **商店财务**。
13. 选择 **已过帐的报表** 选项卡。

