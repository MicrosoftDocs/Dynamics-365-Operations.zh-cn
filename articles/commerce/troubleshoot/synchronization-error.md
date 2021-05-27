---
title: 与默认付款服务有关的订单同步错误
description: 本主题提供了故障排除指南，可以帮助解决同步在线订单时可能发生的错误。
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021119"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>与默认付款服务有关的订单同步错误

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，可以帮助解决同步在线订单时可能发生的错误。

## <a name="description"></a>说明

同步在线订单时，您会收到以下错误消息：“必须有默认的付款服务才能处理信用卡交易。”

![缺少默认付款服务错误](media/default-payment-method-error.jpg)

## <a name="resolution"></a>解决方法

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>在 Commerce Headquarters 中确认或设置默认付款服务

要在 Commerce Headquarters 中确认或设置默认付款服务，请按照以下步骤操作。

1. 转至 **应收帐款 \> 付款设置 \> 付款服务**。
1. 确保对一项付款服务将 **新信用卡的默认处理程序** 选项设置为 **是**。

## <a name="additional-resources"></a>其他资源

[信用卡设置、授权和获取](../../finance/accounts-receivable/credit-card-authorizations.md)