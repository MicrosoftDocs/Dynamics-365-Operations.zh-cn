---
title: 由于负荷行数量为零，无法确认装运
description: 由于负荷行数量为零，无法确认装运。
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344226"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>由于负荷行数量为零，无法确认装运

错误代码：WAX:LoadTableWarningAllLinesZero、WAX2543

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 负荷 %1 中的所有行的数量均为零。  
> 无法确认负荷 %1 的装运。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

系统根据创建的工作 ID、负荷行数量和欠交百分比评估是否可以对负荷行确认装运。 如果系统发现没有工作 ID，并且欠交百分比设置为 100%，则无法确认装运。

例如，如果工作已取消，并且负荷行上的欠交百分比是 100％，则可能发生此问题。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装运确认失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行，以确保所有相关工作已在最终装运库位完成，并且数量匹配。
- 查看您的负荷行，确保欠交百分比和数量与领取的工作保持一致。

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>查看您的负荷行，以确保所有相关工作已在最终装运库位完成，并且数量匹配

使用以下过程查看您的负荷行，以确保所有相关工作已在最终装运库位完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 打开无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 如果发现不匹配，请取消相关工作，重新配置位置指令，然后重新发布负荷。 有关说明，请参阅[由于未选取物料，无法确认装运](picked-quantity-is-not-on-final.md)。
1. 对所有负荷行重复此过程，确保满足所有条件。

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>查看您的负荷行，确保欠交百分比和数量与领取的工作保持一致

使用以下过程查看您的负荷行，确保欠交百分比和数量与领取的工作保持一致。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 打开无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，为超出欠交百分比的物料选择负荷行。
1. 根据需要调整 **欠交** 字段或 **数量** 字段的值。

> [!TIP]
> 如果问题仍未解决，您可能必须为相关销售订单或转移单完成更多领料工作，直到可用数量与负荷或装运一致。
