---
title: "供应商付款工作区"
description: "此主题提供有关供应商付款工作区的信息。 供应商付款工作区显示与处理供应商付款有关的信息。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.assetid: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: eb46062efed399180a66453c36c1b5de6adbbc23
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-payments-workspace"></a>供应商付款工作区

[!include[banner](../includes/banner.md)]

**供应商付款**工作区显示与处理供应商付款有关的信息。 该工作区包括一个**我的工作**视图和一个**分析**页。 **我的工作**视图显示汇总磁贴、供应商交易记录网格和相关供应商信息。 **分析**页使用 Microsoft Power BI 的功能显示与供应商付款相关的视觉对象。

## <a name="my-work-view"></a>我的工作视图

### <a name="summary-tiles"></a>汇总磁贴

在**汇总**部分的磁贴提供您的付款信息状态的概览。 您可以查看未过帐的付款日记帐、逾期发票、所有供应商以及处于暂停状态的供应商。 从**汇总**部分，可以创建新的付薪周期。

**汇总**部分的信息适用于您登录到的公司。

### <a name="vendor-transactions-grids"></a>供应商交易记录网格

**供应商交易记录**部分包含显示逾期发票和未结算付款的网格。 从**逾期发票**网格可以查看所选发票的结算历史记录。 从**未结算付款**网格可以查看所选发票的结算历史记录和结算发票。

统一付款人员可以使用出现在各网格顶部的筛选器选择公司。 随后将筛选网格，使其仅显示在统一付款组织层次结构中定义且统一付款职员有权查看的公司。

**供应商交易记录**部分的**查找交易记录**选项卡允许您搜索供应商交易记录。

### <a name="related-information"></a>相关信息

您可以使用工作区的**相关信息**部分中的链接查看**供应商帐龄**报表和**付款汇总(按日期)**报表。

## <a name="analytics-page"></a>分析页

**分析**页提供重要指标，例如逾期的供应商发票和在将来到期的供应商发票。 此页包含九个报表页。 一页提供概览，另外八页提供关于应付账款付款指标的详细信息。

下表显示在每个报表页上可用的可视化项。

| 报表页 | 可视化 |
|-------------|---------------|
| 供应商付款概览 | <ul><li>逾期未付的发票</li><li>今日到期发票</li><li>已采用的折扣到已丢失的折扣</li><li>在现金折扣日期之前将来到期的发票</li><li>在到期日期之前将来到期的发票</li><li>延期付款的发票到按时付款的发票</li><li>付款工作流分配</li><li>供应商到客户余额</li><li>具有付款暂停的未结发票</li></ul> |
| 逾期未付的发票 | <ul><li>逾期未付的发票</li><li>发票逾期明细</li><li>未结发票合计</li><li>逾期发票(按供应商组)</li><li>逾期发票(按公司)</li></ul> |
| 今日到期发票 | <ul><li>今日到期发票</li><li>今日到期发票明细</li><li>今日到期发票(按公司)</li><li>今日到期发票(按供应商组)</li></ul> |
| 已采用的折扣到已丢失的折扣 | <ul><li>已采用的折扣到已丢失的折扣</li><li>已采用的折扣到已丢失的折扣明细</li><li>已采用的折扣到已丢失的折扣(按公司)</li><li>已采用的折扣到已丢失的折扣(按供应商组)</li></ul> |
| 将来到期的发票 | <ul><li>将来到期的发票</li><li>将来到期的发票明细</li><li>将来到期的发票(按公司)</li><li>将来到期的发票(按供应商组)</li><li>在现金折扣日期之前将来到期的发票</li><li>在到期日期之前将来到期的发票</li></ul> |
| 延期付款的发票 | <ul><li>在到期日期后付款的发票</li><li>在到期日期后付款的发票明细</li><li>在到期日期后付款的发票(按公司)</li><li>在到期日期后付款的发票(按供应商组)</li><li>延期付款的发票与按时付款的发票</li></ul> |
| 付款工作流 | <ul><li>供应商付款工作流实例</li><li>供应商付款工作流实例(按审批人)</li><li>供应商付款工作流实例(按公司)</li><li>工作流中的平均天数(按审批人)</li></ul> |
| 供应商到客户余额 | <ul><li>供应商到客户余额</li><li>供应商到客户余额(按公司)</li><li>供应商到客户余额明细</li></ul> |
| 具有付款暂停的发票 | <ul><li>具有付款暂停的发票</li><li>具有付款暂停的发票明细</li><li>具有付款暂停的发票(按公司)</li><li>具有付款暂停的发票(按供应商组)</li></ul> |

