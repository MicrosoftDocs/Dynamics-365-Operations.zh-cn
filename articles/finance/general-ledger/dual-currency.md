---
title: 双货币
description: 本文提供有关双货币的信息，其中的申报币种用作 Microsoft Dynamics 365 Finance 的第二记帐币种。
author: kweekley
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 19337b2651830d79543361d525bf24c4f794e825
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065737"
---
# <a name="dual-currency"></a>双货币

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance 版本 8.1（2018 年 10 月）中引入的功能支持重新确定申报币种的用途，可以将其用作第二会计币种。 此功能称为 *双货币*。 双货币的更改不能通过 Configuration Key 或参数关闭。 由于申报币种用作第二记帐币种，申报币种在过帐逻辑中的计算方法已更改。

此外，已增强多个模块，以在不同流程中跟踪、报告和使用申报币种。 受影响的模块包括：

- 总帐 
- 财务报告 
- 应付帐款
- 应收帐款 
- 现金和银行管理 
- 固定资产 
- 合并

升级后，您必须为“现金和银行管理”和“固定资产”完成特定步骤。 因此，请务必阅读并理解本文中的相关章节。

## <a name="posting-process"></a>过帐流程

生成总帐的会计条目的所有交易记录的过帐逻辑均已更改。 这里是申报币种以前的计算方法：

交易币种金额 \> 记帐币种金额 \> 申报币种金额

例如，交易记录使用加拿大元 (CAD) 货币输入。 CAD 金额转换为记帐币种，即美元 (USD)。 USD 金额然后转换为申报币种，即欧元 (EUR)。 因此，汇率必须为 CAD 到 USD 和 USD 到 EUR 的汇率。

新计算如下：

交易币种金额 \> 记帐币种金额

交易币种金额 \> 申报币种金额

由于此更改，汇率现在必须为 CAD 到 USD 和 CAD 到 EUR 的汇率。

## <a name="reports-and-inquiries"></a>报表和查询

各类报表和查询现在同时显示申报币种金额和记帐币种金额。 未更新每个报表和查询。 例如，仅使用交易币种显示金额的报表未更改。

更改遵循以下两种模式之一：

- 如果报表或查询具有足够的空间来同时显示记帐币种和申报币种的金额，则会添加申报币种金额。
- 如果报表或查询没有足够的空间同时显示两个币种的金额，则会添加选项，以便用户可以选择显示的币种。

对于各种报表和查询，还添加了当申报币种与记帐币种相同或申报币种未在法人的分类帐中定义时取消申报币种金额的逻辑。

## <a name="financial-journals"></a>财务日记帐

财务日记帐（例如普通日记帐和供应商发票日记帐）已经更新，以便其包括有关申报币种的附加信息。 凭证和日记帐的合计现在显示为申报币种。 此外，有关申报币种汇率的信息现在显示在日记帐行的 **常规** 选项卡上。 因此，在输入交易记录时，您可以覆盖申报币种的汇率。

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>供应商发票、销售订单和销售协议
供应商订单、销售订单和销售协议已更新，现在包含申报币种的固定汇率。 可以在交易记录币种不同时同时为记帐币种和申报币种定义固定汇率。 如果记帐币种和申报币种相同，将通过把记帐币种的固定汇率用作申报币种的固定汇率来让记帐币种和申报币种保持同步。 不能更改此配置的申报币种固定汇率。 如果记帐币种与申报币种不同，可以在录入交易记录时同时为记帐币种和申报币种定义固定汇率。 如果尚未在分类帐中定义申报币种，将不启用 **申报币种固定汇率** 字段，也不计算申报币种金额。

## <a name="module-changes"></a>模块更改

以下模块使用申报币种作为第二记帐币种：

