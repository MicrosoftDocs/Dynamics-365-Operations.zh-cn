---
title: 使用模板
description: 此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用模板。
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
ms.openlocfilehash: a3fc4259a76f6edcfaa0b8f6e08292477c6c0835
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269858"
---
# <a name="work-with-templates"></a><span data-ttu-id="cb87b-103">使用模板</span><span class="sxs-lookup"><span data-stu-id="cb87b-103">Work with templates</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb87b-104">此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用模板。</span><span class="sxs-lookup"><span data-stu-id="cb87b-104">This topic describes how to work with templates in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb87b-105">概览</span><span class="sxs-lookup"><span data-stu-id="cb87b-105">Overview</span></span>

<span data-ttu-id="cb87b-106">[模板和布局概述](templates-layouts-overview.md)中已介绍过，模板定义可供下游作者使用的一组选项。</span><span class="sxs-lookup"><span data-stu-id="cb87b-106">As was discussed in [Templates and layouts overview](templates-layouts-overview.md), templates define the set of options that is available to downstream authors.</span></span> <span data-ttu-id="cb87b-107">多个原因让模块对企业的 Web 制作团队非常有用，而精心构造的模板可以帮助达成下面的所有目标：</span><span class="sxs-lookup"><span data-stu-id="cb87b-107">Templates are useful to an enterprise's web authoring team for several reasons, and well-structured templates can help with all the following goals:</span></span>

- <span data-ttu-id="cb87b-108">简化日常内容编辑者角色的创作体验</span><span class="sxs-lookup"><span data-stu-id="cb87b-108">Simplify the authoring experience for day-to-day content editor roles.</span></span>

    - <span data-ttu-id="cb87b-109">筛选模块选项，以便对特定页面部分仅显示相关模块。</span><span class="sxs-lookup"><span data-stu-id="cb87b-109">Filter module options so that only relevant modules are shown for a specific page section.</span></span> <span data-ttu-id="cb87b-110">（例如，可以将模板的市场营销部分配置为筛选掉不应在该上下文中使用的无关模板，仅使内容创作任务在显示时复杂化。）</span><span class="sxs-lookup"><span data-stu-id="cb87b-110">(For example, a marketing section of a template can be configured to filter out irrelevant modules that should never be used in that context, and that will just complicate content authoring tasks if they are shown.)</span></span>
    - <span data-ttu-id="cb87b-111">配置默认模块设置以帮助提高创作效率。</span><span class="sxs-lookup"><span data-stu-id="cb87b-111">Configure default module setting to help improve authoring efficiency.</span></span>
    - <span data-ttu-id="cb87b-112">定义默认页面片段以帮助提高创作效率。</span><span class="sxs-lookup"><span data-stu-id="cb87b-112">Define default page fragments to help improve authoring efficiency.</span></span> <span data-ttu-id="cb87b-113">（例如，每个下游页中都将自动显示模板中的页眉和页脚片段。）</span><span class="sxs-lookup"><span data-stu-id="cb87b-113">(For example, header and footer fragments in a template will automatically appear on every downstream page.)</span></span>

- <span data-ttu-id="cb87b-114">通过定义一组批准的模块安排和配置选项，让企业站点保持品牌化。</span><span class="sxs-lookup"><span data-stu-id="cb87b-114">Keep enterprise sites on-brand by defining an approved set of module arrangement and configuration options.</span></span>

    > [!TIP] 
    > <span data-ttu-id="cb87b-115">成功的电子商务站点为客户提供的是属性、可重复和品牌化的用户体验 (UX) 设计模式。</span><span class="sxs-lookup"><span data-stu-id="cb87b-115">Successful e-Commerce sites provide customers with familiar, repeatable, and on-brand user experience (UX) design patterns.</span></span> <span data-ttu-id="cb87b-116">通过使用模板，可帮助控制站点中的一致性。</span><span class="sxs-lookup"><span data-stu-id="cb87b-116">By using templates, you help control consistency across your site.</span></span>

