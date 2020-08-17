---
title: 购买框模块
description: 此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9780aabbac6d01d41dae526c7c06139eba07de4e
ms.sourcegitcommit: 074fe7e77feb795148c3daf2e6ccbb8a88679343
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2020
ms.locfileid: "3645331"
---
# <a name="buy-box-module"></a><span data-ttu-id="8cff0-103">购买框模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8cff0-104">此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="8cff0-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8cff0-105">概览</span><span class="sxs-lookup"><span data-stu-id="8cff0-105">Overview</span></span>

<span data-ttu-id="8cff0-106">术语*购买框*通常指的是产品详细信息页中的“第一屏”区域，用于承载进行产品购买所需全部最重要信息。</span><span class="sxs-lookup"><span data-stu-id="8cff0-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="8cff0-107">（“第一屏”区域在首次加载页面时显示，所以用户不必向下滚动即可看到。）</span><span class="sxs-lookup"><span data-stu-id="8cff0-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="8cff0-108">购买框模块是特殊容器，用于承载产品详细信息页购买框区域中显示的所有模块。</span><span class="sxs-lookup"><span data-stu-id="8cff0-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="8cff0-109">产品详细信息页的 URL 中包含产品 ID。</span><span class="sxs-lookup"><span data-stu-id="8cff0-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="8cff0-110">显示购买框模块所需全部信息派生自此产品 ID。</span><span class="sxs-lookup"><span data-stu-id="8cff0-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="8cff0-111">如果不提供产品 ID，则不能在页面中正确显示购买框模块。</span><span class="sxs-lookup"><span data-stu-id="8cff0-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="8cff0-112">因此，购买框模块只能在具有产品上下文的页面上使用。</span><span class="sxs-lookup"><span data-stu-id="8cff0-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="8cff0-113">要在没有产品上下文的页面（例如，主页或市场营销页面）上使用它，您必须进行其他自定义。</span><span class="sxs-lookup"><span data-stu-id="8cff0-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="8cff0-114">下图显示了产品详细信息页上的购买框模块的示例。</span><span class="sxs-lookup"><span data-stu-id="8cff0-114">The following image shows an example of a buy box module on a product details page.</span></span>

