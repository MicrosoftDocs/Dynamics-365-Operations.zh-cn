---
title: 您无法确认装运，因为数量超过了欠交百分比
description: 您无法确认装运，因为数量超过了欠交百分比
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a6a5b1140d1bc5d09a1bc582fb1d2ac9446fae0920cbb9957797dbdea4c684e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760314"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>您无法确认装运，因为数量超过了欠交百分比

错误代码：WAX1686

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 负荷 %1 的装运无法确认，因为物料 %2 的数量超出了为欠交定义的百分比。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷或装运的数量仅部分领取。 数量当前少于领料数量的百分比数超过了允许的欠交百分比。

## <a name="resolution"></a>解决方法

要解决此问题，请完成以下任务之一：

- 设置负荷行数量。
- 设置欠交百分比。

### <a name="set-the-load-line-quantity"></a>设置负荷行数量

要设置负荷行数量，请执行以下步骤。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，为超出欠交百分比的物料选择负荷行。
1. 在 **行详细信息** 快速选项卡上，选择 **订单**。
1. 在 **数量** 字段中，将值设置为领料数量（即设置为 **创建的工作数量** 值），以可以进行装运确认。

### <a name="set-the-underdelivery-percentage"></a>设置欠交百分比

要设置欠交百分比，请执行以下步骤。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，为超出欠交百分比的物料选择负荷行。
1. 在 **行详细信息** 快速选项卡上，选择 **常规**。
1. 在 **欠交** 字段中，将值设置为可接受根据负荷数量领取的数量的更大百分比，以可以进行装运确认。
