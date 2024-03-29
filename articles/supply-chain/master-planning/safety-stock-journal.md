---
title: 使用安全存货日记帐更新最小物料覆盖范围
description: 本文介绍如何使用安全存货日记帐通过基于历史交易计算最小覆盖范围方案来更新物料的安全存货数量。
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 385144738b83fcf6873eae5204b4784d6ecd5b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851759"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>使用安全存货日记帐更新最小物料覆盖范围

[!include [banner](../../includes/banner.md)]

安全存货是指为帮助降低物料库存不足的风险，在库存中应该持有该物料的额外数量。 安全存货用于当接到销售订单，但供应商无法满足客户的要求装运日期时的缓冲。

本文介绍如何使用安全存货日记帐根据历史交易计算最小覆盖范围方案，然后使用这些方案更新物料覆盖范围。

## <a name="overview-of-minimum-coverage-usage"></a>最小覆盖范围使用概述

安全存货在 **物料覆盖范围** 页上为每个物料设置。 不同类型的补货由不同的覆盖范围代码表示。 （有关详细信息，请参阅 [物料的安全存货履行](safety-stock-replenishment.md)。）但是，所有覆盖范围代码都使用在 **物料覆盖范围** 页上的 **最小** 字段中为每个物料设置的值。 使用 **最小** 字段有两种主要方法：

- **用于最小/最大目的的最小数量** – 此方法将最小数量与最小/最大逻辑一起使用。 当相关物料或覆盖范围组的 **覆盖范围代码** 字段被设置为 *最小/最大* 时适用此方法。 **最小** 数量表示平均每日使用量乘以物料的提前期。
- **用于库存计划目的的最小数量** – 此方法使用最小数量表示库存计划与需求预测相结合。 当相关物料或覆盖范围组的 **覆盖范围代码** 字段被设置为 *期间* 或 *要求* 时适用此方法。 **最小** 数量表示的库存计划反映所需的客户服务级别，以帮助减少缺货、部分装运和交货提前期。 最小数量反映给定物料的预测准确度百分比。 它不表示所需的库存位置。

**最小** 值可以通过三种方式设置：

- 在 **物料覆盖范围** 页上手动设置
- 通过数据管理框架（*物料覆盖范围* 数据实体）
- 通过安全存货日记帐进行的安全存货计算

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>根据历史使用情况计算最小覆盖范围

安全存货日记帐用于根据物料的历史使用情况计算建议的最小数量，用于最小/最大目的或库存计划目的。 历史使用情况表示指定期间内的所有发货交易。 这些发货交易包括销售订单交易和库存调整。 此计算还确定建议的最小数量对库存值的影响，以及与当前最低数量相比库存值的变化。

每个安全存货日记帐行表示一个物料及其覆盖范围维度。 这些日记帐行在 **安全库存货记帐行** 页面上创建和显示（**主计划 \> 主计划 \> 运行 \> 安全存货计算**）。 本文稍后将介绍使用安全存货日记帐计算建议的最小数量的业务流程。

规划员使用安全存货日记帐根据选定期间的历史使用情况计算选定物料的建议最小数量。 建议的最小值可以根据需要手动替代，您可以查看建议的最小值对库存值的潜在影响。 过帐日记帐时，物料覆盖范围中关联的最小数量会自动更新。

### <a name="create-a-new-safety-stock-journal-name"></a>新建安全存货日记帐名称

您必须至少创建一个安全存货日记帐名称，然后才能生成此类日记帐。 您通常将使用多个日记帐名称来帮助区分安全存货计算。

1. 转到 **主计划 \> 设置 \> 安全存货日记帐名称**。
1. 在操作窗格上，选择 **新建**。
1. 在新行上，设置以下字段：

    - **名称** – 为日记帐输入一个简短名称。
    - **描述** – 输入日记帐的描述。
    - **用户组专用** – 要限制当前日记帐名称的受众，选择一个用户组。
    - **过帐后删除行** – 选中此复选框可在过帐时默认清理日记帐行。 通过清除来保留所有已过帐的行。

    **日记帐类型** 字段是只读的，预设为 *安全存货*。

