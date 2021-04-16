---
title: 礼品卡模块
description: 此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797663"
---
# <a name="gift-card-module"></a><span data-ttu-id="0b06c-103">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b06c-104">此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="0b06c-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0b06c-105">结帐模块中可以使用礼品卡模块接受礼品卡，这是电子商务交易中的一种常用付款方式。</span><span class="sxs-lookup"><span data-stu-id="0b06c-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="0b06c-106">礼品卡模块支持 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="0b06c-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="0b06c-107">SVS 和 Givex 礼品卡通过 Adyen 支付方兑换。</span><span class="sxs-lookup"><span data-stu-id="0b06c-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="0b06c-108">有关支持外部礼品卡（如 SVS 和 Givex）的详细信息，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)。</span><span class="sxs-lookup"><span data-stu-id="0b06c-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0b06c-109">在结帐流中兑换 SVS 和 Givex 礼品卡的支持在 Dynamics 365 Commerce 10.0.11 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="0b06c-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="0b06c-110">有两种礼品卡模块：</span><span class="sxs-lookup"><span data-stu-id="0b06c-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="0b06c-111">**礼品卡** - 可以在结帐页面中使用此模块兑换礼品卡作为支付方式。</span><span class="sxs-lookup"><span data-stu-id="0b06c-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="0b06c-112">**礼品卡余额检查** - 任何页面中都可以使用此模块检查礼品卡的余额。</span><span class="sxs-lookup"><span data-stu-id="0b06c-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="0b06c-113">Commerce 版本 10.0.14 及更高版本中提供此模块。</span><span class="sxs-lookup"><span data-stu-id="0b06c-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="0b06c-114">对礼品卡余额检查模块的支持在 Dynamics 365 Commerce 10.0.14 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="0b06c-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="0b06c-115">下图显示了结帐页上的礼品卡模块的示例。</span><span class="sxs-lookup"><span data-stu-id="0b06c-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![礼品卡模块示例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="0b06c-117">模块属性</span><span class="sxs-lookup"><span data-stu-id="0b06c-117">Module properties</span></span>

- <span data-ttu-id="0b06c-118">**显示其他字段** - 此属性定义除了礼品卡编号（默认始终显示），还应该显示礼品卡的哪些字段。</span><span class="sxs-lookup"><span data-stu-id="0b06c-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="0b06c-119">例如，某些礼品卡支持显示个人标识号 (PIN)，其他则支持显示 PIN 和到期日期。</span><span class="sxs-lookup"><span data-stu-id="0b06c-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="0b06c-120">错误，还可以将此属性设置为“无”，这将仅显示礼品卡编号，不显示其他字段。</span><span class="sxs-lookup"><span data-stu-id="0b06c-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="0b06c-121">支持的值：</span><span class="sxs-lookup"><span data-stu-id="0b06c-121">Supported values:</span></span>
-   <span data-ttu-id="0b06c-122">PIN</span><span class="sxs-lookup"><span data-stu-id="0b06c-122">PIN</span></span>
-   <span data-ttu-id="0b06c-123">到期日期</span><span class="sxs-lookup"><span data-stu-id="0b06c-123">Expiration date</span></span>
-   <span data-ttu-id="0b06c-124">PIN 和到期日期</span><span class="sxs-lookup"><span data-stu-id="0b06c-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="0b06c-125">None</span><span class="sxs-lookup"><span data-stu-id="0b06c-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="0b06c-126">礼品卡模块的站点设置</span><span class="sxs-lookup"><span data-stu-id="0b06c-126">Site settings for gift card modules</span></span>

<span data-ttu-id="0b06c-127">在 Commerce 站点构建器中 **站点设置 \> 扩展** 下，有一个礼品卡模块设置，名称为 **支持的礼品卡类型**。</span><span class="sxs-lookup"><span data-stu-id="0b06c-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="0b06c-128">此设置支持三个值：</span><span class="sxs-lookup"><span data-stu-id="0b06c-128">This setting supports three values:</span></span>
- <span data-ttu-id="0b06c-129">**Dynamics 365 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 Dynamics 365 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="0b06c-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="0b06c-130">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="0b06c-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="0b06c-131">**SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="0b06c-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="0b06c-132">此设置支持 e-Commerce 站点中的已登录用户和匿名用户。</span><span class="sxs-lookup"><span data-stu-id="0b06c-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="0b06c-133">**Dynamics 365、SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块允许兑换 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="0b06c-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="0b06c-134">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="0b06c-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b06c-135">这些设置在 Dynamics 365 Commerce 10.0.11 版本中可用，仅在您需要 SVS 或 Givex 礼品卡支持时才需要。</span><span class="sxs-lookup"><span data-stu-id="0b06c-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="0b06c-136">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="0b06c-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="0b06c-137">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="0b06c-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="0b06c-138">向页面添加礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-138">Add a gift card module to a page</span></span>

<span data-ttu-id="0b06c-139">有关如何向结帐页添加礼品卡模块和设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="0b06c-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b06c-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="0b06c-140">Additional resources</span></span>

[<span data-ttu-id="0b06c-141">购物车模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0b06c-142">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0b06c-143">结帐模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0b06c-144">付款模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0b06c-145">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0b06c-146">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0b06c-147">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0b06c-148">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="0b06c-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0b06c-149">对外部礼品卡的支持</span><span class="sxs-lookup"><span data-stu-id="0b06c-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="0b06c-150">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="0b06c-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]