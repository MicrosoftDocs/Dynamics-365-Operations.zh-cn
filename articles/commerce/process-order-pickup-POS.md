---
title: 在 POS 中处理客户订单提货
description: 本主题说明销售点 (POS) 应用程序中用于处理客户订单提货的功能。
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e7df580557486c67fc82af19f742bc8002cb881
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231072"
---
# <a name="process-customer-order-pickups-in-pos"></a>在 POS 中处理客户订单提货

[!include [banner](includes/banner.md)]

当创建要在商店提货的[客户订单](customer-orders-overview.md)时，商店用户可以使用销售点 (POS) 应用程序开始库存提货。 POS 将根据需要运行最终付款捕获。 另外还将完成提货数量的库存和财务过帐。

如果您是商店用户，可以使用 POS 中的 **撤回订单** 操作或 **订单履行** 操作来执行提货。 要让 **提货** 操作可用，您必须首先执行以下步骤之一：

- 要使用 **撤回订单** 操作，搜索并选择将要提货的订单。
- 要使用 **订单履行** 操作，搜索并选择一个或多个订单行。

如果未将所选订单或订单行配置为在该特定商店提货，或者订单已完全提货，**提货** 操作将不可用。

![提货操作](media/pickupoperation.png)

在 Microsoft Dynamics 365 Commerce 版本 10.0.17 及更高版本中，可以通过 Commerce Headquarters 中的“功能管理”打开 **销售点中改进的提货订单处理用户体验** 功能。 如果此功能关闭，用户则无法选择提货数量。 默认情况下，为行订购的全部数量是要提货的数量。 此体验可能会存在问题，因为用户在通过订单履行执行提货时可能会忘记选择其中一些要提货的产品。

**销售点中改进的提货订单处理用户体验** 功能让用户可以更进一步地控制对要提货的产品的选择以及要提货的产品的数量。 在选择 **提货** 之前，用户无需先在订单履行页面上选择销售订单的每一行。 可以提货的所有产品都会显示。 用户可以为提货指定多个行，即使只选择了一个产品行。

当 **销售点中改进的提货订单处理用户体验** 功能打开时，选择 **提货** 操作，**提货** 对话框将出现。 在那里，您可以选择要提货的产品和数量。 默认情况下，任何具有处于已提货或已包装状态的库存的订购数量都会被视为符合提货条件。 默认情况下，该数量设置为提货数量。 您可以更改输入的数量，前提是该数量不是 0（零）且不超过所选行的未结总数量（即未开票）。

![提货对话框](media/pickupselect.png)

选择要提货的数量后，选择 **提货**，将出现交易页面。 如果[全渠道付款](omni-channel-payments.md)功能已打开，并且有预授权的信用卡付款记录在案，您必须进行付款。

在交易页面上，系统通过计算所选提货产品的应付总额，然后减去任何先前应用的存款或授权的信用卡付款来计算应付金额。 您必须处理付款才能完成提货交易。 如果交易页面的 [屏幕布局](pos-screen-layouts.md)配置被配置为包括 **完成交易** 操作，并且没有应付金额，您无需选择付款方式即可完成交易。 如果 **完成交易** 操作不可用，您可以选择 **总计** 窗格中的 **$0.00 应付金额** 链接来完成交易，而无需选择付款方式。

![客户订单提货交易的交易页面](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>更改提货行或数量

如果在选择了要提货的产品后必须更改提货数量，可以选择 **设置数量**。 您不能将提货数量设置为 **0**（零）或将其增加到超过订购行剩余的未开票数量的值。 要从交易购物车中删除提货行，请选择 **取消交易**。 当前交易将停止，**提货** 操作的流将重新启动。

如果 **销售点中改进的提货订单处理用户体验** 功能打开，组织可以在交易页面的屏幕布局中为 **更改提货行** 操作添加按钮。 在 POS 中创建提货交易购物车并选择产品后，如果您必须更改提货产品但又不想要取消整个交易，您可以选择 **更改提货行**。 在出现的 **更改提货行** 对话框中，您可以更改提货产品和数量。 交易购物车然后会更新以反映您的更改。

![更改提货产品对话框](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]