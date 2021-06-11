---
title: 搜索结果模块
description: 此主题介绍搜索结果模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 05/28/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 645022000d8746db3793a8a8611ab8f17c7bcc6e
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117125"
---
# <a name="search-results-module"></a><span data-ttu-id="44a0f-103">搜索结果模块</span><span class="sxs-lookup"><span data-stu-id="44a0f-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="44a0f-104">此主题介绍搜索结果模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="44a0f-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="44a0f-105">搜索结果模块返回产品搜索结果和产品的适用优化器列表。</span><span class="sxs-lookup"><span data-stu-id="44a0f-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="44a0f-106">Dynamics 365 Commerce 站点上的搜索结果模块可用于呈现以下场景的页面：</span><span class="sxs-lookup"><span data-stu-id="44a0f-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="44a0f-107">由用户搜索发起的搜索结果</span><span class="sxs-lookup"><span data-stu-id="44a0f-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="44a0f-108">显示一组特定产品的搜索结果，如“购买外观相似的商品”</span><span class="sxs-lookup"><span data-stu-id="44a0f-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="44a0f-109">属于某个类别的产品的列表</span><span class="sxs-lookup"><span data-stu-id="44a0f-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="44a0f-110">有关类别和搜索结果页面的详细信息，请参阅[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="44a0f-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="44a0f-111">下图显示了 Fabrikam 站点上某个类别的搜索结果页面的示例。</span><span class="sxs-lookup"><span data-stu-id="44a0f-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Fabrikam 站点上的搜索结果页面的示例](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="44a0f-113">搜索结果模块属性</span><span class="sxs-lookup"><span data-stu-id="44a0f-113">Search results module properties</span></span>

<span data-ttu-id="44a0f-114">下表列出了搜索结果模块的属性，以及它们的值和描述。</span><span class="sxs-lookup"><span data-stu-id="44a0f-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="44a0f-115">属性</span><span class="sxs-lookup"><span data-stu-id="44a0f-115">Property</span></span> | <span data-ttu-id="44a0f-116">值</span><span class="sxs-lookup"><span data-stu-id="44a0f-116">Values</span></span> | <span data-ttu-id="44a0f-117">说明</span><span class="sxs-lookup"><span data-stu-id="44a0f-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="44a0f-118">每页的项数</span><span class="sxs-lookup"><span data-stu-id="44a0f-118">Items per page</span></span> | <span data-ttu-id="44a0f-119">整数</span><span class="sxs-lookup"><span data-stu-id="44a0f-119">Integer</span></span> | <span data-ttu-id="44a0f-120">每页上应显示的项目数。</span><span class="sxs-lookup"><span data-stu-id="44a0f-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="44a0f-121">允许在 PDP 上后退</span><span class="sxs-lookup"><span data-stu-id="44a0f-121">Allow back on PDP</span></span> | <span data-ttu-id="44a0f-122">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="44a0f-122">**True** or **False**</span></span> | <span data-ttu-id="44a0f-123">如果将此属性设置为 **True**，当用户在搜索结果页面上选择产品时，打开的产品详细信息页 (PDP) 上的痕迹导航将显示“返回到结果”链接。</span><span class="sxs-lookup"><span data-stu-id="44a0f-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="44a0f-124">扩展精简项</span><span class="sxs-lookup"><span data-stu-id="44a0f-124">Expand Refiners</span></span> | <span data-ttu-id="44a0f-125">**所有**、**1**、**2**、**3** 或 **4**</span><span class="sxs-lookup"><span data-stu-id="44a0f-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="44a0f-126">加载页面时应该展开的排在前面的优化器的数量。</span><span class="sxs-lookup"><span data-stu-id="44a0f-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="44a0f-127">例如，如果此属性设置为 **3**，页面上的前三个优化器将展开。</span><span class="sxs-lookup"><span data-stu-id="44a0f-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="44a0f-128">隐藏类别层次结构显示</span><span class="sxs-lookup"><span data-stu-id="44a0f-128">Hide category hierarchy display</span></span> | <span data-ttu-id="44a0f-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="44a0f-129">**True** or **False**</span></span> | <span data-ttu-id="44a0f-130">如果将此属性设置为 **True**，页面上显示的类别层次结构将被隐藏。</span><span class="sxs-lookup"><span data-stu-id="44a0f-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="44a0f-131">如果您使用 [痕迹导航模块](add-breadcrumb.md)显示类别层次结构，此属性应设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="44a0f-132">在搜索结果中包括产品属性</span><span class="sxs-lookup"><span data-stu-id="44a0f-132">Include product attributes in search results</span></span> | <span data-ttu-id="44a0f-133">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="44a0f-133">**True** or **False**</span></span> | <span data-ttu-id="44a0f-134">如果将此属性设置为 **True**，将在搜索结果中返回产品的属性。</span><span class="sxs-lookup"><span data-stu-id="44a0f-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="44a0f-135">虽然这些属性可以在 Commerce 站点上显示，但需要扩展。</span><span class="sxs-lookup"><span data-stu-id="44a0f-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="44a0f-136">显示隶属关系价格</span><span class="sxs-lookup"><span data-stu-id="44a0f-136">Show affiliation prices</span></span> | <span data-ttu-id="44a0f-137">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="44a0f-137">**True** or **False**</span></span> | <span data-ttu-id="44a0f-138">如果将此属性设置为 **True**，登录用户浏览页面时，产品的从属价格将显示在搜索结果中。</span><span class="sxs-lookup"><span data-stu-id="44a0f-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |
| <span data-ttu-id="44a0f-139">更新优化器面板</span><span class="sxs-lookup"><span data-stu-id="44a0f-139">Update refiner panel</span></span> | <span data-ttu-id="44a0f-140">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="44a0f-140">**True** or **False**</span></span> | <span data-ttu-id="44a0f-141">如果此属性设置为 **True**，选择优化器时，将更新优化器面板。</span><span class="sxs-lookup"><span data-stu-id="44a0f-141">If this property is set to **True**, the refiner panel will be updated when refiners are selected.</span></span> <span data-ttu-id="44a0f-142">在此模式下，当优化器面板更新时，某些多选优化器的行为将类似于单选优化器。</span><span class="sxs-lookup"><span data-stu-id="44a0f-142">In this mode, some multiple-selection refiners will behave like single-selection refiners when the refiner panel is updated.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="44a0f-143">在 Commerce 版本 10.0.16 及更高版本中，**显示从属价格** 配置可用于在页面上显示从属价格。</span><span class="sxs-lookup"><span data-stu-id="44a0f-143">In the Commerce version 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>
>
> <span data-ttu-id="44a0f-144">在 Commerce 版本 10.0.20 和更高版本中，**更新优化器面板** 配置可以用于在优化器选择期间更新优化器面板。</span><span class="sxs-lookup"><span data-stu-id="44a0f-144">In the Commerce version 10.0.20 release and later, the **Update refiner panel** configuration can be used to update the refiner panel during refiner selection.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="44a0f-145">支持的模块</span><span class="sxs-lookup"><span data-stu-id="44a0f-145">Supported modules</span></span>

