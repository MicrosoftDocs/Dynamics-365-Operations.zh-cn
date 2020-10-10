---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818267"
---
# <a name="cart-module"></a><span data-ttu-id="e1a42-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1a42-104">此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="e1a42-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e1a42-105">概览</span><span class="sxs-lookup"><span data-stu-id="e1a42-105">Overview</span></span>

<span data-ttu-id="e1a42-106">购物车模块显示客户继续结帐之前已添加到购物车中的物品。</span><span class="sxs-lookup"><span data-stu-id="e1a42-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="e1a42-107">此模块还显示订单摘要，并让客户可以应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="e1a42-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="e1a42-108">购物车模块支持登录结帐和访客结帐。</span><span class="sxs-lookup"><span data-stu-id="e1a42-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="e1a42-109">它还支持**返回购物**链接。</span><span class="sxs-lookup"><span data-stu-id="e1a42-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="e1a42-110">您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。</span><span class="sxs-lookup"><span data-stu-id="e1a42-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="e1a42-111">购物车模块根据购物车 ID 呈现数据，购物车 ID 是整个站点可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="e1a42-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="e1a42-112">下图显示了 Fabrikam 站点上购物车页面的示例。</span><span class="sxs-lookup"><span data-stu-id="e1a42-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Fabrikam 站点上的购物车模块示例](./media/cart2.PNG)

<span data-ttu-id="e1a42-114">下图显示了 Fabrikam 站点上购物车页面的示例。</span><span class="sxs-lookup"><span data-stu-id="e1a42-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="e1a42-115">在此示例中，行项有手续费。</span><span class="sxs-lookup"><span data-stu-id="e1a42-115">In this example, there is a handling fee for a line item.</span></span>

![行项包含手续费的购物车模块的示例](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="e1a42-117">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="e1a42-117">Cart module properties and slots</span></span>

| <span data-ttu-id="e1a42-118">属性</span><span class="sxs-lookup"><span data-stu-id="e1a42-118">Property</span></span> | <span data-ttu-id="e1a42-119">值</span><span class="sxs-lookup"><span data-stu-id="e1a42-119">Values</span></span> | <span data-ttu-id="e1a42-120">说明</span><span class="sxs-lookup"><span data-stu-id="e1a42-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e1a42-121">标题</span><span class="sxs-lookup"><span data-stu-id="e1a42-121">Heading</span></span> | <span data-ttu-id="e1a42-122">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="e1a42-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e1a42-123">购物车的标题，如“购物袋”或“购物车内的商品”。</span><span class="sxs-lookup"><span data-stu-id="e1a42-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="e1a42-124">显示库存不足错误</span><span class="sxs-lookup"><span data-stu-id="e1a42-124">Show out of stock errors</span></span> | <span data-ttu-id="e1a42-125">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e1a42-125">**True** or **False**</span></span> | <span data-ttu-id="e1a42-126">如果此属性设置为 **True**，购物车页面将显示与库存相关的错误。</span><span class="sxs-lookup"><span data-stu-id="e1a42-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="e1a42-127">如果在站点上应用了库存检查，我们建议您将此属性设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="e1a42-128">显示行项的装运费用</span><span class="sxs-lookup"><span data-stu-id="e1a42-128">Show shipping charges for line items</span></span> | <span data-ttu-id="e1a42-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e1a42-129">**True** or **False**</span></span> | <span data-ttu-id="e1a42-130">如果将此属性设置为 **True**，购物车行项将显示装运费用（如果有此信息）。</span><span class="sxs-lookup"><span data-stu-id="e1a42-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="e1a42-131">Fabrikam 主题不支持此功能，因为用户仅在结帐流中选择装运。</span><span class="sxs-lookup"><span data-stu-id="e1a42-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="e1a42-132">不过，如果适用，可以在其他工作流中打开此功能。</span><span class="sxs-lookup"><span data-stu-id="e1a42-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="e1a42-133">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="e1a42-134">**文本块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="e1a42-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="e1a42-135">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="e1a42-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="e1a42-136">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="e1a42-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="e1a42-137">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="e1a42-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="e1a42-138">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="e1a42-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="e1a42-139">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a42-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="e1a42-140">模块属性</span><span class="sxs-lookup"><span data-stu-id="e1a42-140">Module properties</span></span>

<span data-ttu-id="e1a42-141">以下购物车模块设置可以在**站点设置 \> 扩展**中配置：</span><span class="sxs-lookup"><span data-stu-id="e1a42-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="e1a42-142">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="e1a42-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="e1a42-143">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="e1a42-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="e1a42-144">**库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a42-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="e1a42-145">**返回购物** – 该属性用于指定**返回购物**链接的路由。</span><span class="sxs-lookup"><span data-stu-id="e1a42-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="e1a42-146">可以在站点级别配置路由，让零售商可以将客户带回到站点的主页或其他任何页面。</span><span class="sxs-lookup"><span data-stu-id="e1a42-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="e1a42-147">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="e1a42-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="e1a42-148">购物车模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="e1a42-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="e1a42-149">浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="e1a42-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="e1a42-150">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-150">Add a cart module to a page</span></span>

<span data-ttu-id="e1a42-151">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e1a42-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e1a42-152">转到**片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="e1a42-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="e1a42-153">在**新建片段**对话框中，选择**购物车**模块。</span><span class="sxs-lookup"><span data-stu-id="e1a42-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="e1a42-154">在**片段名称**下，输入名称**购物车片段**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="e1a42-155">选择**购物车**插槽。</span><span class="sxs-lookup"><span data-stu-id="e1a42-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="e1a42-156">在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。</span><span class="sxs-lookup"><span data-stu-id="e1a42-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="e1a42-157">在**购物车**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e1a42-158">在**添加模块**对话框中，选择**商店选择器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e1a42-159">选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="e1a42-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e1a42-160">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="e1a42-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e1a42-161">在**新建模板**对话框的**模板名称**下，为模板输入名称。</span><span class="sxs-lookup"><span data-stu-id="e1a42-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="e1a42-162">在大纲树中，选择**正文**插槽，选择省略号 (**...**)，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="e1a42-163">在**选择片段**对话框中，选择**购物车片段**片段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e1a42-164">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="e1a42-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e1a42-165">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="e1a42-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e1a42-166">在**选择模板**对话框中，选择您创建的模板，输入页面名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e1a42-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="e1a42-167">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="e1a42-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e1a42-168">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="e1a42-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1a42-169">其他资源</span><span class="sxs-lookup"><span data-stu-id="e1a42-169">Additional resources</span></span>

[<span data-ttu-id="e1a42-170">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e1a42-171">结帐模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e1a42-172">付款模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e1a42-173">装运地址模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e1a42-174">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e1a42-175">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e1a42-176">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="e1a42-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="e1a42-177">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="e1a42-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
