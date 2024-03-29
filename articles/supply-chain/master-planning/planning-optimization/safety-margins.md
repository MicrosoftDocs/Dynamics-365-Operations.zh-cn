---
title: 安全宽限期
description: 本文介绍主计划期间安全宽限期的工作原理。
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 87b38276a2723374969a67c5413dde15537d04ec
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740433"
---
# <a name="safety-margins"></a>安全宽限期

[!include [banner](../../includes/banner.md)]

本文介绍主计划期间安全宽限期的工作原理。

## <a name="safety-margins-overview"></a>安全宽限期概述

安全宽限期的用途是启用设置以提供比正常提前期更长的一些缓冲时间。 例如，如果在供应商的物料到达后必须拆开物料的包装或检查物料，则不能仅向购买提前期添加额外时间，因为这种方法将为提供商提供额外缓冲时间。 在此示例中，可以使用收货宽限期确保供应商提早交货。 这种方法提供了缓冲时间，以便在内部处理货物。

安全宽限期有三种类型：

- **再订购宽限期** – 用于下达供应订单的缓冲时间
- **收货宽限期** – 用于处理传入供应的缓冲时间
- **发货宽限期** – 用于处理装运的缓冲时间

下图显示这些安全宽限期在一段时间的应用情况。

![安全宽限期。](media/safety-margins-1.png)

所有宽限期均以天为单位定义。 默认值 *0*（零）表示不应用宽限期。 如果设置多个宽限期，这些宽限期将全部添加到从供应 *订单日期* 到需求 *要求日期* 的总时间。 例如，某个设置没有提前期，并且所有三种宽限期都设置为一天。 在这种情况下，供应订单日期和需求要求日期之间将相隔三天，因此，如果订单日期为 7 月 1 日，则要求日期将为 7 月 4 日。

### <a name="receipt-margin"></a>收货宽限期

收货宽限期可能是这三种安全宽限期中最常用的。 其应用于 *交货日期*，并从 *要求日期* 向后推。 换句话说，产品的接收日期应该比其需求日期早指定的收货宽限期天数。

下图突出显示了收货宽限期。

![收货宽限期。](media/safety-margins-2.png)

收货宽限期通常用作缓冲来确保仓库等记或系统中不作为常规提前期一部分捕获的其他耗时流程提供时间。 对于采购来说，其中一个优点是采购订单的 *计划日期* 相应向前推。 如果增加提前期而不是使用安全宽限期，仍然会请供应商在最后一分钟交货。

请注意，收货宽限期不会改变供应的 *要求日期*。 因此，比较需求和供应的要求日期时（例如，在 **净要求** 页面中），不会直接显示收货宽限期。 例如，如果将收货宽限期设置为四天，而采购订单行计划在该月的第十五天收货，则主计划编制期间将对收货日期做出相应的调整，使得最终算出的收货日期为该月的第十九天。

请注意，在将现有库存用作供应时，不应用收货宽限期。 无论现有库存实际是在何时收到的，都将把所有现有库存视为立即可用。

### <a name="reorder-margin"></a>再订购宽限期

下图突出显示了再订购宽限期。

![再订购宽限期。](media/safety-margins-3.png)

再订购宽限期在主计划期间所有计划订单的物料提前期之前添加。 因此，确保了为下达供应订单提供额外时间。 此宽限期通常用作缓冲来确保为创建供应订单期间所需审批流程或其他内部流程提供时间。 再订购宽限期介于供应 *订单日期* 和 *开始日期* 之间。

### <a name="issue-margin"></a>发货宽限期

下图突出显示了发货宽限期。

![发货宽限期。](media/safety-margins-4.png)

主计划期间将从需求要求日期扣除发货宽限期。 这有助于确保有时间处理和装运传入的需求订单。 此宽限期通常用作缓冲区来确保为装运和相关传出仓库流程提供时间。

请注意，如果应用发货宽限期，则相关供应日期和需求要求日期不匹配。 相反，它们在发货宽限期方面存在不同，因为发货宽限期添加在供应 *要求日期* 和需求 *要求日期* 之间。

## <a name="set-up-safety-margins"></a>设置安全宽限期

### <a name="turn-safety-margins-on-or-off"></a>打开或关闭安全宽限期

要使用此功能，必须为您的系统打开它。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.29，管理员可以通过在 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *计划优化的宽限期* 功能来打开或关闭此功能。

### <a name="define-safety-margins"></a>定义安全宽限期

安全宽限期的设置非常灵活。 *覆盖范围组* 和 *主计划* 中都可以设置。 请务必了解宽限期彼此叠加。 例如，覆盖范围组中为期两天的收货宽限期和主计划中的三天加起来为五天的有效收货宽限期。

