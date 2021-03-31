---
title: 电子商务数字礼品卡
description: 本主题介绍数字礼品卡如何在 Microsoft Dynamics 365 Commerce 的电子商务实现中工作。 另外还概述了重要的配置步骤。
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cbfa84770e4671fdf289e168345d8b815caee4f7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230550"
---
# <a name="e-commerce-digital-gift-cards"></a><span data-ttu-id="fda27-104">电子商务数字礼品卡</span><span class="sxs-lookup"><span data-stu-id="fda27-104">E-commerce digital gift cards</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fda27-105">本主题介绍数字礼品卡如何在 Microsoft Dynamics 365 Commerce 的电子商务实现中工作。</span><span class="sxs-lookup"><span data-stu-id="fda27-105">This topic describes how digital gift cards work in the e-commerce implementation of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="fda27-106">另外还概述了重要的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="fda27-106">It also provides an overview of important configuration steps.</span></span>

<span data-ttu-id="fda27-107">在 Dynamics 365 Commerce 中，数字礼品卡的购买流与系统中其他产品的购买流相同。</span><span class="sxs-lookup"><span data-stu-id="fda27-107">In Dynamics 365 Commerce, the purchase of digital gift cards follows the same flow as the purchase of other products in the system.</span></span> <span data-ttu-id="fda27-108">无需配置其他模块。</span><span class="sxs-lookup"><span data-stu-id="fda27-108">No additional modules have to be configured.</span></span> <span data-ttu-id="fda27-109">如果将多个礼品卡添加到购物车中，礼品卡商品不会在单个销售行上聚合。</span><span class="sxs-lookup"><span data-stu-id="fda27-109">If multiple gift cards are added to the cart, the gift card items aren't aggregated on a single sales line.</span></span> <span data-ttu-id="fda27-110">需要此行为，是因为每个销售行使用单独的礼品卡号开票。</span><span class="sxs-lookup"><span data-stu-id="fda27-110">This behavior is required because each sales line is invoiced by using a separate gift card number.</span></span>

<span data-ttu-id="fda27-111">Dynamics 365 Commerce 10.0.16 版本及更高版本中支持购买数字礼品卡。</span><span class="sxs-lookup"><span data-stu-id="fda27-111">The purchase of digital gift cards is supported in the Dynamics 365 Commerce 10.0.16 release and later.</span></span>

<span data-ttu-id="fda27-112">下图显示了 Fabrikam 电子商务站点上数字礼品卡的产品详细信息页面 (PDP) 的示例。</span><span class="sxs-lookup"><span data-stu-id="fda27-112">The following illustration shows an example of the product details page (PDP) for a digital gift card on the Fabrikam e-commerce site.</span></span>