1. 关闭该页面。

### <a name="create-a-safety-stock-journal-and-lines"></a>创建安全存货日记帐和行

此步骤将创建日记帐并自动向其中添加行。 每一行标识一个物料、物料的覆盖范围维度和使用情况历史记录中的若干个计算出的数量。 计算出的数量包括每个物料提前期的平均发货量、每月平均发货量和每月标准偏差。

#### <a name="automatically-generate-journal-lines"></a>自动生成日记帐行

仅当当前显示的日记帐不存在任何行时，才能自动生成日记帐行。

按照以下步骤自动生成日记帐行。

1. 转到 **主计划 \> 主计划 \> 运行 \> 安全存货计算**。
1. 在操作窗格上，选择 **新建**。 新的安全存货日记帐已创建。
1. 在 **日记帐标头详细信息** 快速选项卡上，设置以下字段：

    - **名称** – 选择要添加行的安全存货日记帐名称。
    - **描述** – 默认值是您选择的日记帐名称的描述。 但是，您可以根据需要编辑此值。
    - **过帐后删除行** – 选中此复选框可在过帐时清理日记帐行。 通过清除来保留所有已过帐的行。 此设置继承自所选日记帐名称。

    **日记帐** 字段是只读的，显示您正在创建和添加行的日记帐的 ID 号。

1. 在 **日记帐行** 快速选项卡上，在工具栏上选择 **创建行**。
1. 在 **为建议的最小库存级别创建日记帐行** 对话框中，设置以下字段：

    - **开始日期** – 选择应在计算中包括发货的期间的开始日期。
    - **结束日期** – 选择应在此计算中包括发货的期间的结束日期。 开始日期和结束日期之间必须至少相隔两个月。
    - **计算标准偏差** – 将此选项设置为 *是* 将计算标准偏差。 您必须将此选项设置为 *是*，才能在计算建议时使用 **使用服务级别** 选项（如本文后面所述）。

1. 在 **要包括的记录** 快速选项卡上，您可以设置筛选器和约束来定义包含哪些物料。 （例如，您可以按 **覆盖范围组** 值筛选。）选择 **筛选器** 打开标准查询编辑器对话框，您可以在其中定义选择条件、排序条件和联接。 这些字段的工作方式与它们用于 Microsoft Dynamics 365 Supply Chain Management 中其他类型的查询时一样。
1. 在 **在后台运行** 快速选项卡上，选择是否应该以批处理模式运行作业，和/或设置定期计划。 这些字段的工作方式与它们用于 Supply Chain Management 中其他类型的[后台作业](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)时一样。
1. 选择 **确定**。 将为包含库存交易记录的维度创建行。

#### <a name="manually-add-or-remove-journal-lines"></a>手动添加或删除日记帐行

您可以随时手动添加和/或删除日记帐行（在自动生成行之后或代替自动生成行）。 使用 **日记帐行** 快速选项卡工具栏上的以下按钮：

- **新** – 添加新行。 然后在每列中输入一个值来定义要计算和应用新的最小值的产品。 由于建议的最小计算不能用于手动添加的行，因此不会为它们显示新的 **计算所得的最小数量** 值。 因此，您必须手动输入 **新的最小数量** 值。 不过，您仍然可以查看 **新的最小数量** 值对库存值的潜在影响，以及与当前指定的最小值相比库存的潜在变化。
- **删除** – 删除选中的行。
- **删除日记帐行** – 删除日记帐中的所有行。

### <a name="calculate-a-proposal"></a>计算建议值

此步骤计算每个日记帐行的建议最小值以及该行对库存值的潜在影响。 （建议的最小值显示为 **计算所得的最小数量** 值。）您可以根据需要多次进行计算。 计算将更新为所有日记帐行显示的 **计算所得的最小数量** 值。