- [总帐](#general-ledger)
- [财务申报](#financial-reporting)
- [应付帐款](#accounts-payable-and-accounts-receivable)
- [应收帐款](#accounts-payable-and-accounts-receivable)
- [现金和银行管理](#cash-and-bank-management)
- [固定资产](#fixed-assets)
- [合并](#consolidations)

### <a name="general-ledger"></a>总帐

如果申报币种在分类帐中定义，总帐已跟踪每个会计条目的申报币种金额。 但是，这些金额现在已从交易币种金额转换。

**总帐** 模块上还进行了以下更改：

- 申报币种的单独汇率类型可以在分类帐中定义。 如果组织不希望使用不同的汇率类型，可以将申报币种的汇率类型字段留为空白。 或者，可以选择用于记帐币种的同一汇率类型。 如果您将此字段保留为空，系统将使用记帐币种的汇率类型。
- 一种新日记帐，申报币种调整日记帐支持将调整只过帐到申报币种的会计科目。 此日记帐支持仅过帐到会计科目。 它不支持内部公司，而且币种必须是过帐日记帐的法人的申报币种。 将日记帐过帐时，交易币种和记帐币种金额为 0（零），申报币种金额过帐为在交易记录中输入的金额。 由于 **应付帐款**、**应收帐款** 和 **固定资产** 模块中使用申报币种的方式已更改，此日记帐可以在升级后用于调整。 有关显示如何使用此日记帐的示例，请参阅这些模块的相应部分。
- 期间分配的流程已更新，以在交易、记帐和申报币种之间分摊金额。 以前，金额在交易和记帐币种之间分摊，然后记帐币种金额转换为申报币种。 该行为可能导致余额仍留在申报币种的会计科目中。 现在，当计算金额并用于会计条目时，不进行转换。
- 外币重估的过程已重估了申报币种的金额。 不过，申报币种金额现在通过交易币种金额计算，如本文前面的[过帐流程](#posting-process)一节所述。
- 总帐中的很多报表和查询已具有申报币种，但有些没有。 一个例子是 **试算平衡表** 列表页。 此列表页现在同时包括记帐币种和申报币种的列。 请注意，如果记帐币种和申报币种相同，或未在分类帐中定义申报币种，申报币种列将隐藏。

### <a name="financial-reporting"></a>财务申报

**财务申报** 模块的增强功能允许您以两种方法在财务报表中包括申报币种。 在列定义中，您可以直接在过帐到分类帐的申报币种金额中申报（新功能）。 或者，您可以继续将金额从记帐币种转换为申报币种（现有功能）。

此更改通过列定义的 **币种显示** 设置提供。 如果您选择 **从分类帐申报币种**，列中的金额将不转换。 而是直接从总帐申报。 如果您希望列显示转换的金额，请选择 **转换到 XXXX** 选项，其中 *XXXX* 是列应显示的申报币种。 在这种情况下，记帐币种金额将使用现有的转换功能转换为所选币种。

### <a name="accounts-payable-and-accounts-receivable"></a>应付帐款和应收帐款

**应付帐款** 和 **应收帐款** 模块已经跟踪申报币种金额。 但是，金额不为各个流程显示或使用。 进行了下列更改：

- 申报币种金额现在同时显示在客户和供应商的交易记录中。 申报币种金额也会为每个交易记录的未结余额显示。
- 帐龄流程已经更新，以便组织可以使用记帐币种或申报币种查看帐龄时段。
- 各种查询和报表已经更新，以便其显示申报币种金额。 示例包括 **客户分类帐对帐** 和 **供应商分类帐对帐** 报表。
- 外币重估的过程已重估了申报币种的金额。 不过，申报币种金额现在通过交易币种金额计算，如[过帐流程](#posting-process)部分所述。
- **升级注意事项：** 在升级前，单据（发票、付款等）的申报币种金额通过记帐币种计算。 例如，发票在组织升级前过帐，且发票不支付。 在升级期间，发票的会计条目不更改。 但是，在升级后，双货币的更改将生效。 因此，在为发票付款时，付款的申报币种金额现在通过交易币种金额计算。 在结算付款和发票时，已实现利润/损失金额的计算可能稍有不同，因为申报币种金额现在计算有所不同。 如果计算的差异被认为明显，新的申报币种调整日记帐可用于调整仅使用申报币种的已实现利润/损失和应付帐款/应收帐款会计科目的余额。

### <a name="cash-and-bank-management"></a>现金和银行管理

以前，**现金和银行管理** 模块不跟踪按每个银行帐户过帐的交易记录的任何申报币种金额。 升级后，自动跟踪过帐的任何新交易记录的申报币种金额。 但是，申报币种金额必须添加到子分类帐中之前过帐的交易记录。

- **升级注意事项：** 由于银行帐户交易记录以前不跟踪子分类帐中的申报币种金额，因此添加了向导，以便您可以将申报币种金额添加到银行帐户交易记录。 此向导 **不** 再次过帐到总帐。 而是从总帐获取申报币种金额，并在子分类帐表中更新它们。

    - 若要开始该向导，请选择 **现金和银行管理** \> **设置** \> **将申报币种金额添加至银行帐户交易记录**。
    - 向导显示申报币种金额为 0（零）的当前公司中所有银行帐户的交易记录。 仅在升级前过帐的交易记录包括在内。
    - 对于每个银行帐户交易记录，向导在总帐中查找对应的会计条目并输入默认申报币种金额。 尽管可以编辑金额，但我们建议您 **不要** 编辑它们。 否则，您有可能无法将银行帐户余额与总帐对帐。 仅当无法在总帐中找到申报币种金额时，您才应该编辑金额。 在这种情况下，向导将为申报币种显示 0（零）金额。
    - 如果在向导中选择 **取消**，在您下一次运行向导前，银行帐户交易记录和对申报币种金额的任何更改都将保存。 但是，不在银行帐户交易记录中更新申报币种金额。 只有当您在向导中选择 **完成** 时才会更新。 您可以多次运行向导。 因此，如果您犯了错误，您可以修改任何不正确的申报币种金额。

- 现金和银行管理中没有流程更改，但更新了各个报表和查询，以使其显示申报币种金额。 现金流量预测报表除外。 它们未更新来包含申报币种金额。

### <a name="fixed-assets"></a>固定资产

以前，**固定资产** 模块不跟踪按每个固定资产帐簿过帐的交易记录的任何申报币种金额。 升级后，自动跟踪过帐的任何新交易记录的申报币种金额。 但是，申报币种金额必须添加到子分类帐中之前过帐的交易记录。

此外，还对折旧流程进行了主要更改。 这些更改需要用户在升级后执行操作。 阅读并了解以下变化很重要，即使您尚未使用固定资产。

- 折旧流程确定申报币种金额的方法已更改。 以下场景比较折旧以前如何确定申报币种金额，以及现在如何确定申报币种金额。



    **折旧场景**

    资产已购置并过帐为以下金额。 请注意，申报币种金额在总帐中过帐，但不存储在固定资产子分类帐表中。

    | 交易记录类型 | 交易金额 | 汇率 | 记帐币种金额 | 汇率 | 申报币种金额 |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | 购置      | 1,000,000 DKK      | 2.0           | 500,000 美元                | 2.5           | 200,000 欧元               |

    **以前的申报币种折旧**

    年底，折旧方案运行并计算以下金额。

    | 交易记录类型 | 交易金额 | 汇率 | 记帐币种金额 | 汇率 | 申报币种金额 |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | 折旧     | 50,000 美元         | 1.0           | 50,000 美元                 | 2.6           | 19,230.77 欧元             |

    如果折旧方案运行时，它使用折旧方法计算记帐币种金额。 然后使用当前的 USD 和 EUR 汇率将该金额转换为申报币种。 此转换导致出现问题，因为在使用即期汇率时，资产无法使用申报币种完全折旧。

    **新的申报币种折旧**

    折旧流程已更改，以便还使用折旧方法计算申报币种金额。 这是折旧对资产运行时得出的结果。

    | 交易记录类型 | 交易金额 | 汇率 | 记帐币种金额 | 汇率                                                       | 申报币种金额 |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | 折旧     | 50,000 美元         | 1.0           | 50,000 美元                 | 2.5<blockquote>[!NOTE] 虽然显示此汇率，但它不用于转换为申报币种。</blockquote> | 20,000 欧元                |

    当折旧方案运行时，它使用折旧方法同时计算记帐币种金额和申报币种金额。 此金额随后在总帐的会计条目中使用。 不会进行转换来确定申报币种金额。

- **升级注意事项：** 由于固定资产帐簿交易记录以前不跟踪申报币种，因此添加了向导，以便您可以将申报币种金额添加到固定资产帐簿交易记录。 此向导 **不** 再次过帐到总帐。 由于折旧方案计算申报币种金额的方法已更改，向导 **必须** 为每个公司运行并完成，然后组织才能够输入折旧交易记录。

    - 若要开始向导，请选择 **固定资产** \> **设置** \> **将申报币种金额添加至固定资产帐簿**。
    - 向导显示申报币种金额为 0（零）的当前公司中所有固定资产帐簿的交易记录。 仅在升级前过帐的交易记录包括在内。
    - 向导 **不** 从总帐提取申报币种金额。 如前面的场景中所述，最初过帐到总帐的申报币种金额错误地使用了即期汇率。 这些金额不应该显示在固定资产子分类帐中，因为下一个折扣计算将使用不正确的金额。 向导则会查找首次购置日期的汇率。 然后使用该汇率来建议应在子分类帐中过帐的申报币种金额。 例如，这里是向导可能为前面的场景显示的内容。

        | 固定资产 | 预订      | 交易记录类型 | 交易日期 | 货币 | 用交易币种表示的金额 | 时长  | 汇率 | 申报币种金额 |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | 购置      | 6/3/2016         | DKK      | 1,000,000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | 折旧     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | 折旧     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | 折旧     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - 许多客户在工作簿中跟踪资产交易记录详细信息。 这些详细信息包括汇率和金额。 如果您在工作簿中有此数据，则可以创建自定义的汇率类型并将其更新为工作簿中的汇率。 此汇率类型然后将用于在购置日期输入默认汇率，并计算申报币种金额。 如果未选择汇率类型，向导将使用在分类帐中定义的汇率类型。
    - 汇率和申报币种金额可以更改。 如果汇率发生变化，申报币种金额将使用新的汇率重新计算。
    - 如果在向导中选择 **取消**，在您下一次运行向导前，固定资产帐簿交易记录和对汇率或申报币种金额的任何更改都将保存。 但是，不在固定资产帐簿交易记录中更新申报币种金额。 只有当您在向导中选择 **完成** 时才会更新。 您可以多次运行向导。 因此，如果您犯了错误，您可以修改任何不正确的申报币种金额。
    - 当申报币种金额在子分类帐中完全更新后，您 **必须** 将 **是否已更新固定资产帐簿交易记录中的所有申报币种金额?** 选项设置为 **是**，然后选择 **完成**。 折旧计算无法完成，直到您将 **是否已更新固定资产帐簿交易记录中的所有申报币种金额?** 选项设置为 **是**。 在将该选项设置为 **是** 后，向导不再可用。
    - 在子分类帐中的固定资产交易记录更新为申报币种金额之后，这些金额将不同于最初过帐到总帐的金额。 但是，申报币种调整日记帐可以用于更新总帐中折旧会计科目的余额，以使其与最初过帐的金额相同。
    - 已在 **数据管理** 工作区中添加的新 **资产交易记录申报币种金额** 实体允许您从向导中导出数据。 您随后可以使用此数据来确定折旧交易记录的固定资产子分类帐中的余额。 该余额然后可以用于确定总帐中申报币种调整的金额。

- **升级注意事项：** 新的设置字段已添加到固定资产并用于折旧计算。 您可能必须在下一次折旧计算前更新这些字段。

    - 在固定资产帐簿（**固定资产** \> **帐簿**）上，**常规** 快速选项卡具有新的 **以申报币种表示的购置价格** 字段。
    - 在固定资产帐簿（**固定资产** \> **帐簿**）上，**折旧** 快速选项卡具有新的 **以申报币种表示的预期残值** 字段。
    - 在固定资产参数（**固定资产** \> **设置** \> **固定资产参数**）中，**常规** 快速选项卡具有新的 **以申报币种表示的最小折旧金额** 字段。
    - 在帐簿上（**固定资产** \> **设置** \> **帐簿**），**常规** 快速选项卡有两个新字段：**化整以申报币种表示的折旧** 和 **以申报币种表示帐面净值**。

- 由于折旧方案现在同时使用记帐币种和申报币种计算金额，固定资产日记帐已更新，以使其以申报币种显示折旧金额。 对于折旧交易记录，交易币种始终是记帐币种。 因此，这些金额将继续出现在 **借方** 和 **贷方** 列。 两个新列 **以申报币种表示的借记** 和 **以申报币种表示的贷记** 已添加到网格。

    - 只有当交易记录类型是以下四个折旧类型之一时新字段才可用：**折旧**、**折旧调整**、**特别折旧** 或 **特殊折旧补偿**。
    - 如果在固定资产日记帐中输入了折旧交易记录类型，申报币种金额将显示在新列中。 这些金额可以更改。
    - 如果分类帐中的记帐币种和申报币种相同，金额将保持同步。如果您更改 **贷方** 金额，**以申报币种表示的贷方** 金额将自动更改，以使它们相同。
    - 如果在固定资产日记帐中输入了任何其他交易记录类型，**以申报币种表示的借方** 和 **以申报币种表示的贷方** 金额永远不会显示，不论是在过帐之前还是之后。 记帐币种和申报币种金额在过帐到总帐的凭证中仍然显示。
    
### <a name="consolidations"></a>合并
    
Dynamics 365 Finance 版本 10.0.5（2019 年 10 月）中将引入的功能可用于通过文档管理使用功能，从而提高合并和双货币的灵活性。 若要启用此功能，请转到 **功能管理** 工作区，然后选择 **在总帐合并中启用双货币功能**。

在“总帐合并”中，已添加了一个新选项，用于合并来自源公司的记帐或申报币种金额。 如果此记帐或申报币种与合并公司中的记帐或申报币种相同，将把直接复制此金额，不经过换算。

-  现在可选择是否将源公司的记帐币种或申报币种用作合并公司中的交易币种。

- 如果源公司中的记帐或申报币种与合并公司中的相同，将把源公司的币种金额直接复制到合并公司中的币种金额。 如果币种不同，将在合并公司中使用汇率计算记帐和申报币种金额。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