- <span data-ttu-id="cb87b-117">可通过确保可重复且可以编程方式定义的页面定义和元数据来提高搜索引擎优化 (SEO) 分数。</span><span class="sxs-lookup"><span data-stu-id="cb87b-117">Improve search engine optimization (SEO) scores by ensuring repeatable and programmatically defined page definitions and metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="cb87b-118">虽然模板旨在控制站点中的一致性，理论上也可以配置为不实现任何一致性。</span><span class="sxs-lookup"><span data-stu-id="cb87b-118">Although templates are designed to control consistency across a site, they can theoretically be configured so that they don't enforce any consistency.</span></span> <span data-ttu-id="cb87b-119">品牌和站点管理员可为其站点中的页面定义任何可变性级别。</span><span class="sxs-lookup"><span data-stu-id="cb87b-119">Brand and site administrators can define any level of variability for the pages on their site.</span></span> <span data-ttu-id="cb87b-120">例如，可以让模板完全开放，这样内容创作者就可以创建选择的任何页面设计。</span><span class="sxs-lookup"><span data-stu-id="cb87b-120">For example, a template can be left entirely open, so that content authors can create any page design that they choose.</span></span> <span data-ttu-id="cb87b-121">在此情况下，不能享受上一个列表中的任何优点。</span><span class="sxs-lookup"><span data-stu-id="cb87b-121">In this case, none of the benefits in the preceding list are applicable.</span></span>

## <a name="modify-a-template"></a><span data-ttu-id="cb87b-122">修改模板</span><span class="sxs-lookup"><span data-stu-id="cb87b-122">Modify a template</span></span>

<span data-ttu-id="cb87b-123">可使用模板编辑器修改模板。</span><span class="sxs-lookup"><span data-stu-id="cb87b-123">Templates are modified by using the template editor.</span></span>

<span data-ttu-id="cb87b-124">若要打开模板编辑器，请执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="cb87b-124">To open the template editor, follow one of these steps:</span></span>

- <span data-ttu-id="cb87b-125">在站点的导航窗格中，选择**模板**，然后选择要修改的模板。</span><span class="sxs-lookup"><span data-stu-id="cb87b-125">In the navigation pane of your site, select **Templates**, and then select the template to modify.</span></span>
- <span data-ttu-id="cb87b-126">在现有页面的页面编辑器中，选择左侧大纲树中的顶级节点。</span><span class="sxs-lookup"><span data-stu-id="cb87b-126">In the page editor for an existing page, select the top node in the outline tree on the left.</span></span> <span data-ttu-id="cb87b-127">然后，在右侧属性窗格中，选择**编辑模板**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-127">Then, in the property pane on the right, select **Edit Template**.</span></span>

<span data-ttu-id="cb87b-128">左侧大纲树视图将显示子布局和页面的可用模块选项和结构。</span><span class="sxs-lookup"><span data-stu-id="cb87b-128">The outline tree view on the left shows the module options and structures that are available to child layouts and pages.</span></span> <span data-ttu-id="cb87b-129">在大纲树中选择模块之后，可在右侧属性窗格中查看所选模块的模板属性。</span><span class="sxs-lookup"><span data-stu-id="cb87b-129">When you select a module in the outline tree, you can view the template properties for the selected module in the property pane on the right.</span></span> <span data-ttu-id="cb87b-130">这些属性中的一些专用于编辑模板。</span><span class="sxs-lookup"><span data-stu-id="cb87b-130">Some of these properties are unique to template editing.</span></span> <span data-ttu-id="cb87b-131">下表描述这些属性。</span><span class="sxs-lookup"><span data-stu-id="cb87b-131">The following table describes these properties.</span></span>

