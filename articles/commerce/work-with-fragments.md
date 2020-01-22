---
title: 使用片段
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914692"
---
# <a name="work-with-fragments"></a><span data-ttu-id="cc86c-103">使用片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cc86c-104">此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。</span><span class="sxs-lookup"><span data-stu-id="cc86c-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cc86c-105">概览</span><span class="sxs-lookup"><span data-stu-id="cc86c-105">Overview</span></span>

<span data-ttu-id="cc86c-106">片段为必须在整个站点中重复使用的模块配置提供集中式创作体验。</span><span class="sxs-lookup"><span data-stu-id="cc86c-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="cc86c-107">例如，页眉、页脚和横幅通常配置为片段，因为它们在许多页面之间共享。</span><span class="sxs-lookup"><span data-stu-id="cc86c-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="cc86c-108">可以将片段视为可插入站点中的其他页面的微型页面。</span><span class="sxs-lookup"><span data-stu-id="cc86c-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="cc86c-109">片段有自己的生命周期。</span><span class="sxs-lookup"><span data-stu-id="cc86c-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="cc86c-110">换句话说，它们在创作工具中作为独立实体创建、引用和删除。</span><span class="sxs-lookup"><span data-stu-id="cc86c-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="cc86c-111">配置后的片段可以在您的站点结构中任何可使用模块的位置使用。</span><span class="sxs-lookup"><span data-stu-id="cc86c-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="cc86c-112">可以在页面、布局、模板和其他片段中引用片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="cc86c-113">片段在其他片段内的嵌套深度最高可达十一级。</span><span class="sxs-lookup"><span data-stu-id="cc86c-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="cc86c-114">例如，如果要在站点中的多个页面开展季节促销活动，可以使用片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="cc86c-115">创建新片段的流程中，第一步是选择基础模块类型。</span><span class="sxs-lookup"><span data-stu-id="cc86c-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="cc86c-116">在本示例中，可以基于主图模块生成片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="cc86c-117">可以基于任何模块类型生成片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="cc86c-118">然后可以为主图片段配置特定促销内容。</span><span class="sxs-lookup"><span data-stu-id="cc86c-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="cc86c-119">也可以根据需要本地化。</span><span class="sxs-lookup"><span data-stu-id="cc86c-119">You can also localize it as you require.</span></span> <span data-ttu-id="cc86c-120">然后可以在整个站点中将新的独立主图片段用作预配置的模块。</span><span class="sxs-lookup"><span data-stu-id="cc86c-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="cc86c-121">可以将其轻松添加到模板、特定页面或包含主图模块的其他片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="cc86c-122">在其中添加了该片段的所有位置都是对您创建的中心主图片段的引用。</span><span class="sxs-lookup"><span data-stu-id="cc86c-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="cc86c-123">如果发布对该片段的更改，将立即在站点中引用该片段的所有位置体现这些更改。</span><span class="sxs-lookup"><span data-stu-id="cc86c-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="cc86c-124">因此，片段是在站点中重复使用和集中管理模块配置的强大、高效的方法。</span><span class="sxs-lookup"><span data-stu-id="cc86c-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="cc86c-125">通过有效利用它们，您可以大大提升灵活性，并帮助降低站点内容的管理成本。</span><span class="sxs-lookup"><span data-stu-id="cc86c-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="cc86c-126">下图显示如何使用片段在电子商务站点中集中创作共享模块配置。</span><span class="sxs-lookup"><span data-stu-id="cc86c-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![显示如何使用片段在电子商务站点中集中创作共享模块配置的插图](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="cc86c-128">创建片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-128">Create a fragment</span></span>

<span data-ttu-id="cc86c-129">可以创建新片段，也可以将现有模块配置另存为片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="cc86c-130">创建新片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-130">Create a new fragment</span></span>

