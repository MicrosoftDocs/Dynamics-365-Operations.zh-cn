---
title: 预测缩减参数
description: 文本提供显示如何设置缩减参数的示例。 它包含有关各种缩减参数设置以及每个结果的信息。 可以使用缩减参数以定义如何缩减预测需求。
author: t-benebo
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0efd7245d100730622e9862554f484ed6b17d1ed
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739916"
---
# <a name="forecast-reduction-keys"></a>预测缩减参数

[!include [banner](../includes/banner.md)]

本文提供有关用于减少预测需求的不同方法的信息。 其中包括每种方法的结果的示例。 还介绍如何创建、设置和使用预测缩减参数。 一些方法使用预测缩减参数缩减预测需求。

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>用于缩减预测需求的方法

向主计划添加预测时，可以选择包含实际需求时如何缩减预测需求。 请注意，主计划中不包含过去的预测要求，即当天以前的所有预测要求。

若要在主计划中添加预测并选择用于缩减预测需求的方法，请转到 **主计划 \> 设置 \> 计划 \> 主计划**。 在 **预测模型** 字段中，选择一个预测模型。 在 **用于减少预测需求的方法** 字段中，选择一个方法。 选项如下：

- 无
- 百分比 - 缩减参数
- 交易记录 - 缩减参数
- 交易记录 - 动态期间

以下部分提供有关每个选项的详细信息。

### <a name="none"></a>无

如果您选择 **无**，则在主计划编制期间不缩减预测需求。 在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。 这些计划订单中维持建议的数量，不考虑其他类型的需求。 例如，如果下达销售订单，主计划将创建更多计划订单以供给销售订单。 将不缩减预测需求的数量。

### <a name="percent--reduction-key"></a>百分比 - 缩减参数

如果选择 **百分比 - 缩减参数**，则根据百分比和缩减参数定义的百分比和期间来缩减预测需求。 在此案例中，主计划创建计划订单，在此类订单中，数量的计算方法是预测数量 × 各期间的缩减参数。 如果有其他类型的需求，主计划还将创建计划订单以满足该需求。

#### <a name="example-percent--reduction-key"></a>示例：百分比 - 缩减参数

此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。

对于本示例，将在主计划中包含以下需求预测。

| 月    | 需求预测 |
|----------|-----------------|
| 一月  | 1,000           |
| 二月 | 1,000           |
| 三月    | 1,000           |
| 四月    | 1,000           |

在 **缩减参数** 页上，设置以下行。

| 找零 | 单位  | 百分比 |
|--------|-------|---------|
| 1      | 月 | 100     |
| 2      | 月 | 75      |
| 3      | 月 | 50      |
| 4      | 月 | 25      |

将缩减参数分配给物料的覆盖范围组。 然后在 **主计划** 页的 **用于缩减预测需求的方法** 字段中，选择 **百分比 - 缩减参数**。

在此案例中，如果在 1 月 1 日运行预测计划编制，则将根据您在 **缩减参数** 页上设置的百分比来消耗销售预测需求。 以下需求数量将转移到主计划。

| 月                | 计划订单数量 | 计算    |
|----------------------|------------------------|----------------|
| 一月              | 0                      | = 0% × 1,000   |
| 二月             | 250                    | = 25% × 1,000  |
| 三月                | 500                    | = 50% × 1,000  |
| 四月                | 750                    | = 75% × 1,000  |
| 五月到十二月 | 1,000                  | = 100% × 1,000 |

### <a name="transactions--reduction-key"></a>交易记录 - 缩减参数

如果将 **用于减少预测需求的方法** 字段设置为 *交易记录 - 缩减参数*，将由缩减参数定义的期间发生的符合资格的需求交易记录减少预测需求。

符合资格的需求由 **覆盖范围组** 页中的 **预测减少依据** 字段定义。 如果将 **预测减少依据** 字段设置为 *订单*，则仅将销售订单交易记录视为符合资格的需求。 如果将其设置为 *所有交易记录*，则将所有非内部公司发货库存交易记录都视为符合资格的需求。 如果也应将内部公司销售订单视为符合资格的需求，请将 **包括内部公司订单** 选项设置为 *是*。

