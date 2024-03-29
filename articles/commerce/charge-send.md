---
title: 使用“费用发送”功能从其他商店装运订单
description: 本文描述“费用发送”功能。
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863505"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>使用“费用发送”功能从其他商店装运订单

[!include [banner](includes/banner.md)]

使用 Commerce 中的“费用发送”功能，可以在一个商店下达客户订单，从另一个商店装运。

销售点 (POS) 客户端的客户订单支持多个履行选项。 一些履行选项的示例包括：

- 在不同日期从同一个商店提货。
- 在相同日期或不同日期从不同商店提货。
- 从分配给商店的默认装运仓库装运，在特定日期交货。

“费用发送”功能使用以下 POS 操作：装运所有产品和装运所选产品。 这允许商店职员选择订单或订单行可从中履行的“装运自”位置。 默认情况下，“发货”位置是与商店关联的装运仓库。 但是，商店职员可以更改此位置，选择在分配给商店的商店定位符组中定义的任何商店。

选择“收货”地址的功能保持不变。

可用于履行订单行的装运方法基于有效的产品交货方式和地址的配置。 由于有关有效交货方式的规则仅在总部 (HQ) 维护，POS 客户端将进行实际的调用来提取装运行的有效交货方式。


[!INCLUDE[footer-include](../includes/footer-banner.md)]