<span data-ttu-id="cc86c-131">若要创建新片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc86c-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="cc86c-132">在左侧的导航窗格中，选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="cc86c-133">选择**新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="cc86c-134">将显示一个对话框，其中显示所有可用模块类型。</span><span class="sxs-lookup"><span data-stu-id="cc86c-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="cc86c-135">前文中介绍过，可以基于任何模块类型创建片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="cc86c-136">为片段选择模块类型，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="cc86c-137">如果必须在以后更新和配置片段，选择通用容器模块类型的灵活性最大。</span><span class="sxs-lookup"><span data-stu-id="cc86c-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="cc86c-138">将现有模块配置另存为片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="cc86c-139">若要将以前配置的模块转换为可重复使用的片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc86c-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="cc86c-140">打开其中包含要将片段转换为的模块的页面或模板。</span><span class="sxs-lookup"><span data-stu-id="cc86c-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="cc86c-141">在左侧大纲窗格中，选择模块名称旁边的省略号按钮 (**...**)，然后选择**另存为片段**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="cc86c-142">对话框出现</span><span class="sxs-lookup"><span data-stu-id="cc86c-142">A dialog box appears.</span></span>
1. <span data-ttu-id="cc86c-143">为片段输入名称和元数据。</span><span class="sxs-lookup"><span data-stu-id="cc86c-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="cc86c-144">选择**确定**将模块配置保存为可添加到其他页面的片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="cc86c-145">在页面中添加，删除或编辑片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="cc86c-146">以下过程介绍如何添加，删除和编辑片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="cc86c-147">添加片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-147">Add a fragment</span></span>

<span data-ttu-id="cc86c-148">若要向页面添加片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc86c-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="cc86c-149">在左侧的大纲窗格中，选择可向其添加子模块的容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="cc86c-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="cc86c-150">选择容器或插槽名称旁边的省略号按钮，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="cc86c-151">对话框出现</span><span class="sxs-lookup"><span data-stu-id="cc86c-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cc86c-152">如果容器或插槽不支持新子模块，则**添加片段**选项不可用。</span><span class="sxs-lookup"><span data-stu-id="cc86c-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="cc86c-153">在对话框中，搜索并选择要添加的片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="cc86c-154">如果未列出可用片段，可能必须先基于所选容器或插槽支持的模块类型创建片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="cc86c-155">选择**确定**将所选片段添加到页面中的所选容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="cc86c-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="cc86c-156">容器或插槽中允许的模块由页面的模板或模块自己的定义定义。</span><span class="sxs-lookup"><span data-stu-id="cc86c-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="cc86c-157">删除片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-157">Remove a fragment</span></span>

<span data-ttu-id="cc86c-158">若要从站点中的插槽或容器删除片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc86c-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="cc86c-159">在左侧大纲窗格中，选择要删除的片段的名称旁边的省略号按钮，然后选择废纸篓按钮。</span><span class="sxs-lookup"><span data-stu-id="cc86c-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="cc86c-160">系统提示确认要删除片段时，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc86c-161">从页面中删除片段时，仅从页面中删除对该片段的引用。</span><span class="sxs-lookup"><span data-stu-id="cc86c-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="cc86c-162">切**勿**从站点中删除片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="cc86c-163">若要从站点中删除片段，必须使用片段检查器用户界面 (UI)。</span><span class="sxs-lookup"><span data-stu-id="cc86c-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="cc86c-164">只能删除当前没有任何页面、模板或其他片段正在引用的片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="cc86c-165">编辑片段</span><span class="sxs-lookup"><span data-stu-id="cc86c-165">Edit a fragment</span></span>

<span data-ttu-id="cc86c-166">若要编辑片段，必须使用片段编辑器 UI。</span><span class="sxs-lookup"><span data-stu-id="cc86c-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="cc86c-167">这是设计制订的限制。</span><span class="sxs-lookup"><span data-stu-id="cc86c-167">This restriction is by design.</span></span> <span data-ttu-id="cc86c-168">这样有助于确保作者不会混淆特定页面的模块编辑流程和可能在多个页面之间共享的片段的编辑流程。</span><span class="sxs-lookup"><span data-stu-id="cc86c-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="cc86c-169">若要编辑片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc86c-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="cc86c-170">在左侧的导航窗格中，选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="cc86c-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="cc86c-171">在**片段**下，选择要编辑的片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="cc86c-172">根据需要编辑片段的模块属性和结构。</span><span class="sxs-lookup"><span data-stu-id="cc86c-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="cc86c-173">此流程类似在页面编辑器视图中编辑模块的流程。</span><span class="sxs-lookup"><span data-stu-id="cc86c-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="cc86c-174">也可以通过在页面、模板或父片段中打开片段，然后在右侧属性窗格中选择**编辑片段**来编辑片段。</span><span class="sxs-lookup"><span data-stu-id="cc86c-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc86c-175">其他资源</span><span class="sxs-lookup"><span data-stu-id="cc86c-175">Additional resources</span></span>

[<span data-ttu-id="cc86c-176">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="cc86c-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="cc86c-177">使用模板</span><span class="sxs-lookup"><span data-stu-id="cc86c-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="cc86c-178">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="cc86c-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="cc86c-179">使用发布组</span><span class="sxs-lookup"><span data-stu-id="cc86c-179">Work with publish groups</span></span>](publish-groups.md)
