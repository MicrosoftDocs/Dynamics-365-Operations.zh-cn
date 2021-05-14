---
title: 由于日历有问题，您无法确认装运
description: 由于日历有问题，您无法确认装运
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938429"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>由于日历有问题，您无法确认装运

错误代码：TRX2716

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 日历类型 %1 需要签入和签出预约 %2。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷存在活动预约。 例如，有规则要求驾驶员签入。 因此，负荷当前处于装运确认失败的状态。

## <a name="resolution"></a>解决方法

您必须调查并解决链接到负荷的活动预约的所有问题。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在操作窗格的 **运输** 选项卡上，在 **预约** 组中，选择 **预约计划**。
1. 按以下步骤之一：

    - 确保驾驶员已完成预约的签入/签出。
    - 完成或取消预约。
    - 针对相关预约规则禁用 **需要驾驶员签入** 选项。
