---
title: 在装箱单生成期间领料数量不足
description: 当生成装箱单时，出站负荷包含的领料数量与负荷行上创建的工作数量不匹配。
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
ms.openlocfilehash: 6febc340f140d0b3a3f08ea32a59d9eb4e6e5204
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920440"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>在装箱单生成期间领料数量不足

错误代码：SYS54073

## <a name="symptoms"></a>故障特征

当生成装箱单时，出站负荷包含的领料数量与负荷行上创建的工作数量不匹配。

当您尝试生成装箱单时，系统显示以下错误消息：

> 由于已领取 %1，如果后面的余额必须是 %3，则不足以更新 %2。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

装箱单无法在其当前状态下生成，因为可能存在以下一种情况：

- 相关工作尚未领取并被移至最终装运位置。
- 领取的工作数量与负荷行上创建的工作数量不匹配。
- 负荷行数量、工作创建数量和领料数量不匹配。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。
- 调整负荷行数量。
- 冲销所有领料登记，然后重新执行领料。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配

使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 对所有负荷行重复此过程，确保满足所有条件。

### <a name="adjust-the-load-line-quantity"></a>调整负荷行数量

使用以下过程调整负荷行数量。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。
1. 在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。
1. 选择 **减少领料数量** 以调整领料数量。
1. 设置 **减少负荷行** 字段以反映对负荷行的调整。

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>冲销所有领料登记，然后重新执行领料

因为有人使用了领料登记关闭没有工作的负荷行，因此可能会出现此问题。 在这种情况下，必须冲销手动领料登记，然后必须使用 Warehouse Management 移动应用完成领料。

使用以下过程冲销领料登记。

1. 转到 **应收帐款 \> 订单 \> 所有订单**。
1. 选择无法为其过帐负荷的装箱单的销售订单。
1. 在 **销售订单行** 选项卡上，选择为其完成领料登记的销售订单行。
1. 选择 **更新行 \> 领料** 以取消领料物料。
