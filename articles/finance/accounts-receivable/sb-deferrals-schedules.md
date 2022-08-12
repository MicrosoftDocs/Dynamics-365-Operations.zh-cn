---
title: 收入和费用延期中的延期计划
description: 本文介绍收入和费用延期中的延期计划。
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: 093005f9b66d7ce741689b55612f006fa5123910
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903354"
---
# <a name="deferral-schedules"></a>延期计划

延期计划在过帐交易记录后创建。

您可以使用 **所有延期计划** 或 **有效延期计划** 页面查看延期计划的详细信息。 显示的信息取决于延期计划的类型（直线或基于事件）和交易记录类型。 其中包括延期计划行和延期计划的总金额。 您可以使用此页面修改延期计划。

## <a name="recognize-revenue"></a>确认收入

> [!NOTE]
> - 要确认一个延期计划的收入，请从步骤 1 开始。
> - 要确认多个延期的收入，请从步骤 2 开始。

1. 在 **所有延期计划** 页面的 **计划行** 网格中，选择您要确认的行，然后选择 **确认**。
2. 在 **确认处理** 页面上，将 **确认操作** 字段设置为 **创建确认日记帐**。
3. 在 **截止日期** 字段中，选择截止日期。 处理将仅包括结束日期早于或与所选截止日期相同的行。
4. 选择 **筛选器**，然后添加数据过滤器，以使列表仅显示您需要的记录范围。
5. 选择 **查看预览** 查看行。
6. 在行列表中，选择您不想处理的任何行，然后选择 **删除**。
7. 选择是否要汇总确认日记帐条目。
8. 在 **交易记录日期** 部分，您可以使用特定日期替代交易记录日期来处理该交易记录。 可以为已关闭期间指定交易记录日期。
9. 要作为批处理的一部分进行处理，选择 **批处理**。 在 **批处理** 对话框中，设置批处理参数，然后选择 **确定** 返回 **确认处理** 页面。 收入确认将在稍后处理批处理时处理。
10. 选择 **流程**。 如果您未将交易记录添加到批处理，将立即处理所有行。 否则，将在处理批处理时处理行。

## <a name="modify-a-schedule"></a>修改计划

要修改计划，请按照以下步骤操作。

1. 在 **所有延期计划** 页面上，选择延期计划，然后选择 **会计 \> 修改计划**。
2. 在 **修改计划** 页面上，编辑要更改的选项。 根据延期计划，您将无法编辑所有选项。
3. 选择 **预览** 查看对延期计划的更改。
4. 选择 **确定**。

### <a name="straight-line-deferral-schedules"></a>直线延期计划

如果延期计划没有已确认或外部过帐的行，您可以修改整个延期计划，包括开始日期。

如果延期计划有任何已确认或外部过帐的行，在您修改延期计划时，延期计划的结果行为取决于重新计算日期和已确认行的延期结束日期。 默认情况下，未确认的第一个期间确定延期结束日期。

要使用确认日期，在 **计划开始** 字段中选择以下值之一： 
- **跟进** – 重新计算所有已确认行后的金额。
- **冲销** – 使用指定的日记帐名称和过帐日期对重新计算日期之后的任何行进行冲销。 重新计算日期之后的金额然后会重新计算。

如果使用模板，将忽略跳过的期间，模板将仅用于计算结束日期。

### <a name="event-based-deferral-schedules"></a>基于事件的延期计划

对于基于事件的延期计划，您可以修改所有未确认的行。

如果延期计划有任何已确认或外部过帐的行，您无法修改延期计划的模板和分配类型。 当您修改现有的延期计划时，您无法更改 **按单位创建单独事件** 字段的值。

如果行已确认或在外部过帐，**已确认** 复选框将被选中。

## <a name="modify-a-deferral-or-recognition-account"></a>修改延期或确认科目

要修改延期计划的延期或确认科目，请按照以下步骤操作。

1. 在 **所有延期计划** 页面上，选择延期计划，然后选择 **会计 \> 修改科目**。
2. 在 **修改科目** 页面上，选择您要更改的科目（延期、短期或确认）。
3. 在 **新科目** 字段中，选择新科目。
4. 选择对科目的更改是否创建调整日记帐条目。
5. 如果您在上一步中将此选项设置为 **是**，在 **日记帐名称** 字段中选择日记帐名称，然后在 **交易记录日期** 字段中指定交易记录日期。
6. 选择 **确定**。

