---
title: "总帐和财务报表主页"
description: "使用总帐定义和管理法人的财务记录。"
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2177110dc16528de7eddedb0667faae553a36b12
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="general-ledger"></a>总帐 

[!include [banner](../includes/banner.md)]

使用总帐定义和管理法人的财务记录。 总帐是借方和贷方登记条目。 这些条目进行分类使用在会计科目表中列出的科目。 

 - [计划您的会计科目表](plan-chart-of-accounts.md)
 - [主科目类型](main-account-types.md)

分配是基于分配规则将金额分配到一个或多个帐户或帐户/维度组合的过程。 存在两种类型的分配：固定和可变。 您还可以在结算会计科目之间的交易记录和重估原币金额。 在某一会计年度结束时，您必须为下一会计年度准备您的科目，并且关闭当前会计年度。 您可以使用合并功能以合并若干子公司的财务结果为唯一的合并公司的财务结果。 这些子公司可以存在于相同的 Microsoft Dynamics 365 for Finance and Operations 数据库中或在单独的数据库中。

- [合并和清除概览](../budgeting/consolidation-elimination-overview.md)
- [总帐科目余额](general-ledger-account-balances.md)
- [财务维度](financial-dimensions.md)

[![业务流程](./media/GL-process.PNG)](./media/GL-process.PNG)

## <a name="sales-tax"></a>销售税
每个公司都需要向各种税务主管机构缴纳税款。 规则和比率根据国家/地区、省/市/自治区、县和城市而改变。
此外，当税务主管部门更改它们的要求时，必须定期更新规则。 增值税代码包含您收取以及支付给主管机构的金额数的信息。 当您设置增值税代码时，您定义了必须收取的金额或百分比。 您还定义了将这些金额或百分比应用到交易记录金额中的各种方法。 本节中的主题提供了如何针对您的税务主管机构要求的方法和比率设置增值税的信息。

 - [销售税概览](indirect-taxes-overview.md)
 - [基于“边际基数”和“计算方法”的销售税比率](marginal-base-field.md)
 - [销售税支付和舍入规则](round-sales-tax-payments.md)


## <a name="additional-resources"></a>其他资源

### <a name="whats-new-and-in-development"></a>新增功能和开发中的功能

转到 [Microsoft Dynamics 365 路线图](https://roadmap.dynamics.com/)以了解已发布和正在开发的新功能。 

### <a name="blogs"></a>博客

您可以在 [Microsoft Dynamics 365 博客](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)上查找有关应付账款的意见、新闻和其他信息以及其他解决方案。

[Microsoft Dynamics AX 产品团队博客](https://blogs.msdn.microsoft.com/dax/)上有很多有关总帐的帖子。 尽管一些文章是针对总帐的旧版本编写的，但相同的概念仍适用，并且过程在当前版本中也是相似的。

[Microsoft Dynamics Operations 合作伙伴社区博客](https://community.dynamics.com/partner/b/operationspartnercommunityblog)可为 Microsoft Dynamics 合作伙伴提供了解 MBS Operations 中的新增功能和趋势的单一资源。

### <a name="task-guides"></a>任务指南
其他帮助在 Finance and Operations 中作为任务指南提供。 若要访问任务指南，请单击任何页面上的“帮助”按钮。

### <a name="videos"></a>视频

查看当前在 [Microsoft Dynamics 365 YouTube 频道](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)上提供的操作方法视频。


