---
title: 过帐模板的建议做法
description: 本文介绍了用于配置过帐模板的建议做法。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849893"
---
# <a name="recommended-practices-for-posting-profiles"></a>过帐模板的建议做法

在系统中配置过帐模板时，您应遵循一些建议的做法。 本文介绍了不同的方案和相应的建议做法。

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>设置“不允许手动输入”标志

在 **主科目** 页面上，应为用于过帐模板的任何主科目选中 **不允许手动输入** 复选框。 此设置会阻止用户将日记帐条目手动过帐到主科目。 因此，它有助于确保子分类帐与总帐保持平衡，并帮助简化对帐流程。

如果需要对由系统控制并自动过帐的科目进行调整，您可以使用以下方法之一：

- 创建可在其中过帐调整的次要主科目。 然后，使用财务报表上的“合计科目”或特殊行将科目组合在一起并进行合计。
- 冲销相应子分类帐中的原始交易，进行任何必需的更正，然后通过同一子分类帐重新过帐交易。

## <a name="changing-posting-profiles-after-transactions-exist"></a>存在交易后更改过帐模板

如果在存在交易后更改过帐模板，则对帐可能会失败，并且您的子分类帐和分类帐可能变得不平衡。 一般情况下，我们建议您 **不要** 在存在交易后更改过帐模板。

如果需要更改，请使用以下准则来帮助确保系统的完整性：

- 在期间结束过程中进行更改。
- 在系统中未发生其他交易时进行更改。
- 在进行更改之前和之后验证分类帐并将其与子分类帐对帐。
- 如果更改过帐模板，则不会更新已过帐的交易。 请仔细考虑更改是否需要任何调整条目。
- 如果您要更改库存过帐模板，请考虑这些更改将如何影响您的现有库存和分类帐余额。 某些更改可能需要将库存恢复到 0（零）、关闭库存，然后在进行更改后将重新引入库存。
- 在生产中进行更改之前，请始终在非生产环境中测试您的更改。

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>使用数据库日志记录审核对过帐模板所做的更改

考虑为控制过帐的每个过帐模板和参数表设置数据库日志记录。 然后，如果更改了参数或模板，则您将有一个完整审计记录，其中记录了更改了什么值、谁更改了值、何时更改了值以及上一个值是什么。 在对帐过程中，此信息可能至关重要，您的审核员可能需要支持文档。

有关详细信息，请参阅[配置数据库日志记录](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md)。

将下表用作与过帐模板和相关过帐参数有关的常见表名称的参考。

| 页面名称 | 导航路径 | 表名 |
|-----------|-----------------|------------|
| 应付帐款参数 | 应付帐款 &gt; 设置 &gt; 应付帐款参数 | VendParm |
| 供应商过帐模板 | 应付帐款 &gt; 设置 &gt; 供应商过帐模板 | VendPosting |
| 费用代码 | 应付帐款 &gt; 费用设置 &gt; 费用代码或应收帐款 &gt; 费用设置 &gt; 费用代码 | MarkupTable |
| 付款方式 | 应付帐款 &gt; 付款设置 &gt; 付款方式 | VendPaymMode |
| 现金折扣 | 应付帐款 &gt; 付款设置 &gt; 现金折扣或应收帐款 &gt; 付款设置 &gt; 现金折扣 | CashDisc |
| 付款费用（供应商） | 应付帐款 &gt; 付款设置 &gt; 付款费用 | VendPaymFee |
| 应收帐款参数 | 应收帐款 &gt; 设置 &gt; 应收帐款参数 | CustParm |
| 客户过帐模板 | 应收帐款 &gt; 设置 &gt; 客户过帐模板 | CustPosting |
| 付款方式 | 应收帐款 &gt; 付款设置 &gt; 付款方式 | CustPaymMode |
| 付款费用（客户） | 应收帐款 &gt; 付款设置 &gt; 付款方式 | CustPaymFee |
| 资产租赁参数 | 资产租赁 &gt; 设置 &gt; 资产租赁参数 | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| 银行帐户 | 现金和银行管理 &gt; 银行帐户 &gt; 银行帐户 | BankAccountsTable |
| 银行交易记录类型 | 现金和银行管理 &gt; 设置 &gt; 银行交易类型 | BankTransType |
| 清除规则 | 合并 &gt; 设置 &gt; 清除规则 | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| 支出类别 | 费用管理 &gt; 设置 &gt; 普通 &gt; 费用类别 | ProjCategories |
| 固定资产参数 | 固定资产 &gt; 设置 &gt; 固定资产参数 | AssetParameters |
| 固定资产过帐模板 | 固定资产 &gt; 设置 &gt; 固定资产过帐模板 | AssetLedgerAccounts<br>AssetDisposalParameters |
| 币种重估帐户 | 总帐 &gt; 货币 &gt; 币种重估科目 | CurrencyLedgerGainLossAccount |
| 自动交易记录帐户 | 总帐 &gt; 过帐设置 &gt; 自动交易科目 | LedgerSystemAccounts |
| 内部公司 | 总帐 &gt; 过帐设置 &gt; 内部公司科目 | LedgerIntercompany |
| 交易记录过帐定义 | 总帐 &gt; 过帐设置 &gt; 交易过帐定义 | JournalizingDefinitionTrans |
| 过帐定义 | 总帐 &gt; 过帐设置 &gt; 过帐定义 | JournalizingDefintion |
| 过帐（库存） | 库存管理 &gt; 设置 &gt; 过帐 &gt; 过帐 | InventPosting |
| 成本类型代码 | 到岸成本 &gt; 成本计算设置 &gt; 成本类型代码 | ITMCostTypeTable |
| 资源 | 生产控制 &gt; 设置 &gt; 资源 &gt; 资源 | WrkCtrTable |
| 资源组 | 生产控制 &gt; 设置 &gt; 资源 &gt; 资源组 | WrkCtrResourceGroup |
| 生产组 | 生产控制 &gt; 设置 &gt; 生产 &gt; 生产组 | ProdGroup |
| 成本类别 | 生产控制 &gt;设置 &gt; 工艺路线 &gt; 成本类别 | ProjCategory |
| 项目组 | 项目管理和核算 &gt; 设置 &gt; 过帐 &gt; 项目组 | ProjGroup |
| 分类帐记帐设置（项目） | 项目管理与核算 &gt; 设置 &gt; 过帐 &gt; 分类帐过帐设置 | ProjPosting |
| 支出的默认抵销帐户 | 项目管理和核算 &gt; 设置 &gt; 过帐 &gt; 费用的默认对方科目 | ProjDefaultOffsetSetup |
| 返点管理过帐模板 | 返点管理 &gt; 返点管理过帐设置 &gt; 返点管理过帐模板 | TAMRebatePosting |
| 分类帐记帐组（税） | 纳税 &gt; 设置 &gt; 销售税 &gt; 分类帐过帐组 | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>存在交易后更改组

