---
title: 丰富类别登陆页面
description: 此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269835"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="72d1e-103">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="72d1e-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72d1e-104">此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="72d1e-105">概览</span><span class="sxs-lookup"><span data-stu-id="72d1e-105">Overview</span></span>

<span data-ttu-id="72d1e-106">Commerce 提供显示类别数据时使用的默认类别登陆页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="72d1e-107">默认类别页中包含必需的元素，如优化器、已分类的产品放置、排序选项、选项汇总和分页控件。</span><span class="sxs-lookup"><span data-stu-id="72d1e-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="72d1e-108">但是，不应使用默认类别页，而是使用包含更多内容和更多特定元素的“扩充的”类别登陆页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="72d1e-109">典型的扩充包括向类别页添加类别特定的市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="72d1e-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="72d1e-110">此内容可能包括交叉销售用途的交叉类别产品放置、编辑列表、图像、视频和其他文本。</span><span class="sxs-lookup"><span data-stu-id="72d1e-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="72d1e-111">可以修改默认类别页或为特定类别定义其他类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![扩充的类别登陆页面](./media/CategoryLandingPages.png)

<span data-ttu-id="72d1e-113">在 Commerce 站点构建器中，**产品**页包含渠道中分配给站点的类别的列表。</span><span class="sxs-lookup"><span data-stu-id="72d1e-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="72d1e-114">如果为类别页选择**扩充**状态，则说明该类别页已扩充。</span><span class="sxs-lookup"><span data-stu-id="72d1e-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="72d1e-115">否则，对类别使用默认类别页和内容。</span><span class="sxs-lookup"><span data-stu-id="72d1e-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="72d1e-116">可通过选择类别名称预览类别的扩充类别页和未扩充类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="72d1e-117">若要扩充类别页，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="72d1e-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="72d1e-118">在**产品**页中，选择要扩充其类别页的类别的名称。</span><span class="sxs-lookup"><span data-stu-id="72d1e-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="72d1e-119">将在页面编辑器中打开所选类别的默认类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="72d1e-120">选择**扩充类别页**。</span><span class="sxs-lookup"><span data-stu-id="72d1e-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="72d1e-121">选择已扩充类别页的模板。</span><span class="sxs-lookup"><span data-stu-id="72d1e-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="72d1e-122">如果仅进行微小更改，可选择默认类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="72d1e-123">也可以选择特定类别页模板。</span><span class="sxs-lookup"><span data-stu-id="72d1e-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="72d1e-124">选择模板后，将打开页面编辑器，并使用所选模板为所选类别创建新的类别页。</span><span class="sxs-lookup"><span data-stu-id="72d1e-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="72d1e-125">将把此页签出给您，而您现在可进行更改。</span><span class="sxs-lookup"><span data-stu-id="72d1e-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="72d1e-126">使用类别规范数据的模块使用所选类别的数据。</span><span class="sxs-lookup"><span data-stu-id="72d1e-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="72d1e-127">您选择的模板的设置决定您可以进行的更改。</span><span class="sxs-lookup"><span data-stu-id="72d1e-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72d1e-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="72d1e-128">Additional resources</span></span>

[<span data-ttu-id="72d1e-129">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="72d1e-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="72d1e-130">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="72d1e-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="72d1e-131">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="72d1e-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="72d1e-132">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="72d1e-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="72d1e-133">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="72d1e-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="72d1e-134">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="72d1e-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="72d1e-135">验证页面内容可访问性</span><span class="sxs-lookup"><span data-stu-id="72d1e-135">Verify page content accessibility</span></span>](verify-accessibility.md)
