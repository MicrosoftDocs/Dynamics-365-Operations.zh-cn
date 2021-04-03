---
title: 快速查看模块
description: 此主题介绍快速查看模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243785"
---
# <a name="quick-view-module"></a><span data-ttu-id="e6a27-103">快速查看模块</span><span class="sxs-lookup"><span data-stu-id="e6a27-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e6a27-104">此主题介绍快速查看模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="e6a27-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e6a27-105">快速查看模块让用户在浏览列表页上的产品时可以快速查看产品信息，并从列表页将一个或多个产品添加到购物车中，而不必转到产品详细信息页 (PDP)。</span><span class="sxs-lookup"><span data-stu-id="e6a27-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="e6a27-106">快速查看模块提供用户作出“添加到购物车”决定所需的产品信息的概览。</span><span class="sxs-lookup"><span data-stu-id="e6a27-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="e6a27-107">它还提供到 PDP 的链接，让用户可以查看其他产品详细信息和购买选项。</span><span class="sxs-lookup"><span data-stu-id="e6a27-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="e6a27-108">快速查看模块由[产品集合](product-collection-module-overview.md)和[搜索结果](search-result-module.md)模块支持。</span><span class="sxs-lookup"><span data-stu-id="e6a27-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6a27-109">快速查看模块自 Commerce 版本 10.0.17 开始提供。</span><span class="sxs-lookup"><span data-stu-id="e6a27-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="e6a27-110">下图显示了产品列表页上的快速查看模块的示例。</span><span class="sxs-lookup"><span data-stu-id="e6a27-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![产品列表页上的快速查看模块的示例](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="e6a27-112">模块属性</span><span class="sxs-lookup"><span data-stu-id="e6a27-112">Module properties</span></span>

<span data-ttu-id="e6a27-113">快速查看模块支持与购买框模块相同的功能。</span><span class="sxs-lookup"><span data-stu-id="e6a27-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="e6a27-114">因此，快速查看模块的属性类似于购买框模块的属性。</span><span class="sxs-lookup"><span data-stu-id="e6a27-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="e6a27-115">属性</span><span class="sxs-lookup"><span data-stu-id="e6a27-115">Property</span></span> | <span data-ttu-id="e6a27-116">值</span><span class="sxs-lookup"><span data-stu-id="e6a27-116">Values</span></span> | <span data-ttu-id="e6a27-117">说明</span><span class="sxs-lookup"><span data-stu-id="e6a27-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e6a27-118">标题标记</span><span class="sxs-lookup"><span data-stu-id="e6a27-118">Heading tag</span></span> | <span data-ttu-id="e6a27-119">**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**</span><span class="sxs-lookup"><span data-stu-id="e6a27-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="e6a27-120">此属性定义产品标题的标题标签。</span><span class="sxs-lookup"><span data-stu-id="e6a27-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="e6a27-121">如果快速查看模块位于页面顶部，此属性应设置为 **H1** 以达到可访问性标准。</span><span class="sxs-lookup"><span data-stu-id="e6a27-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="e6a27-122">允许自定义价格</span><span class="sxs-lookup"><span data-stu-id="e6a27-122">Allow custom price</span></span> | <span data-ttu-id="e6a27-123">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e6a27-123">**True** or **False**</span></span> | <span data-ttu-id="e6a27-124">如果将此属性设置为 **True**，用户可以输入自定义价格。</span><span class="sxs-lookup"><span data-stu-id="e6a27-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="e6a27-125">最低价格</span><span class="sxs-lookup"><span data-stu-id="e6a27-125">Minimum price</span></span> | <span data-ttu-id="e6a27-126">整数</span><span class="sxs-lookup"><span data-stu-id="e6a27-126">Integer</span></span> | <span data-ttu-id="e6a27-127">仅当 **允许自定义价格** 属性设置为 **True** 时，此属性才适用。</span><span class="sxs-lookup"><span data-stu-id="e6a27-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="e6a27-128">它定义用户可以输入的最低价格（例如，$1）。</span><span class="sxs-lookup"><span data-stu-id="e6a27-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="e6a27-129">最高价格</span><span class="sxs-lookup"><span data-stu-id="e6a27-129">Maximum price</span></span> | <span data-ttu-id="e6a27-130">整数</span><span class="sxs-lookup"><span data-stu-id="e6a27-130">Integer</span></span> | <span data-ttu-id="e6a27-131">仅当 **允许自定义价格** 属性设置为 **True** 时，此属性才适用。</span><span class="sxs-lookup"><span data-stu-id="e6a27-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="e6a27-132">它定义用户可以输入的最高价格（例如，$1,000）。</span><span class="sxs-lookup"><span data-stu-id="e6a27-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="e6a27-133">Commerce 站点构建器设置</span><span class="sxs-lookup"><span data-stu-id="e6a27-133">Commerce site builder settings</span></span>

<span data-ttu-id="e6a27-134">与购买框模块一样，快速查看模块遵照 **站点设置 \> 扩展 \> 将产品添加到购物车** 的设置。</span><span class="sxs-lookup"><span data-stu-id="e6a27-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="e6a27-135">但是，**导航到购物车页面** 设置将被忽略，因为它与快速查看模块的目的不一致，后者的目的是让用户能够在列表页上浏览多个产品并将其添加到购物车，而无需离开列表页。</span><span class="sxs-lookup"><span data-stu-id="e6a27-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="e6a27-136">将快速查看模块添加到产品集合模块</span><span class="sxs-lookup"><span data-stu-id="e6a27-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="e6a27-137">可以将快速查看模块添加到产品集合和搜索结果模块。</span><span class="sxs-lookup"><span data-stu-id="e6a27-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="e6a27-138">要将快速查看模块添加到 Commerce 站点构建器中的产品集合模块，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e6a27-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6a27-139">转到 **页面**，然后选择 Fabrikam 站点的主页。</span><span class="sxs-lookup"><span data-stu-id="e6a27-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="e6a27-140">转到主页上的任何 **产品集合** 模块，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="e6a27-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6a27-141">在 **添加模块** 对话框中，选择 **快速查看** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e6a27-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6a27-142">在 **快速查看** 模块的属性窗格中，选择 **标题**。</span><span class="sxs-lookup"><span data-stu-id="e6a27-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="e6a27-143">在 **标题** 对话框中，将 **标题级别** 字段设置为 **H2**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e6a27-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="e6a27-144">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="e6a27-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6a27-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="e6a27-145">Additional resources</span></span>

[<span data-ttu-id="e6a27-146">模块库概览</span><span class="sxs-lookup"><span data-stu-id="e6a27-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e6a27-147">购买框模块</span><span class="sxs-lookup"><span data-stu-id="e6a27-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e6a27-148">产品集合模块</span><span class="sxs-lookup"><span data-stu-id="e6a27-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="e6a27-149">搜索结果模块</span><span class="sxs-lookup"><span data-stu-id="e6a27-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]