更改主数据中的组时请务必小心谨慎。 如果您要使用组定义过帐模板，则对主记录上的组所做的任何更改都可能会对将分类帐与子分类帐进行对帐的功能产生负面影响。 例如，您可以配置销售订单收入的库存过帐模板，以便对每个物料组使用其他收入科目。 如果在存在交易后更改分配给物料的物料组，则新交易的收入将过帐到更新后的科目。 但是，更改之前过帐的任何收入都将保留在原始科目中。

## <a name="testing-posting-profiles"></a>测试过帐模板

在启用之前，以及对过帐模板或相关参数进行任何更改或添加后，您应测试每个方案。 至少，您应测试每个过帐类型以验证过帐是否正常工作。 但是，建议的方法是测试每个过帐模板交易和组合。

例如，您有两个客户过帐模板，每个都有三条特定于客户组的记录。 在这种情况下，您应测试每种交易类型。

**过帐模板：**

- **GEN** - 一般过帐模板，其中具有一个员工组、一个客户组和一个内部公司组。 每个组都指向其他应收帐款贸易科目。
- **PRE** - 预付款过帐模板，其中包含指向客户预付款科目的一条所有预付款相关记录。

### <a name="testing-scenarios"></a>测试方案

- 使用 **GEN** 过帐模板的 **员工** 组中客户的普通发票
- 使用 **PRE** 过帐模板的 **员工** 组中客户的普通发票
- 使用 **GEN** 过帐模板的 **员工** 组中客户的销售订单发票
- 使用 **PRE** 过帐模板的 **员工** 组中客户的销售订单发票
- 使用 **GEN** 过帐模板的 **员工** 组中客户的客户付款日记帐
- 使用 **PRE** 过帐模板的 **员工** 组中客户的客户付款日记帐

对于前一个示例，请重复执行每个客户组的一个测试方案，并重复执行每个附加交易类型的每组测试方案（例如项目发票和服务管理）。

## <a name="reconciling-the-ledger-to-the-subledger"></a>将分类帐与子分类帐进行对帐

每个期间都应将分类帐与子分类帐进行对帐。 许多模块包含可用于帮助执行此对帐的现成报表。 但是，根据您的本地要求，您可能必须开发自定义报表或扩展现有报表以满足您的报告要求。

我们建议您在启用前先结束模拟期间并将每个子分类帐与分类帐进行对帐。 我们还建议您在初始启用前对所有未结余额和未结交易进行模拟转换。 在此流程中，您应运行一次完整的对帐，以确保迁移余额且未结交易与旧系统保持平衡，并且在创建新交易之前所有子分类帐与分类帐保持平衡。
