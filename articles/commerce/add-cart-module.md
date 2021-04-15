---
title: 购物车模块
description: 本主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 12/15/2020
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
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797855"
---
# <a name="cart-module"></a><span data-ttu-id="91d3e-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91d3e-104">本主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="91d3e-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91d3e-105">购物车模块显示客户继续结帐之前已添加到购物车中的物品。</span><span class="sxs-lookup"><span data-stu-id="91d3e-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="91d3e-106">此模块还显示订单摘要，并让客户可以应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="91d3e-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="91d3e-107">购物车模块支持登录结帐和访客结帐。</span><span class="sxs-lookup"><span data-stu-id="91d3e-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="91d3e-108">它还支持 **返回购物** 链接。</span><span class="sxs-lookup"><span data-stu-id="91d3e-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="91d3e-109">您可以在 **站点设置 \> 扩展 \> 路由** 中为此链接配置路由。</span><span class="sxs-lookup"><span data-stu-id="91d3e-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="91d3e-110">购物车模块根据购物车 ID 呈现数据，购物车 ID 是整个站点可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="91d3e-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="91d3e-111">下图显示了 Fabrikam 站点上购物车页面的示例。</span><span class="sxs-lookup"><span data-stu-id="91d3e-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Fabrikam 站点上的购物车模块示例](./media/cart2.PNG)

<span data-ttu-id="91d3e-113">下图显示了 Fabrikam 站点上购物车页面的示例。</span><span class="sxs-lookup"><span data-stu-id="91d3e-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="91d3e-114">在此示例中，行项有手续费。</span><span class="sxs-lookup"><span data-stu-id="91d3e-114">In this example, there is a handling fee for a line item.</span></span>

