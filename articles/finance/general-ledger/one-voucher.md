---
title: 一个凭证
description: 财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的一个凭证让您可以在单个凭证的上下文中输入多个子分类帐交易记录。
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 233f31bd0b20ad5dd8ba21077797dd2f65069deb
ms.sourcegitcommit: bc6db23825c94cd8305ef37bc18296765e9ce8a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2019
ms.locfileid: "2810691"
---
# <a name="one-voucher"></a>一个凭证

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>什么是“一个凭证”？

财务日记帐（普通日记帐、固定资产日记帐、供应商付款日记帐等）的这个现有功能让您可以在单个凭证的上下文中输入多个子分类帐交易记录（客户、供应商、固定资产、项目和银行）。 Microsoft 将此功能称为*一个凭证*。 可以使用以下方法之一来创建一个凭证：

- 设置日记帐名称（**总帐** \> **日记帐设置** \> **日记帐名称**），以便**新凭证**字段设置为**仅一个凭证号**。 您添加到日记帐的各行现在都包括在同一凭证中。 因此，凭证可以作为多行凭证、同一行上的科目/对方科目或组合输入。

    [![单行](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > “一个凭证”的定义**不**包括日记帐名称设置为**仅一个凭证号**，但用户随后输入仅包含会计科目类型的凭证的情况。 在本主题中，“一个凭证”意味着有单个凭证包含多个供应商、客户、银行、固定资产或项目。

- 输入没有对方科目的多行凭证。

    [![多行凭证](./media/Multi-line.png)](./media/Multi-line.png)

- 输入科目和对方科目都包含子分类帐科目类型（如**供应商**/**供应商**、**客户**/**客户**、**供应商**/**客户**或**银行**/**银行**）的凭证。

    [![子分类帐凭证](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>一个凭证存在的问题

“一个凭证”功能会在结算、纳税计算、交易记录冲销、子分类帐与总帐的对帐、财务报告等期间导致问题。 （有关结算期间可能发生的问题的详细信息，请参阅如[具有多个客户或供应商记录的单个凭证](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records)。）为了正确工作和报告，这些流程和报告需要交易记录明细。 尽管取决于您的组织的设置，某些可能方案仍能正确工作，但当在一个凭证中输入多个交易记录时通常会有问题。

例如，您过帐以下多行凭证。

[![示例](./media/example.png)](./media/example.png)

然后您在**财务见解**工作区生成**按供应商分类的费用**报表。 在此报表中，支出帐户余额按供应商组然后按供应商分组。 当生成报表时，系统不能确定哪些供应商组/供应商发生了 250.00 费用。 因为交易记录明细缺少，系统假定所有 250.00 费用是由在凭证中找到的第一个供应商产生。 因此，250.00 费用（包含在主科目 600120 的余额中）显示在该供应商组/供应商下。 但是，凭证中的第一个供应商很有可能不是正确的供应商。 因此，报表可能不正确。

[![支出](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>一个凭证的未来

由于之前所提到的问题，“一个凭证”功能将被废弃。 但是，因为存在依赖此功能的功能空白，此功能不会一次全部废弃。 而是使用以下计划：

- **2018 年春季发布** – 默认情况下，该功能将通过**总帐参数**页的**常规**选项卡上的**一个凭证可以允许多个交易记录**参数默认关闭。 但是，如果您的组织有属于本主题后面列出的功能空白之一的方案，您可以打开此功能。

    - 如果客户的业务方案不需要一个凭证，他们不应打开此功能。 如果使用此功能，即使存在另一种解决方案，Microsoft 也不会修复本主题后面确定的区域的 "bug"。
    - 除非需要使用一个凭证来填补其中一个功能空白，否则请停止使用此功能来集成。

- **以后发布** – 将填补所有功能空白。 **在填补功能空白并提供新功能后，在关闭“一个凭证”之前至少还会留有一年时间**，因为客户和独立软件供应商 (ISV) 必须有足够的时间来对新功能作出反应。 例如，他们可能必须更新其业务流程、实体和集成。

> [!IMPORTANT]
> 日记帐名称设置中尚**未**移除**仅一个凭证号**选项。 凭证仅包含会计科目类型时，仍然支持此选项。 客户在使用此设置时应小心谨慎，因为如果使用**仅一个凭证号**选项，但随之输入多个客户、供应商、银行、固定资产或项目，则该凭证将不过帐。 而且，客户仍然可以在包含**供应商**/**银行**科目类型的单个凭证内输入子分类帐科目类型，如付款。

## <a name="why-use-one-voucher"></a>为何使用一个凭证？

基于与客户的对话，Microsoft 汇编了客户使用一个凭证功能或使用原因的以下场景列表。 这些业务要求中有一些只能使用一个凭证满足。 但是，对于很多场景，替代方案即可以满足同一业务要求。

### <a name="scenarios-that-require-one-voucher"></a>需要一个凭证的场景

以下场景只能使用一个凭证功能完成。 如果您的组织遇到这些场景案中的任何一个，您必须启用要在凭证中输入的多个交易记录，方法是更改**总帐参数**页上**一个凭证可以允许多个交易记录**参数的设置。。 这些功能空白将通过以后发布的其他功能填补。

> [!Note]
> [对于以下每个场景，必须在**总帐参数**页面上的**常规**快速选项卡中将**一个凭证可以允许多个交易记录**设置为“是”。]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>将汇总窗体中的供应商或客户付款过帐到银行帐户

**场景**组织将供应商和金额列表传达给银行，银行使用此列表代表组织向供应商付款。 银行通过银行帐户的单次提款形式过帐付款总额。

仅通过一个凭证支持供应商付款的汇总。 每个供应商输入为一个单独行以在应付帐款子分类帐中维护详细信息。 不过，所有付款的汇总金额将冲销到银行帐户的一个行。 因此，提款在银行子分类帐中显示为单个汇总金额。

**场景**组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。

客户付款的汇总通常通过存款功能来支持。 但是，如果您在付款方式中使用“过渡”，此场景只通过一个凭证来支持。 客户付款的输入方式与所述的供应商付款汇总相同。

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>用于分组业务事件交易记录的机制

**场景**组织有触发多个交易的单个业务事件。 不过，会计部门希望同时查看会计条目以提高可审计性。

如果组织必须同时查看业务事件的会计条目，则必须使用一个凭证。 

### <a name="country-specific-features"></a>特定于国家/地区的功能

**场景**波兰的欧共体统一单证 (SAD) 功能当前要求使用单一凭证。 在分组选项可用于此功能前，您必须继续使用“一个凭证”功能。 可能还有其他一些特定于国家/地区的功能需要“一个凭证”功能。

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>在多个“行”有税款的客户预付款付款日记帐

在此场景中，因为此交易记录模拟客户订单的行，单个凭证中的客户为同一客户。 预付款必须在单个凭证中输入，因为税金计算必须在客户支付的单个付款的行中进行。

### <a name="customer-reimbursement"></a>客户偿还

**场景**客户进行订单的预付款，并且订单的行具有必须为预付款记录的不同税。 预付款客户付款是一个模拟订单行的交易记录，因此，相应的税可为每一行的金额记录。

如果“偿还”定期任务从应收帐款模块运行，它将创建将余额从客户移至供应商的交易记录。 对于此场景，“一个凭证”必须用于偿还客户。

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>固定资产维护：采纳折旧、拆分资产、计算处置折旧
以下固定资产交易记录还在单个凭证中创建多个交易记录：

- 对资产进行其他购置，以及计算“采纳”折旧。
- 拆分资产。
- 计算处置折旧的参数打开，然后处置资产。
- 资产的服务日期在购置日期之前。 因此，折旧调整将过帐。

> [!Note]
> 输入交易记录时，请确保所有交易记录都适用于同一固定资产。 如果凭证包含多个固定资产，凭证不会过帐，即使在总帐的**日记帐名称**页面上将**新凭证**字段设置为“仅一个凭证号”。 如果凭证中包含多个固定资产，则会显示消息**每个凭证只能有一个固定资产交易记录**，您将无法过帐凭证。  

### <a name="bills-of-exchange-and-promissory-notes"></a> 汇票和本票
汇票和本票需要使用“一个凭证”，因为交易记录根据付款状态将客户或供应商余额从一个应收帐款/应付帐款会计科目移至另一个。

## <a name="scenarios-that-dont-require-one-voucher"></a>不需要一个凭证的场景

以下场景可以通过其他方法完成，不应使用“一个凭证”功能。

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>将汇总窗体中的客户付款过帐到银行帐户

组织存入客户付款或银行代表组织存入客户付款，存款在银行帐户中显示为总计。

不在付款方式中使用“过渡”时，通过存款功能支持客户付款的汇总。

### <a name="netting"></a>净额结算

在净额结算中，因为供应商和客户是同一方，供应商和客户的余额根据彼此进行净额结算。 此方法可以最小化组织和客户/供应商当事方之间的货币交换。

净额结算可以通过在单独凭证中输入增加和减少，然后过帐冲销以清算会计科目来完成。

### <a name="post-in-summary-to-the-general-ledger"></a>汇总过帐到总帐

组织通常想要过帐到汇总窗体中的总帐以最小化数据量。 但是，这些组织通常仍需要维护交易记录明细。 在通过单个凭证在汇总窗体中完成过帐时，交易记录明细未知且无法维护。

- 因为交易记录明细当前不能维护，我们建议组织**不要**使用“一个凭证”在汇总窗体中过帐。
- 删除一个凭证支持后，原始凭证和会计框架可以在日记帐中实现。 这些框架然后将维护交易记录明细并支持汇总到总帐。


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>将多项未过帐付款结算到同一发票

此场景通常在客户可以使用多种付款方式支付采购的零售组织中遇到。 在此场景中，组织必须可以记录多个未过帐付款并对照客户发票进行结算。

Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月）中添加的新功能支持对照单个发票结算多个未过帐的付款。 不必再在单个凭证中输入多个客户付款。

### <a name="import-bank-statement-transactions"></a>导入银行对帐单交易记录

银行经常代表组织支付和接收付款，这些交易记录通过从银行收到的文件记录在 Finance 中。 组织通常希望在文件中使用银行对帐单编号将这些交易记录分组到一起。 由于每个交易记录都在银行对帐单中详细显示，银行子分类帐中不需要进行汇总。

交易记录可以使用日记帐中的其他字段分组，例如日记帐批处理号或单据编号。


### <a name="transfer-balances"></a>转移余额

组织可能必须将一个供应商的余额转账给其他供应商，或者由于错误，或者因为其他供应商接收了负债。 此类型转账对于如**客户**和**银行**等科目类型也会发生。

将余额从一个帐户（供应商、客户、银行等）转账到其他帐户可以通过单独的凭证完成，并且可以过帐冲销来清算会计科目。

### <a name="enter-beginning-balances"></a>输入期初余额

组织通常作为一个凭证交易记录输入子分类帐科目（供应商、客户、固定资产等）的期初余额。 每个子分类帐科目的期初余额可以输入为单独的凭证，并且可以过帐冲销来清算会计科目。

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>更正过帐的客户或供应商单据的会计条目

组织可能必须更正已过帐发票的会计条目的应收帐款或应付帐款会计科目，但该发票不能通过其他机制冲销或更正。

如果必须对应收帐款或应付帐款会计科目进行更正，必须直接对该会计科目进行调整。 调整不能由通过供应商或客户的过帐进行。 此方法要求调整在“停机”期间进行，以便会计科目可以暂时允许手动输入。

### <a name="the-system-allows-it"></a>系统允许使用

组织使用“一个凭证”功能经常只是因为系统允许他们使用，而不了解影响。