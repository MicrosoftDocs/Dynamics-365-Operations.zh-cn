---
title: 年终活动常见问题解答
description: 本文列出了在年终结算时可能出现的问题，以及有助于开展年终结算活动的问题解答。
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853031"
---
# <a name="year-end-activities-faq"></a>年终活动常见问题解答 

[!include [banner](../includes/banner.md)]

本文列出了在年终结算时可能出现的问题，以及有助于开展年终结算活动的问题解答。 本文中的信息主要集中于与总帐和应付帐款的年终结算活动有关的问题。

## <a name="general-ledger-year-end-enhancements"></a>总帐年终增强

Microsoft Dynamics 365 Finance 版本 10.0.20 推出了年终结算增强。 此增强功能从版本 10.0.25 开始默认启用，从版本 10.0.29 开始强制启用。 如果您的组织使用低于 10.0.25 的版本，我们建议先启用此功能，然后再开始年终结算流程。 必须在系统中开启此功能，然后才能使用。 管理员可以使用 **功能管理** 工作区检查功能状态和开启功能（如果需要）。 在此工作区，此功能按以下方式列出：

- **模块：** 总帐
- **功能名称：** 总帐年终增强

年终结算模板的设置已移至新的设置页面，即 **年终结算模板设置**。 现有的年终结算页面将变为类似于 **总帐外币重估** 的页面，每次运行或冲销年终结算时，页面上都会显示列表。 该页面不会显示有关启用该功能之前完成的年终结算的历史信息。 会计经理可以从新的页面启动年终结算。

要冲销年终结算，请为适当的法人选择最近一个会计年度，然后选择 **冲销年终结算**。 冲销将删除上一次年终结算的会计条目，并且不会自动重新运行年终结算。 如果您在完成年终结算后启用 **总帐年终增强** 功能，并且想要冲销历史年终结果，请在启用 **重新结算年度时删除现有年终结算条目** 总帐参数后，再次运行历史年终结算。

您可以针对会计年度和法人重新启动流程来重新运行年终结算。 该流程将继续使用总帐参数设置来确定重新运行的年终结算将只计入新的或更改的交易记录，还是针对所有交易记录重新运行该流程并完全冲销上一次结算。

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>总帐：总帐年终增强功能已启用。 为什么我无法在年终结算页面的历史记录部分查看我上一年的结算？

在启用 **总帐年终增强** 功能之前，会跟踪上次运行年终结算流程的日期和时间， 并不是每次执行年终结算时都跟踪历史记录。 因此，无法显示每次年终结算运行的详细信息。 启用该功能后，会对后续年终结算流程信息进行维护。 可在 **凭证交易记录** 页面上查看所有年终结算流程的凭证，包括在启用增强功能之前运行的凭证。 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>总帐：由于以下错误，年终结算流程失败：“无法运行年终结算，因为已过帐到要结算的会计年度中的一个或多个交易记录已结算到其他会计年度中的分类帐交易记录。” 这个错误是什么意思？

由于启用了 **区分分类帐结算与年终结算** 功能，因此系统仅从期初余额中排除了会计年度中已结算的分类帐交易记录。 这会导致借方和贷方失去平衡。 有关详细信息，请参阅[区分分类帐结算与年终结算](awareness-between-ledger-settlement-year-end-close.md)。

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>总帐：由于以下错误，冲销年终结算流程操作失败：“2022 年 1 月 1 日的年终结算无法冲销，因为期初余额交易记录已在 2023 年 1 月 1 日所在会计年度进行了分类帐结算。” 这个错误是什么意思？

由于启用了 **区分分类帐结算与年终结算** 功能，如果期初交易记录已在新的会计年度中结算，则无法冲销年终处理。 在您冲销 2022 年 1 月 1 日的年终结算之前，请冲销新的 2023 会计年度的分类帐结算。 或者，重新结算 2022 年 1 月 1 日所在的年度，但仅限于新的调整条目。 要仅针对调整来重新结算年度，请禁用 **重新结算年度时删除现有的年终条目** 总帐参数。

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>总帐：为什么分类帐结算自动化不处理 12 月的分类帐结算交易？

**自动化分类帐结算** 功能将对从会计年度的第一天到事件运行时当前日期的交易运行自动化。 对于在 12 月 31 日结束的会计年度，您可能必须调整事件的执行日期以确保自动化在 12 月能正常运行。 例如，可以将自动化设置为在每个月的第一天运行。 该自动化将于 2022 年 12 月 1 日运行，并计划下次于 2023 年 1 月 1 日运行。 我们建议您将 2023 年 1 月 1 日更改为 2022 年 12 月 31 日。 此更改将确保 12 月 2 日至 31 日的交易记录纳入自动结算。

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>总帐：冲销年终结算的操作和总帐中的在重新结算时删除现有年终条目的参数之间的区别是什么？

**冲销年终结算** 这一操作和总帐中 **在重新结算时删除现有年终条目** 这一参数（**总帐 \> 分类帐设置 \> 总帐参数**）之间的差异可能存在混淆。

