---
title: 在装箱单生成期间数量超过超交百分比
description: 生成装箱单时，出站负荷包含的数量超过超交百分比。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bc74c5748950b1f0f001fd89acb2e023640065ee
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920042"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>在装箱单生成期间数量超过超交百分比

错误代码：SYS24920

## <a name="symptoms"></a>故障特征

生成装箱单时，出站负荷包含的数量超过超交百分比。

当您尝试生成装箱单时，系统显示以下错误消息：

> 行超交百分比是 %1，但允许的超交百分比只有 %2。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

负荷或装运的领料数量大于订购数量且不在超交百分比的范围内。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 调整负荷行数量。
- 调整超交百分比。
- 冲销并进行调整。

### <a name="adjust-the-load-line-quantity"></a>调整负荷行数量

使用以下过程调整负荷行数量。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。
1. 在 **负荷行** 选项卡上，为超过超交百分比的物料选择负荷行。
1. 选择 **减少领料数量** 以调整领料数量。
1. 在 **行详细信息** 选项卡上，选择 **订单**。
1. 将 **数量** 字段设置为领料数量（即，**工作创建数量** 字段的值），以便可以继续生成装箱单。

### <a name="adjust-the-over-delivery-percentage"></a>调整超交百分比

使用以下过程调整超交百分比。

1. 转到 **应收帐款 \> 订单 \> 所有订单**。
1. 选择无法为其过帐负荷的装箱单的销售订单。
1. 在 **销售订单行** 选项卡上，为超过超交百分比的物料选择销售订单行。
1. 在 **行详细信息** 选项卡上，选择 **交货**。
1. 将 **超交** 字段设置为可接受根据负荷数量领料的数量的更大百分比，以便可以继续生成装箱单。

### <a name="reverse-and-make-adjustments"></a>冲销并进行调整

冲销已为负荷过帐的所有内容（例如，装箱单、装运确认和工作），进行销售订单调整，将订单重新发放到仓库，并完成装运过程。

使用以下过程取消装箱单。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **取消装箱单**。

使用以下过程冲销装运确认。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。

使用以下过程来冲销工作。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **负荷** 选项卡上，在 **工作** 组中，选择 **冲销工作**。
