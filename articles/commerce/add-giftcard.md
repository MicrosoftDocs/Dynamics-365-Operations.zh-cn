---
title: 礼品卡模块
description: 此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962755"
---
# <a name="gift-card-module"></a><span data-ttu-id="922f7-103">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="922f7-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="922f7-104">此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="922f7-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="922f7-105">结帐模块中可以使用礼品卡模块接受礼品卡，这是电子商务交易中的一种常用付款方式。</span><span class="sxs-lookup"><span data-stu-id="922f7-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="922f7-106">礼品卡模块支持 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="922f7-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="922f7-107">SVS 和 Givex 礼品卡通过 Adyen 支付方兑换。</span><span class="sxs-lookup"><span data-stu-id="922f7-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="922f7-108">有关支持外部礼品卡（如 SVS 和 Givex）的详细信息，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)。</span><span class="sxs-lookup"><span data-stu-id="922f7-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="922f7-109">在结帐流中兑换 SVS 和 Givex 礼品卡的支持在 Dynamics 365 Commerce 10.0.11 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="922f7-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="922f7-110">有两种礼品卡模块：</span><span class="sxs-lookup"><span data-stu-id="922f7-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="922f7-111">**礼品卡** – 可以在结帐页面中使用此模块兑换礼品卡作为支付方式。</span><span class="sxs-lookup"><span data-stu-id="922f7-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="922f7-112">**礼品卡余额检查** – 任何页面中都可以使用此模块检查礼品卡的余额。</span><span class="sxs-lookup"><span data-stu-id="922f7-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="922f7-113">Commerce 版本 10.0.14 及更高版本中提供此模块。</span><span class="sxs-lookup"><span data-stu-id="922f7-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="922f7-114">对礼品卡余额检查模块的支持在 Dynamics 365 Commerce 10.0.14 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="922f7-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="922f7-115">下图显示了结帐页上的礼品卡模块的示例。</span><span class="sxs-lookup"><span data-stu-id="922f7-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![礼品卡模块示例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="922f7-117">模块属性</span><span class="sxs-lookup"><span data-stu-id="922f7-117">Module properties</span></span>

- <span data-ttu-id="922f7-118">**显示其他字段** – 此属性定义除了礼品卡编号（默认始终显示），还应该显示礼品卡的哪些字段。</span><span class="sxs-lookup"><span data-stu-id="922f7-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="922f7-119">例如，某些礼品卡支持显示个人标识号 (PIN)，其他则支持显示 PIN 和到期日期。</span><span class="sxs-lookup"><span data-stu-id="922f7-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="922f7-120">错误，还可以将此属性设置为“无”，这将仅显示礼品卡编号，不显示其他字段。</span><span class="sxs-lookup"><span data-stu-id="922f7-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="922f7-121">支持的值：</span><span class="sxs-lookup"><span data-stu-id="922f7-121">Supported values:</span></span>
-   <span data-ttu-id="922f7-122">PIN</span><span class="sxs-lookup"><span data-stu-id="922f7-122">PIN</span></span>
-   <span data-ttu-id="922f7-123">到期日期</span><span class="sxs-lookup"><span data-stu-id="922f7-123">Expiration date</span></span>
-   <span data-ttu-id="922f7-124">PIN 和到期日期</span><span class="sxs-lookup"><span data-stu-id="922f7-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="922f7-125">None</span><span class="sxs-lookup"><span data-stu-id="922f7-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="922f7-126">礼品卡模块的站点设置</span><span class="sxs-lookup"><span data-stu-id="922f7-126">Site settings for gift card modules</span></span>

