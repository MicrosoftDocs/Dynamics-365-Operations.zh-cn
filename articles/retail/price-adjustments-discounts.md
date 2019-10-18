---
title: 价格调整和折扣
description: 本文提供有关 Dynamics 365 Retail 中价格调整和折扣的信息。
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9461496cf5334ff0a25361b9b426cacc0aa1f88c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025233"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="708e9-103">价格调整和折扣</span><span class="sxs-lookup"><span data-stu-id="708e9-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="708e9-104">本文提供有关 Dynamics 365 Retail 中价格调整和折扣的信息。</span><span class="sxs-lookup"><span data-stu-id="708e9-104">This article provides information about price adjustments and discounts in Dynamics 365 Retail.</span></span>

<span data-ttu-id="708e9-105">在 Retail 中，您可以对产品进行价格调整，并可以设置应用于销售点 (POS) 上、呼叫中心销售订单中或在线订单中的一个行项或交易记录的折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-105">In Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="708e9-106">价格调整和折扣都可以链接到价格组。</span><span class="sxs-lookup"><span data-stu-id="708e9-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="708e9-107">对于价格调整和折扣，您可以指定单一开始日期和结束日期或重复期间、折扣代码和若干其他属性。</span><span class="sxs-lookup"><span data-stu-id="708e9-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="708e9-108">价格调整和折扣可以应用于产品、变型或类别。</span><span class="sxs-lookup"><span data-stu-id="708e9-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="708e9-109">如果对某一产品应用多个折扣，客户可能根据折扣的配置接收折扣或组合折扣的一个折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="708e9-110">Retail 将自动应用提供最佳价格给客户的折扣或折扣组合。</span><span class="sxs-lookup"><span data-stu-id="708e9-110">Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="708e9-111">在设置价格调整或折扣时，请确保确认价格组分配给您希望折扣应用于的正确渠道、类别、隶属关系或会员计划。</span><span class="sxs-lookup"><span data-stu-id="708e9-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="708e9-112">而且，如果您想要自动生成折扣 ID，可以在定义新的价格调整或折扣前在**零售参数**页中设置编号序列。</span><span class="sxs-lookup"><span data-stu-id="708e9-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="708e9-113">您可以删除价格调整或折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="708e9-114">但是，统计信息会丢失。</span><span class="sxs-lookup"><span data-stu-id="708e9-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="708e9-115">折扣类型</span><span class="sxs-lookup"><span data-stu-id="708e9-115">Types of discounts</span></span>

<span data-ttu-id="708e9-116">存在四种零售折扣：</span><span class="sxs-lookup"><span data-stu-id="708e9-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="708e9-117">**简单折扣** –一个单一百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="708e9-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="708e9-118">**数量折扣** – 在两个或多个产品购置时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="708e9-119">**组合购买折扣** – 在购买特定产品组合时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="708e9-120">**阈值折扣** – 交易记录合计大于指定金额时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="708e9-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="708e9-121">价格调整和折扣都可以关联到价格组。</span><span class="sxs-lookup"><span data-stu-id="708e9-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="708e9-122">价格组可与渠道、类别、隶属关系和会员计划关联。</span><span class="sxs-lookup"><span data-stu-id="708e9-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
