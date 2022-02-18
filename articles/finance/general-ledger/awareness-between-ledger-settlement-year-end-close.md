---
title: 区分分类帐结算与年终结算
description: 本主题提供有关影响分类帐结算和总帐年终结算的增强功能的信息。
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075560"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>区分分类帐结算与年终结算

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

在 Microsoft Dynamics 365 Finance 版本 10.0.25 中，**区分分类帐结算与年终结算** 功能在 **功能管理** 工作区提供。 此功能添加了两个影响分类帐结算和总帐年终结算的主要增强功能。

在总帐年终结算期间，已结算的分类帐交易记录将不再包含在下一会计年度的期初余额中。 此增强可确保期初余额中仅包含未结算的分类帐交易记录。 此增强在运行总帐外币重估时非常重要。 外币重估仅对状态为 **未结算** 的分类帐交易记录运行。 但是，在 **区分分类帐结算与年终结算** 功能发布之前，期初余额会汇总状态为 **已结算** 的交易记录和状态为 **未结算**，汇总金额的状态设置为 **未结算**。

通过第二项增强，您可以在总帐年终结算期间过帐详细的期初余额交易记录。 如果 **年终结算期间保留详细信息** 选项设置为 **是**，将为每个未结算的分类帐交易记录创建单独的期初余额。 此设置为分类帐结算设置中的每个主科目定义。 通过保留期初余额的详细交易记录，您可以显著提高在下一会计年度结算未结分类帐交易记录的能力。

为了支持新的增强功能，对分类帐结算和年终结算进行了更改。

### <a name="changes-to-ledger-settlement"></a>对分类帐结算的更改

- 分类帐结算必须在会计年度内完成。
- 必须对单个主科目中的交易记录进行分类帐结算。现在，主科目是 **分类帐结算** 页面的必需筛选器。
- 无法对已结算会计年度（换言之，已运行年终结算）内过帐的交易记录执行分类帐结算和分类帐结算冲销。

### <a name="changes-to-year-end-close"></a>对年终结算的更改

- 如果在下一会计年度已结算任何期初余额交易记录，则无法冲销年终结算。 当冲销年终结算或重新运行年终结算并且在总帐参数中 **在重新结算年份时删除现有年终条目** 选项设置为 **是** 时，此更改适用。
- 如果分类帐结算中任何资产负债表科目的 **年终结算期间保留详细信息** 选项设置为 **是**，将为该主科目创建更详细的期初余额交易记录。

## <a name="before-you-enable-the-feature"></a>启用此功能之前

由于功能和数据模型的更改，您必须先考虑以下几点，然后再启用此功能：

- 启用此功能后，已标记为要结算但尚未结算的所有交易记录将自动取消标记。 为防止任何工作丢失，应先结算所有已标记的交易记录，然后再启用此功能。
- 有些组织在同一会计年度多次运行年终结算。 如果年终结算已运行一次，将要在同一会计年度再次运行，则不要启用此功能。 此功能必须在您处理会计年度的第一次年终结算之前或处理最后一次年终结算之后启用。

  如果要启用此功能，但年终结算已运行一次，您必须先冲销年终结算，然后才能启用此功能。

- 由于不再允许跨会计年度结算，我们建议您在开始年终结算流程之前启用此功能。 然后，为了确保下一会计年度的期初余额不受以前的跨会计年度结算的影响，应为正在结算的会计年度结算期初余额交易记录。
- 由于不再允许跨主科目进行结算，应根据需要调整会计科目表或流程，以确保可以在同一主科目中完成分类帐结算。
- 如果正在使用公共部门年终结算流程，则无法启用此功能。

## <a name="set-up-ledger-settlement"></a>设置分类帐结算

启用此功能后，在运行下一个年终结算之前，每个组织必须确定是否在年终结算期间保留交易记录详细信息。 此选择不会影响上一年终结算流程中的期初余额过帐。

