---
title: 创建计费计划
description: 本文说明如何创建、删除和编辑计费计划。
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903383"
---
# <a name="create-billing-schedules"></a>创建计费计划

[!include [banner](../includes/banner.md)]

在 **计费计划** 页面上，您可以创建、删除或编辑计费计划。 您还可以查看计费计划列表。 创建计费计划时，其默认值由与其关联的计费组确定。 其他信息在 **定期合同计费参数** 页面设置。

## <a name="create-a-billing-schedule"></a>创建计费计划

要创建计费计划，请按照以下步骤操作。

1. 在 **计费计划** 页面上，选择 **新建**。
2. 在 **创建计费计划** 对话框的 **计费计划组** 字段中，选择一个计费计划组。
3. 在 **客户帐户** 字段中，选择一个客户帐户。
4. 在 **开始日期** 字段中，选择开始日期，然后在 **周期数** 字段中输入周期数。 **结束日期** 字段会根据您输入的周期数进行更新。 如果您更新 **计费结束日期** 字段，**周期数** 字段将更新为 **0**（零）。
5. 选择 **确定**。
6. 在 **计费计划** 页面，在 **常规** 选项卡的 **说明** 字段中，输入计费计划的说明。
7. 在 **里程碑模板** 字段中，为 **里程碑开票** 选择里程碑模板。

**发票帐户** 和 **货币代码** 等字段会根据客户的信息进行更新。

**记帐频率** 和 **记帐间隔** 字段将根据所选计费计划组自动设置。

8. 要创建单独的发票，将 **单独开票** 选项设置为 **是**。
9. 要在最终计费周期后自动续订计费计划，请将 **自动续订** 选项设置为 **是**，然后设置 **按续订添加行** 字段。

**参数** 字段将根据 **定期合同计费参数** 页面上的值自动设置。

10. 要按比例分配计费计划的金额，将 **按比例分配部分期间** 选项设置为 **是**。
11. 要将计费计划详细信息行与月末保持一致，将 **与月份对齐** 选项设置为 **是**。
12. 在 **合同开始日期** 和 **合同结束日期** 字段中，输入合同的开始日期和结束日期。 这些日期仅用于提供信息。

**付款** 字段显示来自客户的客户付款信息。 当行物料处于暂停或终止状态时，无法更改付款信息。

> [!NOTE]
> 当您按项目合并发票时，**付款期限**、**方式** 和 **计费计划** 字段的值必须匹配。 否则，无法合并发票。

13. 在 **地址** 选项卡上，您可以查看和更新 **交货地址** 和 **帐单邮寄地址** 字段。
14. 在 **联系人信息** 选项卡上，您可以将最终用户帐户与计费计划相关联。
15. 在 **联系人信息** 字段中，您可以输入联系人、电子邮件地址和 Internet 地址。
16. 要跟踪合作伙伴佣金信息，请设置 **合作伙伴帐户** 和 **合作伙伴佣金比率** 字段。 这些字段仅用于提供信息。
17. 在 **总计** 选项卡上，您可以查看为计费计划计算的各项总计。
18. 在 **暂停** 选项卡上，您可以查看有关在取消暂停后何时暂停计费计划的审计信息。
19. 在 **终止** 选项卡上，您可以查看应用到计费计划或从计费计划中删除的终止历史记录。
20. 选择 **保存**。
21. 在 **计费计划行** 快速选项卡上，选择 **添加行**。
22. 在 **物料编号** 字段中，选择物料编号。 如果添加的物料是收入拆分中的父物料，行会自动更新子物料。 您只能编辑收入拆分中的父物料。 然后所有子物料会相应更新。
23. 在 **物料类型** 字段中，选择物料类型。
24. 更新开始日期和结束日期。
25. 在创建发票之前，您可以通过更新 **记帐频率** 字段来更改记帐频率。 创建计费计划的第一个发票后，将无法更改记帐频率。
26. 在 **单位** 字段中，选择物料的度量单位。
27. 在 **定价方法** 字段中，选择物料的定价方法。

**单价** 字段将根据库存自动设置。 但是，如果您将定价方法更改为 **统一**，则可以对其进行更新。

## <a name="remove-a-line-item"></a>删除行物料

要从计费计划中删除物料，请按照这些步骤操作。

1. 在 **计费计划** 页面的 **计划编号** 字段中，选择要编辑的计费计划的编号。
2. 在 **计费计划行** 快速选项卡上，选择要删除的行，然后选择 **删除**。
3. 选择 **保存**。

本文的其余部分介绍可用于 **计费计划行** 快速选项卡上的行的操作和详细信息。

## <a name="billing-schedule-line-actions"></a>计费计划行操作

**计费计划行** 快速选项卡上的按钮可让您对各个行应用操作。

