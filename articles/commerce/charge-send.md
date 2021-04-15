---
title: 使用“费用发送”功能从其他商店装运订单
description: 此主题描述“费用发送”功能。
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
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800463"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="02787-103">使用“费用发送”功能从其他商店装运订单</span><span class="sxs-lookup"><span data-stu-id="02787-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02787-104">使用 Commerce 中的“费用发送”功能，可以在一个商店下达客户订单，从另一个商店装运。</span><span class="sxs-lookup"><span data-stu-id="02787-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="02787-105">销售点 (POS) 客户端的客户订单支持多个履行选项。</span><span class="sxs-lookup"><span data-stu-id="02787-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="02787-106">一些履行选项的示例包括：</span><span class="sxs-lookup"><span data-stu-id="02787-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="02787-107">在不同日期从同一个商店提货。</span><span class="sxs-lookup"><span data-stu-id="02787-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="02787-108">在相同日期或不同日期从不同商店提货。</span><span class="sxs-lookup"><span data-stu-id="02787-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="02787-109">从分配给商店的默认装运仓库装运，在特定日期交货。</span><span class="sxs-lookup"><span data-stu-id="02787-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="02787-110">“费用发送”功能使用以下 POS 操作：装运所有产品和装运所选产品。</span><span class="sxs-lookup"><span data-stu-id="02787-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="02787-111">这允许商店职员选择订单或订单行可从中履行的“装运自”位置。</span><span class="sxs-lookup"><span data-stu-id="02787-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="02787-112">默认情况下，“发货”位置是与商店关联的装运仓库。</span><span class="sxs-lookup"><span data-stu-id="02787-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="02787-113">但是，商店职员可以更改此位置，选择在分配给商店的商店定位符组中定义的任何商店。</span><span class="sxs-lookup"><span data-stu-id="02787-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="02787-114">选择“收货”地址的功能保持不变。</span><span class="sxs-lookup"><span data-stu-id="02787-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="02787-115">可用于履行订单行的装运方法基于有效的产品交货方式和地址的配置。</span><span class="sxs-lookup"><span data-stu-id="02787-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="02787-116">由于有关有效交货方式的规则仅在总部 (HQ) 维护，POS 客户端将进行实际的调用来提取装运行的有效交货方式。</span><span class="sxs-lookup"><span data-stu-id="02787-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]