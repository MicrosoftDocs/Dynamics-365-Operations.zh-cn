---
title: 退货单上的退款被拒绝
description: 本文提供了故障排除指南，当由于用于开票的信用卡与原始付款授权期间使用的信用卡不同而导致退货单上的退款被拒绝时，该指南可提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8360be76fe5ef5ddfbcf290cf6272825bc1849f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879969"
---
# <a name="refund-on-a-return-order-is-declined"></a>退货单上的退款被拒绝

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，当由于用于开票的信用卡与原始付款授权期间使用的信用卡不同而导致退货单上的退款被拒绝时，该指南可提供帮助。

## <a name="description"></a>说明

当用于对退货单开具发票的信用卡与原始付款授权期间使用的信用卡不同时，退款将被拒绝。 您收到以下错误信息：“某些付款的状态不正确，因此无法过帐。 请在开具发票之前重新验证所有付款的状态。”

付款授权详细信息将包括以下错误消息：“Adyen 网关 SendRequest() 失败，状态为 'InternalServerError'.22144；从 Adyen 返回了空响应。(22001)；”

![退货单上的拒绝退款错误。](media/refund-order-decline.jpg)

## <a name="resolution"></a>解决方法

### <a name="enable-blind-returns-in-adyen"></a>在 Adyen 中启用盲目退款

要启用盲目退款，请执行[解决适用于 Adyen 的 Dynamics 365 付款连接器问题](adyen-support.md)中的步骤，与 Adyen 支持团队联系，并要求在您的 Adyen 商户帐户上启用盲目退款。

## <a name="additional-resources"></a>其他资源

[适用于 Adyen 的 Dynamics 365 付款连接器](../dev-itpro/adyen-connector.md)

[设置适用于 Dynamics 365 的 Adyen 付款连接器](https://docs.adyen.com/plugins/microsoft-dynamics)
