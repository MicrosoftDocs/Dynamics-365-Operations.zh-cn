---
title: 在结帐时信用卡录入页显示错误
description: 本主题提供了在“付款方式”部分未加载并显示错误消息时可能会有所帮助的故障排除指南。
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018498"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>在结帐时信用卡录入页显示错误

[!include [banner](../../includes/banner.md)]

本主题提供了在 **付款方式** 部分未加载并显示错误消息时可能会有所帮助的故障排除指南。

## <a name="description"></a>说明

当您打开在线商店的结帐页面时，**付款方式** 部分未加载，并显示以下错误消息：“出了点问题。 请稍后重试。”

![付款模块错误](media/payment-module-error.jpg)

## <a name="resolution"></a>解决方法

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>等待 Commerce Scale Unit 缓存过期

在线商店结帐页面上的付款服务设置缓存在 Commerce Scale Unit 上，最多可能需要 15 分钟才能显示在电子商务网站上。 这些付款服务设置包括对商家帐户 ID、云 API 密钥的更改，以及与付款方式相关的各种配置设置。

## <a name="additional-resources"></a>其他资源

[设置在线渠道](../channel-setup-online.md)
