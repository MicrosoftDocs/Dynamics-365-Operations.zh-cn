---
title: 地图模块
description: 此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646870"
---
# <a name="map-module"></a><span data-ttu-id="a079f-103">地图模块</span><span class="sxs-lookup"><span data-stu-id="a079f-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a079f-104">此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。</span><span class="sxs-lookup"><span data-stu-id="a079f-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a079f-105">概览</span><span class="sxs-lookup"><span data-stu-id="a079f-105">Overview</span></span>

<span data-ttu-id="a079f-106">地图模块在使用[必应地图 V8 Web 控件](https://docs.microsoft.com/bingmaps/v8-web-control/)呈现的交互式地图上显示商店位置。</span><span class="sxs-lookup"><span data-stu-id="a079f-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="a079f-107">必须提供必应地图 API 密钥，并且必须将其添加到 Commerce headquarters 内的共享参数页面中。</span><span class="sxs-lookup"><span data-stu-id="a079f-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="a079f-108">地图模块提供不同的视图，如道路、空中和街边，用户可以选择这些视图来查看地图位置。</span><span class="sxs-lookup"><span data-stu-id="a079f-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="a079f-109">它们还允许进行交互，如缩放和使用用户的位置。</span><span class="sxs-lookup"><span data-stu-id="a079f-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="a079f-110">将地图模块与商店选择器模块结合使用可以确定必须在地图上呈现的商店的地理位置。</span><span class="sxs-lookup"><span data-stu-id="a079f-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="a079f-111">当用户在站点页面上的其中一个模块中选择商店时，商店选择器和地图模块进行交互。</span><span class="sxs-lookup"><span data-stu-id="a079f-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="a079f-112">除了与商店选择器模块进行交互外，地图模块还可以针对其他场景扩展。</span><span class="sxs-lookup"><span data-stu-id="a079f-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="a079f-113">但是，需要对模块进行自定义。</span><span class="sxs-lookup"><span data-stu-id="a079f-113">However, module customization is required.</span></span>

<span data-ttu-id="a079f-114">地图模块在 Commerce 版本 10.0.13 中引入。</span><span class="sxs-lookup"><span data-stu-id="a079f-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="a079f-115">下图显示了商店位置页面上使用的地图块模块的示例。</span><span class="sxs-lookup"><span data-stu-id="a079f-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![商店选择器模块的示例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="a079f-117">模块属性</span><span class="sxs-lookup"><span data-stu-id="a079f-117">Module properties</span></span>

| <span data-ttu-id="a079f-118">属性名称</span><span class="sxs-lookup"><span data-stu-id="a079f-118">Property name</span></span>             | <span data-ttu-id="a079f-119">值</span><span class="sxs-lookup"><span data-stu-id="a079f-119">Value</span></span>                 | <span data-ttu-id="a079f-120">说明</span><span class="sxs-lookup"><span data-stu-id="a079f-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="a079f-121">标题</span><span class="sxs-lookup"><span data-stu-id="a079f-121">Heading</span></span> | <span data-ttu-id="a079f-122">文本</span><span class="sxs-lookup"><span data-stu-id="a079f-122">Text</span></span> | <span data-ttu-id="a079f-123">模块的标题。</span><span class="sxs-lookup"><span data-stu-id="a079f-123">The heading for the module.</span></span> |
| <span data-ttu-id="a079f-124">图钉选项：默认图标</span><span class="sxs-lookup"><span data-stu-id="a079f-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="a079f-125">头像</span><span class="sxs-lookup"><span data-stu-id="a079f-125">Image</span></span> | <span data-ttu-id="a079f-126">用于地图上显示的商店的图钉符号图像。</span><span class="sxs-lookup"><span data-stu-id="a079f-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="a079f-127">图钉选项：活动图标</span><span class="sxs-lookup"><span data-stu-id="a079f-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="a079f-128">头像</span><span class="sxs-lookup"><span data-stu-id="a079f-128">Image</span></span> | <span data-ttu-id="a079f-129">用于在地图上选择的商店的图钉符号图像。</span><span class="sxs-lookup"><span data-stu-id="a079f-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="a079f-130">图钉选项：默认图标颜色</span><span class="sxs-lookup"><span data-stu-id="a079f-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="a079f-131">字符串</span><span class="sxs-lookup"><span data-stu-id="a079f-131">Character string</span></span> | <span data-ttu-id="a079f-132">地图上图钉符号颜色的文本或十六进制值。</span><span class="sxs-lookup"><span data-stu-id="a079f-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="a079f-133">图钉选项：活动图标颜色</span><span class="sxs-lookup"><span data-stu-id="a079f-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="a079f-134">字符串</span><span class="sxs-lookup"><span data-stu-id="a079f-134">Character string</span></span> | <span data-ttu-id="a079f-135">地图上所选图钉符号的颜色的文本或十六进制值。</span><span class="sxs-lookup"><span data-stu-id="a079f-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="a079f-136">显示索引</span><span class="sxs-lookup"><span data-stu-id="a079f-136">Show index</span></span> | <span data-ttu-id="a079f-137">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="a079f-137">**True** or **False**</span></span> | <span data-ttu-id="a079f-138">如果将此属性设置为 **True**，表示商店的每个图钉符号将显示一个索引。</span><span class="sxs-lookup"><span data-stu-id="a079f-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="a079f-139">此索引将与商店选择器模块显示的列表视图中的索引匹配。</span><span class="sxs-lookup"><span data-stu-id="a079f-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="a079f-140">将允许的映射 URL 添加到站点的内容安全策略指令中</span><span class="sxs-lookup"><span data-stu-id="a079f-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="a079f-141">要使地图模块与必应地图交互，您必须确保根据站点的内容安全策略 (CSP) 允许以下映射 URL（也称为“加入允许列表”）。</span><span class="sxs-lookup"><span data-stu-id="a079f-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="a079f-142">通过在各个站点 CSP 指令中添加允许的 URL（例如，**img-src**），在 Commerce 站点构建器中完成此设置。</span><span class="sxs-lookup"><span data-stu-id="a079f-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="a079f-143">有关详细信息，请参阅[内容安全策略](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="a079f-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="a079f-144">对于 **connect-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="a079f-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="a079f-145">对于 **img-src** 指令，添加 **&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="a079f-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="a079f-146">对于 **script-src** 指令，添加 **&#42;.bing.com、&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="a079f-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="a079f-147">对于 **script style-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="a079f-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="a079f-148">向页面添加地图模块</span><span class="sxs-lookup"><span data-stu-id="a079f-148">Add a map module to a page</span></span>

<span data-ttu-id="a079f-149">有关如何在页面上配置地图模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="a079f-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="a079f-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="a079f-150">Additional resources</span></span>

[<span data-ttu-id="a079f-151">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="a079f-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a079f-152">购买框模块</span><span class="sxs-lookup"><span data-stu-id="a079f-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a079f-153">购物车模块</span><span class="sxs-lookup"><span data-stu-id="a079f-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a079f-154">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="a079f-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a079f-155">为您的组织管理必应地图</span><span class="sxs-lookup"><span data-stu-id="a079f-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="a079f-156">必应地图 V8 Web 控件</span><span class="sxs-lookup"><span data-stu-id="a079f-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
