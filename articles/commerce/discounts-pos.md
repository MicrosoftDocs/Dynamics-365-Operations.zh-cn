---
title: 在 POS 中显示折扣
description: 此主题说明 Microsoft Dynamics 365 Commerce 如何帮助销售助理了解促销和如何将其用于交叉销售和向上销售动态。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 0ffa7ca6294c7b523ec743f1cb9bc4aef8ef46a8
ms.sourcegitcommit: 4d5bcda288341572076364559125c86e2ec05273
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "3334700"
---
# <a name="show-discounts-in-pos"></a><span data-ttu-id="32cfc-103">在 POS 中显示折扣</span><span class="sxs-lookup"><span data-stu-id="32cfc-103">Show discounts in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32cfc-104">促销在促使客户做出购买决定时起着重要作用。</span><span class="sxs-lookup"><span data-stu-id="32cfc-104">Promotions play an important role in motivating customers who are making purchasing decisions.</span></span> <span data-ttu-id="32cfc-105">例如，节假日可能为零售商带来最高的销售额，因为整个零售市场到处都是诱人的促销和折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-105">For example, holidays can produce the highest number of sales for retailers, because the whole retail market is flooded with enticing promotions and discounts.</span></span> <span data-ttu-id="32cfc-106">如果商店助理了解并理解可用促销，可以轻松利用这些促销交叉销售和向上销售商品。</span><span class="sxs-lookup"><span data-stu-id="32cfc-106">If store associates know about and understand the promotions that are available, they can easily take advantage of those promotions to cross-sell and upsell items.</span></span> <span data-ttu-id="32cfc-107">此主题说明 Microsoft Dynamics 365 Commerce 如何帮助销售助理了解促销和如何将其用于交叉销售和向上销售动态。</span><span class="sxs-lookup"><span data-stu-id="32cfc-107">This topic explains how Microsoft Dynamics 365 Commerce helps sales associates learn about promotions and how they can be used for cross-sell and upsell motions.</span></span>

## <a name="learn-about-store-discounts"></a><span data-ttu-id="32cfc-108">了解商店折扣</span><span class="sxs-lookup"><span data-stu-id="32cfc-108">Learn about store discounts</span></span>

<span data-ttu-id="32cfc-109">Commerce 中有一项操作，名称为“查看所有折扣”。</span><span class="sxs-lookup"><span data-stu-id="32cfc-109">Commerce includes an operation that is named "View all discounts."</span></span> <span data-ttu-id="32cfc-110">此操作显示商店中当前正在实施的所有折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-110">This operation shows all the discounts that are currently running in a store.</span></span> <span data-ttu-id="32cfc-111">可以将“查看所有折扣”操作映射到 销售点 (POS) 中的按钮，而该按钮可以添加到**欢迎**页或**交易记录**页。</span><span class="sxs-lookup"><span data-stu-id="32cfc-111">The "View all discounts" operation can be mapped to a button in the point of sale (POS), and that button can be added to the **Welcome** page or the **Transaction** page.</span></span> <span data-ttu-id="32cfc-112">下图显示打开的**所有折扣**页的示例。</span><span class="sxs-lookup"><span data-stu-id="32cfc-112">The following illustration shows an example of the **All discounts** page that is opened.</span></span>

<span data-ttu-id="32cfc-113">![“所有折扣”页](./media/View_all_discounts.png "“所有折扣”页")</span><span class="sxs-lookup"><span data-stu-id="32cfc-113">![All discounts page](./media/View_all_discounts.png "All discounts page")</span></span>

<span data-ttu-id="32cfc-114">为了显示折扣，系统将查找与下面的一个或多个条件匹配的所有折扣：</span><span class="sxs-lookup"><span data-stu-id="32cfc-114">To show discounts, the system looks for all the discounts that match one or more of the following conditions:</span></span>

- <span data-ttu-id="32cfc-115">折扣的价格组与商店的价格组匹配。</span><span class="sxs-lookup"><span data-stu-id="32cfc-115">The price group of the discount matches the price group of the store.</span></span>
- <span data-ttu-id="32cfc-116">折扣的价格组映射到隶属或会员计划。</span><span class="sxs-lookup"><span data-stu-id="32cfc-116">The price group of the discount is mapped to an affiliation or loyalty program.</span></span>
- <span data-ttu-id="32cfc-117">折扣的价格组映射到与商店关联的目录。</span><span class="sxs-lookup"><span data-stu-id="32cfc-117">The price group of the discount is mapped to a catalog that is associated with the store.</span></span>