![Fabrikam 电子商务站点上数字礼品卡 PDP 的示例](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a><span data-ttu-id="fda27-114">在 Commerce headquarters 中打开数字礼品卡功能</span><span class="sxs-lookup"><span data-stu-id="fda27-114">Turn on the digital gift card feature in Commerce headquarters</span></span>

<span data-ttu-id="fda27-115">要让数字礼品卡的购买流在 Dynamics 365 Commerce 中运行，必须在 Commerce headquarters 中打开 **通过电子商务功能购买礼品卡** 功能。</span><span class="sxs-lookup"><span data-stu-id="fda27-115">For the purchase flow for digital gift cards to work in Dynamics 365 Commerce, the **Purchasing gift card on e-Commerce feature** feature must be turned on in Commerce headquarters.</span></span> <span data-ttu-id="fda27-116">您可以在 Commerce headquarters 中的 **功能管理** 工作区中找到此功能，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="fda27-116">You can find the feature in the **Feature management** workspace in Commerce headquarters, as shown in the following illustration.</span></span>

![Commerce headquarters 中的“功能管理”工作区](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a><span data-ttu-id="fda27-118">在 Commerce headquarters 中配置数字礼品卡</span><span class="sxs-lookup"><span data-stu-id="fda27-118">Configure a digital gift card in Commerce headquarters</span></span>

<span data-ttu-id="fda27-119">数字礼品卡产品应在 Commerce headquarters 中配置。</span><span class="sxs-lookup"><span data-stu-id="fda27-119">Digital gift card products should be configured in Commerce headquarters.</span></span> <span data-ttu-id="fda27-120">流程类似于其他产品的流程。</span><span class="sxs-lookup"><span data-stu-id="fda27-120">The process resembles the process for other products.</span></span> <span data-ttu-id="fda27-121">但是，以下重要步骤特定于购买礼品卡的配置。</span><span class="sxs-lookup"><span data-stu-id="fda27-121">However, the following important steps are specific to the configuration of gift cards for purchase.</span></span> <span data-ttu-id="fda27-122">有关如何创建和配置产品的详细信息，请参阅[在 Commerce 中创建新产品](create-new-product-commerce.md)。</span><span class="sxs-lookup"><span data-stu-id="fda27-122">For more information about how to create and configure products, see [Create a new product in Commerce](create-new-product-commerce.md).</span></span>

- <span data-ttu-id="fda27-123">在 **新建产品** 对话框中配置数字礼品卡产品时，将 **产品类别** 字段设置为 **服务**。</span><span class="sxs-lookup"><span data-stu-id="fda27-123">When you configure digital gift card products in the **New product** dialog box, set the **Product type** field to **Service**.</span></span> <span data-ttu-id="fda27-124">（要打开此对话框，转到 **零售和商业 \> 产品和类别 \> 产品(按类别)**，选择 **新建**。）在下订单之前，不会检查 **服务** 类型的产品的可用库存。</span><span class="sxs-lookup"><span data-stu-id="fda27-124">(To open the dialog box, go to **Retail and commerce \> Products and categories \> Products by category**, and select **New**.) Products of the **Service** type aren't checked for available inventory before an order is placed.</span></span> <span data-ttu-id="fda27-125">有关详细信息，请参阅[创建新产品](create-new-product-commerce.md#create-a-new-product)。</span><span class="sxs-lookup"><span data-stu-id="fda27-125">For more information, see [Create a new product](create-new-product-commerce.md#create-a-new-product).</span></span>
- <span data-ttu-id="fda27-126">在 **Commerce 参数** 页上的 **过帐** 选项卡上，**礼品卡产品** 字段必须设置为 **数字礼品卡**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="fda27-126">On the **Commerce parameters** page, on the **Posting** tab, the **Gift card product** field must be set to **Digital Gift Card**, as shown in the following illustration.</span></span> <span data-ttu-id="fda27-127">如果产品是外部礼品卡，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)了解详细信息。</span><span class="sxs-lookup"><span data-stu-id="fda27-127">If the product is an external gift card, see [Support for external gift cards](./dev-itpro/gift-card.md) for more information.</span></span>

    ![Commerce headquarters 中的礼品卡产品字段](./media/PostGiftcard.png)

- <span data-ttu-id="fda27-129">如果礼品卡必须支持多个预定义金额（例如，$25、$50 和 $100），**尺寸** 维度应用于设置这些预定义金额。</span><span class="sxs-lookup"><span data-stu-id="fda27-129">If a gift card must support multiple predefined amounts (for example, $25, $50, and $100), the **Size** dimension should be used to set up those predefined amounts.</span></span> <span data-ttu-id="fda27-130">每个预定义金额是一个变型。</span><span class="sxs-lookup"><span data-stu-id="fda27-130">Each predefined amount will be a variant.</span></span> <span data-ttu-id="fda27-131">有关详细信息，请参阅[产品维度](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="fda27-131">For more information, see [Product dimensions](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).</span></span>
- <span data-ttu-id="fda27-132">如果客户必须能够为礼品卡指定自定义金额，请首先设置允许自定义金额的变型。</span><span class="sxs-lookup"><span data-stu-id="fda27-132">If customers must be able to specify a custom amount for a gift card, first set up a variant that allows for a custom amount.</span></span> <span data-ttu-id="fda27-133">接下来，从 **类别中的已发布产品** 页打开产品，然后在 **Commerce** 快速选项卡上，将 **键入价格** 字段设置为 **必须键入新价格**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="fda27-133">Next, open the product from the **Released products in category** page, and then, on the **Commerce** FastTab, set the **Key in price** field to **Must key in new price**, as shown in the following illustration.</span></span> <span data-ttu-id="fda27-134">此设置可确保客户在 PDP 上浏览产品时可以输入价格。</span><span class="sxs-lookup"><span data-stu-id="fda27-134">This setting ensures that customers can enter a price when they browse the product on a PDP.</span></span>

    ![Commerce headquarters 中的“键入价格”字段](./media/KeyInPrice.png)

- <span data-ttu-id="fda27-136">数字礼品卡的交货方式必须设置为 **电子**。</span><span class="sxs-lookup"><span data-stu-id="fda27-136">The mode of delivery for a digital gift card must be set to **Electronic**.</span></span> <span data-ttu-id="fda27-137">在 **交货方式** 页上（**零售和商业 \> 渠道设置 \> 交货方式**），在列表窗格中选择 **电子** 交货方式，然后将数字礼品卡产品添加到 **产品** 快速选项卡上的网格中，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="fda27-137">On the **Modes of delivery** page (**Retail and commerce \> Channel setup \> Modes of delivery**), select the **Electronic** mode of delivery in the list pane, and then add the digital gift card product to the grid on the **Products** FastTab, as shown in the following illustration.</span></span> <span data-ttu-id="fda27-138">有关详细信息，请参阅[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。</span><span class="sxs-lookup"><span data-stu-id="fda27-138">For more information, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

    ![Commerce headquarters 中“交货方式”页上的数字礼品卡产品](./media/ElectronicMode.PNG)

- <span data-ttu-id="fda27-140">确保已创建在线功能配置文件，并将其与 Commerce headquarters 中的在线商店关联。</span><span class="sxs-lookup"><span data-stu-id="fda27-140">Make sure that an online functionality profile has been created and associated with your online store in Commerce headquarters.</span></span> <span data-ttu-id="fda27-141">在功能配置文件中，将 **聚合产品** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="fda27-141">In the functionality profile, set the **Aggregate products** option to **Yes**.</span></span> <span data-ttu-id="fda27-142">此设置将确保聚合除礼品卡以外的所有商品。</span><span class="sxs-lookup"><span data-stu-id="fda27-142">This setting ensures that all items except gift cards are aggregated.</span></span> <span data-ttu-id="fda27-143">有关详细信息，请参阅[创建在线功能配置文件](online-functionality-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="fda27-143">For more information, see [Create an online functionality profile](online-functionality-profile.md).</span></span>
- <span data-ttu-id="fda27-144">要确保为礼品卡开票后客户能够收到电子邮件，在 **电子邮件通知配置文件** 页上创建新的电子邮件通知类型，并将 **电子邮件通知类型** 字段设置为 **发放礼品卡**。</span><span class="sxs-lookup"><span data-stu-id="fda27-144">To ensure that customers receive an email after a gift card is invoiced, create a new email notification type on the **Email notification profiles** page, and set the **Email notification type** field to **Issue gift card**.</span></span> <span data-ttu-id="fda27-145">有关详细信息，请参阅[设置电子邮件通知配置文件](email-notification-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="fda27-145">For more information, see [Set up an email notification profile](email-notification-profiles.md).</span></span>

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a><span data-ttu-id="fda27-146">将产品图像添加到 Commerce 站点构建器媒体库</span><span class="sxs-lookup"><span data-stu-id="fda27-146">Add product images to the Commerce site builder Media library</span></span>

<span data-ttu-id="fda27-147">您必须将数字礼品卡产品的产品图像添加到 Commerce 站点构建器媒体库中。</span><span class="sxs-lookup"><span data-stu-id="fda27-147">You must add product images for digital gift card products to the Commerce site builder Media library.</span></span> <span data-ttu-id="fda27-148">确保礼品卡图像文件的文件名遵循您的站点的产品图像的命名约定。</span><span class="sxs-lookup"><span data-stu-id="fda27-148">Make sure that the file names of the gift card image files follow your site's naming conventions for product images.</span></span> <span data-ttu-id="fda27-149">有关详细信息，请参阅[上载图像](dam-upload-images.md)。</span><span class="sxs-lookup"><span data-stu-id="fda27-149">For more information, see [Upload images](dam-upload-images.md).</span></span>

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a><span data-ttu-id="fda27-150">在 Commerce 站点构建器中为数字礼品卡配置自定义金额</span><span class="sxs-lookup"><span data-stu-id="fda27-150">Configure a custom amount for a digital gift card in Commerce site builder</span></span>

<span data-ttu-id="fda27-151">如果将数字礼品卡配置为允许自定义金额，还必须在您的站点的 PDP 上使用的[购买框模块](add-buy-box.md)中启用此行为。</span><span class="sxs-lookup"><span data-stu-id="fda27-151">If a digital gift card is configured to allow for a custom amount, this behavior must also be enabled in the [buy box module](add-buy-box.md) that is used on your site's PDPs.</span></span> <span data-ttu-id="fda27-152">购买框模块支持允许自定义金额的模块配置。</span><span class="sxs-lookup"><span data-stu-id="fda27-152">The buy box module supports module configuration to allow for custom amounts.</span></span> <span data-ttu-id="fda27-153">您还可以定义自定义金额允许的最小和最大金额。</span><span class="sxs-lookup"><span data-stu-id="fda27-153">You can also define the minimum and maximum amounts that are allowed for custom amounts.</span></span>

<span data-ttu-id="fda27-154">要在 Commerce 站点构建器中为数字礼品卡配置自定义金额，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fda27-154">To configure a custom amount for a digital gift card in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fda27-155">转到您的站点的 PDP 上使用的购买框模块。</span><span class="sxs-lookup"><span data-stu-id="fda27-155">Go to the buy box module that is used on your site's PDPs.</span></span> <span data-ttu-id="fda27-156">此购买框模块可以在片段、模板或页面中实现。</span><span class="sxs-lookup"><span data-stu-id="fda27-156">This buy box module might be implemented in a fragment, in a template, or on a page.</span></span>
1. <span data-ttu-id="fda27-157">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="fda27-157">Select **Edit**.</span></span>
1. <span data-ttu-id="fda27-158">在右侧的属性窗格中，选中 **允许自定义价格** 复选框。</span><span class="sxs-lookup"><span data-stu-id="fda27-158">In the properties pane on the right, select the **Allow custom price** check box.</span></span>
1. <span data-ttu-id="fda27-159">可选：要定义自定义金额的最小和最大金额，在 **最低价格** 和 **最高价格** 下输入金额。</span><span class="sxs-lookup"><span data-stu-id="fda27-159">Optional: To define minimum and maximum amounts for custom amounts, enter amounts under **Minimum price** and **Maximum price**.</span></span>
1. <span data-ttu-id="fda27-160">选择 **完成编辑**，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="fda27-160">Select **Finish editing**, and then select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fda27-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="fda27-161">Additional resources</span></span>

[<span data-ttu-id="fda27-162">购买框模块</span><span class="sxs-lookup"><span data-stu-id="fda27-162">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fda27-163">结帐模块</span><span class="sxs-lookup"><span data-stu-id="fda27-163">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fda27-164">购物车模块</span><span class="sxs-lookup"><span data-stu-id="fda27-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fda27-165">在 Commerce 中创建新产品</span><span class="sxs-lookup"><span data-stu-id="fda27-165">Create a new product in Commerce</span></span>](create-new-product-commerce.md)

[<span data-ttu-id="fda27-166">设置交货模式</span><span class="sxs-lookup"><span data-stu-id="fda27-166">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="fda27-167">产品维度</span><span class="sxs-lookup"><span data-stu-id="fda27-167">Product dimensions</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[<span data-ttu-id="fda27-168">设置电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="fda27-168">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="fda27-169">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="fda27-169">Create an online functionality profile</span></span>](online-functionality-profile.md)

[<span data-ttu-id="fda27-170">对外部礼品卡的支持</span><span class="sxs-lookup"><span data-stu-id="fda27-170">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]