| <span data-ttu-id="cb87b-132">属性名称</span><span class="sxs-lookup"><span data-stu-id="cb87b-132">Property name</span></span> | <span data-ttu-id="cb87b-133">说明</span><span class="sxs-lookup"><span data-stu-id="cb87b-133">Description</span></span> |
|---|---|
| <span data-ttu-id="cb87b-134">最小发生次数</span><span class="sxs-lookup"><span data-stu-id="cb87b-134">Min Occurs</span></span> | <span data-ttu-id="cb87b-135">此属性定义所选模块的最小发生次数。</span><span class="sxs-lookup"><span data-stu-id="cb87b-135">This property defines the minimum number of occurrences for the selected module.</span></span> <span data-ttu-id="cb87b-136">例如，如果此值设置为 **1**，则下游作者需要此模块，而如果此值设置为 **0**（零），则此模块可选。</span><span class="sxs-lookup"><span data-stu-id="cb87b-136">For example, if the value is set to **1**, the module is required for downstream authors, whereas if the value is set to **0** (zero), the module is optional.</span></span> |
| <span data-ttu-id="cb87b-137">最大发生次数</span><span class="sxs-lookup"><span data-stu-id="cb87b-137">Max Occurs</span></span> | <span data-ttu-id="cb87b-138">此属性定义所选模块的最大发生次数。</span><span class="sxs-lookup"><span data-stu-id="cb87b-138">This property defines the maximum number of occurrences for the selected module.</span></span> <span data-ttu-id="cb87b-139">例如，如果此值设置为 **1**，则此模块只能添加一次。</span><span class="sxs-lookup"><span data-stu-id="cb87b-139">For example, if the value is set to **1**, the module can be added only one time.</span></span> |
| <span data-ttu-id="cb87b-140">最小模块数量（容器）</span><span class="sxs-lookup"><span data-stu-id="cb87b-140">Min Modules (Containers)</span></span> | <span data-ttu-id="cb87b-141">对于其中包含其他模块的模块（即对于*容器模块*），此属性定义应该作为子代添加的模块的最小总数。</span><span class="sxs-lookup"><span data-stu-id="cb87b-141">For modules that contain other modules (that is, for *containers modules*), this property defines the minimum number of total modules that should be added as children.</span></span> <span data-ttu-id="cb87b-142">例如，对于传送模块，此值可以设置为大于 1 的数字。</span><span class="sxs-lookup"><span data-stu-id="cb87b-142">For example, for a carousel module, the value might be set to a number that is more than 1.</span></span> |
| <span data-ttu-id="cb87b-143">最大模块数量（容器）</span><span class="sxs-lookup"><span data-stu-id="cb87b-143">Max Modules (Containers)</span></span> | <span data-ttu-id="cb87b-144">对于容器模块，此属性定义应该作为子代添加的模块的最大总数。</span><span class="sxs-lookup"><span data-stu-id="cb87b-144">For container modules, this property defines the maximum number of total modules that should be added as children.</span></span> <span data-ttu-id="cb87b-145">例如，对于传送模块，此值可以设置为小于 10 的数字。</span><span class="sxs-lookup"><span data-stu-id="cb87b-145">For example, for a carousel module, the value might be set to a number that is less than 10.</span></span> |
| <span data-ttu-id="cb87b-146">已锁定</span><span class="sxs-lookup"><span data-stu-id="cb87b-146">Locked</span></span> | <span data-ttu-id="cb87b-147">所有核心模块属性旁边都会显示一个**已锁定**布尔值控件。</span><span class="sxs-lookup"><span data-stu-id="cb87b-147">A **Locked** Boolean control appears next to all core module properties.</span></span> <span data-ttu-id="cb87b-148">模块作者可将其用于锁定模板中的模块设置。</span><span class="sxs-lookup"><span data-stu-id="cb87b-148">It lets the template author lock a module setting in the template.</span></span> <span data-ttu-id="cb87b-149">任何子布局或页面都不能替代已锁定的模块设置。</span><span class="sxs-lookup"><span data-stu-id="cb87b-149">A module setting that is locked can't be overridden by any child layouts or pages.</span></span> <span data-ttu-id="cb87b-150">它将成为所有使用模板的布局和页面的可集中编辑的属性值。</span><span class="sxs-lookup"><span data-stu-id="cb87b-150">It becomes a centrally editable property value for all layouts and pages that use the template.</span></span> |

