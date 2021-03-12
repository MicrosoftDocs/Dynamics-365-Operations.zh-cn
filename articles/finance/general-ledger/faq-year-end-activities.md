---
title: 年终活动常见问题解答
description: 本主题编译为提供有关年终结算活动的帮助。
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d10f54913ca8dff56a59ea597a9bd7c3e69d4bc
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107687"
---
# <a name="year-end-activities-faq"></a>年终活动常见问题解答 

本主题编译为提供有关年终结算活动的帮助。 本主题中的信息主要集中于与总帐和应付帐款的年终结算活动有关的问题。

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>总帐：怎样知道我们正在运行年终结算而不是撤消年终结算？
我们已经注意到一些组织尝试运行年终结算，而不是对年终结算执行撤消操作。 如果年终结算很快将完成或者年终结算未产生期初余额，请验证 **年终结算** 中的 **撤消上一次结算** 设置（**总帐 > 期间结算 > 年终结算 > 运行会计结算**）。 

[![运行年终结算与撤消年终结算](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

如果 **撤消上一次结算** 选择设置为 **是**，将反转上一次年终结算。 运行撤消操作时，将删除所有期末余额和期初余额条目，好像从未运行年终结算一样。 已删除凭证。 将不会自动重新运行年终结算。 您必须重新启动该流程，此时会将 **撤消上一次结算** 更改为 **否**。 

> [!NOTE]
> 可以选择在结算年份中创建期末余额条目。 仅当总帐参数 **在转移期间创建期末交易记录** 设置为 **是** 时，才会发生此情况。 始终会创建期初余额条目，因为这是下一年的期初余额。  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>总帐：针对年终结算的“撤消总帐”和“删除总帐”参数有何差别？
**年终结算** 对话框中的 **撤消上一次结算** 参数与总帐中的 **在转移期间删除年末结转交易记录** 参数（**总帐 > 期间结算 > 年终结算 > 运行会计结算**）之间的差异可能存在混淆。  

[![针对年终结算的“撤消总帐”和“删除总帐”参数有何差别？](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

运行年终结算流程时选择下拉对话框中的 **撤消上一次结算**，可以删除所有期末余额和期初余额，好像从未运行年终结算一样。 将删除凭证。 将不会自动重新运行年终结算。 要运行年终结算，必须再次启动此流程，此时会将 **撤消上一次结算** 更改为 **否**（**总帐 > 分类帐设置 > 总帐参数**）。 

[![总帐参数设置](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

仅当运行（非撤消）年终结算（**撤消上一次结算** 选择设置为 **否**）时，才会使用总帐中的 **在转移期间删除年末结转交易记录** 参数。 如果该参数设置为 **是**，将会删除所有期末余额和期初余额条目，并将再次运行年终结算。 如果组织想要在单个会计条目中过帐期末余额和期初余额条目的所有交易记录，包括自上一次年终结算以来的调整，将使用此流程。 

如果此选项设置为 **否**，则所有期末余额和期初余额条目将保持不变。 将不会删除这些条目。 相反，将仅为自该会计年度的上一次年终结算以来过帐的增量或新交易记录创建新的期末余额和期初余额条目。  

> [!NOTE]
> 将在结算年份中创建期末余额条目。 仅当总帐中的 **在转移期间创建期末交易记录** 参数设置为 **是** 时，才会发生此情况。 始终会创建期初余额条目，因为这是下一年的期初余额。 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>总帐：可以更改哪些内容以增强年终处理的性能？ 
您可以进行很多更改以提高年终结算的性能。 我们建议您评估这些建议的更改，以考虑该更改是否适合您的组织。  

### <a name="dimension-sets"></a>维度集
当运行年终结算时，将重新生成每个维度集余额，这会直接影响性能。 一些组织创建维度集，并不一定是因为在某个时间或者可能在某些时间使用过这些维度集。  年终结算期间，仍会重新生成这些不必要的维度集，这会增加处理时间。 花点时间评估您的维度集，并删除任何不必要的维度集。

不必要的维度集也会影响批处理作业 **BudgetDimensionFocusInitializeBalance**（**总帐 > 会计科目表 > 维度 > 财务维度集**）。

[![财务维度集](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>年终结算模板配置
组织可以使用年终结算模板，来选择当将损益余额转移到留存收益时要维护的财务维度级别。 当将余额移至留存收益或选择将金额汇总为单个维度值（**结算单个**）时，组织可以使用这些设置维护详细的财务维度（**结算全部**）。 可以针对每个财务维度进行此定义。 有关这些设置的详细信息，请参阅[年终结算](year-end-close.md)主题。

我们建议您评估组织的要求，如果可能，请使用 **结算单个** 年终选项结算尽可能多的维度，以提高性能。 通过结算到单个维度值（也可以是空白值），系统在确定留存收益科目条目的余额时，将减少计算的明细。

### <a name="10013-update-or-later"></a>10.0.13 更新或更高版本
如果您的组织自上次运行年终结算以来已更新到版本 10.0.13 或更高版本，则年终结算处理可能会由于 [HashV2 功能实现](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2)而花费更长的时间。 （术语 *哈希* 指的是从其他字符串字段计算得出的字段。 更新了用于计算哈希 GUID 值的 API，以增强安全性。）要加快年终结算过程，我们建议在运行年终结算之前重建生成维度集余额。 如果您在执行 10.0.13 更新后，已重新生成了维度集余额，则无需再次运行重新生成过程。
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>总帐 – 期间结算 – 年终计算执行哪些操作？
 
[![期间结算、年终结算](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>用于重新生成财务维度集的性能改进（新功能）
版本 10.0.16 中添加的新功能提高了年终结算和合并流程的性能。 该新功能命名为“用于重新生成财务维度集的性能改进”。 此功能将更改重新生成维度集的方式，以便仅在相关时间范围内重新生成维度集。 在先前的版本中，为会所有日期重新生成维度集。 例如，如果您要对 2020 年进行结算，则系统将仅重新生成 2020 会计年度内的交易记录的余额。 如果您对 2020 年 11 月 1 日至 2020 年 11 月 30 日的日期范围运行合并，则系统将仅重新生成该日期范围的余额。

由于此功能被认为是中断性变更，因此您需要使用 **功能管理** 工作区来启用它。
 
[![年终结算](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>应付帐款：做出了哪些更改以支持 2020 年 1099 年终报告？

为 2020 年的 1099 年终更改添加了两个新的监管功能。 第一个功能是 **应用对 2020 年的 1099-NEC 和 1099-MISC 表格的更改**，此功能在年中作为一项必需功能发布。 其目的是确保可以跟踪新的 1099-NEC 表格在 2020 年的 1099 交易数据。 此功能添加了支持新 1099-NEC 所需的 1099 字段，并更新了 1099-MISC 字段。 此更新还升级了 1099 栏信息的供应商记录数据。 

第二个监管功能是 **针对 2020 年税法更新的 1099 声明**，包含以下更改。

- 1099-OID - IRS 已转换该表格以供继续使用。
   - 打印时必须填写报告年度的第 3 个和第 4 个数字。 使用 **1099 税打印选项** 中的 **报告年度** 字段的第 3 个和第 4 个数字。 

- 1099-NEC – 新的 2020 年表格。 此表格记录非员工薪酬。 

-   1099-MISC – 由于创建了 1099-NEC 表格，IRS 修订了 1099-MISC 表格并重新排列了栏数字，以用于报告某些收入。
下面列出了收入报告中的更改和表格的栏编号。
   - 付款人在栏 7 中创建了 $5,000 或以上的直接销售额（复选框）。
   - 农作物保险收益在栏 9 中报告。
   - 律师总收益在栏 10 中报告。
   - 409A 部分延期在栏 12 中报告。
   - 不合格的延期薪酬收入在栏 14 中报告。
   - 栏 15、16 和 17 分别报告州预缴税金、州标识号和在该州赚取的收入金额。

- 未对 2020 年的 1099-DIV 或 1099-INT 进行更改。

- 电子归档 - 格式已更改以适应新的 NEC 表格，MISC 栏更改如上所述。 有关电子归档要求的特定信息，请参阅 [IRS 发布 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf)。

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>应付帐款：1099 – 对于全年都未跟踪 1099 信息的供应商，如何更改该供应商的 1099 栏和值？
使用更新 1099 功能（**应付帐款 > 供应商 > 所有供应商 > 选择供应商 > 功能区中的“供应商”选项卡 > 更新 1099**）检查先前已付款的账单交易记录，以根据 **供应商** 页面上的 **1099 税** 选项卡中的设置相应地重新分配 1099 数据。

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>我可以一次对我的所有供应商运行更新 1099 吗？
否。 一次只能针对单个供应商执行更新 1099 例程。 如果您的组织需要此要求，请投票支持标题为[用于更新供应商的 1099 数据的批处理流程](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8)的创意。

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>应付帐款：1099 - 更新 1099 实用程序中的“重新计算现有的 1099 金额”与“全部更新”。
与 **全部更新** 复选框一起使用时，**重新计算现有的 1099 金额** 复选框会将 1099 金额重置为总付款值。 

[![1099 税交易记录：运行更新例程之前](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

仅当账单中存在部分 1099 值或在 1099 税表格中修改了值时，**重新计算现有的 1099 金额** 复选框才会起效。 例如，假设您的账单价值为 $1000.00，但是用户在账单中将 1099 金额手动键入为 $500.00。

[![1099 税交易记录：同时标记“全部更新”和“重新计算现有的 1099 金额”](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

支付此款项后，$500.00 将为支付的 1099 金额。 如果执行重新计算例程，系统会将 1099 金额更改为 $1000.00，这是已支付的总额。

[![1099 税交易记录：运行 1099 例程后](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>应付帐款：1099 - 手动创建 1099 交易记录
组织可能需要手动创建与账单不相关的 1099 交易记录。 您可以通过转到 **应付帐款 > 定期任务 > 1099 税 > 用于 1099 的供应商结算**，来添加手动 1099 交易记录。 选择 **手动 1099 交易记录** 按钮。 

使用 **更新 1099** 实用程序中的 **全部更新** 流程或 **重新计算现有的 1099 金额** 流程未更新手动创建的 1099 交易记录。

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>应付帐款：1099 - Dynamics 365 Finance 是否支持 1096 表格？ 

Dynamics 365 Finance 未打印“美国信息返回的 1096 年度摘要和传送”表格。

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>应付帐款：1099 - 是否有任何新功能支持公共部门 1099 报告？ 
增添了一个新的公共部门功能，即 **通过主帐户更新 1099 信息**，您可以在 **功能管理** 工作区中启用该功能。 利用此功能可以通过会计分配中的主帐户（而不是供应商记录中的默认帐户）关联供应商的 1099 值。

有关详细信息，请参阅[设置供应商进行 1099 申报](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]