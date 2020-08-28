---
title: 礼品卡模块
description: 此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661234"
---
# <a name="gift-card-module"></a><span data-ttu-id="19875-103">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="19875-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19875-104">此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="19875-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19875-105">概览</span><span class="sxs-lookup"><span data-stu-id="19875-105">Overview</span></span>

<span data-ttu-id="19875-106">礼品卡是一种常见付款方式，可在结帐模块中使用礼品卡模块接受礼品卡。</span><span class="sxs-lookup"><span data-stu-id="19875-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="19875-107">礼品卡模块支持 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="19875-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="19875-108">SVS 和 Givex 礼品卡通过 Adyen 支付方兑换。</span><span class="sxs-lookup"><span data-stu-id="19875-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="19875-109">有关支持外部礼品卡（如 SVS 和 Givex）的详细信息，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="19875-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="19875-110">下图显示了结帐页上的礼品卡模块的示例。</span><span class="sxs-lookup"><span data-stu-id="19875-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![礼品卡模块示例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="19875-112">模块属性</span><span class="sxs-lookup"><span data-stu-id="19875-112">Module properties</span></span>

- <span data-ttu-id="19875-113">**显示其他字段** - 此属性定义除了礼品卡编号（默认始终显示），还应该显示礼品卡的哪些字段。</span><span class="sxs-lookup"><span data-stu-id="19875-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="19875-114">例如，某些礼品卡支持显示个人标识号 (PIN)，其他则支持显示 PIN 和到期日期。</span><span class="sxs-lookup"><span data-stu-id="19875-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="19875-115">错误，还可以将此属性设置为“无”，这将仅显示礼品卡编号，不显示其他字段。</span><span class="sxs-lookup"><span data-stu-id="19875-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="19875-116">支持的值：</span><span class="sxs-lookup"><span data-stu-id="19875-116">Supported values:</span></span>
-   <span data-ttu-id="19875-117">PIN</span><span class="sxs-lookup"><span data-stu-id="19875-117">PIN</span></span>
-   <span data-ttu-id="19875-118">到期日期</span><span class="sxs-lookup"><span data-stu-id="19875-118">Expiration date</span></span>
-   <span data-ttu-id="19875-119">PIN 和到期日期</span><span class="sxs-lookup"><span data-stu-id="19875-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="19875-120">None</span><span class="sxs-lookup"><span data-stu-id="19875-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="19875-121">礼品卡模块的站点设置</span><span class="sxs-lookup"><span data-stu-id="19875-121">Site settings for gift card modules</span></span>

<span data-ttu-id="19875-122">在 Commerce 站点构建器中**站点设置 \> 扩展**下，有一个礼品卡模块设置，名称为**支持的礼品卡类型**。</span><span class="sxs-lookup"><span data-stu-id="19875-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="19875-123">此设置支持三个值：</span><span class="sxs-lookup"><span data-stu-id="19875-123">This setting supports three values:</span></span>
- <span data-ttu-id="19875-124">**Dynamics 365 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 Dynamics 365 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="19875-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="19875-125">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="19875-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="19875-126">**SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="19875-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="19875-127">此设置支持 e-Commerce 站点中的已登录用户和匿名用户。</span><span class="sxs-lookup"><span data-stu-id="19875-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="19875-128">**Dynamics 365、SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块允许兑换 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="19875-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="19875-129">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="19875-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="19875-130">向页面添加礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="19875-130">Add a gift card module to a page</span></span>

<span data-ttu-id="19875-131">有关如何向结帐页添加礼品卡模块和设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="19875-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19875-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="19875-132">Additional resources</span></span>

[<span data-ttu-id="19875-133">购物车模块</span><span class="sxs-lookup"><span data-stu-id="19875-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="19875-134">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="19875-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="19875-135">结帐模块</span><span class="sxs-lookup"><span data-stu-id="19875-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="19875-136">付款模块</span><span class="sxs-lookup"><span data-stu-id="19875-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="19875-137">装运地址模块</span><span class="sxs-lookup"><span data-stu-id="19875-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="19875-138">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="19875-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="19875-139">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="19875-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="19875-140">对外部礼品卡的支持</span><span class="sxs-lookup"><span data-stu-id="19875-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
