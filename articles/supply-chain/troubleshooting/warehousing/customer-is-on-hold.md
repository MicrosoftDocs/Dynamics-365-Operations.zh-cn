---
title: 由于客户处于暂停状态，无法确认装运
description: 由于客户处于暂停状态，无法确认装运。
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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344256"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>由于客户处于暂停状态，无法确认装运

错误代码：WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 无法确认装运 %1，因为客户因 %2 而暂停。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷或装运的客户帐户处于暂停状态。 因此，客户的状态会阻止装运确认。

## <a name="resolution"></a>解决方法

使用以下过程解锁客户帐户。

1. 转到 **应付帐款 \> 客户 \> 所有客户**。
1. 打开无法为其确认装运的客户帐户。
1. 在 **信用和收款** 快速选项卡上，将 **开票和交货暂停** 字段设置为 *否*。
1. 为负荷的所有已阻止客户重复此过程。