<span data-ttu-id="32cfc-118">**所有折扣**页仅显示基于优惠券的部分折扣，因为零售商通常会对特定客户创建成千上万的优惠券和相应折扣，而此页不应显示特定于客户的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-118">The **All discounts** page shows only some coupon-based discounts, because retailers typically create thousands of coupons and corresponding discounts for unique customers, and this page isn't intended to show customer-specific discounts.</span></span> <span data-ttu-id="32cfc-119">仅当在每个优惠券页眉中开启了**应用但不使用优惠券代码**选项时才显示基于优惠券的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-119">Coupon-based discounts are shown only if the **Apply without a coupon code** option is turned on in each coupon header.</span></span> <span data-ttu-id="32cfc-120">在此情况下，收银员应用优惠券时不必输入或扫描任何优惠券代码或条形码。</span><span class="sxs-lookup"><span data-stu-id="32cfc-120">In that case, cashiers can apply the coupon without having to enter or scan any coupon code or bar code.</span></span>

<span data-ttu-id="32cfc-121">如果开启了**应用但不使用优惠券**选项，则可使用多种方案。</span><span class="sxs-lookup"><span data-stu-id="32cfc-121">When the **Apply without a coupon code** option is turned on, various scenarios become available.</span></span> <span data-ttu-id="32cfc-122">例如，收银员可以为了安抚客户或因为产品有瑕疵，向客户提供额外折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-122">For example, cashiers can give additional discounts to customers for customer appeasement purposes or because of product defects.</span></span> <span data-ttu-id="32cfc-123">不必向收银员分发印刷的优惠券代码或条形码。</span><span class="sxs-lookup"><span data-stu-id="32cfc-123">Printed coupon codes or bar codes don't have to be distributed to cashiers.</span></span> <span data-ttu-id="32cfc-124">相反，收银员可以选择**应用优惠券**按钮。</span><span class="sxs-lookup"><span data-stu-id="32cfc-124">Instead, cashiers can select the **Apply coupon** button.</span></span> <span data-ttu-id="32cfc-125">然后将把优惠券自动应用于交易。</span><span class="sxs-lookup"><span data-stu-id="32cfc-125">The coupon is then automatically applied to the transaction.</span></span> <span data-ttu-id="32cfc-126">如果一个优惠券页眉有多个优惠券，系统将自动选择交易记录中的第一个有效优惠券。</span><span class="sxs-lookup"><span data-stu-id="32cfc-126">If multiple coupons exist for a coupon header, the system automatically selects the first active coupon on the transaction.</span></span>

<span data-ttu-id="32cfc-127">销售助理还可以在**所有折扣**页中按关键字搜索折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-127">On the **All discounts** page, sales associates can also search discounts by keywords.</span></span> <span data-ttu-id="32cfc-128">关键字搜索在包含折扣名称和折扣描述的字段中进行。</span><span class="sxs-lookup"><span data-stu-id="32cfc-128">The keyword search looks in the fields that hold the discount name and discount description.</span></span> <span data-ttu-id="32cfc-129">销售助理还可以根据折扣是否需要优惠券代码来筛选折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-129">Sales associates can also filter discounts based on whether a discount requires a coupon code.</span></span>

## <a name="cross-sell-and-upsell-by-using-discounts"></a><span data-ttu-id="32cfc-130">使用折扣交叉销售和向上销售</span><span class="sxs-lookup"><span data-stu-id="32cfc-130">Cross-sell and upsell by using discounts</span></span>

<span data-ttu-id="32cfc-131">多行折扣（如数量折扣、组合购买折扣和阈值折扣）非常适合刺激客户购买更多产品以享受更大折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-131">Multiline discounts, such as quantity discounts, mix-and-match discounts, and threshold discounts, are a great way to motivate customers to buy more products to get larger discounts.</span></span> <span data-ttu-id="32cfc-132">因此，也有助于增加客户购物车的大小和提高零售商的收入。</span><span class="sxs-lookup"><span data-stu-id="32cfc-132">Therefore, they also help increase the size of a customer's cart and retailer revenue.</span></span> <span data-ttu-id="32cfc-133">可以在电子商务网站、社交媒体和店内标语中公布这些折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-133">These discounts can be publicized on e-commerce websites, on social media, and on banners in the store.</span></span>

<span data-ttu-id="32cfc-134">但是，即使使用了所有这些宣传方式，客户也可能错过享受促销的机会。</span><span class="sxs-lookup"><span data-stu-id="32cfc-134">However, even when all these publicity methods are used, customers might miss the opportunity to take advantage of promotions.</span></span> <span data-ttu-id="32cfc-135">为了方便销售助理了解哪些促销适用于选定的行，或者甚至适用于整个购物车，零售商可以将“查看可用折扣”操作的按钮添加到**交易**页上的按钮网格中。</span><span class="sxs-lookup"><span data-stu-id="32cfc-135">To make it easy for sales associates to learn what promotions are applicable to a selected line, or even to the whole cart, retailers can add the button for the "View available discounts" operation to the button grid on the **Transaction** page.</span></span> <span data-ttu-id="32cfc-136">这样，销售助理可以选择一个交易行，然后选择按钮以显示可用于所选行的所有折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-136">In this way, a sales associate can select a transaction line and then select the button to show all the discounts that are available for the selected line.</span></span> <span data-ttu-id="32cfc-137">销售助理还可以选择另一个选项卡以显示适用于整个交易的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-137">The sales associate can also select another tab to show discounts that apply to the whole transaction.</span></span>

