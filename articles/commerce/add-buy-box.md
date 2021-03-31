---
title: 购买框模块
description: 此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ddaf34ed2dec882310e5363db643bb522be1238
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206527"
---
# <a name="buy-box-module"></a><span data-ttu-id="b5faa-103">购买框模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5faa-104">此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="b5faa-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b5faa-105">术语 *购买框* 通常指的是产品详细信息页中的“第一屏”区域，用于承载进行产品购买所需全部最重要信息。</span><span class="sxs-lookup"><span data-stu-id="b5faa-105">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="b5faa-106">（“第一屏”区域在首次加载页面时显示，所以用户不必向下滚动即可看到。）</span><span class="sxs-lookup"><span data-stu-id="b5faa-106">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="b5faa-107">购买框模块是特殊容器，用于承载产品详细信息页购买框区域中显示的所有模块。</span><span class="sxs-lookup"><span data-stu-id="b5faa-107">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="b5faa-108">产品详细信息页的 URL 中包含产品 ID。</span><span class="sxs-lookup"><span data-stu-id="b5faa-108">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="b5faa-109">显示购买框模块所需全部信息派生自此产品 ID。</span><span class="sxs-lookup"><span data-stu-id="b5faa-109">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="b5faa-110">如果不提供产品 ID，则不能在页面中正确显示购买框模块。</span><span class="sxs-lookup"><span data-stu-id="b5faa-110">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="b5faa-111">因此，购买框模块只能在具有产品上下文的页面上使用。</span><span class="sxs-lookup"><span data-stu-id="b5faa-111">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="b5faa-112">要在没有产品上下文的页面（例如，主页或市场营销页面）上使用它，您必须进行其他自定义。</span><span class="sxs-lookup"><span data-stu-id="b5faa-112">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="b5faa-113">下图显示了产品详细信息页上的购买框模块的示例。</span><span class="sxs-lookup"><span data-stu-id="b5faa-113">The following image shows an example of a buy box module on a product details page.</span></span>

