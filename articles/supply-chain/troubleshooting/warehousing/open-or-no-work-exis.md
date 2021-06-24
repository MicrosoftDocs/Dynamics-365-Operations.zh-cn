---
title: 由于工作不完整或缺失，您无法确认装运
description: 由于工作不完整或缺失，您无法确认装运
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123835"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>由于工作不完整或缺失，您无法确认装运

错误代码：WAX515

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 无法确认负荷 %1 的装运，因为必须完成负荷的所有工作。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷或装运当前处于装运确认失败的状态。 负荷必须至少有一些工作，并且所有工作的状态必须为 *已关闭* 或 *已取消*，然后您才能够确认装运。

## <a name="resolution"></a>解决方法

请检查相关销售订单或转移单的负荷或装运，确保所有相关工作均已完成或取消。

您可以在几个页面上处理装运和负荷。 以下小节提供了一些示例。

### <a name="all-loads-page"></a>所有负荷页面

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 检查每个工作 ID 的状态。 跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。
1. 当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。

### <a name="all-shipments-page"></a>所有装运页面

1. 转到 **仓库管理 \> 装运 \> 所有装运**。
1. 选择无法确认的装运。
1. 在操作窗格的 **装运** 选项卡上，在 **工作** 组中，选择 **工作详细信息**。
1. 检查每个工作 ID 的状态。 跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。
1. 当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。

### <a name="all-work-page"></a>所有工作页面

1. 转到 **仓库管理 \> 工作 \> 所有工作**。
1. 选择无法确认装运的订单编号的工作。
1. 在操作窗格上的 **装运** 选项卡上，在 **装运** 组中，选择 **确认装运**。
1. 检查每个工作 ID 的状态。 跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。
1. 当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。