运行年终结算流程时选择 **冲销年终结算** 操作，可以删除所有期末余额和期初余额条目，效果就像从未运行年终结算一样。 在这种情况下，将删除凭证。 将不会自动重新运行年终结算。 要运行年终结算，请选择 **运行年终结算** 操作。

总帐中的 **重新结算年度时删除现有的年终条目** 参数仅在运行（而非冲销）年终结算时使用。 如果该参数设置为 **是**，将会删除所有期末余额和期初余额条目，并将再次运行年终结算。 如果组织想要在单个会计条目中过帐期末余额和期初余额条目的所有交易记录，包括自上一次年终结算以来的调整，可使用此选项。 如果该参数设置为 **否**，则所有期末余额和期初余额条目将保持不变。 将不会删除这些条目。 相反，将仅为自该会计年度的上一次年终结算以来已过帐的增量或新交易记录创建新的期末余额和期初余额条目。

> [!NOTE]
> 将在结算年份中创建期末余额条目。 仅当总帐中的 **在转移期间创建期末交易记录** 参数设置为 **是** 时，才会发生此情况。 始终会创建期初余额条目，因为这是下一年的期初余额。

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>总帐：年终结算流程中转移损益维度部分的“结算全部”和“结算单个”选项有什么区别？

**结算全部** 会保留来自已过帐交易的原始财务维度值，并将其用于为留存收益科目创建期初余额。 将为财务维度值的每个唯一组合创建单独的留存利润期初余额。 如果选择 **结算单个**，会将具有该财务维度的所有已过帐交易汇总到在 **结算单个** 之后出现的字段中输入的维度值的留存收益期初余额。 

例如，会计年度所有交易均以主科目 - 部门的科目结构过帐。 对于模板中的部门财务维度，选择 **结算单个**，维度值输入 100。 如果过帐到部门 200、300 和 400 的所有交易的总收入为 100,000 美元，将为留存收益 - 100 创建一个期初余额。 如果选择 **结算单个**，但将财务维度值保留为空，所有交易将过帐到留存收益，维度值将为空。

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>总帐：当我在年终结算流程中的转帐损益维度部分选择“结算单个”选项时，我的详细交易信息是否会丢失？

**结算全部** 和 **结算单个** 选项用于指定过帐到损益科目的交易中，哪些财务维度将转移到留存收益主科目。 到损益科目的历史详细过帐不受影响，其详细信息将得到保留。 该选项会影响新年度期初余额转移到留存收益科目的详细程度。 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>总帐：因当年申报币种不平衡，年终结算流程失败。 这是什么意思？

启用 **区分分类帐结算与年终结算** 功能（区分功能）后，可能会遇到此错误。 启用该功能后，在运行总帐年终结算时，已结算的分类帐交易将不再计入下一会计年度的期初余额。 如果分类帐用申报币种定义，则在年终结算时排除已结算的分类帐交易可能会给客户造成困扰。   
分类帐结算仅针对记帐币种进行。  在分类帐交易结算时，验证仅用于确保记帐币种借项与贷项相等。 这些分类帐交易的申报币种金额未经验证，可能无法确保借项与贷项相等。  此外，分类帐结算不会自动计算和过帐申报币种的损益。  由于这些限制，在执行分类帐结算时，损益交易必须以申报币种进行。  如果损益未包含在分类帐结算中，年终结算将显示余额不足的消息。  有关详细信息，请参阅[了解分类帐结算功能和申报币种余额不足](reporting-currency-yec.md)。

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>总帐：可以通过更改哪些内容来增强年终处理的性能？

您可以进行一些更改以提高年终结算的性能。 我们建议您评估这些推荐进行的更改，以确定这些更改是否适合您的组织。

### <a name="optimize-year-end-close-service"></a>优化年终结算服务

借助 **优化年终结算** 服务，Microsoft Dynamics 365 Finance 客户可以将繁重的年终处理转移到微服务，进而加快年终结算。 高效的年终结算可为各个 Finance 团队节省时间，使其能够及时对所需的调整做出反应，最终生成财务报告。 通过在微服务处理年终结算，节省宝贵的资源。 处理方式的进步最大限度地减少了 SQL Server 的负载，并使客户有机会更快完成年终结算处理。

**优化年终结算** 服务已在版本 10.0.31 中推出，这样更多客户就可以在 2022 年结束前用上新的服务。 此外，版本 10.0.30 和 10.0.29 已追加该服务。 有关详细信息，请参阅[优化年终结算](optimize-year-end-close.md)。

### <a name="dimension-sets"></a>维度集

当运行年终结算时，将重新生成每个维度集余额。 这会对性能产生直接影响。 一些组织创建维度集，并不一定是因为在某个时间或者可能在某些时间使用过这些维度集， 而是因为年终结算期间，仍会重新生成这些不必要的维度集，这会增加处理时间。 花点时间评估您的维度集，并删除任何不必要的维度集。

不必要的维度集也会影响批处理作业 **BudgetDimensionFocusInitializeBalance**（**总帐 \> 会计科目表 \> 维度 \> 财务维度集**）。