![购买框模块的示例](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="8cff0-116">购买框模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="8cff0-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="8cff0-117">在产品详细信息页，购买框拆分为两个区域：左侧媒体区域，右侧内容区域。</span><span class="sxs-lookup"><span data-stu-id="8cff0-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="8cff0-118">默认情况下，媒体区域列的宽度与内容区域列的宽度之比为 2:1。</span><span class="sxs-lookup"><span data-stu-id="8cff0-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="8cff0-119">在移动设备上，这两个区域堆叠，所以一个区域在另一个区域下方显示。</span><span class="sxs-lookup"><span data-stu-id="8cff0-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="8cff0-120">主题可用于自定义列宽和堆叠等级。</span><span class="sxs-lookup"><span data-stu-id="8cff0-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="8cff0-121">购买框模块呈现产品的标题、描述、价格和等级。</span><span class="sxs-lookup"><span data-stu-id="8cff0-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="8cff0-122">还可以让客户选择具有不同产品属性（例如尺寸、样式和颜色）的产品变型。</span><span class="sxs-lookup"><span data-stu-id="8cff0-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="8cff0-123">如果选择了产品变型，将更新购买框中的其他属性（如产品描述和图像）以反映变型信息。</span><span class="sxs-lookup"><span data-stu-id="8cff0-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="8cff0-124">提供数量选择器，以便客户可以指定要购买的商品数量。</span><span class="sxs-lookup"><span data-stu-id="8cff0-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="8cff0-125">可以在站点设置中定义可以购买的最大数量。</span><span class="sxs-lookup"><span data-stu-id="8cff0-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="8cff0-126">客户还可以从购买框中执行一些操作，例如将产品添加到购物车，将产品添加到其愿望列表以及选择取货地点。</span><span class="sxs-lookup"><span data-stu-id="8cff0-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="8cff0-127">可以在产品或产品变型上执行这些操作。</span><span class="sxs-lookup"><span data-stu-id="8cff0-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="8cff0-128">要将产品添加到愿望列表中，客户必须先登录。</span><span class="sxs-lookup"><span data-stu-id="8cff0-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="8cff0-129">主题可用于删除或更改购买框产品属性和操作控件的顺序。</span><span class="sxs-lookup"><span data-stu-id="8cff0-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="8cff0-130">模块属性</span><span class="sxs-lookup"><span data-stu-id="8cff0-130">Module properties</span></span>

- <span data-ttu-id="8cff0-131">**标题标签** – 此属性定义产品标题的标题标签。</span><span class="sxs-lookup"><span data-stu-id="8cff0-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="8cff0-132">如果购买框位于页面顶部，则此属性应设置为 **h1** 以达到可访问性标准。</span><span class="sxs-lookup"><span data-stu-id="8cff0-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="8cff0-133">购买框模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="8cff0-134">**媒体库** – 此模块用于展示产品详细信息页上的产品图像。</span><span class="sxs-lookup"><span data-stu-id="8cff0-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="8cff0-135">有关此模块的详细信息，请参阅[媒体库模块](mediagallery-module.md)。</span><span class="sxs-lookup"><span data-stu-id="8cff0-135">For more information about this module, see [Media gallery module](mediagallery-module.md).</span></span>
- <span data-ttu-id="8cff0-136">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="8cff0-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8cff0-137">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="8cff0-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="8cff0-138">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="8cff0-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="8cff0-139">购买框模块设置</span><span class="sxs-lookup"><span data-stu-id="8cff0-139">Buy box module settings</span></span>

<span data-ttu-id="8cff0-140">以下购买框模块设置可以在**站点设置 \> 扩展**中配置：</span><span class="sxs-lookup"><span data-stu-id="8cff0-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="8cff0-141">**购物车行数量限制** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="8cff0-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8cff0-142">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="8cff0-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8cff0-143">**库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="8cff0-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="8cff0-144">**添加到购物车** - 此属性用于指定将商品添加到购物车后的行为。</span><span class="sxs-lookup"><span data-stu-id="8cff0-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="8cff0-145">可能的值为**导航到购物车**、**不导航到购物车**和**显示通知**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="8cff0-146">当此值设置为**导航到购物车**时，用户将在添加商品后被发送到购物车页面。</span><span class="sxs-lookup"><span data-stu-id="8cff0-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="8cff0-147">当此值设置为**不导航到购物车**时，用户在添加商品后不会被发送到购物车页面。</span><span class="sxs-lookup"><span data-stu-id="8cff0-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="8cff0-148">当此值设置为**显示通知**时，会向用户显示一条确认通知，用户可以继续在产品详细信息页浏览。</span><span class="sxs-lookup"><span data-stu-id="8cff0-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="8cff0-149">下图显示了 Fabrikam 站点上“已添加到购物车”确认通知的示例。</span><span class="sxs-lookup"><span data-stu-id="8cff0-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![通知模块示例](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="8cff0-151">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="8cff0-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="8cff0-152">购买框模块使用 Commerce Scale Unit 应用程序编程接口 (API) 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="8cff0-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="8cff0-153">产品详细信息页中的产品 ID 用于检索所有信息。</span><span class="sxs-lookup"><span data-stu-id="8cff0-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="8cff0-154">向页面添加购买框模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-154">Add a buy box module to a page</span></span>

<span data-ttu-id="8cff0-155">若要向新页面添加购买框模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8cff0-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8cff0-156">转到**页面片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="8cff0-156">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="8cff0-157">在**新建页面片段**对话框中，选择**购买框**模块。</span><span class="sxs-lookup"><span data-stu-id="8cff0-157">In the **New Page Fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="8cff0-158">在**页面片段名称**下，输入名称**购买框片段**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-158">Under **Page Fragment Name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-159">在购买框模块的**媒体库**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8cff0-160">在**添加模块**对话框中，选择**媒体库**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-161">在购买框模块的**商店选择器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8cff0-162">在**添加模块**对话框中，选择**商店选择器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-163">选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="8cff0-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="8cff0-164">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="8cff0-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="8cff0-165">在**新建模板**对话框的**模板名称**下，输入 **PDP 模板**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-166">在**正文**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8cff0-167">在**添加模块**对话框中，选择**默认页面**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-168">在默认页的**主**插槽中，选择省略号 (**...**)，然后选择**添加页面片段**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="8cff0-169">在**选择页面片段**对话框中，选择您之前创建的**购买框片段**片段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-169">In the **Select Page Fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-170">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="8cff0-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="8cff0-171">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="8cff0-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="8cff0-172">在**选择模板**对话框中，选择 **PDP 模板**模板。</span><span class="sxs-lookup"><span data-stu-id="8cff0-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="8cff0-173">在**页面名称**下，输入 **PDP 页面**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-174">在新页面的**主**插槽中，选择省略号 (**...**)，然后选择**添加页面片段**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="8cff0-175">在**选择页面片段**对话框中，选择您之前创建的**购买框片段**片段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-175">In the **Select Page Fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="8cff0-176">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="8cff0-176">Save and preview the page.</span></span> <span data-ttu-id="8cff0-177">在上一页的 URL 中添加查询字符串参数 **?productid=&lt;product id&gt;**。</span><span class="sxs-lookup"><span data-stu-id="8cff0-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="8cff0-178">这样，将把产品上下文用于加载和显示上一页。</span><span class="sxs-lookup"><span data-stu-id="8cff0-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="8cff0-179">选择**保存**，选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="8cff0-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="8cff0-180">应该会在产品详细信息页显示一个购买框。</span><span class="sxs-lookup"><span data-stu-id="8cff0-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cff0-181">其他资源</span><span class="sxs-lookup"><span data-stu-id="8cff0-181">Additional resources</span></span>

[<span data-ttu-id="8cff0-182">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="8cff0-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8cff0-183">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8cff0-184">媒体库模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="8cff0-185">容器模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8cff0-186">购物车模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8cff0-187">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8cff0-188">结帐模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8cff0-189">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8cff0-190">标题模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8cff0-191">页脚模块</span><span class="sxs-lookup"><span data-stu-id="8cff0-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="8cff0-192">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="8cff0-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