如果希望模拟特定计划的更长提前期或不确定性，同时不影响日常计划，则在主计划中设置宽限期这一功能非常有用。

#### <a name="coverage-group-safety-margins"></a>覆盖范围组安全宽限期

若要对覆盖范围组应用安全宽限期，请执行以下步骤。

1. 转至 **主计划 \> 设置 \> 覆盖范围组**。
1. 在列表窗格中，选择所需的覆盖范围组。
1. 在 **其他** 快速选项卡的 **安全宽限期(天)** 部分中，使用以下字段设置所需的安全宽限期（以天为单位）：

    - 添加到需求日期的收货宽限期
    - 从需求日期扣除的发货宽限期
    - 已添加到物料提前期的再订购宽限期

#### <a name="master-plan-safety-margins"></a>主计划安全宽限期

若要对主计划应用安全宽限期，请执行以下步骤。

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 在列表窗格中，选择所需的主计划。
1. 在 **安全宽限期(天)** 快速选项卡中，使用以下字段设置所需的安全宽限期（以天为单位）：

    - 添加到需求日期的收货宽限期
    - 从需求日期扣除的发货宽限期
    - 已添加到物料提前期的再订购宽限期

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>定义计算基于日历日还是工作日

可以设置所有安全宽限期，以便基于日历日或工作日进行计算。

1. 转到 **主计划 \> 设置 \> 主计划参数**。
1. 在 **常规** 选项卡的 **安全宽限期(天)** 部分中，将 **工作日** 选项设置为 *是* 以基于工作日计算宽限期。 将选项设置为 *否* 则根据日历日计算宽限期。

例如，日历在星期一到星期五打开，在星期六到星期日关闭。 如果收货宽限期为一天，则星期一的要求日期生成前一个星期五的交货日期，因为星期六和星期日不是工作日。

用于确定工作日的日历取决于设置和供应类型。 可以由覆盖范围组的日历、仓库和供应商控制。

> [!NOTE]
> 如果覆盖范围维度中不包含 *仓库*（即计划仅基于 *站点*），则不使用仓库日历。

系统可以处理定义了一个或多个日历的设置。 以下小节介绍可用于控制结果的组合。

#### <a name="calendar-that-is-used-for-the-duration"></a>用于持续时间的日历

定义的日历控制日历日中从供应订单日期到需求要求日期的实际总提前期。 将使用以下日历优先级：

- **采购提前期** – 仅考虑覆盖范围组日历。
- **收货宽限期** – 使用覆盖范围组日历（如果已定义）。 否则，会使用仓库日历。
- **发货宽限期** – 使用覆盖范围组日历（如果已定义）。 否则，会使用仓库日历。
- **订单提前期** – 仅考虑覆盖范围组日历。

#### <a name="calendar-that-is-used-for-the-final-date"></a>用于结束日期的日历

将应用以下规则以确定计划引擎是否可对给定日期类型使用给定日期：

- **采购收货日期** – 使用供应商日历（如果已定义）。 否则，使用覆盖范围组日历（如果已定义）。 如果未定义这两个日历中的任何一个，则使用仓库日历。
- **转移收货日期** – 使用覆盖范围组日历（如果已定义）。 否则，会使用仓库日历。
- **生产收货日期** – 使用覆盖范围组日历（如果已定义）。 否则，会使用仓库日历。
- **需求发货开始日期** – 使用仓库日历（如果已定义）。 否则，使用覆盖范围组日历。
- **订单开始日期** – 使用覆盖范围组日历和供应商日历的组合（交集）。 必须打开这两种日历才能使用该日期。 如果仅定义这些日历中的一个，则单独使用该日历。

#### <a name="calendar-setup-overview-matrix"></a>日历设置概览矩阵

下图提供矩阵来汇总计算安全宽限期时应用哪些日历。 （选择图像打开其高分辨率版本。）以下缩写和颜色用于指示指定每种日历的位置：

- **覆盖范围组 (CG)：** 绿色
- **仓库 (WH)：** 白色
- **供应商 (V)：** 蓝色

[![日历设置概览矩阵。](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>计算延迟

系统确定订单是否已延迟时，将包括所有三种安全宽限期。

例如，一件商品的提前期为一天，收货宽限期为三天。 此商品的销售订单根据需要设置为今天。 在此情况下，延迟的计算方法为 *提前期* + *收货宽限期* = 四天。 因此，如果今天是 8 月 14 日，则四天的延迟会导致交货日期为 8 月 18 日。 下图显示此示例。

![延迟计算示例。](media/safety-margins-delays.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]