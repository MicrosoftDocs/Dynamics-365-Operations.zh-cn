---
title: 您尝试更新的数量超过收货/交货的数量。
description: 生成装箱单时，出站负荷包含的数量超过为销售订单领料和预留的工作数量。
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249067"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>您尝试更新的数量超过收货/交货的数量

错误代码：SYS7676

## <a name="symptoms"></a>故障特征

生成装箱单时，出站负荷包含的数量超过为销售订单领料和预留的工作数量。

当您尝试生成装箱单时，系统显示以下错误消息：

> 您正尝试更新的数量超过了接收/交付的数量。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

领取的工作数量与负荷行上创建的工作数量不匹配。 例如，如果负荷行数量、工作创建数量或领料数量不准确，则可能会出现此问题。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。
- 调整负荷行数量。
- 冲销所有领料登记，然后重新执行领料。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配

使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法生成装运的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 对所有负荷行重复此过程，确保满足所有条件。

### <a name="adjust-the-load-line-quantity"></a>调整负荷行数量

使用以下过程调整负荷行数量。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。
1. 在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。
1. 选择 **减少领料数量** 以调整领料数量。
1. 设置 **减少负荷行** 字段以反映对负荷行的调整。

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>冲销所有领料登记，然后重新执行领料

如果有人使用领料登记关闭没有工作的负荷行，则负荷行数量和领料数量之间可能会出现差异。 在这种情况下，必须冲销手动领料登记，然后必须使用 Warehouse Management 移动应用完成领料。

使用以下过程冲销领料登记。

1. 转到 **应收帐款 \> 订单 \> 所有订单**。
1. 选择无法为其过帐负荷的装箱单的销售订单。
1. 在 **销售订单行** 选项卡上，选择为其完成领料登记的销售订单行。
1. 选择 **更新行 \> 领料** 以取消领料物料。
