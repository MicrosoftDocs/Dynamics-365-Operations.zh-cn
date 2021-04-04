---
title: 跟踪入站航行和装运集装箱行程
description: 本主题说明如何使用“入站跟踪”页跟踪航行和装运集装箱行程的进度。
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 678f2b6cda0592e0393bb15f372cb4be84778932
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501238"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>跟踪入站航行和装运集装箱行程

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

使用 **入站跟踪** 页，您可以跟踪航行和装运集装箱行程的进度。 每个航行和行程都按 *活动* 分解，在页面上都有其自己的一行。 您可以使用此页面按活动查看和输入估计日期和实际日期。

通常，根据[跟踪控制中心](delivery-information-setup.md#tracking-control-center)的设置，这些活动会自动显示在最终目的地的估计登陆日期。 同样也是根据此设置，最终日期通常会更新交货日期或采购订单行上的确认日期。 对于转移单行，您可以将系统设置为更新收货日期。

要打开 **入站跟踪** 页，请转到 **登陆成本 \> 跟踪 \> 入站跟踪**。

## <a name="filter-the-activities-list"></a>筛选活动列表

您可以使用 **入站跟踪** 页顶部的 **航行** 和 **装运集装箱** 字段来筛选页面，让页面仅显示与所选航行和/或装运集装箱关联的活动。

## <a name="update-tracking-information"></a>更新跟踪信息

要更新航行或行程的计划，请输入第一个活动的开始日期。 最后一个活动的估计结束日期随后将更新。 [跟踪控制中心](delivery-information-setup.md#tracking-control-center)中每个支线和行程模板的设置确定估计的提前期。 估计结束日期使用从活动开始日期开始的提前期。 然后，当记录了实际结束日期时，下一个活动的开始日期将更新为与上一个活动的实际结束日期相同的日期。 实际提前期将更新，以可以进行比较和分析。 可以在 **注释** 字段中输入其他注释。

网格中活动的顺序由相关行程模板中支线的顺序确定。 如果附加行程中支线的顺序更改，跟踪控制也会更改。

您可以通过在操作窗格中选择 **更新开始日期** 或 **更新实际结束日期** 来更新所有集装箱的日期。 或者，您可以输入装运中每个集装箱的日期。 此方法具有更大的灵活性，因为可以在多行程环境中拆分集装箱。

## <a name="buttons-on-the-action-pane"></a>操作窗格上的按钮

您可以使用 **入站跟踪** 页的操作窗格上的按钮处理入站航行和行程。 下表描述了可用按钮。

| 按钮 | 说明 |
|---|---|
| 编辑​​ | 编辑航行或装运集装箱行程。 |
| 新项 | 创建新航行或装运集装箱行程。 |
| Delete | 删除选定航行或装运集装箱行程。 |
| 更新开始日期 | 为航行中的所有集装箱更新活动的开始日期。 当行程的特定活动或支线的开始日期更新时，后续的估计开始日期将根据指定的提前期更新。 |
| 更新实际结束日期 | 为航行中的所有集装箱更新活动的结束日期。 当特定活动的结束日期更新时，后续活动将根据指定的提前期更新。 |
| 添加活动 | 将活动手动添加到航行中。 例如，您可以添加熏烟活动。 添加可能会导致船只或航行中确认的货物交货日期发生更改。 将活动添加到行程中后，直到更新行程支线的开始日期时，才输入估计天数。 |

## <a name="information-and-settings-on-the-overview-tab"></a>概览选项卡上的信息和设置

**概览** 选项卡显示在页面顶部选择的属于航行和/或装运集装箱的所有活动的列表。 下表说明了可用于每个活动的字段。

| 字段 | 说明 |
|---|---|
| 支线 | 行程模板定义的活动的支线 ID。 |
| 交货模式 | 活动的预期交货方式。 |
| 活动 | 此字段通常确定与活动关联的作业或任务。 典型示例包括 *航行* 和 *清关*。 |
| 说明 | 更详细的活动描述。 |
| 开始日期 | 此字段最初显示活动的估计开始日期。 但是，在输入上一个活动的实际结束日期之后，它会显示实际开始日期。 此字段用于根据提前期确定估计结束日期。 |
| 估计结束日期 | 此字段的值根据开始日期和提前期计算。 您通常不会直接编辑此值。 |
| 实际结束日期 | 活动发生后，用户应尽快更新此字段。 实际提前期随后将更新。 |
| 预计天数 | 完成活动所需的估计时间（以天为单位）。 |
| 实际天数 | 完成活动所需的实际时间（以天为单位）。 |
| 备注 | 使用此字段可以添加有关活动的其他注释和详细信息。 |

## <a name="information-and-settings-on-the-general-tab"></a>常规选项卡上的信息和设置

**常规** 选项卡显示有关在 **概览** 选项卡上选择的支线的信息。它会重复显示 **概览** 选项卡上的某些信息，也会包含有关所选支线的其他信息。