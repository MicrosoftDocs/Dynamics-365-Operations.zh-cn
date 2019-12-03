---
title: 应付帐款主页
description: 此主题概要介绍了应付帐款。
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e9fbc0e3f3960f25930f9587d489009bc34181c7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772229"
---
# <a name="accounts-payable-home-page"></a>应付帐款主页

[!include [banner](../includes/banner.md)]

此主题概要介绍了应付帐款。 

您可以手动输入供应商发票或通过数据实体以电子方式接收这些发票。 在输入或接收发票后，可以通过使用发票审核日记帐或**供应商发票**页查看和审核发票。 您可以使用发票匹配、供应商发票策略和工作流来实现审核流程自动化，以便自动审核满足特定条件的发票，并标记其余的发票由得到授权的用户进行审核。

**业务流程**

[![业务流程图](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>设置应付帐款

设置供应商组、供应商、过帐模板、不同的付款选项，并设置涉及供应商、费用、交货和目的地、本票以及其他应付帐款信息类型的参数。 

[配置应付帐款概览](accounts-payable-overview.md)

[会计分配和供应商发票的子分类日记帐条目](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[应付帐款和应收帐款的外币重估](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>配置供应商发票

使用应付帐款可以跟踪对供应商的发票和相关支出。

[发票匹配应付帐款概览](accounts-payable-invoice-matching.md)

[供应商过帐模板](vendor-posting-profiles.md)

[设置发票匹配应付帐款验证](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[三向匹配政策](three-way-matching-policies.md)

[发票匹配和内部公司采购订单](invoice-matching-intercompany-purchase-orders.md)

[解决发票合计匹配期间出现的差异概览](resolve-invoice-totals-invoice-matching-discrepancies.md)

[供应商发票日记帐和发票审核日记帐的默认对方科目](default-offset-accounts-vendor-invoice-journals.md)

[移动发票审核](mobile-invoice-approvals.md)

[供应商协作开票工作区](vendor-portal-invoicing-workspace.md)

[供应商发票自动化](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>配置供应商付款 

将系统定义的付款类型（例如支票、电子付款或本票）分配给任何用户定义的付款方式。 付款类型是可选的，但在以下情况下它们可能会很有用：在您验证电子付款以及必须迅速确定付款使用哪种付款类型时。 

[供应商付款工作区](vendor-payments-workspace.md)

[定义供应商付款费用](tasks/define-vendor-payment-fees.md)

[定义供应商付款期限](tasks/define-vendor-payment-terms.md)

[付款确认概览](positive-pay-overview.md)

[设置和生成付款确认文件](set-up-generate-positive-pay-files.md)

[使用付款方案创建供应商付款](create-vendor-payments-payment-proposal.md)

[部分金额的供应商付款](vendor-payments-partial-amount.md)

[执行高于供应商付款的计算折扣的折扣](take-discount-more-calculated-discount-vendor-payment.md)

[在现金折扣期间之外执行现金折扣](take-cash-discount-outside-cash-discount-timeframe.md)

[电子报告示例供应商支票](electronic-reporting-sample-vendor-checks.md)

[冲销供应商付款](reverse-vendor-payment.md)

[预付款发票与预付款](prepayments-invoices-vs-prepayments.md)

[应付帐款的集中付款](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>结算

以下主题提供有关结算的信息。 结算是使用发票结算付款的流程。 

[配置结算](../cash-bank-management/configure-settlement.md)

[在折扣日期之前结算部分供应商付款并在折扣日期之后完成最后付款](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[结算在供应商贷方通知单上已折扣的部分供应商付款](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[结算具有多个折扣期间的部分供应商付款](settle-partial-vendor-payment-multiple-discount-periods.md)

[在折扣日期之前结算部分供应商付款并完全结算最后付款](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[具有多个客户或供应商记录的单个凭证](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>其他资源

#### <a name="whats-new-and-in-development"></a>新增功能和开发中的功能

转到 [Microsoft Dynamics 365 版本计划](https://go.microsoft.com/fwlink/?linkid=2010158)，了解规划了哪些新功能。 

#### <a name="blogs"></a>博客

您可以在 [Microsoft Dynamics 365 博客](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)和 [Microsoft Dynamics 365 Finance - 财务博客](https://community.dynamics.com/365/financeandoperations/b/financials)上查找有关应付帐款的意见、新闻和其他信息以及其他解决方案。

[Microsoft Dynamics Operations 合作伙伴社区博客](https://community.dynamics.com/partner/b/operationspartnercommunityblog)可为 Microsoft Dynamics 合作伙伴提供了解 MBS Operations 中的新增功能和趋势的单一资源。

#### <a name="community-blogs"></a>社区博客

[如何管理 Dynamics 365 Finance 中的应付款项](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>任务指南
其他帮助在应用程序中作为任务指南提供。 若要访问任务指南，请单击任何页面上的“帮助”按钮。

#### <a name="videos"></a>视频

查看当前在 [Microsoft Dynamics 365 YouTube 频道](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)上提供的操作方法视频。