在 **分类帐结算设置** 页面上为每个主科目设置 **年终结算期间保留详细信息** 选项。

1.  转到 **总分类记帐** > **分类记帐设置** > **总分类记帐参数**。
2.  在 **分类帐结算** 选项卡上，选择 **分类帐结算科目**。

- 或者 -

1.  转到 **总帐** > **定期任务** > **分类帐结算**。
2.  选择 **分类帐结算科目**。

两列已添加到 **分类帐结算** 页面：
    
- **主科目类型** – 此列仅用于提供信息。 显示分配给主科目的类型。
- **在年终结算期间保留详细信息** – 默认情况下，此选项设置为 **否**。 只有 **主科目类型** 的值为 **资产负债表**、**资产** 或 **负债** 时，才可以设置为 **是**。 当此选项设置为 **否** 时，期初余额将在汇总中过帐，与年终结算期间的典型做法一样。 如果设置为 **是**，将为未为主科目结算的每个分类帐交易记录详细创建期初余额。

## <a name="year-end-close"></a>年终结算

当您通过转到 **总帐** > **期间结算** > **年终结算** 运行年终结算时，此流程将创建为分类帐结算定义的主科目的期初余额。 根据分类帐结算设置，以汇总或详细方式创建期初余额。 此流程不包括已结算的分类帐记录，无论您是汇总还是详细过帐每个主科目的期初余额。

例如，多个交易记录将过帐到 2021 会计年度的主科目 130100。

| 日记帐号 | 凭证  | 日期       | 类型      | 会计帐户 | 帐户名称        | Description       | 货币 | 金额(交易币种) | 金额  | 申报币种金额 |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 2021 年 12 月 3 日  | 正在操作 | 130100-001-    | 应收帐款 | 服务费       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 2021 年 12 月 5 日  | 正在操作 | 130100-002-    | 应收帐款 | 公用事业         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 2021 年 12 月 16 日 | 正在操作 | 130100-001-    | 应收帐款 | 退款            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 2021 年 12 月 20 日 | 正在操作 | 130100-002-    | 应收帐款 |                   | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 2021 年 12 月 20 日 | 正在操作 | 130100-002-    | 应收帐款 |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 2021 年 12 月 21 日 | 正在操作 | 130100-002-    | 应收帐款 | 科目的贷方 | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 2021 年 12 月 28 日 | 正在操作 | 130100-001-    | 应收帐款 | 公用事业         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 2021 年 12 月 29 日 | 正在操作 | 130100-002-    | 应收帐款 | 服务           | USD      | 300                            | 300     | 300                          |

在这些交易记录中，有三个在分类帐结算期间结算。

有 175 美元 (USD 175) 的发票。 此发票以欧元 (EUR) 支付，使用了现金折扣。

| 日记帐号 | 凭证  | 日期       | 类型      | 会计帐户 | 帐户名称        | Description | 货币 | 金额(交易币种) | 金额  | 申报币种金额 |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 2021 年 12 月 5 日  | 正在操作 | 130100-002-    | 应收帐款 | 公用事业   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 2021 年 12 月 20 日 | 正在操作 | 130100-002-    | 应收帐款 |             | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 2021 年 12 月 20 日 | 正在操作 | 130100-002-    | 应收帐款 |             | EUR      | -127.11                        | -174.12 | -174.12                      |

主科目 130100 的结果取决于是否在运行年终结算之前启用此功能。 如果已启用此功能，结果还取决于“在年终结算期间保留详细信息”选项的设置。

### <a name="the-feature-isnt-enabled"></a>此功能未启用
年终结算在 2022 年为主科目 130100 创建三个期初余额交易记录。 以记帐币种计的交易记录的总和为 USD 525。

| 日记帐号 | 凭证  | 日期     | 类型    | 会计帐户 | 帐户名称        | Description | 货币 | 金额(交易币种) | 金额  | 申报币种金额 |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-002-    | 应收帐款 |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-001-    | 应收帐款 |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-002-    | 应收帐款 |             | EUR      | -127.11                        | -174.12 | -174.12                      |

