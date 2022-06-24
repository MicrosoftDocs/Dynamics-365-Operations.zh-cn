---
title: 批量确认资产租赁付款计划
description: 本文说明如何批量确认多个付款计划。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895042"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>批量确认资产租赁付款计划

[!include [banner](../includes/banner.md)]

本文说明如何批量确认多个付款计划。 付款计划可以逐个租赁进行确认，也可以通过确认批处理流程进行确认。 只能针对其付款计划已确认的租赁过帐日记帐条目。 确认付款计划是对租赁财务信息的最终批准。 对租赁财务信息的所有未来更改（例如付款和租赁期）均构成租赁调整，应以这种方式进行处理。

要确认多个付款计划，请按照下列步骤操作。

1. 转到 **资产租赁 \> 定期 \> 批量确认**。
2. 在 **批量确认** 页面上，选择 **批量确认**。
3. 在出现的对话框中，筛选以找到要确认的帐簿。

    - 要确认特定租赁组中的所有帐簿，请在 **租赁组** 字段中选择该组。
    - 要确认特定帐簿，请在 **帐簿 ID** 字段中选择该帐簿。
    - 要确认所有帐簿，请打开 **所有帐簿** 参数。

**已确认帐簿** 页面中将显示新确认的帐簿的信息。 确认付款计划后，可以针对租赁过帐初始确认日记帐。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
