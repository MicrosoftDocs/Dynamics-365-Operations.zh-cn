---
title: 地图模块
description: 此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794179"
---
# <a name="map-module"></a><span data-ttu-id="061f4-103">地图模块</span><span class="sxs-lookup"><span data-stu-id="061f4-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="061f4-104">此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。</span><span class="sxs-lookup"><span data-stu-id="061f4-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="061f4-105">地图模块在使用[必应地图 V8 Web 控件](https://docs.microsoft.com/bingmaps/v8-web-control/)呈现的交互式地图上显示商店位置。</span><span class="sxs-lookup"><span data-stu-id="061f4-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="061f4-106">必须提供必应地图 API 密钥，并且必须将其添加到 Commerce headquarters 内的共享参数页面中。</span><span class="sxs-lookup"><span data-stu-id="061f4-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="061f4-107">地图模块提供不同的视图，如道路、空中和街边，用户可以选择这些视图来查看地图位置。</span><span class="sxs-lookup"><span data-stu-id="061f4-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="061f4-108">它们还允许进行交互，如缩放和使用用户的位置。</span><span class="sxs-lookup"><span data-stu-id="061f4-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="061f4-109">将地图模块与商店选择器模块结合使用可以确定必须在地图上呈现的商店的地理位置。</span><span class="sxs-lookup"><span data-stu-id="061f4-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="061f4-110">当用户在站点页面上的其中一个模块中选择商店时，商店选择器和地图模块进行交互。</span><span class="sxs-lookup"><span data-stu-id="061f4-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="061f4-111">除了与商店选择器模块进行交互外，地图模块还可以针对其他场景扩展。</span><span class="sxs-lookup"><span data-stu-id="061f4-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="061f4-112">但是，需要对模块进行自定义。</span><span class="sxs-lookup"><span data-stu-id="061f4-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="061f4-113">此地图模块在 Dynamics 365 Commerce 10.0.13 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="061f4-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="061f4-114">下图显示了商店位置页面上使用的地图块模块的示例。</span><span class="sxs-lookup"><span data-stu-id="061f4-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![商店选择器模块的示例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="061f4-116">模块属性</span><span class="sxs-lookup"><span data-stu-id="061f4-116">Module properties</span></span>

| <span data-ttu-id="061f4-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="061f4-117">Property name</span></span>             | <span data-ttu-id="061f4-118">值</span><span class="sxs-lookup"><span data-stu-id="061f4-118">Value</span></span>                 | <span data-ttu-id="061f4-119">说明</span><span class="sxs-lookup"><span data-stu-id="061f4-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="061f4-120">标题</span><span class="sxs-lookup"><span data-stu-id="061f4-120">Heading</span></span> | <span data-ttu-id="061f4-121">文本</span><span class="sxs-lookup"><span data-stu-id="061f4-121">Text</span></span> | <span data-ttu-id="061f4-122">模块的标题。</span><span class="sxs-lookup"><span data-stu-id="061f4-122">The heading for the module.</span></span> |
| <span data-ttu-id="061f4-123">图钉选项：默认图标</span><span class="sxs-lookup"><span data-stu-id="061f4-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="061f4-124">头像</span><span class="sxs-lookup"><span data-stu-id="061f4-124">Image</span></span> | <span data-ttu-id="061f4-125">用于地图上显示的商店的图钉符号图像。</span><span class="sxs-lookup"><span data-stu-id="061f4-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="061f4-126">图钉选项：活动图标</span><span class="sxs-lookup"><span data-stu-id="061f4-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="061f4-127">头像</span><span class="sxs-lookup"><span data-stu-id="061f4-127">Image</span></span> | <span data-ttu-id="061f4-128">用于在地图上选择的商店的图钉符号图像。</span><span class="sxs-lookup"><span data-stu-id="061f4-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="061f4-129">图钉选项：默认图标颜色</span><span class="sxs-lookup"><span data-stu-id="061f4-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="061f4-130">字符串</span><span class="sxs-lookup"><span data-stu-id="061f4-130">Character string</span></span> | <span data-ttu-id="061f4-131">地图上图钉符号颜色的文本或十六进制值。</span><span class="sxs-lookup"><span data-stu-id="061f4-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="061f4-132">图钉选项：活动图标颜色</span><span class="sxs-lookup"><span data-stu-id="061f4-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="061f4-133">字符串</span><span class="sxs-lookup"><span data-stu-id="061f4-133">Character string</span></span> | <span data-ttu-id="061f4-134">地图上所选图钉符号的颜色的文本或十六进制值。</span><span class="sxs-lookup"><span data-stu-id="061f4-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="061f4-135">显示索引</span><span class="sxs-lookup"><span data-stu-id="061f4-135">Show index</span></span> | <span data-ttu-id="061f4-136">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="061f4-136">**True** or **False**</span></span> | <span data-ttu-id="061f4-137">如果将此属性设置为 **True**，表示商店的每个图钉符号将显示一个索引。</span><span class="sxs-lookup"><span data-stu-id="061f4-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="061f4-138">此索引将与商店选择器模块显示的列表视图中的索引匹配。</span><span class="sxs-lookup"><span data-stu-id="061f4-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="061f4-139">将允许的映射 URL 添加到站点的内容安全策略指令中</span><span class="sxs-lookup"><span data-stu-id="061f4-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="061f4-140">若要使地图模块与必应地图交互，您必须确保根据站点的内容安全策略 (CSP) 允许以下映射 URL。</span><span class="sxs-lookup"><span data-stu-id="061f4-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="061f4-141">通过在各个站点 CSP 指令中添加允许的 URL（例如，**img-src**），在 Commerce 站点构建器中完成此设置。</span><span class="sxs-lookup"><span data-stu-id="061f4-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="061f4-142">有关详细信息，请参阅[内容安全策略](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="061f4-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="061f4-143">对于 **connect-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="061f4-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="061f4-144">对于 **img-src** 指令，添加 **&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="061f4-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="061f4-145">对于 **script-src** 指令，添加 **&#42;.bing.com、&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="061f4-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="061f4-146">对于 **script style-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="061f4-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="061f4-147">向页面添加地图模块</span><span class="sxs-lookup"><span data-stu-id="061f4-147">Add a map module to a page</span></span>

<span data-ttu-id="061f4-148">有关如何在页面上配置地图模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="061f4-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="061f4-149">其他资源</span><span class="sxs-lookup"><span data-stu-id="061f4-149">Additional resources</span></span>

[<span data-ttu-id="061f4-150">模块库概述</span><span class="sxs-lookup"><span data-stu-id="061f4-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="061f4-151">购买框模块</span><span class="sxs-lookup"><span data-stu-id="061f4-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="061f4-152">购物车模块</span><span class="sxs-lookup"><span data-stu-id="061f4-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="061f4-153">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="061f4-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="061f4-154">为您的组织管理必应地图</span><span class="sxs-lookup"><span data-stu-id="061f4-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="061f4-155">必应地图 V8 Web 控件</span><span class="sxs-lookup"><span data-stu-id="061f4-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]