## <a name="create-a-new-template"></a><span data-ttu-id="cb87b-151">创建新模板</span><span class="sxs-lookup"><span data-stu-id="cb87b-151">Create a new template</span></span>

<span data-ttu-id="cb87b-152">若要创建新模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cb87b-152">To create a new template, follow these steps.</span></span>

1. <span data-ttu-id="cb87b-153">在站点的导航窗格中，选择**模板**打开模板检查器视图。</span><span class="sxs-lookup"><span data-stu-id="cb87b-153">In the navigation pane of your site, select **Templates** to open the template inspector view.</span></span>
1. <span data-ttu-id="cb87b-154">选择**新建模板**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-154">Select **New Template**.</span></span>
1. <span data-ttu-id="cb87b-155">在模板创建对话框中，输入模板的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="cb87b-155">In the template creation dialog box, enter a name and description for the template.</span></span> <span data-ttu-id="cb87b-156">作者创建新页面时，将对作者显示您输入的值。</span><span class="sxs-lookup"><span data-stu-id="cb87b-156">The values that you enter will be shown to authors when they create new pages.</span></span> <span data-ttu-id="cb87b-157">因此，输入对页面作者有用的元数据。</span><span class="sxs-lookup"><span data-stu-id="cb87b-157">Therefore, enter metadata that will be useful to page authors.</span></span> <span data-ttu-id="cb87b-158">例如，为描述输入**使用此模板创建常规市场营销页**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-158">For example, enter **Use this template to create general marketing pages** as the description.</span></span> <span data-ttu-id="cb87b-159">以后可以编辑此元数据。</span><span class="sxs-lookup"><span data-stu-id="cb87b-159">This metadata can be edited later.</span></span>
1. <span data-ttu-id="cb87b-160">选择**确定**创建新模板，然后打开模板编辑器。</span><span class="sxs-lookup"><span data-stu-id="cb87b-160">Select **OK** to create the new template and open the template editor.</span></span> <span data-ttu-id="cb87b-161">模板编辑器将在左侧显示大纲树，在右侧显示属性窗格。</span><span class="sxs-lookup"><span data-stu-id="cb87b-161">The template editor shows an outline tree on the left and a property pane on the right.</span></span>
1. <span data-ttu-id="cb87b-162">在大纲树中，展开节点，然后选择 **HTML 标头**插槽。</span><span class="sxs-lookup"><span data-stu-id="cb87b-162">In the outline tree, expand the nodes, and select the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cb87b-163">如果此插槽中还没有任何模块，请选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-163">If there aren't yet any modules in this slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb87b-164">在**添加模块**对话框中，选择**定义页面摘要**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-164">In the **Add Module** dialog box, select **Default page summary**, and then select **OK**.</span></span>
1. <span data-ttu-id="cb87b-165">在大纲树中，选择新模块，然后在属性窗格中，输入应该为模板所有子页自动配置的任何默认设置。</span><span class="sxs-lookup"><span data-stu-id="cb87b-165">In the outline tree, select the new module, and then, in the property pane, enter any default settings that should be automatically configured for all child pages of the template.</span></span> <span data-ttu-id="cb87b-166">如果不需要任何默认设置，请将值保留为空。</span><span class="sxs-lookup"><span data-stu-id="cb87b-166">If you don't want any default settings, leave the values blank.</span></span>
1. <span data-ttu-id="cb87b-167">在大纲树中，选择**正文**插槽，选择省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-167">In the outline tree, select the **Body** slot, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb87b-168">选择页面容器模块（可能只有一个选项），然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-168">Select a page container module (there might be only one option), and then select **OK**.</span></span>

