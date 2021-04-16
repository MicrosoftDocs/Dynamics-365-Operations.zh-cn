---
title: 丰富类别登陆页面
description: 此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799003"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="448d4-103">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="448d4-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="448d4-104">此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="448d4-105">Commerce 提供显示类别数据时使用的默认类别登陆页。</span><span class="sxs-lookup"><span data-stu-id="448d4-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="448d4-106">默认类别页中包含必需的元素，如优化器、已分类的产品放置、排序选项、选项汇总和分页控件。</span><span class="sxs-lookup"><span data-stu-id="448d4-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="448d4-107">但是，不应使用默认类别页，而是使用包含更多内容和更多特定元素的“扩充的”类别登陆页。</span><span class="sxs-lookup"><span data-stu-id="448d4-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="448d4-108">典型的扩充包括向类别页添加类别特定的市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="448d4-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="448d4-109">此内容可能包括交叉销售用途的交叉类别产品放置、编辑列表、图像、视频和其他文本。</span><span class="sxs-lookup"><span data-stu-id="448d4-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="448d4-110">可以修改默认类别页或为特定类别定义其他类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![扩充的类别登陆页面](./media/CategoryLandingPages.png)

<span data-ttu-id="448d4-112">在 Commerce 站点构建器中，**产品** 页包含渠道中分配给站点的类别的列表。</span><span class="sxs-lookup"><span data-stu-id="448d4-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="448d4-113">如果为类别页选择 **扩充** 状态，则说明该类别页已扩充。</span><span class="sxs-lookup"><span data-stu-id="448d4-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="448d4-114">否则，对类别使用默认类别页和内容。</span><span class="sxs-lookup"><span data-stu-id="448d4-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="448d4-115">可通过选择类别名称预览类别的扩充类别页和未扩充类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="448d4-116">若要扩充类别页，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="448d4-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="448d4-117">在 **产品** 页中，选择要扩充其类别页的类别的名称。</span><span class="sxs-lookup"><span data-stu-id="448d4-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="448d4-118">将在页面编辑器中打开所选类别的默认类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="448d4-119">选择 **扩充类别页**。</span><span class="sxs-lookup"><span data-stu-id="448d4-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="448d4-120">选择已扩充类别页的模板。</span><span class="sxs-lookup"><span data-stu-id="448d4-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="448d4-121">如果仅进行微小更改，可选择默认类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="448d4-122">也可以选择特定类别页模板。</span><span class="sxs-lookup"><span data-stu-id="448d4-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="448d4-123">选择模板后，将打开页面编辑器，并使用所选模板为所选类别创建新的类别页。</span><span class="sxs-lookup"><span data-stu-id="448d4-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="448d4-124">将把此页签出给您，而您现在可进行更改。</span><span class="sxs-lookup"><span data-stu-id="448d4-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="448d4-125">使用类别规范数据的模块使用所选类别的数据。</span><span class="sxs-lookup"><span data-stu-id="448d4-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="448d4-126">您选择的模板的设置决定您可以进行的更改。</span><span class="sxs-lookup"><span data-stu-id="448d4-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="448d4-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="448d4-127">Additional resources</span></span>

[<span data-ttu-id="448d4-128">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="448d4-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="448d4-129">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="448d4-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="448d4-130">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="448d4-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="448d4-131">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="448d4-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="448d4-132">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="448d4-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="448d4-133">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="448d4-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="448d4-134">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="448d4-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="448d4-135">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="448d4-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