<span data-ttu-id="922f7-127">在 Commerce 站点构建器中 **站点设置 \> 扩展** 下，有一个礼品卡模块设置，名称为 **支持的礼品卡类型**。</span><span class="sxs-lookup"><span data-stu-id="922f7-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="922f7-128">此设置支持三个值：</span><span class="sxs-lookup"><span data-stu-id="922f7-128">This setting supports three values:</span></span>
- <span data-ttu-id="922f7-129">**Dynamics 365 礼品卡** – 如果应用此设置，则礼品卡模块仅允许兑换 Dynamics 365 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="922f7-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="922f7-130">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="922f7-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="922f7-131">**SVS 和 Givex 礼品卡** – 如果应用此设置，则礼品卡模块仅允许兑换 SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="922f7-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="922f7-132">此设置支持 e-Commerce 站点中的已登录用户和匿名用户。</span><span class="sxs-lookup"><span data-stu-id="922f7-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="922f7-133">**Dynamics 365、SVS 和 Givex 礼品卡** – 如果应用此设置，则礼品卡模块允许兑换 Dynamics 365、SVS 和 Givex 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="922f7-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="922f7-134">此设置仅支持 e-Commerce 站点中的已登录用户。</span><span class="sxs-lookup"><span data-stu-id="922f7-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="922f7-135">这些设置在 Dynamics 365 Commerce 10.0.11 版本中可用，仅在您需要 SVS 或 Givex 礼品卡支持时才需要。</span><span class="sxs-lookup"><span data-stu-id="922f7-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="922f7-136">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="922f7-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="922f7-137">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="922f7-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="922f7-138">扩展内部礼品卡以用于电子商务店面</span><span class="sxs-lookup"><span data-stu-id="922f7-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="922f7-139">默认情况下，内部礼品卡未针对电子商务店面进行优化。</span><span class="sxs-lookup"><span data-stu-id="922f7-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="922f7-140">因此，在允许使用内部礼品卡付款之前，应通过扩展对它们进行配置，以帮助使其更加安全。</span><span class="sxs-lookup"><span data-stu-id="922f7-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="922f7-141">在允许内部礼品卡用于生产之前，应扩展以下礼品卡区域：</span><span class="sxs-lookup"><span data-stu-id="922f7-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="922f7-142">**礼品卡编号** – 编号规则用于为内部礼品卡生成礼品卡编号。</span><span class="sxs-lookup"><span data-stu-id="922f7-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="922f7-143">由于可以轻松预测编号规则，因此您应该扩展礼品卡编号的生成，以将随机的密码安全的字符串用于发布的礼品卡编号。</span><span class="sxs-lookup"><span data-stu-id="922f7-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="922f7-144">**GetBalance** – **GetBalance** API 用于查找礼品卡余额。</span><span class="sxs-lookup"><span data-stu-id="922f7-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="922f7-145">默认情况下，此 API 是公共的。</span><span class="sxs-lookup"><span data-stu-id="922f7-145">By default, this API public.</span></span> <span data-ttu-id="922f7-146">如果不需要 PIN 来查找礼品卡余额，则存在暴力攻击可以使用 **GetBalance** API 尝试查找具有余额的礼品卡编号的风险。</span><span class="sxs-lookup"><span data-stu-id="922f7-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="922f7-147">通过同时实现内部礼品卡的 PIN 要求和 API 限制，您可以帮助缓解风险。</span><span class="sxs-lookup"><span data-stu-id="922f7-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="922f7-148">**PIN** – 默认情况下，内部礼品卡不支持 PIN。</span><span class="sxs-lookup"><span data-stu-id="922f7-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="922f7-149">您应该扩展内部礼品卡，以需要 PIN 才能查找余额。</span><span class="sxs-lookup"><span data-stu-id="922f7-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="922f7-150">此功能还可用于在连续的错误尝试输入 PIN 后锁定礼品卡。</span><span class="sxs-lookup"><span data-stu-id="922f7-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="922f7-151">为来宾结帐启用礼品卡付款</span><span class="sxs-lookup"><span data-stu-id="922f7-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="922f7-152">默认情况下，来宾（匿名）结帐不启用礼品卡付款。</span><span class="sxs-lookup"><span data-stu-id="922f7-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="922f7-153">若要启用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="922f7-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="922f7-154">在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。</span><span class="sxs-lookup"><span data-stu-id="922f7-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="922f7-155">选择并按住（或右键单击）网格的标头，然后选择 **插入列**。</span><span class="sxs-lookup"><span data-stu-id="922f7-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="922f7-156">在 **插入列** 对话框中，选中 **AllowAnonymousAccess** 复选框。</span><span class="sxs-lookup"><span data-stu-id="922f7-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="922f7-157">选择 **更新**。</span><span class="sxs-lookup"><span data-stu-id="922f7-157">Select **Update**.</span></span>
1. <span data-ttu-id="922f7-158">对于操作 **520**（礼品卡余额）和 **214**，将 **AllowAnonymousAccess** 值设置为 **1**。</span><span class="sxs-lookup"><span data-stu-id="922f7-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="922f7-159">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="922f7-159">Select **Save**.</span></span>
1. <span data-ttu-id="922f7-160">运行 **1090** 计划程序作业将更改同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="922f7-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="922f7-161">向页面添加礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="922f7-161">Add a gift card module to a page</span></span>

<span data-ttu-id="922f7-162">有关如何向结帐页添加礼品卡模块和设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="922f7-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="922f7-163">其他资源</span><span class="sxs-lookup"><span data-stu-id="922f7-163">Additional resources</span></span>

[<span data-ttu-id="922f7-164">购物车模块</span><span class="sxs-lookup"><span data-stu-id="922f7-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="922f7-165">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="922f7-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="922f7-166">结帐模块</span><span class="sxs-lookup"><span data-stu-id="922f7-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="922f7-167">付款模块</span><span class="sxs-lookup"><span data-stu-id="922f7-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="922f7-168">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="922f7-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="922f7-169">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="922f7-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="922f7-170">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="922f7-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="922f7-171">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="922f7-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="922f7-172">对外部礼品卡的支持</span><span class="sxs-lookup"><span data-stu-id="922f7-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="922f7-173">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="922f7-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