<span data-ttu-id="cb87b-169">在新页面容器模块下，可以看到一组新插槽（**页眉**、**主**等）。</span><span class="sxs-lookup"><span data-stu-id="cb87b-169">Under the new page container module, you will see a new set of slots (**Header**, **Main**, and so on).</span></span> <span data-ttu-id="cb87b-170">可在此处添加和配置当作者基于此模板创建页面时的可用模块选项。</span><span class="sxs-lookup"><span data-stu-id="cb87b-170">Here, you can add and configure the module options that will be available to authors when they create pages from this template.</span></span> <span data-ttu-id="cb87b-171">默认情况下，如果不向插槽添加任何模块，则该插槽支持所有可用模块类型。</span><span class="sxs-lookup"><span data-stu-id="cb87b-171">By default, if you don't add any modules to a slot, all available modules types are supported for that slot.</span></span>

<span data-ttu-id="cb87b-172">从技术角度来说，此模板现在有效，可以保存，签入和用于创建新页面。</span><span class="sxs-lookup"><span data-stu-id="cb87b-172">The template is now technically valid, and it can be saved, checked in, and used to create new pages.</span></span> <span data-ttu-id="cb87b-173">但是，下面的三个部分介绍您可能希望先配置的其他一些默认设置。</span><span class="sxs-lookup"><span data-stu-id="cb87b-173">However, the next three sections describe some other default settings that you might want to configure first.</span></span>

## <a name="add-a-header-and-a-footer"></a><span data-ttu-id="cb87b-174">添加页眉和页脚</span><span class="sxs-lookup"><span data-stu-id="cb87b-174">Add a header and a footer</span></span>

<span data-ttu-id="cb87b-175">如果站点已经有页眉片段，请执行以下步骤向模板添加页眉和引脚。</span><span class="sxs-lookup"><span data-stu-id="cb87b-175">If your site already has a header fragment, follow these steps to add a header and a footer to a template.</span></span>

1. <span data-ttu-id="cb87b-176">在大纲树中，展开**正文**插槽及其子页模块。</span><span class="sxs-lookup"><span data-stu-id="cb87b-176">In the outline tree, expand the **Body** slot and its child page module.</span></span>
1. <span data-ttu-id="cb87b-177">选择**页眉**插槽。</span><span class="sxs-lookup"><span data-stu-id="cb87b-177">Select the **Header** slot.</span></span>
1. <span data-ttu-id="cb87b-178">选择**页眉**插槽的省略号按钮，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-178">Select the ellipsis button for the **Header** slot, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="cb87b-179">搜索并选择站点的页眉片段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-179">Search for and select your site's header fragment, and then select **OK**.</span></span>

<span data-ttu-id="cb87b-180">所有使用模板的页面将自动继承此页眉片段。</span><span class="sxs-lookup"><span data-stu-id="cb87b-180">All pages that use the template will now automatically inherit this header fragment.</span></span>