<span data-ttu-id="32cfc-138">**所有折扣**页面仅显示不与任何已应用折扣竞争的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-138">The **All discounts** page shows only discounts that don't compete with any of the applied discounts.</span></span> <span data-ttu-id="32cfc-139">此行为有助于确保在销售助理向客户介绍折扣，并且客户执行了所需操作（例如，客户多购买一件商品以享受 10% 的折扣）时，将该折扣应用于交易。</span><span class="sxs-lookup"><span data-stu-id="32cfc-139">This behavior helps ensure that, if a sales associate informs a customer about a discount, and the customer takes the required action (for example, the customer buys one more item to get 10 percent off), the discount is applied to the transaction.</span></span> <span data-ttu-id="32cfc-140">仅在启用了**应用但不使用优惠券代码**选项时，才会显示基于优惠券的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-140">The coupon-based discounts are shown only when the **Apply without a coupon code** option is turned on.</span></span>

<span data-ttu-id="32cfc-141">在所有折扣的优先级相同，折扣并发模式为**复合型**，并且折扣并发模式设置为**最优价格和复合位于优先级中，请勿跨多个优先级进行复合**这样的简单方案中,**所有折扣**页显示产品的所有可用折扣，因为所有折扣均为复合型，并且彼此不冲突。</span><span class="sxs-lookup"><span data-stu-id="32cfc-141">In a simple scenario where all discounts have the same priority, the discount concurrency mode is **Compounded**, and the discount concurrency control is set to **Best price and compound within priority, never compound across priorities**, the **All discounts** page shows all available discounts for a product, because all the discounts are compounded and don't compete with each other.</span></span>

<span data-ttu-id="32cfc-142">下图显示的逻辑决定高级方案（如折扣并发模式为**最佳价格**或**排除**，并且使用了两个或更多优先级）中显示哪些折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-142">The following illustrations show the logic that determines which discounts are shown in advanced scenarios, such as a scenario where the discount concurrency mode is **Best price** or **Exclusive**, and two or more priorities are used.</span></span> <span data-ttu-id="32cfc-143">在这些方案中，将根据折扣并发控件设置为**最优价格和复合位于优先级中，请勿跨多个优先级进行复合**还是**最优价格仅位于优先级中，请始终跨多个优先级进行复合**进一步影响显示的折扣。</span><span class="sxs-lookup"><span data-stu-id="32cfc-143">In these scenarios, the discounts that are shown are further affected based on whether the discount concurrency control is set to **Best price and compound within priority, never compound across priorities** or **Best price only within priority, always compound across priority**.</span></span>

<span data-ttu-id="32cfc-144">下图显示当折扣并发控件设置为**最优价格和复合位于优先级中，请勿跨多个优先级进行复合**时使用的逻辑。</span><span class="sxs-lookup"><span data-stu-id="32cfc-144">The following illustration shows the logic that is used when the discount concurrency control is set to **Best price and compound within priority, never compound across priorities**.</span></span>

<span data-ttu-id="32cfc-145">![“最优价格和复合位于优先级中，请勿跨多个优先级进行复合”的逻辑](./media/Model_1.png "“最优价格和复合位于优先级中，请勿跨多个优先级进行复合”的逻辑")。</span><span class="sxs-lookup"><span data-stu-id="32cfc-145">![Logic for Best price and compound within priority, never compound across priorities](./media/Model_1.png "Logic for Best price and compound within priority, never compound across priorities").</span></span>

<span data-ttu-id="32cfc-146">下图显示当折扣并发控件设置为**最优价格仅位于优先级中，请始终跨多个优先级进行复合**时使用的逻辑。</span><span class="sxs-lookup"><span data-stu-id="32cfc-146">The following illustration shows the logic that is used when the discount concurrency control is set to **Best price only within priority, always compound across priority**.</span></span>

<span data-ttu-id="32cfc-147">![“最优价格仅位于优先级中，请始终跨多个优先级进行复合”的逻辑](./media/Model_2.png "“最优价格仅位于优先级中，请始终跨多个优先级进行复合”的逻辑")。</span><span class="sxs-lookup"><span data-stu-id="32cfc-147">![Logic for Best price only within priority, always compound across priority](./media/Model_2.png "Logic for Best price only within priority, always compound across priority").</span></span>
