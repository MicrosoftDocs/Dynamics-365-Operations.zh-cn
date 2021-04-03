---
title: 总帐和财务报表概览
description: 使用总帐定义和管理法人的财务记录。
author: ShylaThompson
manager: AnnBe
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3fc00cc29e37c853d7cabfa928d8e069c40a581
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249183"
---
# <a name="general-ledger-home-page"></a>总帐主页

[!include [banner](../includes/banner.md)]

使用总帐定义和管理法人的财务记录。 总帐是借方和贷方登记条目。 这些条目进行分类使用在会计科目表中列出的科目。 

 - [计划您的会计科目表](plan-chart-of-accounts.md)
 - [主科目类型](main-account-types.md)

分配是基于分配规则将金额分配到一个或多个帐户或帐户/维度组合的过程。 存在两种类型的分配：固定和可变。 您还可以在结算会计科目之间的交易记录和重估原币金额。 在某一会计年度结束时，您必须为下一会计年度准备您的科目，并且关闭当前会计年度。 您可以使用合并功能以合并若干子公司的财务结果为唯一的合并公司的财务结果。 这些字公司可以存在于相同的数据库中或在单独的数据库中。

- [合并和清除概览](../budgeting/consolidation-elimination-overview.md)
- [总帐科目余额](general-ledger-account-balances.md)
- [财务维度](financial-dimensions.md)

[![业务流程](./media/GL-process.PNG)](./media/GL-process.PNG)

## <a name="sales-tax"></a>销售税
每个公司都需要向各种税务主管机构缴纳税款。 规则和比率根据国家/地区、省/市/自治区、县和城市而改变。
此外，当税务主管部门更改它们的要求时，必须定期更新规则。 增值税代码包含您收取以及支付给主管机构的金额数的信息。 当您设置增值税代码时，您定义了必须收取的金额或百分比。 您还定义了将这些金额或百分比应用到交易记录金额中的各种方法。 本节中的主题提供了如何针对您的税务主管机构要求的方法和比率设置增值税的信息。

 - [销售税概览](indirect-taxes-overview.md)
 - [基于“边际基数”和“计算方法”的销售税比率](marginal-base-field.md)
 - [销售税支付和化整规则](round-sales-tax-payments.md)


## <a name="additional-resources"></a>其他资源

#### <a name="whats-new-and-in-development"></a>新增功能和开发中的功能

转到 [Microsoft Dynamics 365 版本计划](https://go.microsoft.com/fwlink/?linkid=2010158)，了解已经规划了哪些新功能。 

#### <a name="financial-reporting"></a>财务报告
转到 [Financial reporting 概述](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)主题，了解有关财务报表的信息。

#### <a name="blogs"></a>博客

您可以在 [Microsoft Dynamics 365 博客](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)和 [Microsoft Dynamics 365 Finance and Operations - 财务博客](https://community.dynamics.com/365/financeandoperations/b/financials)上查找意见、新闻和其他信息。

[Microsoft Dynamics Operations 合作伙伴社区博客](https://community.dynamics.com/partner/b/operationspartnercommunityblog)可为 Microsoft Dynamics 合作伙伴提供了解 Dynamics 365 中的新增功能和趋势的单一资源。

### <a name="videos"></a>视频

查看当前在 [Microsoft Dynamics 365 YouTube 频道](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)上提供的操作方法视频。

#### <a name="community-blogs"></a>社区博客

- [Dynamics 365 for Finance and Operations 中应该了解的分类帐信息](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]