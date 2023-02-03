---
title: 年终结算之前感知分类帐结算功能
description: 本文介绍如何在运行总帐年终结算流程之前使用“感知分类帐结算”功能。
author: kweekley
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832152"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>年终结算之前感知分类帐结算功能

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>准备年终结算之前分类帐结算感知功能

**区分分类帐结算与年终结算** 功能（**感知** 功能）的一个主要变化是不能跨会计年度进行分类帐结算。 此跨年度限制仅与分类账结算相关，与应收账款或应付账款结算无关。

在启用 **感知** 功能之前，将进行年终结算的会计年度不得有任何跨会计年度结算的分类帐交易。 具体而言，在已过帐到其他会计年度的交易中，任何已过帐到您运行年终结算的会计年度的交易都不能处于未结算状态。 然后，这些交易必须按照相同会计年度内的交易重新结算。

本文介绍识别、取消结算和重新结算跨会计年度结算的分类帐交易所需执行的步骤。 在提供的示例中，2021 会计年度已结帐，您准备运行 2022 会计年度的年终结帐。

## <a name="example-setup"></a>示例设置

下图显示了针对主科目 110190 过帐的交易。 绿色的分类帐交易在相同会计年度内进行过结算，无须更改。 红色的交易已进行了分类帐结算，但它们的交易日期在其他会计年度。 必须识别这些交易，并且可能必须撤销分类帐结算。

![分类帐交易记录。](./media/YEC1.png)

## <a name="example"></a>示例

如果您的组织想要在运行 2022 会计年度年终结算之前使用 **感知** 功能，请按照以下步骤操作。

> [!NOTE]
> 仅当新交易过帐到 2021 或更早会计年度时，才必须重新运行 2021 和更早会计年度的年终结算。 当您完成以下过程时，不会有新交易过帐到 2021 年。 因此，不必重新运行年终结算。
>
> 如果未针对已过帐到 2022 或更晚会计年度的交易对跨会计年度结算的分类帐交易进行结算，则它们仍然可以处于分类帐已结算状态。 例如，如果您跨 2019 年和 2020 年结算交易，则它们可以保持结算状态。

1. 可选：临时启用 **感知** 功能。

    - 如前所述，如果您选择启用该功能，则必须在后续步骤中将其禁用。 现在启用该功能的好处是您可以暂时阻止用户结算已过帐到不同会计年度的分类帐交易。
    - 如果您选择不启用该功能，我们建议您要求您的团队不要跨会计年度结算交易。 如果跨年度结算发生在以下步骤完成之后，那么您将必须重复这些步骤来识别和取消结算分类帐交易。

2. 在 **分类帐结算** 页面上，确定跨 2021 和 2022 会计年度结算的所有交易的总额。

    1. 指定整个 2021 会计年度的日期范围。 例如，如果您使用日历年作为会计年度，则输入 2021 年 1 月 1 日至 2021 年 12 月 31 日。

        如果启用了 **感知** 功能，您会收到一条警告，提示您无法为结束的会计年度结算或取消结算交易。 该警告不相关，因为在此步骤中没有发生结算或取消结算。

    2. 在 **状态** 字段中，选择 **已结算**。
    3. 一次筛选一个会计科目。

        - 您必须为发生分类帐结算的每个会计科目重复这些步骤。
        - 如果不再为分类帐结算设置其他会计科目，您可能必须临时将它们添加回分类帐结算设置k 。 如果这些分类帐科目在 2022 年有交易针对另一个会计年度中的交易进行结算，则完成这些步骤。

    4. 选择并按住（或右击）**状态** 列，然后选择按此列分组。
    5. 选择并按住 **金额(交易币种)** 列，然后选择对此列进行总计。

        - 如果您仅在 2021 年结算交易，则总数将为 0（零）。
        - 如果您有跨会计年度结算的交易，则总额不会为 0（零）。

        在下图中，余额为 $525.00。 此余额是针对其他会计年度中的交易结算的交易总数。 您的总数可能包括 2021 年至 2022 年之间结算的交易，以及 2022 年至 2023 年之间结算的交易。

        ![2021 - 2022 年的分类帐交易。](./media/YEC2.png)

    6. 通过进一步筛选 **结算日期** 值，确定哪些交易是在 2020 年至 2021 年之间结算的。 指定 2021 年 1 月 1 日到 2021 年 12 月 31 日的日期范围的筛选器。 未显示任何交易，因为未针对过帐到 2021 年的交易结算 2020 年的交易。
    7. 通过更改 **结算日期** 值的日期筛选器，确定哪些交易是在 2021 年至 2022 年之间结算的。 指定 2022 年 1 月 1 日到 2022 年 12 月 31 日的日期范围的筛选器。 系统会再次显示交易，总额为 $525.00，因为所有交易均在 2021 年至 2022 年之间结算。