## <a name="put-a-deferral-schedule-on-hold"></a>将延期计划置于暂停状态

要将延期计划置于暂停状态，请按照以下步骤操作。

1. 在 **所有延期计划** 页面上，选择延期计划，然后选择 **暂停 \> 暂停**。
2. 在 **暂停** 页面上，选择要从延期科目还是从暂停科目转移余额。
3. 如果您选择转移余额，在 **日记帐名称** 字段中选择日记帐名称，在 **暂停科目** 字段中选择暂停科目，然后在 **交易记录日期** 字段中指定交易记录日期。
4. 选择 **确定**。

## <a name="remove-a-hold-from-a-deferral-schedule"></a>从延期计划中删除暂停

要从延期计划中删除暂停，请按照以下步骤操作。

1. 在 **所有延期计划** 列表上，选择延期计划，然后选择 **暂停 \> 删除暂停**。
2. 在 **日记帐名称** 字段中，选择日记帐名称。
3. 在 **交易记录日期** 字段中，指定交易记录日期。
4. 选择 **确定**。

## <a name="cancel-unrecognized-amounts"></a>取消未确认的金额

> [!NOTE]
> 任何已确认或外部过帐的行都会被排除在此过程之外。

要取消延期计划中的未确认金额，请按照以下步骤操作。

1. 在 **所有延期计划** 页面上，选择延期计划，然后选择 **取消 \> 未确认金额**。
2. 在 **取消未确认金额** 页面上，选择是否要创建取消条目。
3. 如果您选择创建取消条目，在 **日记帐名称** 字段中选择日记帐名称，在 **取消科目** 字段中选择取消科目，然后在 **交易记录日期** 字段中指定交易记录日期。
4. 选择 **确定**。

## <a name="cancel-a-completed-schedule"></a>取消已完成的计划

使用 **所有延期计划** 页面冲销所有已确认或外部过帐的金额，并取消延期计划以阻止进一步确认。

要取消整个延期计划，请按照以下步骤操作。

1. 在 **所有延期计划** 页面上，选择延期计划，然后选择 **取消 \> 完成的计划**。
2. 在 **取消完成的计划** 页面上，选择是否要创建取消条目。
3. 如果您选择创建取消条目，在 **日记帐名称** 字段中选择日记帐名称，在 **取消科目** 字段中选择科目，然后在 **交易记录日期** 字段中指定交易记录日期。
4. 选择 **确定**。

## <a name="reverse-transactions"></a>冲销交易记录

> [!NOTE]
> - 要冲销一个延期计划的收入确认，请从步骤 1 开始。
> - 要冲销多个计划的收入确认，请从步骤 2 开始。

1. 在 **所有延期计划** 页面的 **计划行** 网格中，选择您要取消确认的行，然后选择 **冲销**。
2. 在 **确认处理** 页面上，将 **确认操作** 字段设置为 **冲销确认日记帐**。
3. 在 **截止日期** 字段中，选择截止日期。 处理将仅包括结束日期早于或与指定截止日期相同的行。
4. 选择 **筛选器**，然后添加数据过滤器，以使列表仅显示您需要的记录范围。
5. 选择 **查看预览** 查看行。
6. 在行列表中，选择您不想处理的任何行，然后选择 **删除**。
7. **名称** 和 **描述** 字段会自动更新为默认日记帐名称和描述。 您可以根据需要更改这些值。 您还可以选择是否要汇总确认日记帐条目。
8. 在 **交易记录日期** 部分，您可以使用特定日期替代交易记录日期来处理该交易记录。 可以为已关闭期间指定交易记录日期。
9. 要作为批处理的一部分进行处理，选择 **批处理**。 在 **批处理** 对话框中，设置批处理参数，然后选择 **确定** 返回 **确认处理** 页面。 冲销收入确认将在稍后处理批处理时处理。
10. 选择 **确定**。 如果您未将交易记录添加到批处理，将立即处理所有行。 否则，将在处理批处理时处理行。

## <a name="apply-or-unapply-a-credit-note"></a>应用或取消应用贷方通知单

要应用贷方通知单，请执行以下步骤。