![购买框模块的示例](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="b5faa-115">购买框模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="b5faa-115">Buy box module properties and slots</span></span> 

<span data-ttu-id="b5faa-116">在产品详细信息页，购买框拆分为两个区域：左侧媒体区域，右侧内容区域。</span><span class="sxs-lookup"><span data-stu-id="b5faa-116">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="b5faa-117">默认情况下，媒体区域列的宽度与内容区域列的宽度之比为 2:1。</span><span class="sxs-lookup"><span data-stu-id="b5faa-117">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="b5faa-118">在移动设备上，这两个区域堆叠，所以一个区域在另一个区域下方显示。</span><span class="sxs-lookup"><span data-stu-id="b5faa-118">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="b5faa-119">主题可用于自定义列宽和堆叠等级。</span><span class="sxs-lookup"><span data-stu-id="b5faa-119">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="b5faa-120">购买框模块呈现产品的标题、描述、价格和等级。</span><span class="sxs-lookup"><span data-stu-id="b5faa-120">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="b5faa-121">还可以让客户选择具有不同产品属性（例如尺寸、样式和颜色）的产品变型。</span><span class="sxs-lookup"><span data-stu-id="b5faa-121">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="b5faa-122">如果选择了产品变型，将更新购买框中的其他属性（如产品描述和图像）以反映变型信息。</span><span class="sxs-lookup"><span data-stu-id="b5faa-122">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="b5faa-123">提供数量选择器，以便客户可以指定要购买的商品数量。</span><span class="sxs-lookup"><span data-stu-id="b5faa-123">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="b5faa-124">可以在站点设置中定义可以购买的最大数量。</span><span class="sxs-lookup"><span data-stu-id="b5faa-124">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="b5faa-125">客户还可以从购买框中执行一些操作，例如将产品添加到购物车，将产品添加到其愿望列表以及选择取货地点。</span><span class="sxs-lookup"><span data-stu-id="b5faa-125">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="b5faa-126">可以在产品或产品变型上执行这些操作。</span><span class="sxs-lookup"><span data-stu-id="b5faa-126">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="b5faa-127">要将产品添加到愿望列表中，客户必须先登录。</span><span class="sxs-lookup"><span data-stu-id="b5faa-127">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="b5faa-128">主题可用于删除或更改购买框产品属性和操作控件的顺序。</span><span class="sxs-lookup"><span data-stu-id="b5faa-128">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="b5faa-129">模块属性</span><span class="sxs-lookup"><span data-stu-id="b5faa-129">Module properties</span></span>

- <span data-ttu-id="b5faa-130">**标题标签** – 此属性定义产品标题的标题标签。</span><span class="sxs-lookup"><span data-stu-id="b5faa-130">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="b5faa-131">如果购买框位于页面顶部，则此属性应设置为 **h1** 以达到可访问性标准。</span><span class="sxs-lookup"><span data-stu-id="b5faa-131">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="b5faa-132">**启用“购买相似外观产品”建议** - 此属性允许购买框显示与最近所查看商品外观类似的产品的链接。</span><span class="sxs-lookup"><span data-stu-id="b5faa-132">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="b5faa-133">Commerce 版本 10.0.13 及更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="b5faa-133">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="b5faa-134">购买框模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-134">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="b5faa-135">**媒体库** – 此模块用于展示产品详细信息页上的产品图像。</span><span class="sxs-lookup"><span data-stu-id="b5faa-135">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="b5faa-136">有关此模块的详细信息，请参阅[媒体库模块](media-gallery-module.md)。</span><span class="sxs-lookup"><span data-stu-id="b5faa-136">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="b5faa-137">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="b5faa-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b5faa-138">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="b5faa-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b5faa-139">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="b5faa-139">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="b5faa-140">**社交共享** - 可将此模块添加到购买框，以便允许用户在社交媒体中共享产品信息。</span><span class="sxs-lookup"><span data-stu-id="b5faa-140">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="b5faa-141">有关详细信息，请参阅[社交共享模块](social-share-module.md)。</span><span class="sxs-lookup"><span data-stu-id="b5faa-141">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="b5faa-142">购买框模块设置</span><span class="sxs-lookup"><span data-stu-id="b5faa-142">Buy box module settings</span></span>

<span data-ttu-id="b5faa-143">以下购买框模块设置可以在 **站点设置 \> 扩展** 中配置：</span><span class="sxs-lookup"><span data-stu-id="b5faa-143">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b5faa-144">**购物车行数量限制** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="b5faa-144">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b5faa-145">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="b5faa-145">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b5faa-146">**库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="b5faa-146">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="b5faa-147">**将产品添加到购物车** - 此属性用于指定将物料添加到购物车后的行为。</span><span class="sxs-lookup"><span data-stu-id="b5faa-147">**Add product to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="b5faa-148">可能的值为 **导航到购物车页面**、**不导航到购物车页面** 和 **显示通知**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-148">The possible values are **Navigate to cart page**, **Do not navigate to cart page**, and **Show notification**.</span></span> <span data-ttu-id="b5faa-149">当此值设置为 **导航到购物车页面** 时，用户将在添加物料后转到购物车页面。</span><span class="sxs-lookup"><span data-stu-id="b5faa-149">When the value is set to **Navigate to cart page**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="b5faa-150">当此值设置为 **不导航到购物车页面** 时，用户在添加物料后不会转到购物车页面。</span><span class="sxs-lookup"><span data-stu-id="b5faa-150">When the value is set to **Do not navigate to cart page**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="b5faa-151">当此值设置为 **显示通知** 时，会向用户显示一条确认通知，用户可以继续在产品详细信息页面上浏览。</span><span class="sxs-lookup"><span data-stu-id="b5faa-151">When the value is set to **Show notification**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b5faa-152">**将产品添加到购物车** 站点设置在 Dynamics 365 Commerce 10.0.11 版本中可用。</span><span class="sxs-lookup"><span data-stu-id="b5faa-152">The **Add product to cart** site settings are available in the Dynamics 365 Commerce 10.0.11 release.</span></span> <span data-ttu-id="b5faa-153">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="b5faa-153">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b5faa-154">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="b5faa-154">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

<span data-ttu-id="b5faa-155">下图显示了 Fabrikam 站点上“已添加到购物车”确认通知的示例。</span><span class="sxs-lookup"><span data-stu-id="b5faa-155">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

![通知模块示例](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b5faa-157">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="b5faa-157">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b5faa-158">购买框模块使用 Commerce Scale Unit 应用程序编程接口 (API) 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="b5faa-158">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="b5faa-159">产品详细信息页中的产品 ID 用于检索所有信息。</span><span class="sxs-lookup"><span data-stu-id="b5faa-159">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="b5faa-160">向页面添加购买框模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-160">Add a buy box module to a page</span></span>

<span data-ttu-id="b5faa-161">若要向新页面添加购买框模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b5faa-161">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b5faa-162">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="b5faa-162">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b5faa-163">在 **新建片段** 对话框中，选择 **购买框** 模块。</span><span class="sxs-lookup"><span data-stu-id="b5faa-163">In the **New fragment** dialog box, select the **Buy box** module.</span></span>
1. <span data-ttu-id="b5faa-164">在 **片段名称** 下，输入名称 **购买框片段**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-164">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-165">在购买框模块的 **媒体库** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-165">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5faa-166">在 **添加模块** 对话框中，选择 **媒体库** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-166">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-167">在购买框模块的 **商店选择器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-167">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5faa-168">在 **添加模块** 对话框中，选择 **商店选择器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-168">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-169">选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b5faa-169">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b5faa-170">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="b5faa-170">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b5faa-171">在 **新建模板** 对话框的 **模板名称** 下，输入 **PDP 模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-171">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-172">在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-172">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5faa-173">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-173">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-174">在默认页的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-174">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b5faa-175">在 **选择片段** 对话框中，选择您之前创建的 **购买框片段** 片段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-175">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-176">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b5faa-176">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b5faa-177">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="b5faa-177">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b5faa-178">在 **选择模板** 对话框中，选择 **PDP 模板** 模板。</span><span class="sxs-lookup"><span data-stu-id="b5faa-178">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="b5faa-179">在 **页面名称** 下，输入 **PDP 页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-179">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-180">在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-180">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b5faa-181">在 **选择片段** 对话框中，选择您之前创建的 **购买框片段** 片段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-181">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="b5faa-182">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="b5faa-182">Save and preview the page.</span></span> <span data-ttu-id="b5faa-183">在上一页的 URL 中添加查询字符串参数 **?productid=&lt;product id&gt;**。</span><span class="sxs-lookup"><span data-stu-id="b5faa-183">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="b5faa-184">这样，将把产品上下文用于加载和显示上一页。</span><span class="sxs-lookup"><span data-stu-id="b5faa-184">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="b5faa-185">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b5faa-185">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="b5faa-186">应该会在产品详细信息页显示一个购买框。</span><span class="sxs-lookup"><span data-stu-id="b5faa-186">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5faa-187">其他资源</span><span class="sxs-lookup"><span data-stu-id="b5faa-187">Additional resources</span></span>

[<span data-ttu-id="b5faa-188">模块库概述</span><span class="sxs-lookup"><span data-stu-id="b5faa-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5faa-189">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-189">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b5faa-190">媒体库模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-190">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="b5faa-191">容器模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-191">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b5faa-192">购物车模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-192">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5faa-193">结帐模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-193">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b5faa-194">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-194">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b5faa-195">标题模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-195">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b5faa-196">页脚模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-196">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="b5faa-197">社交共享模块</span><span class="sxs-lookup"><span data-stu-id="b5faa-197">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="b5faa-198">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="b5faa-198">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="b5faa-199">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="b5faa-199">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]