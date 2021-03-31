---
title: 痕迹导航模块
description: 本主题介绍痕迹导航模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 06f8ffdecd1f77468ed88043929f29b6957c2e6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206551"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="1b1e0-103">痕迹导航模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b1e0-104">本主题介绍痕迹导航模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1b1e0-105">痕迹导航模块用于在站点页面上提供辅助导航。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="1b1e0-106">它们通常显示在页面顶部的标题下方。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="1b1e0-107">痕迹导航模块可以添加到任何页面，但它们最常用于产品详细信息页 (PDP)，来显示产品类别层次结构并提供在站点上快速四处移动的方法。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="1b1e0-108">当用户从搜索或列表页打开 PDP 时，痕迹导航模块还可以用于显示“返回到结果”链接。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="1b1e0-109">这样，用户可以快速返回到筛选后的列表页以继续购物。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="1b1e0-110">在具有产品类别上下文的页面（如 PDP 和类别页面）上，痕迹导航模块显示类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="1b1e0-111">在没有类别上下文的页面上，痕迹导航模块默认显示 **&lt;站点根&gt; / &lt;当前页面&gt;**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="1b1e0-112">痕迹导航模块还可以在其他类型的站点页面上手动配置，以显示指向站点上特定页面的链接。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1e0-113">此痕迹导航模块在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="1b1e0-114">下图显示了痕迹导航模块的示例，该模块显示 PDP 上的类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![痕迹导航模块的示例](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="1b1e0-116">痕迹导航模块设置</span><span class="sxs-lookup"><span data-stu-id="1b1e0-116">Breadcrumb module settings</span></span>

<span data-ttu-id="1b1e0-117">痕迹导航模块依赖于 **PDP 上的痕迹导航显示类型** 设置，此设置在站点构建器中的 **站点设置 \> 扩展** 中定义。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="1b1e0-118">此设置有三个可能的值：</span><span class="sxs-lookup"><span data-stu-id="1b1e0-118">This setting has three possible values:</span></span>

- <span data-ttu-id="1b1e0-119">**显示类别层次结构** – 选择此值时，痕迹导航模块将显示在 PDP 上查看的产品的完整类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="1b1e0-120">**显示返回到结果**– 选择此值时，如果用户从允许“返回到结果”链接的模块打开的 PDP，痕迹导航模块将在 PDP 上显示“返回到结果”链接。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="1b1e0-121">当用户从类别、搜索、列表和建议列表页面导航时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="1b1e0-122">为了支持此功能，产品集合和搜索结果模块具有一个名为 **允许在 PDP 上返回到结果** 的属性。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="1b1e0-123">此属性使您可以灵活地定义哪些模块应该在 PDP 上支持“返回到结果”链接功能。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="1b1e0-124">例如，当为痕迹导航模块的 **PDP 上的痕迹导航显示类型** 设置选择了 **显示返回到结果**，并为搜索页面搜索结果模块选择了 **允许在 PDP 上返回到结果** 时，当用户从搜索页面导航到 PDP 时，将显示“返回到结果”链接。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="1b1e0-125">**显示类别层次结构和返回到结果**– 此值是前两个值的组合。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="1b1e0-126">选择此值时，痕迹导航模块将在 PDP 上显示完整类别层次结构和“返回到结果”链接（如果已配置）。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b1e0-127">这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="1b1e0-128">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1b1e0-129">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="1b1e0-130">痕迹导航模块属性</span><span class="sxs-lookup"><span data-stu-id="1b1e0-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="1b1e0-131">属性名称</span><span class="sxs-lookup"><span data-stu-id="1b1e0-131">Property name</span></span> | <span data-ttu-id="1b1e0-132">值</span><span class="sxs-lookup"><span data-stu-id="1b1e0-132">Values</span></span> | <span data-ttu-id="1b1e0-133">说明</span><span class="sxs-lookup"><span data-stu-id="1b1e0-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="1b1e0-134">根</span><span class="sxs-lookup"><span data-stu-id="1b1e0-134">Root</span></span> | <span data-ttu-id="1b1e0-135">文本或链接</span><span class="sxs-lookup"><span data-stu-id="1b1e0-135">Text or link</span></span>| <span data-ttu-id="1b1e0-136">此可选属性为痕迹导航站点根指定链接文本和链接目标。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="1b1e0-137">如果未配置此属性，将不会定义根。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="1b1e0-138">痕迹导航链接</span><span class="sxs-lookup"><span data-stu-id="1b1e0-138">Breadcrumb link</span></span> | <span data-ttu-id="1b1e0-139">链接</span><span class="sxs-lookup"><span data-stu-id="1b1e0-139">Link</span></span> | <span data-ttu-id="1b1e0-140">此可选属性在需要链接时为手动配置的痕迹导航指定链接。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="1b1e0-141">链接按列出的顺序显示。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="1b1e0-142">向新页面添加痕迹导航模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="1b1e0-143">若要向 PDP 添加痕迹导航模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1b1e0-144">转到 **站点设置 \> 扩展**，然后针对 **PDP 上的痕迹导航显示类型** 设置，选择 **显示类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="1b1e0-145">转到 **模板**，选择 PDP 模板。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="1b1e0-146">在包含购买框模块的 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b1e0-147">在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b1e0-148">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1b1e0-149">转到 **页面**，打开使用 PDP 模板的 PDP。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="1b1e0-150">如果 PDP 尚不存在，请创建一个。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="1b1e0-151">在包含购买框模块的 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b1e0-152">在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b1e0-153">在 **痕迹导航** 插槽的属性窗格中，在 **根** 下，选择 **链接文本**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="1b1e0-154">在 **链接文本** 对话框中，输入 **主页**，然后在 **链接目标** 下，选择 **添加链接**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="1b1e0-155">在 **添加链接** 对话框中，选择痕迹导航根的链接，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="1b1e0-156">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="1b1e0-157">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1b1e0-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b1e0-158">其他资源</span><span class="sxs-lookup"><span data-stu-id="1b1e0-158">Additional resources</span></span>

[<span data-ttu-id="1b1e0-159">模块库概览</span><span class="sxs-lookup"><span data-stu-id="1b1e0-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1b1e0-160">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="1b1e0-161">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="1b1e0-162">默认类别登陆页面和搜索结果页面概览</span><span class="sxs-lookup"><span data-stu-id="1b1e0-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="1b1e0-163">产品集合模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="1b1e0-164">购买框模块</span><span class="sxs-lookup"><span data-stu-id="1b1e0-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1b1e0-165">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="1b1e0-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]