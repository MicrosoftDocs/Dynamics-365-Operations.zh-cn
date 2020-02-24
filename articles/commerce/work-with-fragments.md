---
title: 使用片段
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026032"
---
# <a name="work-with-fragments"></a><span data-ttu-id="04392-103">使用片段</span><span class="sxs-lookup"><span data-stu-id="04392-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="04392-104">此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。</span><span class="sxs-lookup"><span data-stu-id="04392-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="04392-105">概览</span><span class="sxs-lookup"><span data-stu-id="04392-105">Overview</span></span>

<span data-ttu-id="04392-106">片段为必须在整个站点中重复使用的模块配置提供集中式创作体验。</span><span class="sxs-lookup"><span data-stu-id="04392-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="04392-107">例如，页眉、页脚和横幅通常配置为片段，因为它们在许多页面之间共享。</span><span class="sxs-lookup"><span data-stu-id="04392-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="04392-108">可以将片段视为可插入站点中的其他页面的微型页面。</span><span class="sxs-lookup"><span data-stu-id="04392-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="04392-109">片段有自己的生命周期。</span><span class="sxs-lookup"><span data-stu-id="04392-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="04392-110">换句话说，它们在创作工具中作为独立实体创建、引用和删除。</span><span class="sxs-lookup"><span data-stu-id="04392-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="04392-111">配置后的片段可以在您的站点结构中任何可使用模块的位置使用。</span><span class="sxs-lookup"><span data-stu-id="04392-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="04392-112">可以在页面、布局、模板和其他片段中引用片段。</span><span class="sxs-lookup"><span data-stu-id="04392-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="04392-113">片段在其他片段内的嵌套深度最高可达十一级。</span><span class="sxs-lookup"><span data-stu-id="04392-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="04392-114">例如，如果要在站点中的多个页面开展季节促销活动，可以使用片段。</span><span class="sxs-lookup"><span data-stu-id="04392-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="04392-115">创建新片段的流程中，第一步是选择基础模块类型。</span><span class="sxs-lookup"><span data-stu-id="04392-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="04392-116">在本示例中，可以基于主图模块生成片段。</span><span class="sxs-lookup"><span data-stu-id="04392-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="04392-117">可以基于任何模块类型生成片段。</span><span class="sxs-lookup"><span data-stu-id="04392-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="04392-118">然后可以为主图片段配置特定促销内容。</span><span class="sxs-lookup"><span data-stu-id="04392-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="04392-119">也可以根据需要本地化。</span><span class="sxs-lookup"><span data-stu-id="04392-119">You can also localize it as you require.</span></span> <span data-ttu-id="04392-120">然后可以在整个站点中将新的独立主图片段用作预配置的模块。</span><span class="sxs-lookup"><span data-stu-id="04392-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="04392-121">可以将其轻松添加到模板、特定页面或包含主图模块的其他片段。</span><span class="sxs-lookup"><span data-stu-id="04392-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="04392-122">在其中添加了该片段的所有位置都是对您创建的中心主图片段的引用。</span><span class="sxs-lookup"><span data-stu-id="04392-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="04392-123">如果发布对该片段的更改，将立即在站点中引用该片段的所有位置体现这些更改。</span><span class="sxs-lookup"><span data-stu-id="04392-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="04392-124">因此，片段是在站点中重复使用和集中管理模块配置的强大、高效的方法。</span><span class="sxs-lookup"><span data-stu-id="04392-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="04392-125">通过有效利用它们，您可以大大提升灵活性，并帮助降低站点内容的管理成本。</span><span class="sxs-lookup"><span data-stu-id="04392-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="04392-126">下图显示如何使用片段在电子商务站点中集中创作共享模块配置。</span><span class="sxs-lookup"><span data-stu-id="04392-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![显示如何使用片段在电子商务站点中集中创作共享模块配置的插图](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="04392-128">创建片段</span><span class="sxs-lookup"><span data-stu-id="04392-128">Create a fragment</span></span>

<span data-ttu-id="04392-129">可以创建新片段，也可以将现有模块配置另存为片段。</span><span class="sxs-lookup"><span data-stu-id="04392-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="04392-130">将现有模块配置另存为片段</span><span class="sxs-lookup"><span data-stu-id="04392-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="04392-131">若要将以前配置的模块转换为可重复使用的片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04392-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="04392-132">打开其中包含要将片段转换为的模块的页面或模板。</span><span class="sxs-lookup"><span data-stu-id="04392-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="04392-133">在左侧的大纲窗格中，选择模块名称旁边的省略号按钮 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="04392-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="04392-134">选择**共享为片段**。</span><span class="sxs-lookup"><span data-stu-id="04392-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="04392-135">对话框出现</span><span class="sxs-lookup"><span data-stu-id="04392-135">A dialog box appears.</span></span> <span data-ttu-id="04392-136">为片段输入名称和元数据。</span><span class="sxs-lookup"><span data-stu-id="04392-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="04392-137">选择**确定**将模块配置保存为可添加到其他页面的片段。</span><span class="sxs-lookup"><span data-stu-id="04392-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="04392-138">下图显示了如何将模块配置另存为片段。</span><span class="sxs-lookup"><span data-stu-id="04392-138">The following image shows how to save a module configuration as a fragment.</span></span>

![有关如何将模块配置另存为片段的屏幕截图](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="04392-140">创建新片段</span><span class="sxs-lookup"><span data-stu-id="04392-140">Create a new fragment</span></span>

<span data-ttu-id="04392-141">若要创建新片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04392-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="04392-142">在左侧的导航窗格中，选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="04392-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="04392-143">选择**新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="04392-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="04392-144">将显示一个对话框，其中显示所有可用模块类型。</span><span class="sxs-lookup"><span data-stu-id="04392-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="04392-145">前文中介绍过，可以基于任何模块类型创建片段。</span><span class="sxs-lookup"><span data-stu-id="04392-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="04392-146">选择片段的模块类型。</span><span class="sxs-lookup"><span data-stu-id="04392-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="04392-147">下图显示了在哪里创建新片段。</span><span class="sxs-lookup"><span data-stu-id="04392-147">The following image shows where to create a new fragment.</span></span>

![关于在哪里创建新片段的屏幕截图](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="04392-149">如果需要在以后更新和配置片段，则选择通用容器模块类型的灵活性最大。</span><span class="sxs-lookup"><span data-stu-id="04392-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="04392-150">在页面中添加，删除或编辑片段</span><span class="sxs-lookup"><span data-stu-id="04392-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="04392-151">以下过程介绍如何添加，删除和编辑片段。</span><span class="sxs-lookup"><span data-stu-id="04392-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="04392-152">添加片段</span><span class="sxs-lookup"><span data-stu-id="04392-152">Add a fragment</span></span>

<span data-ttu-id="04392-153">若要向页面添加片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04392-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="04392-154">在左侧的大纲窗格中，选择可向其添加子模块的容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="04392-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="04392-155">选择容器或插槽名称旁边的省略号按钮，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="04392-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="04392-156">对话框出现</span><span class="sxs-lookup"><span data-stu-id="04392-156">A dialog box appears.</span></span>

    ![有关如何将现有片段添加到插槽或容器的屏幕截图](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="04392-158">如果容器或插槽不支持新子模块，则**添加片段**选项不可用。</span><span class="sxs-lookup"><span data-stu-id="04392-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="04392-159">在对话框中，搜索并选择要添加的片段。</span><span class="sxs-lookup"><span data-stu-id="04392-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="04392-160">如果未列出可用片段，可能必须先基于所选容器或插槽支持的模块类型创建片段。</span><span class="sxs-lookup"><span data-stu-id="04392-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="04392-161">选择所需的片段以将其添加到页面上的容器或插槽中。</span><span class="sxs-lookup"><span data-stu-id="04392-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![关于片段选择器模式窗口的屏幕截图](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="04392-163">容器或插槽中允许的模块由页面的模板或模块自己的定义定义。</span><span class="sxs-lookup"><span data-stu-id="04392-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="04392-164">删除片段</span><span class="sxs-lookup"><span data-stu-id="04392-164">Remove a fragment</span></span>

<span data-ttu-id="04392-165">若要从站点中的插槽或容器删除片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04392-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="04392-166">在左侧大纲窗格中，选择要删除的片段的名称旁边的省略号按钮，然后选择废纸篓按钮。</span><span class="sxs-lookup"><span data-stu-id="04392-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="04392-167">系统提示确认要删除片段时，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="04392-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="04392-168">从页面中删除片段时，仅从页面中删除对该片段的引用。</span><span class="sxs-lookup"><span data-stu-id="04392-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="04392-169">切**勿**从站点中删除片段。</span><span class="sxs-lookup"><span data-stu-id="04392-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="04392-170">若要从站点中删除片段，必须使用片段检查器用户界面 (UI)。</span><span class="sxs-lookup"><span data-stu-id="04392-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="04392-171">只能删除当前没有任何页面、模板或其他片段正在引用的片段。</span><span class="sxs-lookup"><span data-stu-id="04392-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="04392-172">编辑片段</span><span class="sxs-lookup"><span data-stu-id="04392-172">Edit a fragment</span></span>

<span data-ttu-id="04392-173">若要编辑片段，必须使用片段编辑器 UI。</span><span class="sxs-lookup"><span data-stu-id="04392-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="04392-174">这是设计制订的限制。</span><span class="sxs-lookup"><span data-stu-id="04392-174">This restriction is by design.</span></span> <span data-ttu-id="04392-175">这样有助于确保作者不会混淆特定页面的模块编辑流程和可能在多个页面之间共享的片段的编辑流程。</span><span class="sxs-lookup"><span data-stu-id="04392-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="04392-176">若要编辑片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04392-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="04392-177">在左侧的导航窗格中，选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="04392-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="04392-178">在**片段**下，选择要编辑的片段。</span><span class="sxs-lookup"><span data-stu-id="04392-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="04392-179">根据需要编辑片段的模块属性和结构。</span><span class="sxs-lookup"><span data-stu-id="04392-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="04392-180">此流程类似在页面编辑器视图中编辑模块的流程。</span><span class="sxs-lookup"><span data-stu-id="04392-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="04392-181">也可以通过在页面、模板或父片段中打开片段，然后在右侧属性窗格中选择**编辑片段**来编辑片段。</span><span class="sxs-lookup"><span data-stu-id="04392-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04392-182">其他资源</span><span class="sxs-lookup"><span data-stu-id="04392-182">Additional resources</span></span>

[<span data-ttu-id="04392-183">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="04392-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="04392-184">使用模板</span><span class="sxs-lookup"><span data-stu-id="04392-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="04392-185">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="04392-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="04392-186">使用发布组</span><span class="sxs-lookup"><span data-stu-id="04392-186">Work with publish groups</span></span>](publish-groups.md)