即使 EUR -127.11 的付款交易记录已完成分类帐结算，此交易记录仍作为期初余额向前结转。

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>功能已启用，“在年终结算期间保留详细信息”= 否

年终结算将在 2022 年为主科目 130100 创建两个期初余额交易记录。 以记帐币种计的交易记录的总和仍为 USD 525，但将从期初余额中排除分类算的交易记录。 科目 130100-002- 的总金额是 USD 125，而不是 USD 299.12，完全排除了 EUR 127.11/USD 174.12 的交易记录。

| 日记帐号 | 凭证  | 日期     | 类型    | 会计帐户 | 帐户名称        | Description | 货币 | 金额(交易币种) | 金额 | 申报币种金额 |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-002-    | 应收帐款 |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-001-    | 应收帐款 |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>功能已启用，“在年终结算期间保留详细信息”= 是

年终结算将在 2022 年为主科目 130100 创建五个期初余额交易记录。 将为未结算的五个交易记录中的每一个创建单独的期初余额交易记录。 以记帐币种计的交易记录的总和仍为 USD 525。

| 日记帐号 | 凭证  | 日期     | 类型    | 会计帐户 | 帐户名称        | Description       | 货币 | 金额(交易币种) | 金额 | 申报币种金额 |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-001-    | 应收帐款 | 服务费       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-001-    | 应收帐款 | 退款            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-002-    | 应收帐款 | 科目的贷方 | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-001-    | 应收帐款 | 公用事业         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | 期初 | 130100-002-    | 应收帐款 | 服务           | USD      | 300                            | 300    | 300                          |

保留交易记录详细信息时，原始的详细交易记录不会受到影响。 在正在结算的会计年度中，它们仍然处于已过帐但未结算状态。 将为期初余额创建这些交易记录的副本。 原始交易记录中的以下值将被复制到期初余额交易记录。

- 会计科目（主科目和所有财务维度）
- 以交易记录、会计和报告币种计的金额
- Description
- 过帐层
- 过帐类型

   > [!NOTE]
   > 不会为其他期初余额交易记录分配过帐类型。 因此，过帐类型可用于区分已详细结转的期初交易记录。

原始交易记录中的某些字段必须在期初余额详细交易记录中更改。 期初余额交易记录的日期始终是下一会计年度的第一天。 日记帐编号必须更改，凭证编号将更改为在年终结算对话框中输入的值。

原始交易记录中的信息可以在 **分类帐结算** 页面找到。 每个详细的期初余额交易记录都将在网格中显示 **原始交易记录日期** 列。 此列可以帮助您匹配新会计年度的交易记录。 您可以选择 **查看原始凭证** 来向后钻取到完整的原始凭证。

## <a name="settle-transactions"></a><a name="settle-transactions"></a>结算交易记录
若要结算分类帐交易，请执行以下步骤。

1. 转到 **总帐** > **定期任务** > **分类帐结算**。
2.  设置页面顶部的筛选器。

    1. 选择日期范围。 或者，选择日期间隔代码来自动填写日期范围。

       - 日期范围不能跨会计年度。 如果日期范围跨会计年度，当您选择 **显示交易记录** 时，将不会显示任何交易记录。
       - 如果日期范围处于未结会计年度，可以结算交易记录，并且可以冲销结算。 如果日期范围处于已结算会计年度，或者如果年终结算已完成，将会显示交易记录，但无法结算或取消结算交易记录。 您只能在已结算的会计年度中取消标记交易记录。 如果日期范围处于已结算会计年度，**标记所选项**、**结算已标记的交易记录** 和 **冲销已标记的交易记录** 按钮将不可用。

    2. 选择要显示其交易记录的主科目。 此字段是必填字段。 此查找将仅显示在公司会计科目表的 **分类帐结算** 页面上选择的主科目。
    3. 选择过帐层。 您无法结算不同过帐层中的交易记录。
    4. 要在单独的列中显示主科目和维度，请选择财务维度集。

