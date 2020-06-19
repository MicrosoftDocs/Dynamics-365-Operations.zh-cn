---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411265"
---
# <a name="cart-module"></a><span data-ttu-id="3d42d-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3d42d-104">此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="3d42d-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3d42d-105">概览</span><span class="sxs-lookup"><span data-stu-id="3d42d-105">Overview</span></span>

<span data-ttu-id="3d42d-106">购物车模块显示客户继续结帐之前已添加到购物车中的物品。</span><span class="sxs-lookup"><span data-stu-id="3d42d-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3d42d-107">此模块还显示订单摘要，并让客户可以应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="3d42d-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3d42d-108">购物车模块支持登录结帐和访客结帐。</span><span class="sxs-lookup"><span data-stu-id="3d42d-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3d42d-109">它还支持**返回购物**链接。</span><span class="sxs-lookup"><span data-stu-id="3d42d-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3d42d-110">您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。</span><span class="sxs-lookup"><span data-stu-id="3d42d-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3d42d-111">购物车模块根据购物车 ID 呈现数据，购物车 ID 是整个站点可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="3d42d-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="3d42d-112">下图显示了 Fabrikam 站点上购物车页面的示例。</span><span class="sxs-lookup"><span data-stu-id="3d42d-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![购物车模块的示例](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3d42d-114">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="3d42d-114">Cart module properties and slots</span></span>

<span data-ttu-id="3d42d-115">购物车模块有一个**标题**属性，此属性可以设置为**购物袋**和**购物车中的商品**之类的值。</span><span class="sxs-lookup"><span data-stu-id="3d42d-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3d42d-116">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3d42d-117">**文本块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="3d42d-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3d42d-118">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="3d42d-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3d42d-119">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="3d42d-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3d42d-120">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="3d42d-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3d42d-121">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="3d42d-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3d42d-122">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="3d42d-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="3d42d-123">模块属性</span><span class="sxs-lookup"><span data-stu-id="3d42d-123">Module properties</span></span>

<span data-ttu-id="3d42d-124">以下购物车模块设置可以在**站点设置 \> 扩展**中配置：</span><span class="sxs-lookup"><span data-stu-id="3d42d-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="3d42d-125">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="3d42d-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3d42d-126">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="3d42d-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3d42d-127">**库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="3d42d-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="3d42d-128">**返回购物** – 该属性用于指定**返回购物**链接的路由。</span><span class="sxs-lookup"><span data-stu-id="3d42d-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3d42d-129">可以在站点级别配置路由，让零售商可以将客户带回到站点的主页或其他任何页面。</span><span class="sxs-lookup"><span data-stu-id="3d42d-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3d42d-130">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="3d42d-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3d42d-131">购物车模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="3d42d-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3d42d-132">浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="3d42d-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3d42d-133">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-133">Add a cart module to a page</span></span>

<span data-ttu-id="3d42d-134">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3d42d-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3d42d-135">转到**页面片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="3d42d-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3d42d-136">在**新建页面片段**对话框中，选择**购物车**模块。</span><span class="sxs-lookup"><span data-stu-id="3d42d-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="3d42d-137">在**页面片段名称**下，输入名称**购物车片段**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="3d42d-138">选择**购物车**插槽。</span><span class="sxs-lookup"><span data-stu-id="3d42d-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="3d42d-139">在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。</span><span class="sxs-lookup"><span data-stu-id="3d42d-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="3d42d-140">在**购物车**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3d42d-141">在**添加模块**对话框中，选择**商店选择器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3d42d-142">选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="3d42d-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3d42d-143">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="3d42d-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3d42d-144">在**新建模板**对话框的**模板名称**下，为模板输入名称。</span><span class="sxs-lookup"><span data-stu-id="3d42d-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="3d42d-145">在大纲树中，选择**正文**插槽，选择省略号 (**...**)，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="3d42d-146">在**选择页面片段**对话框中，选择**购物车片段**片段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3d42d-147">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="3d42d-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3d42d-148">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="3d42d-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3d42d-149">在**选择模板**对话框中，选择您创建的模板，输入页面名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="3d42d-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="3d42d-150">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="3d42d-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3d42d-151">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="3d42d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d42d-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="3d42d-152">Additional resources</span></span>

[<span data-ttu-id="3d42d-153">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="3d42d-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3d42d-154">容器模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3d42d-155">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="3d42d-156">购买框模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3d42d-157">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3d42d-158">结账模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3d42d-159">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3d42d-160">标题模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3d42d-161">页脚模块</span><span class="sxs-lookup"><span data-stu-id="3d42d-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="3d42d-162">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="3d42d-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