预测缩减以缩减参数期间中的第一个（最早）需求预测记录开始。 如果符合资格的库存交易记录数量比同一缩减参数期间的需求预测行数量多，则将使用库存交易记录数量的余额减少上一个期间中的需求预测数量（如果存在未使用的预测）。

如果上一缩减参数期间中未保留未使用的预测，将使用库存交易记录数量的余额减少下月的预测数量（如果有未使用的预测）。

如果 **用于减少预测需求的方法** 字段设置为 *交易记录 - 缩减参数*，则不使用缩减参数行中的 **百分比** 字段的值。 将仅使用这些日期来定义缩减参数期间。

> [!NOTE]
> 当天或之前发布的所有预测都将忽略，不会用于创建计划订单。 例如，如果当月的需求预测是在 1 月 1 日生成的，而您在 1 月 2 日运行其中包括需求预测的主计划，则计算将忽略日期为 1 月 1 日的需求预测。

#### <a name="example-transactions--reduction-key"></a>示例：交易记录 - 缩减参数

此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。

对于本示例，在 **主计划** 页的 **用于缩减预测需求的方法** 字段中，选择 **交易记录 - 缩减参数**。

1 月 1 日存在以下销售订单。

| 月    | 订购的份数 |
|----------|--------------------------|
| 一月  | 956                      |
| 二月 | 1,176                    |
| 三月    | 451                      |
| 四月    | 119                      |

如果您使用上一个示例中使用的同一个每月 1,000 份需求预测，将向主计划转移以下需求数量。

| 月                | 所需的份数 |
|----------------------|---------------------------|
| 一月              | 44                        |
| 二月             | 0                         |
| 三月                | 549                       |
| 四月                | 881                       |
| 五月到十二月 | 1,000                     |

### <a name="transactions--dynamic-period"></a>交易记录 - 动态期间

如果选择 **交易记录 - 动态期间**，将按动态期间进行的实际订单交易记录缩减预测需求。 动态期间涵盖当前预测日期，并在下一预测开始时结束。 在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。 但是，下达实际订单交易记录时，将缩减预测需求。 实际交易记录占用部分预测需求。

在使用此选项时，会发生以下行为：

- 将不需要或不使用缩减参数。 
- 如果完全缩减预测，则当前预测的预测需求变为 0（零）。
- 如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。
- 需求预测减少时限不包括在预测减少计算中。 覆盖范围组时限将用于预测减少。
- 正天数包括在缩减预测计算中。
- 如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。

#### <a name="example-1-transactions--dynamic-period"></a>示例 1：交易记录 - 动态期间

下面是一个简单示例，该示例显示 **交易记录 - 动态期间** 方法的工作原理。

对于本示例，将在主计划中包含以下需求预测。

| 日期       | 需求预测 |
|------------|-----------------|
| 1 月 1 日  | 1,000           |
| 2 月 1 日 | 1,000             |

还将创建以下销售订单。

| 日期        | 销售订单数量 |
|-------------|----------------------|
| 1 月 15 日  | 200                  |
| 2 月 15 日 | 400                  |

在此案例中，将创建以下计划订单。

| 需求预测日期 | 数量 | 摘要                           |
|--------------------- |----------|---------------------------------------|
| 1 月 1 日            | 800      | 预测需求 (= 1,000 – 200) |
| 1 月 15 日           | 200      | 销售订单需求             |
| 2 月 1 日           | 600      | 预测需求 (= 1,000 – 400) |
| 2 月 15 日          | 400      | 销售订单需求             |

#### <a name="example-2-transactions--dynamic-period"></a>示例 2：交易记录 - 动态期间

在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。 这些期间是在缩减参数中定义的。 但是，两个需求预测行之间的时间还可 *提示* 期间。

对于此示例，将为以下日期和数量创建需求预测。

