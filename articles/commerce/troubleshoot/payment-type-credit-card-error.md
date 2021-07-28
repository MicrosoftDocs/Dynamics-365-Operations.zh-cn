---
title: 销售订单页面上的“付款类型必须是信用卡”错误
description: 本主题提供了故障排除指南，当订单同步后在销售订单页面上显示错误消息时，该指南可以提供帮助。
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
ms.openlocfilehash: 1d6813a642aefa59e20a7c77ddcf53ce7d3625eb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347336"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>销售订单页面上的“付款类型必须是信用卡”错误

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，当订单同步后在销售订单页面上显示错误消息时，该指南可以提供帮助。

## <a name="description"></a>说明

同步订单后打开销售订单页面时，收到以下错误消息：“付款类型必须为信用卡，因为已指定了信用卡号。”

![“付款类型必须是信用卡”错误。](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>解决方法

### <a name="set-the-payment-type-in-commerce-headquarters"></a>在 Commerce Headquarters 中设置付款类型

1. 转到 **应收账款 \> 付款设置 \> 付款期限**。
1. 在左侧导航栏中，选择您的付款方式。
1. 在 **付款方式** 字段中，请确保选择了 **信用卡**。

## <a name="additional-resources"></a>其他资源

[过帐在线销售和付款](../tasks/posting-online-sales-payments.md)