[![财务维度集。](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>年终结算模板配置

组织可以使用年终结算模板，来选择当将损益余额转移到留存收益时要维护的财务维度级别。 当将余额移至留存收益或选择将金额汇总为单个维度值（**结算单个**）时，组织可以使用这些设置维护详细的财务维度（**结算全部**）。 可以针对每个财务维度进行此定义。 有关这些设置的详细信息，请参阅[年终结算](year-end-close.md)文章。

我们建议您评估组织的要求，如果可能，请使用 **结算单个** 年终选项结算尽可能多的维度，以提高性能。 通过结算到单个维度值（也可以是空白值），系统在确定留存收益科目分录的余额时，将减少计算的明细。

### <a name="degenerate-dimensions"></a>退化维度

退化维度本身以及与其他维度结合使用时极少或不可以重用。 有两种类型的退化维度。 第一种类型是单独退化的维度。 通常，这种类型的退化维度仅出现在单个交易记录或小型交易记录集中。 第二种类型是与一个或多个其他维度结合使用时发生退化的维度，根据可生成的可能排列，这些维度显示出相同的潜力。 退化维度可能会对年终结算流程的性能产生重大影响。 要最大限度地减少性能问题，请按照上一节中所述，在年终结算设置中将所有退化维度定义为 **结算单个**。

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>应付帐款：做出了哪些更改以支持 2022 年 1099 年终报告？

#### <a name="update-to-all-1099-forms"></a>更新全部 1099 表格

对 2022 纳税年度的全部 1099 表格进行了以下更改：

- 2021 年，年份会在 1099 表格中固定显示。 自 2022 年起，年份会由报告进行填充。

#### <a name="1099-misc"></a>1099-MISC

对 2022 纳税年度的 1099-MISC 表格进行了以下更新：

- 13 栏：现可显示《海外帐户税收合规法案》(FATCA) 的归档要求。
- 14 栏：现可用于报告超额的金色降落伞付款。
- 15 栏：现可用于报告不合格的延期薪酬收入 (NQDC) 计划中的付款。
- 16 栏：现可用于报告州预扣税。
- 17 栏：现可用于报告付款人的税号。
- 18 栏：现可用于报告州应税所得额。

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>应付帐款：1099 - 对于全年都未跟踪 1099 信息的供应商，如何更改该供应商的 1099 栏和值？

使用 **更新 1099** 功能检查先前已付款的发票交易记录，以根据 **供应商** 页面上 **1099 税** 选项卡中的设置相应地重新分配 1099 数据。 要使用 **更新 1099** 功能，请转到 **应付帐款 \> 供应商 \> 所有供应商**，选择供应商，然后在操作窗格上的 **供应商** 选项卡中，选择 **更新 1099**。

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>我可以一次对我的所有供应商运行更新 1099 功能吗？

您可以使用 **更新多个供应商的 1099 信息** 页面更新供应商记录上的 1099 栏，并使用 1099 栏中的信息更新交易。 要打开此页面，请转到 **应付帐款 \> 定期任务 \> 1099 税**。 要访问该页面，您必须拥有 **更新多个供应商的 1099 栏和交易记录** 安全特权。

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>应付帐款：1099 - 更新 1099 实用程序中的“重新计算现有的 1099 金额”与“全部更新”

与 **全部更新** 复选框一起使用时，**重新计算现有的 1099 金额** 复选框会将 1099 金额重置为总付款值。

[![1099 税交易记录：运行更新例程之前。](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

仅当发票中存在部分 1099 值或在 1099 税表格中修改了值时，**重新计算现有的 1099 金额** 复选框才会起效。 例如，您的发票价值为 1,000.00 美元，但是用户在发票中将 1099 金额手动键入为 500.00 美元。

[![1099 税交易记录：同时标记“全部更新”和“重新计算现有的 1099 金额”。](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

支付此发票后，支付的 1099 金额将为 500.00 美元。 如果执行重新计算例程，1099 金额将更改为 1000.00 美元，即已支付的总额。

[![1099 税交易记录：运行 1099 例程后。](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>应付帐款：1099 - 手动创建 1099 交易记录

组织可能需要手动创建与发票不相关的 1099 交易记录。 您可以通过转到 **应付帐款 \> 定期任务 \> 1099 税 \> 用于 1099 的供应商结算**，来添加手动 1099 交易记录。 选择 **手动 1099 交易记录** 按钮。

使用 **更新 1099** 实用程序中的 **全部更新** 流程或 **重新计算现有的 1099 金额** 流程未更新手动创建的 1099 交易记录。

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>应付帐款：1099 - Dynamics 365 Finance 是否支持 1096 表格？

Dynamics 365 Finance 未打印“美国信息返回的 1096 年度摘要和传送”表格。

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>应付帐款：1099 - 是否有任何新功能支持公共部门 1099 报告？

增添了一个新的公共部门功能，即 **通过主帐户更新 1099 信息**，您可以在 **功能管理** 工作区中启用该功能。 利用此功能可以通过会计分配中的主帐户（而不是供应商记录中的默认帐户）关联供应商的 1099 值。

有关详细信息，请参阅[设置供应商进行 1099 申报](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
