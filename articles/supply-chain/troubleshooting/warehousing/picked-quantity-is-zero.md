---
title: 您无法确认装运，因为存在零数量
description: 您无法确认装运，因为存在零数量
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712878"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>您无法确认装运，因为存在零数量

错误代码：LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 由于欠交设置，物料 %1 和装运 %2 的负荷行已更新为数量为零，因此不允许装运任何数量的此物料。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

系统根据领取的数量、负荷行数量和欠交百分比评估领取数量是否在预期限制内。 如果系统发现负荷行上的领取数量为 0（零），您将无法确认装运。 例如，如果工作已取消，并且负荷行上的欠交百分比是 100％，则可能发生此问题。

## <a name="resolution"></a>解决方法

检查您的负荷行，确保欠交百分比和数量与领取的工作保持一致。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，为超出欠交百分比的物料选择负荷行。
1. 根据需要调整 **欠交** 字段或 **数量** 字段的值。

> [!TIP]
> 如果问题仍未解决，您可能必须为相关销售订单或转移单完成更多领料工作，直到可用数量与负荷或装运一致。