![行项包含手续费的购物车模块的示例](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="91d3e-116">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="91d3e-116">Cart module properties and slots</span></span>

| <span data-ttu-id="91d3e-117">属性</span><span class="sxs-lookup"><span data-stu-id="91d3e-117">Property</span></span> | <span data-ttu-id="91d3e-118">值</span><span class="sxs-lookup"><span data-stu-id="91d3e-118">Values</span></span> | <span data-ttu-id="91d3e-119">说明</span><span class="sxs-lookup"><span data-stu-id="91d3e-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="91d3e-120">标题</span><span class="sxs-lookup"><span data-stu-id="91d3e-120">Heading</span></span> | <span data-ttu-id="91d3e-121">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="91d3e-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="91d3e-122">购物车的标题，如“购物袋”或“购物车内的商品”。</span><span class="sxs-lookup"><span data-stu-id="91d3e-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="91d3e-123">显示库存不足错误</span><span class="sxs-lookup"><span data-stu-id="91d3e-123">Show out of stock errors</span></span> | <span data-ttu-id="91d3e-124">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="91d3e-124">**True** or **False**</span></span> | <span data-ttu-id="91d3e-125">如果此属性设置为 **True**，购物车页面将显示与库存相关的错误。</span><span class="sxs-lookup"><span data-stu-id="91d3e-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="91d3e-126">如果在站点上应用了库存检查，我们建议您将此属性设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="91d3e-127">显示行项的装运费用</span><span class="sxs-lookup"><span data-stu-id="91d3e-127">Show shipping charges for line items</span></span> | <span data-ttu-id="91d3e-128">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="91d3e-128">**True** or **False**</span></span> | <span data-ttu-id="91d3e-129">如果将此属性设置为 **True**，购物车行项将显示装运费用（如果有此信息）。</span><span class="sxs-lookup"><span data-stu-id="91d3e-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="91d3e-130">Fabrikam 主题不支持此功能，因为用户仅在结帐流中选择装运。</span><span class="sxs-lookup"><span data-stu-id="91d3e-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="91d3e-131">不过，如果适用，可以在其他工作流中打开此功能。</span><span class="sxs-lookup"><span data-stu-id="91d3e-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="91d3e-132">显示可用促销</span><span class="sxs-lookup"><span data-stu-id="91d3e-132">Show available promotions</span></span>| <span data-ttu-id="91d3e-133">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="91d3e-133">**True** or **False**</span></span> | <span data-ttu-id="91d3e-134">如果将此属性设置为 **True**，购物车会根据购物车中的商品显示可用促销。</span><span class="sxs-lookup"><span data-stu-id="91d3e-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="91d3e-135">Dynamics 365 Commerce 10.0.16 版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="91d3e-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="91d3e-136">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="91d3e-137">**文本块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="91d3e-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="91d3e-138">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="91d3e-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="91d3e-139">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="91d3e-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="91d3e-140">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="91d3e-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="91d3e-141">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="91d3e-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="91d3e-142">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="91d3e-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="91d3e-143">模块属性</span><span class="sxs-lookup"><span data-stu-id="91d3e-143">Module properties</span></span>

<span data-ttu-id="91d3e-144">以下购物车模块设置可以在 **站点设置 \> 扩展** 中配置：</span><span class="sxs-lookup"><span data-stu-id="91d3e-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="91d3e-145">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="91d3e-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="91d3e-146">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="91d3e-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="91d3e-147">**库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="91d3e-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="91d3e-148">**返回购物** – 该属性用于指定 **返回购物** 链接的路由。</span><span class="sxs-lookup"><span data-stu-id="91d3e-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="91d3e-149">可以在站点级别配置路由，让零售商可以将客户带回到站点的主页或其他任何页面。</span><span class="sxs-lookup"><span data-stu-id="91d3e-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91d3e-150">在 Dynamics 365 Commerce 10.0.14 版本及更高版本中，购物车中的物料将基于在 Commerce Headquarters 在线商店的在线功能配置文件中定义的设置进行合计。</span><span class="sxs-lookup"><span data-stu-id="91d3e-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="91d3e-151">有关如何创建在线功能配置文件和设置合计所需的属性的详细信息，请参阅[创建在线功能配置文件](online-functionality-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="91d3e-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="91d3e-152">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="91d3e-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="91d3e-153">购物车模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="91d3e-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="91d3e-154">浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="91d3e-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="91d3e-155">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-155">Add a cart module to a page</span></span>

<span data-ttu-id="91d3e-156">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="91d3e-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="91d3e-157">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="91d3e-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="91d3e-158">在 **新建片段** 对话框中，选择 **购物车** 模块。</span><span class="sxs-lookup"><span data-stu-id="91d3e-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="91d3e-159">在 **片段名称** 下，输入名称 **购物车片段**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="91d3e-160">选择 **购物车** 插槽。</span><span class="sxs-lookup"><span data-stu-id="91d3e-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="91d3e-161">在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。</span><span class="sxs-lookup"><span data-stu-id="91d3e-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="91d3e-162">在 **购物车** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91d3e-163">在 **添加模块** 对话框中，选择 **商店选择器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91d3e-164">选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="91d3e-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="91d3e-165">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="91d3e-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="91d3e-166">在 **新建模板** 对话框的 **模板名称** 下，为模板输入名称。</span><span class="sxs-lookup"><span data-stu-id="91d3e-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="91d3e-167">在大纲树中，选择 **正文** 插槽，选择省略号 (**...**)，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="91d3e-168">在 **选择片段** 对话框中，选择 **购物车片段** 片段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="91d3e-169">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="91d3e-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="91d3e-170">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="91d3e-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="91d3e-171">在 **选择模板** 对话框中，选择您创建的模板，输入页面名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="91d3e-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="91d3e-172">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="91d3e-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="91d3e-173">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="91d3e-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91d3e-174">其他资源</span><span class="sxs-lookup"><span data-stu-id="91d3e-174">Additional resources</span></span>

[<span data-ttu-id="91d3e-175">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="91d3e-176">结帐模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="91d3e-177">付款模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="91d3e-178">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="91d3e-179">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="91d3e-180">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="91d3e-181">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="91d3e-182">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="91d3e-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="91d3e-183">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="91d3e-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="91d3e-184">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="91d3e-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]