3.  选择 **显示交易记录** 将显示与您设置的筛选器匹配的所有交易记录。 如果您更改任何筛选器或维度集，则必须再次选择 **显示交易记录**。
4.  选择行进行结算。 页面顶部的 **选定金额** 字段中的值将增加或减少来反映所选择行中的总金额。
5.  完成选择交易记录时，选择 **标记所选项**。 对于每个选择的交易记录，一个复选标记将在 **已标记** 列中显示。 此外，网格上方的 **标记金额** 字段中的值将增加或减少来反映标记的行中的总金额。
6.  在 **标记金额** 字段中的值是 **0**（零）时，选择 **结算已标记的交易记录**。

    - 不允许部分结算。 例如，您不能用 90 美元的贷方交易记录结算 100 美元的借方交易记录。 其余 10 美元贷方交易记录也必须标记为包含在结算中。
    - 输入结算日期。 此日期必须晚于标记为要结算的交易记录的最新日期。

标记的交易记录的状态将更新为 **已结算**。

> [!IMPORTANT]
> 您标记为要为有效法人和所选主科目结算的所有交易记录都将进行结算。 这些交易记录不一定会显示在页面上。 即使由于有筛选器被隐藏，它们也会完成结算。

有些流程（如交易记录冲销）会自动结算分类帐交易记录。 例如，在应收帐款中结算付款和发票，结算将生成已实现损益。 付款和发票的结算不会结算任何分类帐交易记录，如应收帐款会计科目的交易记录。 但是，如果付款和发票在应收帐款中未结算，在冲销应收帐款结算期间过帐的冲销会计条目将导致原始和冲销会计条目在总帐中进行分类帐结算。 启用 **区分分类帐结算与年终结算** 功能后，如果冲销日期位于其他会计年度，将不会自动发生冲销的分类帐结算。

## <a name="use-excel-for-ledger-settlement"></a>使用 Excel 进行分类帐结算

**分类帐结算** 页面上显示的交易记录可以导出到 Excel。 在 Excel 中，您可以进一步筛选交易记录以确定要标记进行结算的交易记录。
两个分类帐结算实体都只导出在 **分类帐结算** 页面上选择的主科目的分类帐交易记录。 虽然使用 Excel 仍可以标记或取消标记已结算会计年度的交易记录，但无法结算这些交易记录。 此外，还无法冲销该会计年度的已结算交易记录。

## <a name="make-transactions-easier-to-find"></a>让交易记录查找更加轻松

**分类帐结算** 页包括更便于您查看结算交易记录所需的功能。

•   使用 **已标记** 筛选器可以基于交易记录的 **已标记** 复选框是选中还是清除来筛选交易记录。
•   使用 **状态** 筛选器可以根据交易记录的状态筛选交易记录。
•   选择 **按绝对金额排序** 可以按绝对值对金额进行排序。 这样，您可以对具有相同金额的借方和贷方进行分组。

## <a name="reverse-a-settlement"></a>冲销结算

您可以冲销错误进行的结算。

1.  按照[结算交易记录](#settle-transactions)一节中的步骤 1 到 3 可以显示您感兴趣的交易记录。
2.  在 **状态** 筛选器中，选择 **已结算**。
3.  选择行进行冲销。
4.  选择 **冲销已标记的交易记录**。 具有相同结算 ID 的所有交易记录的状态将更新为 **未结算**。

> [!IMPORTANT]
> 具有相同结算 ID 的所有交易记录将全部冲销，即使未进行标记。 例如，已标记和结算了四个行。 所有四个行具有相同的结算 ID。 如果您标记这四个行中的一个，然后选择 **冲销已标记的交易记录**，这四个行将全部被冲销。





