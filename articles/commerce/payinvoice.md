---
title: 设置付款发票方案
description: 本文将介绍如何配置 Dynamics 365 Commerce 以支持与发票付款相关的各种方案。
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 78af54fec771e5012aca095d07fd772988a56029
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885365"
---
# <a name="set-up-pay-invoice-scenarios"></a>设置付款发票方案

[!include [banner](includes/banner.md)]

Dynamics 365 Commerce 中的“付款发票”功能已扩展为支持：

- 单一 POS 交易中多个销售订单发票的结算。
- 各种客户发票类型的支付，包括普通发票、基于项目的发票和贷方通知单。

要启用这些方案，必须按如下所述配置商店的功能配置文件。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，然后选择与您要更改的商店关联的配置文件。
2. 在 **功能** 选项卡上，根据需要配置以下参数。

    - **销售订单发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个基于销售订单的发票。
    - **普通发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个普通发票。
    - **项目发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个基于项目的发票。
    - **销售订单贷方通知单** - 选择 **是** 以允许用户针对未结发票结算多个基于销售订单的贷方通知单，或者向未结贷方通知单的客户处理退款。

> [!NOTE]
> 尚不支持对部分金额进行支付或结算。


[!INCLUDE[footer-include](../includes/footer-banner.md)]