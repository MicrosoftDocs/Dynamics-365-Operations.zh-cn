---
title: 单位中的实际剩余数量不得为零
description: 当您生成装箱单时，向其提供的数据具有非零库存数量，但销售数量为零。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248768"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>单位中的实际剩余数量不得为零

错误代码：SYS19591

## <a name="symptoms"></a>故障特征

当您生成装箱单时，向其提供的数据具有非零库存数量，但销售数量为零。

当您尝试生成装箱单时，系统显示以下错误消息：

> 用单位 %1 表示的实际剩余数量不能为零。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

系统评估库存单位中的实际剩余数量和装运单位中的实际剩余数量。 如果系统发现装运单位中的实际剩余数量为 0（零），但库存单位中的实际剩余数量不为 0，则无法生成装箱单。 例如，如果物料的销售单位和库存单位不同，并且单位之间的转换不准确，则可能会出现此问题。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。
- 查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题。
- 查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。
- 确保库存度量单位小于销售度量单位。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配

使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 对所有负荷行重复此过程，确保满足所有条件。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题

使用以下过程查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现舍入问题。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。
1. 在 **负荷行** 选项卡上，为超过超交的物料选择负荷行。
1. 选择 **减少领料数量** 以调整领料数量。
1. 在  **行详细信息** 选项卡上，选择 **订单**。
1. 将 **数量** 字段设置为领料数量（即，**工作创建数量** 字段的值），以便可以继续生成装箱单。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致

使用以下过程查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在 **负荷行** 快速选项卡上，为导致问题的物料选择负荷行。 记下 **数量** 和 **单位** 字段的值。
1. 转到 **组织管理 \> 单位 \> 单位**。
1. 选择无法为其生成装箱单的单位。
1. 根据需要调整 **小数精度** 字段的值。

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>确保库存度量单位小于销售度量单位

确保库存度量单位小于销售度量单位。 根据需要考虑重新配置物料的度量单位。
