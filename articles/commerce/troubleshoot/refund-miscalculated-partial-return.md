---
title: 可退款费用根据退货数量计算错误
description: 本主题提供故障排除指导，可在收银员在销售点 (POS) 中发现退货物料数量的可退款费用不正确时提供帮助。
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490208"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>可退款费用根据退货数量计算错误

[!include [banner](../../includes/banner.md)]

本主题提供故障排除指导，可在收银员在销售点 (POS) 中发现退货物料数量的可退款费用不正确时提供帮助。

## <a name="description"></a>Description

客户退回为具有行级别可退款费用的销售订单购买的部分数量的物料。 但是，POS 未显示部分退款，而是将所有费用显示为可退款。

例如，客户以每件商品 5 美元的价格购买了五件商品，总费用为 25 美元。 然后，客户退回五件商品中的其中三件。 但是，在 POS 中向收银员显示 25 美元可退款费用，而不是退回的三件商品的预期 15 美元可退款费用。

## <a name="resolution"></a>解决方法

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>打开“根据退款数量启用退款费用”功能

从 Microsoft Dynamics 365 Commerce 版本 10.0.26 开始，**根据退款数量启用退款费用** 功能可以根据退货的物料数量计算行级别可退款费用。

要在 Commerce Headquarters 中启用 **根据退款数量启用退款费用** 功能，请按以下步骤操作。

1. 打开 **功能管理** 工作区（**系统管理员 \> 工作区 \> 功能管理**）。
1. 在可用功能列表中，搜索并选择 **根据退款数量启用退款费用** 功能。
1. 从右窗格中，选择 **立即启用**。