| 纽扣 | Description |
|--------|-------------|
| 添加行 | 在计费计划中添加行。 |
| 从物料列表中添加 | 通过在列表中选择多个物料，将它们添加到计费计划中。 |
| 移动 | <p>从计费计划中删除选定的行。</p><p>对于属于收入拆分的物料，只能删除父物料。 然后会自动删除所有关联的子物料。</p> |
| 查看计费明细 | 查看计费明细。 |
| 终止雇用 | <p>终止选定的行。 仅当所选行的状态为 **活动** 时，此按钮才可用。</p><p>对于属于收入拆分的物料，只能终止父物料。</p> |
| 删除终止项 | <p>从所选行取消终止。 仅当所选行的状态为 **已终止** 时，此按钮才可用。</p><p>对于属于收入拆分的物料，只能从父物料取消终止。</p> |
| 暂停 | <p>选择将所选行置于暂停状态的详细信息。</p><p>对于属于收入拆分的物料，只能将父物料置于暂停状态。</p> |
| 解除暂停 | <p>从选定的行取消暂停。</p><p>对于属于收入拆分的物料，只能从父物料取消暂停。</p> |
| 呈报和折扣 | 此按钮不能用于收入拆分中的物料，但收入拆分使用 **零金额** 分配方法的父物料除外。 |
| 延期 | <p>为所选行输入延期选项。</p><p>此按钮对收入拆分中的父物料不可用。</p> |
| 里程碑分配 | <p>查看和更新选定行的里程碑分配信息。</p><p>仅当计费计划行物料是里程碑物料时，此按钮才可用。</p> |
| 支持和续订 | <p>查看和更新选定行的支持和续订信息。</p><p>仅当计费计划行物料是支持和续订物料时，此按钮才可用。</p> |
| 显示维度 | 显示或隐藏出现在 **计费计划行** 网格中的维度列。 |
| 计算单价 | <p>计算物料的单价，以便客户可以分期支付合同金额（例如，每天、每月、每季度、每半年或每年）。 您可以选择合同价格和价格频率。</p><p>您可以查看更改的审核线索：旧合同价格和频率、新合同价格和频率、进行更改的用户以及更改的日期和时间。</p> |
| 对齐日期 | <p>指定续订物料的对齐日期。</p><p>如果您在 **物料组** 字段中选择物料组，所有物料都将使用计费计划中物料组中第一个物料的对齐日期。 如果 **物料组** 字段为空，您可以指定用于所有物料的对齐日期。</p><p>此按钮仅当 **记帐频率** 字段设置为 **每年** 时才可用。</p> |
| 未计费收入 | <p>将物料设置为使用未计费收入功能。 然后，您可以指定物料的未计费收入和未计费折扣帐户。</p><p>此按钮仅对 **物料类型** 字段设置为 **标准** 的物料可用。 对现有计费计划或已创建发票的计费计划行不可用。</p> |
| 添加收入分成子项 | <p>选择要添加到销售订单的子物料。</p><p>此按钮仅对收入拆分中的父物料可用。</p> |
| 高级定价选项 | 编辑物料的定价选项。 |

## <a name="billing-schedule-line-details"></a>计费计划行详细信息

当您在 **计费计划行** 快速选项卡中选择一行时，您可以查看该行的具体详细信息。 这些详细信息分为不同的选项卡。

### <a name="general-tab"></a>常规选项卡

**常规** 选项卡上提供以下信息。

| 字段或部分 | Description |
|------------------|-------------|
| 使用 | <p>此部分提供有关使用物料的信息。 包含以下字段：</p><ul><li>**使用标识符** – 计量或使用物料的标识符。</li><li>**读取选项** – 使用情况读取选项：**读取** 或 **消耗**。</li><li>**估计消耗量** – 指定具有未创建发票期间的使用物料的估计消耗量。 在 **计费明细** 页上，您可以查看估计消耗量的计费明细行。</li></ul> |
| 外部引用\* | 此部分包含 **外部** 和 **行号** 字段，您可以在其中指定外部参考信息。 |
| 里程碑 | <p>此部分提供有关里程碑物料的信息。 包含 **估计完成日期** 字段，显示物料完成日期。</li></ul> |
| 文本 | 行的注释。 文本将翻译为客户或法人的默认语言。 |
| 物料组 | 行物料的物料组。 |
| 对齐日期 | 计费计划的对齐日期。 |

\* 当您在 **生成发票** 页面上按物料合并发票时，**外部参考** 字段必须匹配。 即使有一个字符不同，物料也不会在发票上合并。 **外部参考** 部分中的字段均不进行验证检查，**行号** 字段中的值必须为正整数。

### <a name="address-tab"></a>“地址”选项卡

**地址** 选项卡上提供以下信息。

| 字段 | Description |
|-------|-------------|
| 交货地址 | <p>选择行物料的交货地址。 默认交货地址是 **地址** 快速选项卡中的主要交货地址。</p><p>更改地址时，可以选择以下地址选项：</p><ul><li>**地址** – 为当前客户选择地址。</li><li>**使用中** – 选择目前用于当前客户的地址。</li><li>**其他地址** – 为任意客户记录选择地址。</li></ul><p>对于使用收入拆分的物料，只能编辑父物料的地址。 子物料的地址与父物料的地址匹配，不能单独编辑。</p> |
| 帐单邮寄地址 | <p>选择行物料的帐单邮寄地址。 默认交货地址是 **地址** 快速选项卡中的主要交货地址。 您可以根据可用地址的用途，根据需要更改地址：</p><ul><li>如果没有地址具有 **发票** 用途，默认的帐单邮寄地址将是客户的主要地址，而不管其用途如何。</li><li>如果一个或多个地址的用途是 **发票**，默认的帐单邮寄地址是最近输入的地址。</li><li>如果一个或多个地址的用途为 **发票**，并且其中一个发票地址设置为主地址，默认的帐单邮寄地址将具有 **发票** 用途，将被设置为主要地址。</li><li>对于使用收入拆分的物料，只能编辑父物料的地址。 子物料的地址与父物料的地址匹配，不能单独编辑。</li></ul> |

