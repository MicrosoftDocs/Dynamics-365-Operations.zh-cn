---
title: 修改现有的站点页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中修改现有站点页面。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410566"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="f8667-103">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="f8667-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8667-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中修改现有站点页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8667-105">概览</span><span class="sxs-lookup"><span data-stu-id="f8667-105">Overview</span></span>

<span data-ttu-id="f8667-106">必须修改页面时，第一步是在页面编辑器中打开该页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="f8667-107">转到其中包含您的页面的站点，然后在页面列表中找到所需页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="f8667-108">如果找不到此页面，可使用创作工具丰富的搜索功能。</span><span class="sxs-lookup"><span data-stu-id="f8667-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="f8667-109">键入精确的页名，或键入页面的前几个字母和星号 (\*)。</span><span class="sxs-lookup"><span data-stu-id="f8667-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="f8667-110">将显示筛选后的页面列表。</span><span class="sxs-lookup"><span data-stu-id="f8667-110">A filtered list of pages appears.</span></span> <span data-ttu-id="f8667-111">可使用此列表查找所需页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="f8667-112">找到正确的页面之后，选择页名在页面编辑器中打开页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="f8667-113">如果页面检查器中显示您的页面，可选择 **编辑**，然后将该页面签出，才能在页面编辑器中打开。</span><span class="sxs-lookup"><span data-stu-id="f8667-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="f8667-114">这样就可以同时签出多个页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="f8667-115">在页面编辑器中打开页面之后，必须确保将其签出给您。</span><span class="sxs-lookup"><span data-stu-id="f8667-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="f8667-116">创作工具中的命令栏动态，上下文相关且状态相关。</span><span class="sxs-lookup"><span data-stu-id="f8667-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="f8667-117">因此，仅显示当前可在页面中执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f8667-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="f8667-118">例如，如果不将页面签出给您，则命令栏中不显示 **保存** 和 **完成编辑** 按钮。</span><span class="sxs-lookup"><span data-stu-id="f8667-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="f8667-119">窗口右侧还显示页面状态。</span><span class="sxs-lookup"><span data-stu-id="f8667-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="f8667-120">如果页面尚未签出给您，请在命令栏中选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="f8667-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="f8667-121">命令栏将变化以体现新的页面状态。</span><span class="sxs-lookup"><span data-stu-id="f8667-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="f8667-122">您还会收到通知，说明已将页面签出给您。</span><span class="sxs-lookup"><span data-stu-id="f8667-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="f8667-123">下一步是进行真正的更改。</span><span class="sxs-lookup"><span data-stu-id="f8667-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="f8667-124">通常使用左侧的页面大纲树查找和选择要更改的模块，然后在右侧属性窗格中进行更改。</span><span class="sxs-lookup"><span data-stu-id="f8667-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="f8667-125">但是，您的更改有时涉及添加或删除模块或片段。</span><span class="sxs-lookup"><span data-stu-id="f8667-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="f8667-126">若要添加片段或模块，请使用页面大纲树查找要向其添加模块或片段的插槽，然后选择该插槽的省略号按钮 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="f8667-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="f8667-127">将显示一个菜单，其中包含用于添加模块或片段的命令。</span><span class="sxs-lookup"><span data-stu-id="f8667-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="f8667-128">若要删除模块或片段，请在页面大纲树中找到并选择，选择省略号按钮，然后选择用于删除模块或片段的命令。</span><span class="sxs-lookup"><span data-stu-id="f8667-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="f8667-129">也可以通过直接选择，查看和编辑可视页面构建器预览中显示的任何模块的属性。</span><span class="sxs-lookup"><span data-stu-id="f8667-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="f8667-130">进行更改并预览其效果之后，应该通过选择命令栏中的 **完成编辑** 签入页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="f8667-131">若要立即发布更改，请选择命令栏中的 **发布**。</span><span class="sxs-lookup"><span data-stu-id="f8667-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="f8667-132">您修改的页面的最新签入版本将发布并可供查看您的站点的外部用户使用。</span><span class="sxs-lookup"><span data-stu-id="f8667-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="f8667-133">示例：更改主页中的视频</span><span class="sxs-lookup"><span data-stu-id="f8667-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="f8667-134">以下示例显示如何通过更改视频播放器模块中显示的视频，修改主页。</span><span class="sxs-lookup"><span data-stu-id="f8667-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="f8667-135">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="f8667-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f8667-136">在左侧的导航窗格中，选择 **页面**。</span><span class="sxs-lookup"><span data-stu-id="f8667-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="f8667-137">转到并选择主页在页面编辑器中将其打开。</span><span class="sxs-lookup"><span data-stu-id="f8667-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="f8667-138">在命令栏中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="f8667-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="f8667-139">在页面大纲中，选择 **主** 插槽。</span><span class="sxs-lookup"><span data-stu-id="f8667-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="f8667-140">在 **主** 插槽下，展开所有流体容器模块。</span><span class="sxs-lookup"><span data-stu-id="f8667-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="f8667-141">找到并选择视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="f8667-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="f8667-142">在右侧属性窗格中，选择 **视频** 属性。</span><span class="sxs-lookup"><span data-stu-id="f8667-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="f8667-143">将显示资产选取器。</span><span class="sxs-lookup"><span data-stu-id="f8667-143">The asset picker appears.</span></span>
1. <span data-ttu-id="f8667-144">在资产选取器中，选择一个可用视频资产，或选择 **上传新资产** 上传一个新视频资产。</span><span class="sxs-lookup"><span data-stu-id="f8667-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="f8667-145">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f8667-145">Select **OK**.</span></span>
1. <span data-ttu-id="f8667-146">选择 **保存**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="f8667-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="f8667-147">在 **注释** 字段中，输入 **已更改视频**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f8667-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="f8667-148">选择 **预览** 预览更新后的页面。</span><span class="sxs-lookup"><span data-stu-id="f8667-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="f8667-149">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="f8667-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="f8667-150">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="f8667-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8667-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="f8667-151">Additional resources</span></span>

[<span data-ttu-id="f8667-152">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="f8667-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f8667-153">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="f8667-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f8667-154">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="f8667-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="f8667-155">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="f8667-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="f8667-156">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="f8667-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="f8667-157">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="f8667-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f8667-158">验证页面内容可访问性</span><span class="sxs-lookup"><span data-stu-id="f8667-158">Verify page content accessibility</span></span>](verify-accessibility.md)