3. 在 **分类帐结算** 页面上，确定跨 2021 和 2022 会计年度结算的所有交易的总额。

    1. 指定整个 2022 会计年度的日期范围。 例如，如果您使用日历年作为会计年度，则指定 2022 年 1 月 1 日至 2022 年 12 月 31 日。
    2. 在 **状态** 字段中，选择 **已结算**。
    3. 一次筛选一个会计科目。
    4. 选择并按住（或右击）**状态** 列，然后选择按此列分组。
    5. 选择并按住（或右击）**以交易币种表示的金额** 列，然后选择对该列进行总计。

        ![分类帐交易总金额。](./media/YEC3.png)

    6. 添加额外的 **结算日期** 值筛选器。 指定 2022 年 1 月 1 日到 2022 年 12 月 31 日的日期范围的筛选器。 此时会显示相同的 $525.00 总额。 此结果证实了跨 2021 年和 2022 年结算的交易总额为 $525.00。

        ![2022 年和 2023 年中结算日期的分类帐交易。](./media/YEC4.png)

    7. 更改额外的 **结算日期** 值筛选器。 指定 2023 年 1 月 1 日到 2023 年 12 月 31 日的日期范围的筛选器。 此时会显示新的 $700 总额。 该总额是跨 2022 年和 2023 年结算的交易总额。
 
4. 对 2023 财年重复步骤 3。 总额应与 2022 年的 $700 一致，因为没有对照 2024 年的交易来结算 2023 年的交易。
5. 如果您在第 1 步中启用了 **感知** 功能，请在继续第 6 步之前将其禁用。 在后续步骤中，您将冲销跨会计年度的分类账结算。 如果启用了 **感知** 功能，则 2021 会计年度的分类帐结算无法冲销。 因此，您必须在继续之前禁用该功能。
6. 禁用 **感知** 功能后，请在 **分类帐结算** 页面上使用相同的筛选器来冲销详细交易的分类帐结算。

    1. 返回 **分类帐结算** 页面，筛选 2021 年的交易日期。 添加额外的 **结算日期** 值筛选器。 指定从 2022 年 1 月 1 日到 2022 年 12 月 31 日的日期范围的筛选器。 然后查找构成 $525 总额的详细交易。 筛选此信息可能并不容易。 您可能需要将数据发送至 Microsoft Excel 以对其进行评估。
    2. 有了交易列表后，请在 **分类帐结算** 页面上选择分类帐交易，然后选择 **标记所选项**。 您不必查看已结算的分类账交易的双方。 如果您标记借方或贷方，则具有相同 **结算 ID** 值的所有内容都将被冲销，即使 **标记的金额** 值不是 **0** （零）也是如此。
    3. 选择 **冲销标记的交易** 来取消结算交易。

    ![冲销已标记的交易。](./media/YEC5.png)

7. 重复第 6 步，对跨 2022 年和 2023 年结算的交易进行结算冲销。

    ![冲销分类帐交易。](./media/YEC6.png)

8. 过帐调整总帐，将 2022 年的期初余额分成两个金额：针对 2021 会计年度交易结算的部分和 2022 年尚未结算的部分。

    - **对上一年结算的期初余额部分：** 第一个金额为 $525，基于所发现的跨 2021 年和 2022 年结算的总额。
    - **对上一年结算的期初余额部分：** 第二个金额为期初余额与结算金额 $525 的差额。 余额为 $1025 – $525 = $500。

    您可以用这种方法按照最初对 2021 年的交易结算的 $525 来结算 2022 年的交易。 必需执行此步骤，因为分类帐结算不允许部分结算。

    1. 转到总帐，然后过帐调整额。 您的组织必须根据未结的期间来决定要使用的交易日期。 这些交易可能已使用 2022 年 1 月或 2 月的结算日期进行了结算，但如果那是唯一的未结期间，则可能必须在 12 月对调整额进行过帐。
    2. 您可能需要在 **主科目** 页面上暂时关闭 **不允许手动输入** 参数。 如果主科目不允许手动输入，则不会过帐此调整额。

    ![未过帐调整额。](./media/YEC7.png)

9. 您现在可以重新结算未结算的交易。 返回到 **分类帐结算** 页面，将日期范围限定为 2022 年 1 月 1 日至 2022 年 12 月 31 日。 下图显示了现存的未结算交易。

    ![未结算的交易。](./media/YEC8.png)

    - 可以针对 -$1,025 的调整额结算 $1,025 的期初余额。
    - 可以对照 $525.00 的调整额对未结算的 -$400、-$50 和 -$75 的详细交易进行结算。

    ![详细交易。](./media/YEC9.png)

10. 启用 **感知** 功能。 您现在已准备就绪，可以运行年终结算。

    - 在运行年终结算之前，考虑在所有资产负债表科目的分类帐结算设置中选择 **保留详细信息** 选项。 有关完成此步骤的好处的更多信息，请参阅感知文档。
    - 当您开始进行 2022 年年终结算时，如果仍然发现跨会计年度结算的交易，年终结算流程将立即通知您。
    - 如果仍然结算 2021 年和 2022 年的交易，您将必须再次禁用 **感知** 功能，并重复之前的步骤来取消交易。 之所以需要采用这种方法，是因为 2021 年已结束，并且无法在已结束的会计年度中取消结算交易。
    - 如果仍然结算 2022 年和 2023 年的交易，则您 **不** 必禁用 **感知** 功能。 因为 2022 年和 2023 年都没有结束，所以您可以使用前面的步骤来取消结算交易。

成功运行 2022 年年终结算后，您可以从现在开始启用 **感知** 功能。