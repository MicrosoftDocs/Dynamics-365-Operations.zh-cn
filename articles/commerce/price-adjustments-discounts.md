---
title: 价格调整和折扣
description: 本文提供有关 Dynamics 365 Commerce 中价格调整和折扣的信息。
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802783"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="cf734-103">价格调整和折扣</span><span class="sxs-lookup"><span data-stu-id="cf734-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf734-104">本文提供有关 Dynamics 365 Commerce 中价格调整和折扣的信息。</span><span class="sxs-lookup"><span data-stu-id="cf734-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cf734-105">在 Commerce 中，您可以对产品进行价格调整，并可以设置应用于销售点 (POS) 上、呼叫中心销售订单中或在线订单中的一个行项或交易记录的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="cf734-106">价格调整和折扣都可以链接到价格组。</span><span class="sxs-lookup"><span data-stu-id="cf734-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="cf734-107">对于价格调整和折扣，您可以指定单一开始日期和结束日期或重复期间、折扣代码和若干其他属性。</span><span class="sxs-lookup"><span data-stu-id="cf734-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="cf734-108">价格调整和折扣可以应用于产品、变型或类别。</span><span class="sxs-lookup"><span data-stu-id="cf734-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="cf734-109">如果对某一产品应用多个折扣，客户可能根据折扣的配置接收折扣或组合折扣的一个折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="cf734-110">Commerce 将自动应用提供最佳价格给客户的折扣或折扣组合。</span><span class="sxs-lookup"><span data-stu-id="cf734-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="cf734-111">在设置价格调整或折扣时，请确保确认价格组分配给您希望折扣应用于的正确渠道、类别、隶属关系或会员计划。</span><span class="sxs-lookup"><span data-stu-id="cf734-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="cf734-112">而且，如果您想要自动生成折扣 ID，可以在定义新的价格调整或折扣前在 **商业参数** 页中设置编号序列。</span><span class="sxs-lookup"><span data-stu-id="cf734-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="cf734-113">您可以删除价格调整或折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="cf734-114">但是，统计信息会丢失。</span><span class="sxs-lookup"><span data-stu-id="cf734-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="cf734-115">折扣类型</span><span class="sxs-lookup"><span data-stu-id="cf734-115">Types of discounts</span></span>

<span data-ttu-id="cf734-116">折扣类型有很多种：</span><span class="sxs-lookup"><span data-stu-id="cf734-116">There are many types of discounts:</span></span>

- <span data-ttu-id="cf734-117">**简单折扣** –一个单一百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="cf734-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="cf734-118">**数量折扣** – 在两个或多个产品购置时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="cf734-119">**组合购买折扣** – 在购买特定产品组合时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="cf734-120">**阈值折扣** – 交易记录合计大于指定金额时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="cf734-121">**基于支付方式的折扣** – 当交易总计大于指定金额并且使用特定付款类型（例如，现金、信用卡或借记卡）付款时将应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="cf734-122">**装运折扣** – 交易总计大于指定金额且订单上使用特定交货方式（例如，两天装运或隔夜装运）时应用的折扣。</span><span class="sxs-lookup"><span data-stu-id="cf734-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="cf734-123">价格调整和折扣都可以关联到价格组。</span><span class="sxs-lookup"><span data-stu-id="cf734-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="cf734-124">价格组可与渠道、类别、隶属关系和会员计划关联。</span><span class="sxs-lookup"><span data-stu-id="cf734-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]