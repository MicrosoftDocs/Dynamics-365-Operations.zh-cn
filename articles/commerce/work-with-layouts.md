---
title: 使用预设布局
description: 此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用预设布局。
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410504"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="2ac64-103">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2ac64-104">此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用预设布局。</span><span class="sxs-lookup"><span data-stu-id="2ac64-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ac64-105">概览</span><span class="sxs-lookup"><span data-stu-id="2ac64-105">Overview</span></span>

<span data-ttu-id="2ac64-106">完成此主题中的过程之前，务必阅读[预设布局和自定义布局](templates-layouts-overview.md#preset-and-custom-layouts)。</span><span class="sxs-lookup"><span data-stu-id="2ac64-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="2ac64-107">有关一般概述，请参阅[模板和布局概述](templates-layouts-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="2ac64-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="2ac64-108">创建新预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-108">Create a new preset layout</span></span>

<span data-ttu-id="2ac64-109">创建预设布局有两种方法。</span><span class="sxs-lookup"><span data-stu-id="2ac64-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="2ac64-110">可以将现有自定义布局另存为预设布局，也可以从头创建预设布局。</span><span class="sxs-lookup"><span data-stu-id="2ac64-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="2ac64-111">基于现有自定义布局创建预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="2ac64-112">若要基于现有自定义布局创建预设布局，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2ac64-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="2ac64-113">打开现在不使用预设布局，并且具有您要用于站点中其他页面的模块结构的现有页面。</span><span class="sxs-lookup"><span data-stu-id="2ac64-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="2ac64-114">选择 **编辑** 签出页面。</span><span class="sxs-lookup"><span data-stu-id="2ac64-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="2ac64-115">选择 **另存为新布局**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-115">Select **Save as new layout**.</span></span> <span data-ttu-id="2ac64-116">将显示 **另存为新布局** 对话框。</span><span class="sxs-lookup"><span data-stu-id="2ac64-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="2ac64-117">为预设布局输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="2ac64-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="2ac64-118">其他作者基于您的布局创建新页面或切换到您的布局时，将对这些作者显示您输入的值。</span><span class="sxs-lookup"><span data-stu-id="2ac64-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="2ac64-119">因此，输入对页面作者有用的值。</span><span class="sxs-lookup"><span data-stu-id="2ac64-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="2ac64-120">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-120">Select **OK**.</span></span>

<span data-ttu-id="2ac64-121">在您创建新页面或在同一个模板层次结构中为页面选择其他布局时，现在可使用预设布局。</span><span class="sxs-lookup"><span data-stu-id="2ac64-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="2ac64-122">若要快速查看特定页面当前是否已绑定到预设布局，请在页面列表视图中选择页面，然后检查右侧的属性窗格中的布局元数据。</span><span class="sxs-lookup"><span data-stu-id="2ac64-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="2ac64-123">创建新预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-123">Create a new preset layout</span></span>

<span data-ttu-id="2ac64-124">若要从头创建预设布局，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2ac64-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="2ac64-125">在左侧的导航窗格中，选择 **布局**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="2ac64-126">选择 **新建布局**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-126">Select **New Layout**.</span></span> <span data-ttu-id="2ac64-127">将显示 **新布局** 对话框。</span><span class="sxs-lookup"><span data-stu-id="2ac64-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="2ac64-128">选择要用于预设布局的模板。</span><span class="sxs-lookup"><span data-stu-id="2ac64-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="2ac64-129">为预设布局输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="2ac64-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="2ac64-130">其他作者基于您的布局创建新页面或切换到您的布局时，将对这些作者显示您输入的值。</span><span class="sxs-lookup"><span data-stu-id="2ac64-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="2ac64-131">因此，输入对页面作者有用的值。</span><span class="sxs-lookup"><span data-stu-id="2ac64-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="2ac64-132">选择 **确定** 创建新预设布局，然后打开布局编辑器。</span><span class="sxs-lookup"><span data-stu-id="2ac64-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="2ac64-133">在布局编辑器中，使用左侧大纲树和右侧属性窗格添加和配置模块。</span><span class="sxs-lookup"><span data-stu-id="2ac64-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="2ac64-134">（此流程类似在模板编辑器中为模板添加和配置模块的流程。）模块的排列和任何已锁定默认设置将成为使用此预设布局的任何页面的中央模块配置。</span><span class="sxs-lookup"><span data-stu-id="2ac64-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="2ac64-135">修改预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-135">Modify a preset layout</span></span>

<span data-ttu-id="2ac64-136">若要修改预设布局，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2ac64-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="2ac64-137">在左侧的导航窗格中，选择 **布局**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="2ac64-138">在布局编辑器中左侧大纲树内，选择要修改的模块。</span><span class="sxs-lookup"><span data-stu-id="2ac64-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="2ac64-139">然后执行以下任何步骤：</span><span class="sxs-lookup"><span data-stu-id="2ac64-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="2ac64-140">若要在模块的父级中上下移动模块，请选择模块的省略号按钮 (**...**)，然后选择 **上移** 或 **下移**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="2ac64-141">若要更改模块的默认设置，请使用属性窗格输入默认值，或者选择对所有下游页面选择锁定它们。</span><span class="sxs-lookup"><span data-stu-id="2ac64-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="2ac64-142">若要向容器模块添加模块或片段，请选择省略号按钮，然后选择 **添加模块** 或 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="2ac64-143">若要从布局中删除模块，请选择省略号按钮，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="2ac64-144">更改预设布局主题</span><span class="sxs-lookup"><span data-stu-id="2ac64-144">Change a preset layout theme</span></span>

<span data-ttu-id="2ac64-145">典型实践是为使用预设布局的所有页面设置默认主题。</span><span class="sxs-lookup"><span data-stu-id="2ac64-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="2ac64-146">若要设置或更改使用预设布局的所有子页面的主题，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2ac64-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="2ac64-147">在布局编辑器中左侧大纲树内，选择页面容器模块。</span><span class="sxs-lookup"><span data-stu-id="2ac64-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="2ac64-148">（此模块通常是第二个节点，名称为 **默认页**。）</span><span class="sxs-lookup"><span data-stu-id="2ac64-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="2ac64-149">在右侧的属性窗格中 **主题** 字段内，选择一个主题。</span><span class="sxs-lookup"><span data-stu-id="2ac64-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="2ac64-150">保存，签入，预览和发布预设布局</span><span class="sxs-lookup"><span data-stu-id="2ac64-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="2ac64-151">若要保存和签入预设布局，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2ac64-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="2ac64-152">选择布局编辑器顶部的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="2ac64-153">保存的更改在签入前，不影响下游页。</span><span class="sxs-lookup"><span data-stu-id="2ac64-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="2ac64-154">选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-154">Select **Finish editing**.</span></span> <span data-ttu-id="2ac64-155">现在可为下游工作流发现更改。</span><span class="sxs-lookup"><span data-stu-id="2ac64-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="2ac64-156">若要预览更改，请打开使用预设布局的现有页面，或基于布局创建新页面。</span><span class="sxs-lookup"><span data-stu-id="2ac64-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="2ac64-157">预览对预设布局的更改之后，执行以下步骤之一将布局发布到您的活动站点：</span><span class="sxs-lookup"><span data-stu-id="2ac64-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="2ac64-158">转到 **布局**，选择布局，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="2ac64-159">选择布局名称打开布局编辑器，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="2ac64-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="2ac64-160">发布引用未发布布局的页面。</span><span class="sxs-lookup"><span data-stu-id="2ac64-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="2ac64-161">将自动发布布局。</span><span class="sxs-lookup"><span data-stu-id="2ac64-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="2ac64-162">预设布局可以被多个页面引用。</span><span class="sxs-lookup"><span data-stu-id="2ac64-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="2ac64-163">发布预设布局时，请注意，您可能影响多个页面的布局。</span><span class="sxs-lookup"><span data-stu-id="2ac64-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ac64-164">其他资源</span><span class="sxs-lookup"><span data-stu-id="2ac64-164">Additional resources</span></span>

[<span data-ttu-id="2ac64-165">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="2ac64-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2ac64-166">使用模板</span><span class="sxs-lookup"><span data-stu-id="2ac64-166">Work with templates</span></span>](work-with-templates.md)