> [!NOTE]
> 当您从 **销售订单交易记录延期** 页面创建贷方通知单并将 **调整现有计划** 选项设置为 **是** 时，过帐贷方通知单时，贷方通知单会自动应用于计划。

1. 在 **所有延期计划** 页面上，选择延期计划。
2. 在 **贷方调整** 列表中，选择一行，然后选择 **应用**。
3. 在 **应用贷方通知单（延期）** 页面上，在 **重新计算日期** 字段中指定重新计算日期，在 **结束日期** 字段中指定结束日期。
4. 在 **标头** 列表中，选择具有贷方通知单的 **销售订单**。
5. 在 **行** 列表中，选择行。
6. 选择 **确定**。
7. 选择 **是**。

> [!NOTE]
> 要将贷项通知单应用到来自不同发票的多个单个物料，您必须重复这些步骤。

要取消应用贷方通知单，请执行以下步骤。

1. 在 **所有延期计划** 页面上，选择延期计划。
2. 在 **贷方调整** 列表中，选择发票，然后选择 **取消应用**。
3. 选择 **是**。

## <a name="fields"></a>字段

**所有延期计划** 页包含以下字段。

| 字段 | Description |
|--------|-------------|
| **页眉** | |
| **计划** | |
| 分配类型 | 基于事件的延期的分配类型：**百分比** 或 **金额**。 |
| 重新分类日期 | <p>处理延期计划的短期重新分类的最近日期。 每次将 **事件短期重新分类** 用于延期计划时，都会更新此日期。</p>只有在使用滚动期间或固定年份短期延期方法时，此字段才可用。 |
| **科目** | |
| 延期帐户 | 用于延期金额的科目。 |
| 确认帐户 | 用于确认金额的科目。 |
| 确认类型 | 确认类型。 |
| 配送类型 | 分配类型。 |
| **交易记录** | |
| 创建源 | 用于创建交易记录的源。 |
| 交易记录类型 | 交易记录类型。 |
| 销售订单 | 销售订单编号。 |
| 发票 | 发票编号。 |
| 项目 | 物料编号。 |
| **计费计划** | |
| 计费计划编号 | 对应计费计划的编号。 |
| 计费行状态 | 对应计费计划行物料的状态。 |
| 外部引用 | 有关计费计划中的外部引用的信息：**外部** 和 **行号**。 |
| 合计 | <p>延期计划的总金额：</p><ul><li>**长期** – 长期延期金额的总和。 仅当 **收入和费用延期参数** 页面的 **短期延期方法** 字段设置为 **无** 或短期金额大于 0（零）时，此值才可用。</li><li>**短期** – 短期延期金额的总和。 仅当 **收入和费用延期参数** 页面的 **短期延期方法** 字段设置为 **无** 或短期金额大于 0（零）时，此值才可用。</li><li>**未确认** – 所有行的未确认金额的总和。</li><li>**有存根** – 所有行的外部过帐金额的总和。</li><li>**已确认** – 所有行的已确认金额的总和。</li><li>**外部过帐和已确认** – 所有行的外部过帐金额和已确认金额的总和。</li><li>**总金额** – 所有行的金额总和。</li></ul> |
| **计划行** | |
| 行 | 行序列号。 |
| 延期开始日期 | 延期计划的开始日期。 |
| 延期结束日期 | 延期计划的结束日期。 |
| 金额 | 延期金额。 |
| 外部过帐 | 指示行是否已外部过帐的值。 |
| 已确认 | 指示行是否已确认的值。 |
| 日记帐批处理号 | 已确认金额的批处理号。 |
| 事件描述 | 事件的描述。 此字段只能用于基于事件的延期计划。 |
| **信用调整** | |
| 发票 | <p>发票编号。</p><p>此值指示已应用于延期计划的贷方通知单调整的发票。</p> |
| 已应用的金额 | 已应用于延期计划的贷方调整金额。 |
| 应用日期 | 应用贷方调整的日期。 |
| **调整** | 仅当为延期计划处理贷方通知单时才会显示调整值。 如果未处理任何贷方通知单，将隐藏这些值。 |
| 调整金额 | 总调整金额，计算方式为 *原始金额* – *计划金额*。 |
| 原始结束日期 | 延期计划的原始结束日期。 |
| 原始计划金额 | 原始延期计划的总计。 |