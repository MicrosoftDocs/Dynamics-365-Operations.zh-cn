---
title: 实际更新数量的小数舍入不正确
description: 当生成装箱单时，出站负荷包含的数量与在单位中定义的小数精度不匹配。
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726553"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>实际更新数量的小数舍入不正确

错误代码：SYS19589

## <a name="symptoms"></a>故障特征

当生成装箱单时，出站负荷包含的数量与在单位中定义的小数精度不匹配。

当您尝试生成装箱单时，系统显示以下错误消息：

> 用单位 %1 表示的实际更新数量的小数舍入不正确。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

系统评估装运数量的小数舍入是否与为装运单位定义的小数精度相对应。 当系统将装运数量舍入到指定的小数位数时，如果发现舍入的装运数量与实际装运数量不匹配，则无法生成装箱单。 例如，如果销售数量为 1.75 千克 (kg)，但小数精度设置为 *1*，可能会发生此问题。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题。
- 查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题

使用以下过程查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法为其生成装箱单的负荷。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。
1. 在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。
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
