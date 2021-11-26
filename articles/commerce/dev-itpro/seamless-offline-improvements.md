---
title: 礼品卡和贷项通知单操作无缝脱机切换
description: 此主题概述特定付款类型无缝脱机切换方面的改进。
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 59f1a0b213bd22906ba8b2c3e7da38a9818f6d4f
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779484"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>礼品卡和贷项通知单操作无缝脱机切换

[!include [banner](../includes/banner.md)]

如果销售点 (POS) 设备断开与渠道数据库之间的连接，收银机收到有关连接断开的警告消息之后，大多数进行中的 POS 操作和交易记录可以继续进行。 但是，在某些情况下，交易记录有一些元素依赖于实时服务，而在 POS 脱机时不支持这些元素。 本文介绍某种在这些情况下可帮助降低连接断开造成的影响的功能。

## <a name="completing-gift-card-transactions-in-offline-mode"></a>在脱机模式下完成礼品卡交易

内部礼品卡依赖于实时服务，因为礼品卡的余额必须集中存储在 Microsoft Dynamics 365 Commerce Headquarters 中。 为了帮助避免欺诈或其他同步问题，礼品卡添加到交易记录之后将立即被锁定。 锁定功能可以确保同一时刻不能在多个终端使用同一个礼品卡。 交易完成后，将更新并解锁该礼品卡。

但是，如果在礼品卡已添加到交易之后 POS 断开连接，礼品卡可能变为不可用。 为了帮助避免发生这种情况，Dynamics 365 Commerce 采用了一个参数，用于在 POS 脱机时完成包含礼品卡行的交易。 如果开启此参数，将把已强制脱机的礼品卡交易记录与脱机交易记录一起保存，并在同步脱机交易记录时间这些交易记录同步到 Commerce Headquarters。 同步还将解锁礼品卡，使其可在另一台终端中使用。

若要在切换到脱机模式后让此功能完成礼品卡交易，请转到 **Commerce 参数** 页中的 **过帐** 选项卡。 在该选项卡上，找到 **礼品卡** 快速选项卡，然后将 **允许在脱机模式下完成礼品卡交易** 设置为 **是**。

![脱机礼品卡设置。](../media/gift.png)

通常将缓存 Commerce 参数。 因此，更新此参数的设置，并且启动了分发计划以将更改同步到渠道之后，更改可能最多需要 24 小时才会生效。 若要让更改立即生效，请重置 Microsoft Internet 信息服务 (IIS)。

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>在脱机模式下完成贷项通知单交易

和内部礼品卡一样，贷项通知单集中存储在 Commerce Headquarters 中。 Commerce 采用了一个参数，用于在 POS 脱机时完成贷项通知单交易。 此参数的工作方式类似上一节中介绍的礼品卡参数。 开启此参数之后，将把已被强制脱机的贷项通知单交易记录和 POS 脱机期间执行的其他交易记录一起同步回渠道数据库。

若要在切换到脱机模式后让此功能完成贷项通知单交易，请转到 **Commerce 参数** 页中的 **过帐** 选项卡。 在该选项卡上，找到 **贷项通知单** 快速选项卡，然后将 **允许在脱机模式下完成贷项通知单交易** 设置为 **是**。

![脱机贷项通知单设置。](../media/creditmemo.png)

通常将缓存 Commerce 参数。 因此，更新此参数的设置，并且启动了分发计划以将更改同步到渠道之后，更改可能最多需要 24 小时才会生效。 若要使更改立即生效，请重置 IIS。

## <a name="related-topics"></a>相关主题

- [脱机销售点 (POS) 功能](../pos-offline-functionality.md)
- [销售点 (POS) 联机和脱机操作](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]