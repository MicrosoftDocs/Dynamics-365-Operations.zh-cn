---
title: 计划优化的净需求和限定标准信息
description: 本主题提供计划优化中有关计算出的净需求的信息和限定标准信息。
author: ChristianRytt
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5dbe4633ef061a054388e1b6aa6300e1c835c36a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569761"
---
# <a name="net-requirements-and-pegging-information-with-planning-optimization"></a>计划优化的净需求和限定标准信息

[!include [banner](../../includes/banner.md)]

在计划优化中运行主计划时，务必了解其输出、现有供应如何满足需求以及生成特定供应的原因。 您可以使用 **净需求** 页面更好地了解主计划生成的计算需求。

**净需求** 页显示计划优化为产品计算的净需求。 它还显示在主计划运行期间应用的覆盖范围设置、按交易记录类型列出的需求明细以及限定标准信息。

## <a name="open-the-net-requirements-page"></a>打开“净需求”页面

您可以通过以下任何方式打开 **净需求** 页面：

- 转到 **产品信息管理 \> 产品 \> 已发布产品**。 选择或打开一个产品。 然后，在操作窗格中 **计划** 选项卡上的 **需求** 组中，选择 **净需求**。
- 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。 打开销售订单。 然后，在 **销售订单行** 快速选项卡的工具栏上，选择 **产品和供应 \> 净需求**。
- 转到 **主计划 \> 主计划 \> 计划订单**。 选择或打开计划订单。 然后，在操作窗格中 **查看** 选项卡上的 **需求** 组中，选择 **需求模板**。

## <a name="use-the-net-requirements-page"></a>使用“净需求”页面

**净需求** 页面由上下两部分组成。 此页面上的操作窗格包含 **更新** 按钮。 选中此按钮后，将显示命令菜单。

### <a name="select-a-master-plan-to-view"></a>选择要查看的主计划

在查看产品的净需求之前，请务必在页面顶部的 **计划** 字段中选择相关的主计划。

### <a name="upper-section"></a>上半部分

页面的上半部分提供以下选项卡：

- **概览** - 查看产品维度的物料需求。
- **物料覆盖范围** - 查看在计算需求期间使用的覆盖范围设置。
- **摘要** - 按交易记录类型查看需求合计细分。
- **期间** - 查看由期间模板定义的每个期间的收货、发货和计划的可用库存。 您还可以获取计划的可用库存的图形视图。

### <a name="lower-section"></a>下半部分

页面的下半部分提供以下选项卡：

- **概览** - 查看在主计划运行期间计算的产品需求的列表，以及与需求相对应的发货和收货交易记录。 默认情况下，列表按需求日期进行了排序。 选择需求时，下半部分中的 **限定标准** 快速选项卡将显示需求的来源或满足需求的交易记录。
- **常规** – 查看有关所选需求的详细信息。
- **操作** - 查看需求的操作消息。

### <a name="the-action-pane"></a>操作窗格

操作窗格上提供以下命令：

- **更新 \> 主计划** – 直接从 **净需求** 页面运行主计划。
- **更新 \> 预测计划** – 直接从 **净需求** 页面运行预测计划。 计划优化尚不支持此操作。
- **更新 \> 连续性计划** - 直接从 **净需求** 页面运行连续性计划。 计划优化尚不支持此操作。

## <a name="example-scenario"></a>示例场景

此示例显示如何在 **净需求** 页面上显示限定标准信息。

### <a name="prerequisites"></a>先决条件

在演练此方案之前，请准备以下先决条件：

1. 您必须使用提供了标准示例数据的系统，并且必须将法人设置为 *USMF*。
2. 此示例使用产品 *1000*，这是 USMF 示例数据的一部分。 确保此产品可用，并且其设置方式如下：

    - **默认订单类型**：*采购订单*
    - **现有库存**：*10.00*

3. 创建数量为 *25.00* 的产品 *1000* 创建一个销售订单。 使用现有库存所在的存储维度。
4. 对 *DynPlan* 主计划运行主计划。

### <a name="review-the-calculated-requirements"></a>查看计算出的需求

接下来，您将打开产品 **1000** 的 *净需求* 页面，以查看计算出的需求的相互对应方式。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择 **物料编号** 值为 *1000* 的产品。
1. 在操作窗格中 **计划** 选项卡上的 **需求** 组中，选择 **净需求**。
1. 在 **净需求** 页面上，将 **计划** 字段设置为 *DynPlan*。
1. 在页面下半部分中的 **概览** 选项卡上，验证以下需求是否列为网格中的行。

    | 参考 | 需求数量 | 累计 |
    |---|---|---|
    | 现有量 | 10.00 | 10.00 |
    | 计划采购订单 | 15.00 | 25.00 |
    | 销售订单 | -25.00 | （空白） |

    > [!NOTE]
    > **需求数量** 字段表示需求所要求（如果值为负）或供应（如果值为正）的总数量。 **累计** 字段表示在所选期间累计的总收货和发货数量。

1. 选择 *现有量* 需求行，然后在 **限定标准** 快速选项卡上查看此供应所满足的需求。 那里应该会显示以下行。

    | 参考 | 需求数量 | 涵盖的数量 |
    |---|---|---|
    | 销售订单 | -25.00 | -10.00 |

    现有的现有库存量可以部分满足销售订单的需求。

    ![现有库存量的限定标准信息](media/pegging-on-hand.png "现有库存量的限定标准信息")

1. 选择 *计划采购订单* 需求行，然后在 **限定标准** 快速选项卡上查看此供应所满足的需求。 那里应该会显示以下行。

    | 参考 | 需求数量 | 涵盖的数量 |
    |---|---|---|
    | 销售订单 | -25.00 | -15.00 |

    由于已部分满足销售订单，因此系统会为剩余的未满足数量创建计划采购订单。

    ![计划采购订单的限定标准信息](media/pegging-planned-purchase-order.png "计划采购订单的限定标准信息")

1. 选择 *销售订单* 需求行，然后在 **限定标准** 快速选项卡上查看满足此需求的需求。 那里应该会显示以下行。

    | 参考 | 需求数量 | 涵盖的数量 |
    |---|---|---|
    | 现有量 | 10.00 | 10.00 |
    | 计划采购订单 | 15.00 | 15.00 |

    ![销售订单的限定标准信息](media/pegging-planned-purchase-order.png "销售订单的限定标准信息")

> [!NOTE]
> 由于计划优化尚不支持某些功能，因此 *净需求* 页面中未包含 *安全库存* 和 **到期的批处理** 需求类型。 有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。
>
> 如果您正在使用内置主计划引擎，则支持批次控制的产品。 对于批次控制的产品，**净需求** 页上显示了过期的现有库存量，但此库存量未与需求要求关联。 在 *净需求* 页上，此类型的已过期现有量行显示为 **到期的批处理** 需求行。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]