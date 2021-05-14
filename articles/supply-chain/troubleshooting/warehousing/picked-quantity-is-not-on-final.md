---
title: 您无法确认装运，因为物料尚未领取
description: 您无法确认装运，因为物料尚未领取
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938427"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>您无法确认装运，因为物料尚未领取

错误代码：LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 负荷 %1 所需的部分物料尚未领料并且已移至最终装运库位。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷或装运无法在其当前状态下确认，因为可能存在以下其中一种情况：

- 相关工作尚未领取并被移至最终装运位置。
- 领取的工作数量与负荷行上创建的工作数量不匹配。

## <a name="resolution"></a>解决方法

检查相关销售订单或转移单的负荷或装运。 确保所有相关工作已在最终装运位置完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 对所有负荷行重复此过程，确保满足所有条件。