<span data-ttu-id="cb87b-181">如果站点还没有页眉片段，请参阅[创建片段](work-with-fragments.md#create-a-fragment)了解有关如何创建片段的信息，然后完成上一个过程。</span><span class="sxs-lookup"><span data-stu-id="cb87b-181">If your site doesn't yet have a header fragment, see [Create a fragment](work-with-fragments.md#create-a-fragment) for information about how to create it, and then complete the previous procedure.</span></span>

## <a name="change-the-template-theme"></a><span data-ttu-id="cb87b-182">更改模板主题</span><span class="sxs-lookup"><span data-stu-id="cb87b-182">Change the template theme</span></span>

<span data-ttu-id="cb87b-183">若要设置所有使用模板的页面的默认主题，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cb87b-183">To set the default theme for all pages that use a template, follow these steps.</span></span>

1. <span data-ttu-id="cb87b-184">在左侧的大纲树中，展开**正文**插槽。</span><span class="sxs-lookup"><span data-stu-id="cb87b-184">In the outline tree on the left, expand the **Body** slot.</span></span>
1. <span data-ttu-id="cb87b-185">在**正文**插槽中，选择页面容器模块（例如，**默认页**）。</span><span class="sxs-lookup"><span data-stu-id="cb87b-185">In the **Body** slot, select the page container module (for example, **Default Page**).</span></span>
1. <span data-ttu-id="cb87b-186">在右侧的属性窗格中**主题**字段内，选择一个主题。</span><span class="sxs-lookup"><span data-stu-id="cb87b-186">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

<span data-ttu-id="cb87b-187">默认情况下，所有新页面现在都使用所选主题。</span><span class="sxs-lookup"><span data-stu-id="cb87b-187">By default, all new pages will now use the selected theme.</span></span> <span data-ttu-id="cb87b-188">若要避免页面在布局或页面级别替代此设置，请将**已锁定**布尔值控件设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-188">To prevent pages from overriding this setting at the layout or page level, set the **Locked** Boolean control to **True**.</span></span>

## <a name="add-a-script-to-a-template"></a><span data-ttu-id="cb87b-189">向模板添加脚本</span><span class="sxs-lookup"><span data-stu-id="cb87b-189">Add a script to a template</span></span>

<span data-ttu-id="cb87b-190">可向模板添加其中包含 JavaScript 的 HTML **&lt;script&gt;** 元素。</span><span class="sxs-lookup"><span data-stu-id="cb87b-190">You can add HTML **&lt;script&gt;** elements that contain JavaScript to your template.</span></span> <span data-ttu-id="cb87b-191">这样，就可以向页面的 HTML 标题、正文开始和正文结束部分提供默认脚本行为。</span><span class="sxs-lookup"><span data-stu-id="cb87b-191">In this way, you can provide default script behaviors to the HTML head, body begin, and body end sections of your pages.</span></span>

<span data-ttu-id="cb87b-192">若要向模板添加脚本，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cb87b-192">To add a script to a template, follow these steps.</span></span>

1. <span data-ttu-id="cb87b-193">在左侧的大纲树中，选择要在其中添加 **&lt;script&gt;** 元素（如 HTML 标题、正文开始或正文结束）的插槽。</span><span class="sxs-lookup"><span data-stu-id="cb87b-193">In the outline tree on the left, select the slot where you want to add the **&lt;script&gt;** element (for example, the HTML head, body begin, or body end).</span></span>
1. <span data-ttu-id="cb87b-194">选择插槽的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-194">Select the ellipsis button for the slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb87b-195">在**添加模块**对话框中，选择一个脚本模块（例如，**外部脚本**或**内联脚本**）。</span><span class="sxs-lookup"><span data-stu-id="cb87b-195">In the **Add Module** dialog box, select a script module (for example, **External Script** or **Inline Script**).</span></span>
1. <span data-ttu-id="cb87b-196">在右侧属性窗格中相应脚本属性控件（例如，**内联脚本**或**脚本标记**）中，输入您的脚本。</span><span class="sxs-lookup"><span data-stu-id="cb87b-196">In the property pane on the right, in the appropriate script property control (for example, **Inline Script** or **Script tags**), enter your script.</span></span>
1. <span data-ttu-id="cb87b-197">在属性窗格中，输入要配置的其他任何可选设置。</span><span class="sxs-lookup"><span data-stu-id="cb87b-197">In the property pane, enter any other optional settings that you want to configure.</span></span>

> [!TIP]
> <span data-ttu-id="cb87b-198">如果要重复使用其他模板的任何脚本模块，可将其转换为片段。</span><span class="sxs-lookup"><span data-stu-id="cb87b-198">If you want to reuse any of your script modules for other templates, you can convert them to fragments.</span></span> <span data-ttu-id="cb87b-199">这样，就可以帮助提高创作流程的效率，而您可以集中执行更新流程。</span><span class="sxs-lookup"><span data-stu-id="cb87b-199">In this way, you help make the authoring process more efficient, and you centralize the update process.</span></span> <span data-ttu-id="cb87b-200">有关如何将脚本模块转换为片段的信息，请参阅[将现有模块配置另存为片段](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment)。</span><span class="sxs-lookup"><span data-stu-id="cb87b-200">For information about how to convert a script module to a fragment, see [Save an existing module configuration as a fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span></span>

## <a name="save-check-in-preview-and-publish-a-template"></a><span data-ttu-id="cb87b-201">保存，签入，预览和发布模块</span><span class="sxs-lookup"><span data-stu-id="cb87b-201">Save, check in, preview, and publish a template</span></span>

<span data-ttu-id="cb87b-202">若要保存和签入模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cb87b-202">To save and check in a template, follow these steps.</span></span>

1. <span data-ttu-id="cb87b-203">选择模板编辑器顶部的**保存**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-203">Select **Save** at the top of the template editor.</span></span> <span data-ttu-id="cb87b-204">保存的更改在签入前，不影响下游页。</span><span class="sxs-lookup"><span data-stu-id="cb87b-204">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="cb87b-205">选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-205">Select **Finish editing**.</span></span> <span data-ttu-id="cb87b-206">现在可为下游工作流发现更改。</span><span class="sxs-lookup"><span data-stu-id="cb87b-206">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="cb87b-207">若要预览更改，请打开使用模板的现有页面，或基于模板创建新页面。</span><span class="sxs-lookup"><span data-stu-id="cb87b-207">To preview your changes, either open an existing page that uses the template or create a new page from the template.</span></span>

<span data-ttu-id="cb87b-208">预览对模板的更改之后，执行以下步骤之一将模板发布到您的活动站点：</span><span class="sxs-lookup"><span data-stu-id="cb87b-208">After you've previewed the changes to your template, follow one of these steps to publish the template to your live site:</span></span>

* <span data-ttu-id="cb87b-209">转到**模板**，选择模板，然后选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-209">Go to **Templates**, select the template, and then select **Publish**.</span></span>
* <span data-ttu-id="cb87b-210">选择布局名称打开布局编辑器，然后选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="cb87b-210">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="cb87b-211">发布引用未发布模板的页面。</span><span class="sxs-lookup"><span data-stu-id="cb87b-211">Publish a page that references the unpublished template.</span></span> <span data-ttu-id="cb87b-212">将自动发布此模板。</span><span class="sxs-lookup"><span data-stu-id="cb87b-212">The template is automatically published.</span></span>

> [!WARNING]
> <span data-ttu-id="cb87b-213">模板或其他任何内容管理系统 (CMS) 项发布后，可在 Internet 中发现。</span><span class="sxs-lookup"><span data-stu-id="cb87b-213">When a template, or any other content management system (CMS) item, is published, it's discoverable on the internet.</span></span> <span data-ttu-id="cb87b-214">准备好公开文档或资产之前，切勿发布这些文档或资产。</span><span class="sxs-lookup"><span data-stu-id="cb87b-214">Don't publish documents or assets until you're ready to make them public.</span></span> <span data-ttu-id="cb87b-215">只有已经过身份验证的用户才可以发现已保存且签入，但尚未发布的文档版本。</span><span class="sxs-lookup"><span data-stu-id="cb87b-215">Document versions that have been saved and checked in, but that haven't been published, are discoverable only to authenticated system users.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb87b-216">其他资源</span><span class="sxs-lookup"><span data-stu-id="cb87b-216">Additional resources</span></span>

[<span data-ttu-id="cb87b-217">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="cb87b-217">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="cb87b-218">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="cb87b-218">Work with preset layouts</span></span>](work-with-layouts.md)