除非您在操作窗格中选择 **过帐**，否则显示的计算不会影响每个产品的实际最小数量值。 这个时候，**新的最小数量** 值将应用于每个产品。

1. 转到 **主计划 \> 主计划 \> 运行 \> 安全存货计算**。
1. 打开要计算建议值的日记帐。 或者，按照本文前面所述创建新日记帐。
1. 在 **日记帐行** 快速选项卡上，在工具栏上选择 **计算建议值**。 （您不必选择任何行。）
1. 在 **计算最低库存级别的建议值** 对话框中，设置以下字段：

    - **使用提前期的平均发货量** – 选择此选项可根据指定期间内的平均发货量生成 **计算所得的最小数量** 值。 然后，在 **倍增系数** 字段中，输入一个值以根据需要调整结果。 例如，输入 *1.0* 以使用精确计算的平均值或输入 *1.1* 以添加 10% 的额外缓冲。
    - **使用服务级别** – 选择此选项可根据所需的服务级别计算建议的最小值。 然后，在 **服务级别** 字段中，选择您的首选服务级别。
    - **提前期宽限期**– 输入一个值以延长正常提前期（例如，考虑管理时间）。
    - **使用计算所得的最小数量作为新的最小数量** – 将此选项设置为 *是* 将在计算完成后自动将值从所有行的 **计算所得的最小数量** 列复制到 **新的最小数量** 列。 如果将此选项设置为 *否*，会将所有行的 **当前最小数量** 值复制到 **新的最小数量** 列。 然后，您必须根据需要手动编辑 **新的最小数量** 值。

1. 在 **在后台运行** 快速选项卡上，选择是否应该以批处理模式运行作业，和/或设置定期计划。 这些字段的工作方式与它们用于 Supply Chain Management 中其他类型的[后台作业](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)时一样。
1. 选择 **确定**。 计算结果将显示在 **日记帐行** 快速选项卡上的 **计算所得的最小数量** 列中。 目前，这些值只是尚未应用于您的产品的建议值。

### <a name="update-minimum-quantity"></a>更新最小数量

您可以选择安全存货日记帐中的任何行并手动替代其 **新的最小数量** 字段的值。

1. 转到 **主计划 \> 主计划 \> 运行 \> 安全存货计算**。
1. 打开要编辑的日记帐。 或者，按照前面所述创建新日记帐。
1. 在 **日记帐行** 快速选项卡上，找到要调整的行，然后在 **新的最小数量** 列中编辑值。 例如，您可以设置 **新的最小数量** 值，使其与 **计算所得的最小数量** 值匹配。 如果 **计算所得的最小数量** 值 *0*（零），您可以输入所需的将来值。

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>发布新的最小数量和验证结果

按照以下步骤过帐新的最小数量并验证结果。

1. 转到 **主计划 \> 主计划 \> 运行 \> 安全存货计算**。
1. 打开要过帐新的最小数量的日记帐。 或者，按照前面所述创建新日记帐。
1. 在操作窗格上，选择 **过帐**。
1. 在 **过帐日记帐** 对话框中，根据需要设置 **将所有错误过帐至一个新日记帐** 字段。 然后选择 **确定** 过帐日记帐。
1. 如果您在 **日记帐行** 快速选项卡上更改了行的 **新的最小数量** 值，您可以通过以下步骤确认更改：

    1. 对于您编辑的行，选择 **物料编号** 列中的链接。
    1. 在 **产品信息** 对话框中，选择 **物料编号** 字段中的链接，打开相关的已发布产品记录。
    1. 在操作窗格上，在 **计划** 选项卡上的 **覆盖范围** 组中，选择 **物料覆盖范围**。
    1. 请注意，您使用已过帐的安全存货日记帐调整的站点和仓库的 **最小** 值现已更新以匹配您进行的编辑。

## <a name="additional-resources"></a>其他资源

- [物料的安全存货履行](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