<span data-ttu-id="44a0f-146">搜索结果模块支持[快速查看模块](quick-view-module.md)，让用户可以查看产品信息并将产品从搜索结果页面添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="44a0f-146">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="44a0f-147">将搜索结果模块添加到类别页面</span><span class="sxs-lookup"><span data-stu-id="44a0f-147">Add a search results module to a category page</span></span>

<span data-ttu-id="44a0f-148">要将搜索结果模块添加到类别页面，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="44a0f-148">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="44a0f-149">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="44a0f-149">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="44a0f-150">在 **新建模板** 对话框中，输入名称 **搜索结果**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-150">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="44a0f-151">在 **正文** 插槽中，选择省略号 (...)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-151">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="44a0f-152">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-152">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="44a0f-153">在 **默认页** 模块的 **主** 插槽中，选择省略号 (...)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-153">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="44a0f-154">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-154">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="44a0f-155">在 **容器** 插槽中，选择省略号 (...)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-155">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="44a0f-156">在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-156">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="44a0f-157">在 **痕迹导航** 属性窗格中，为 **最小发生次数** 输入值 **1**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-157">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="44a0f-158">在 **容器** 插槽中，选择省略号 (...)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-158">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="44a0f-159">在 **添加模块** 对话框中，选择 **搜索结果** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-159">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="44a0f-160">在 **搜索结果** 属性窗格中，为 **最小发生次数** 输入值 **1**，然后为搜索结果模块设置任何其他必需的属性。</span><span class="sxs-lookup"><span data-stu-id="44a0f-160">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="44a0f-161">通过在模板中设置这些属性，可以确保对特定类别页面进行的任何自定义都会自动包括这些设置。</span><span class="sxs-lookup"><span data-stu-id="44a0f-161">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="44a0f-162">选择 **完成编辑**，然后选择 **发布** 以发布模板。</span><span class="sxs-lookup"><span data-stu-id="44a0f-162">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="44a0f-163">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="44a0f-163">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="44a0f-164">在 **选择模板** 对话框中，选择您创建的 **搜索结果** 模板，为 **页面名称** 输入 **类别页**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44a0f-164">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="44a0f-165">由于所有值都在模板中设置，因此页面已准备好发布。</span><span class="sxs-lookup"><span data-stu-id="44a0f-165">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="44a0f-166">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="44a0f-166">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44a0f-167">其他资源</span><span class="sxs-lookup"><span data-stu-id="44a0f-167">Additional resources</span></span>

[<span data-ttu-id="44a0f-168">默认类别登陆页面和搜索结果页面概览</span><span class="sxs-lookup"><span data-stu-id="44a0f-168">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="44a0f-169">模块库概览</span><span class="sxs-lookup"><span data-stu-id="44a0f-169">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="44a0f-170">快速查看模块</span><span class="sxs-lookup"><span data-stu-id="44a0f-170">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