| 日期       | 需求预测 |
|------------|-----------------|
| 1 月 1 日  | 1,000           |
| 1 月 5 日  | 500             |
| 1 月 12 日 | 1,000           |

请注意，在此预测中，预测日期之间没有清晰的间隔。 第一个和第二个日期之间的间隔为四天，第二个和第三个日期之间的间隔为七天。 这些间隔就是动态期间。

还将创建以下销售订单行。

| 日期                             | 销售订单数量 |
|----------------------------------|----------------------|
| 上一年度的 12 月 15 日 | 500                  |
| 1 月 3 日                        | 100                  |
| 1 月 10 日                       | 200                  |

在此案例中，将以下面的方式缩减预测：

- 因为第一个销售订单不在任何期间，因此不会缩减任何预测。
- 因为第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会将 1 月 1 日的预测缩减 100。
- 因为第三个销售订单是从 5 月 5 日到 5 月 12 日，因此它会将 5 月 5 日的预测缩减 200。

因此，将创建以下计划订单。

| 需求预测日期             | 数量 | 摘要                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 上一年度的 12 月 15 日 | 500      | 销售订单需求                                            |
| 1 月 1 日                        | 900      | 预测需求期间 1 月 1 日到 1 月 5 日 (= 1,000 – 100) |
| 1 月 3 日                        | 100      | 销售订单需求                                            |
| 1 月 5 日                        | 300      | 预测需求期间 1 月 5 日到 1 月 10 日 (= 500 – 200)  |
| 1 月 12 日                       | 1,000    | 预测需求期间 1 月 12 日到月底                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>创建和设置预测缩减参数

用于缩减预测需求的 **交易记录 - 缩减参数** 和 **百分比- 缩减参数** 方法中使用预测缩减参数。 若要创建和设置缩减参数，请执行以下步骤。

1. 转到 **主计划 \> 设置 \> 覆盖范围 \> 缩减参数**。
2. 选择 **新建** 创建缩减参数。
3. 在 **缩减参数** 字段中，输入预测缩减参数的唯一标识符。 然后在 **名称** 字段中输入名称。 
4. 定义期间和每个期间中的缩减参数百分比：

    - **生效日期** 字段指示开始创建期间的日期。 如果 **使用生效日期** 选项设置为 **是**，期间将在生效日期开始。 如果设置为 **否**，期间将在运行主计划的日期开始。
    - 定义应进行预测缩减的期间。
    - 为具体期间指定应缩减预测需求的百分比。 您可以输入正值以减少需求，或输入负值增加需求。

## <a name="use-a-reduction-key"></a>使用一个缩减参数

必须为物料的覆盖范围组分配预测缩减参数。 若要为物料的覆盖范围组分配缩减参数，请执行以下步骤。

1. 转至 **主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。
2. 在 **其他** 快速选项卡上的 **缩减参数** 字段中，选择缩减参数分配给覆盖范围组。 缩减参数然后运用于属于该覆盖范围组的所有物料。
3. 在主计划编制期间，若要使用缩减参数计算预测缩减，必须在设置预测计划或主计划时定义此设置。 转至以下位置之一：

    - 主计划 \> 设置 \> 计划 \> 预测计划
    - 主计划 \> 设置 \> 计划 \> 主计划

4. 在 **预测计划** 或 **主计划** 页面 **常规** 快速选项卡上的 **用于减少预测需求的方法** 字段中，选择 **百分比 - 缩减参数** 或 **交易记录 - 缩减参数**。

## <a name="reduce-a-forecast-by-transactions"></a>按交易记录缩减预测

如果用于缩减预测需求的方法选择 **交易记录 - 缩减参数** 或 **交易记录 - 动态期间**，则可指定哪些交易记录缩减预测。 如果所有交易记录均应缩减预测，请在 **覆盖范围组** 页面 **其他** 快速选项卡上的 **预测减少依据** 字段中选择 **所有交易记录**，如果只有销售订单才应缩减预测，请选择 **订单**。

## <a name="additional-resources"></a>其他资源

- [主计划概览](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