### <a name="product-tab"></a>“产品”选项卡

**产品** 选项卡上提供以下信息。

| 字段或部分 | Description |
|------------------|-------------|
| 存储维度 | <p>此部分显示物料的存储信息。 包含 **序列号** 字段，该字段显示物料的序列号。</p><p>此序列号在支持和续订过程中从初始销售订单复制。 对于使用收入拆分的物料，父物料的序列号将被复制到所有子物料。 当 **定期合同计费参数** 页面上的 **复制序列号** 选项设置为 **是** 时，将复制序列号。</li></ul> |
| 产品维度 | 物料的产品详细信息和值会根据为计费计划行选择的 **变型编号** 值自动更新。 |

### <a name="account-tab"></a>“帐户”选项卡

**帐户** 选项卡上提供以下信息。

| 字段 | Description |
|-------|-------------|
| 主帐户 | 在销售行上创建的主帐户。 默认值来自销售订单。 此字段可留空。 |
| 物料财务维度 | <p>基于客户和物料记录的默认财务维度值。</p><p>对于使用收入拆分的物料，子物料使用客户和物料记录的财务维度值，如前所述。 如果必须更新子物料的财务维度值，可以导入数据实体。</p> |

### <a name="renewals-tab"></a>“续订”选项卡

**续订** 选项卡上提供以下信息。

| 字段 | Description |
|-------|-------------|
| 自动续订 | <p>指示计费计划行是否为下一个计费周期自动续订的值：</p><ul><li>**是** – 当您创建发票时，会自动为下一个计费周期续订计费计划行。</li><li>**否** – 不自动续订计费计划行。 必须手动续订计费计划。</li></ul> |
| 每次续订要添加的行 | 要添加到计费计划续订的行数。 |

此外，**续订** 选项卡还提供以下按钮。

| 纽扣 | Description |
|--------|-------------|
| 未计费的收入日记帐条目审计 | 查看使用未计费收入功能的物料的所有更改。 |
| 添加续订期限 | 为物料添加续订期限。 新续订期限的开始日期是上一期限结束日期之后的下一个日期。 **续订结束日期**、**延期开始日期**、**延期结束日期**、**物料数量** 和 **单价** 字段可以更新。 |
| 修改续订期限 | <p>修改续订期限。 对于初始期限，您可以在创建初始日记帐条目之前更改延期开始和结束日期。 对于后续期限，无法更改开始日期。 开始日期始终是上一个期限结束之后的下一个日期。</p><p>如果在您修改的期限之后存在续订期限，则无法更改该期限的日期。 在这种情况下，只能更新续订物料的 **数量** 和 **单价** 字段。</p><p>例如，存在三个期限。 <ul><li>无法更改第一个期限，因为它已经开始。</li><li>对于第二个期限，只能更改数量和单价。</li><li>对于第三个期限，可以更改除开始日期之外的所有值。 此外，**通过模板计划** 选项可让您基于未计费收入物料的模板创建延期计划。 当此选项设置为 **是** 时，在 **模板** 字段中选择延期模板，然后根据需要更改延期开始和结束日期。 后续续订期限将使用相同的延期模板。 不过，延期模板可以更改。</p></li></ul> |

### <a name="termination-tab"></a>“终止”选项卡

**终止** 选项卡上提供以下信息。

| 字段 | Description |
|-------|-------------|
| 终止日期 | 计费计划行终止的日期。 默认值来自标头上的 **终止日期** 字段。 您可以根据需要更改此值。 |
| 终止类型 | 终止类型。 默认值来自标头上的 **终止类型** 字段。 |

### <a name="hold-tab"></a>“暂停”选项卡

如果使用收入和费用延期，**暂停** 选项卡将显示延期日期。

### <a name="escalation-and-discount-tab"></a>“升级和折扣”选项卡

**升级和折扣** 选项卡上提供以下信息。

| 字段 | Description |
|-------|-------------|
| 呈报 | <p>选择是否允许计费计划行升级。 创建计费计划行时，将应用标头中的任意升级行。</p><ul><li>**是** – 可以对行应用升级。 选择此选项后，您可以在 **升级和折扣** 页面设置计费计划行的升级。</li><li>**否** – 不能对行应用升级。</li></ul><p>默认设置基于所选的 **计费计划组**。</p> |

### <a name="price-changes-tab"></a>“价格更改”选项卡

对于从 **标准** 价格更改为 **统一** 价格的行，**价格更改** 选项卡上的网格包括以下列：

- 更改日期
- 被用户更改
- 标准价格
- 统一价格
- 价格更新
