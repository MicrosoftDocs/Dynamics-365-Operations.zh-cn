---
title: 使用模块
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。
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
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914786"
---
# <a name="work-with-modules"></a><span data-ttu-id="bec48-103">使用模块</span><span class="sxs-lookup"><span data-stu-id="bec48-103">Work with modules</span></span>

<span data-ttu-id="bec48-104">此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。</span><span class="sxs-lookup"><span data-stu-id="bec48-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="bec48-105">概览</span><span class="sxs-lookup"><span data-stu-id="bec48-105">Overview</span></span>

<span data-ttu-id="bec48-106">模块是构成页面结构的逻辑构建基块，其具有多种用途和作用范围。</span><span class="sxs-lookup"><span data-stu-id="bec48-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="bec48-107">某些模块是高级别容器，唯一用途是容纳和组织其他模块（子模块）。</span><span class="sxs-lookup"><span data-stu-id="bec48-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="bec48-108">其他模块（如简单图像放置模块）具有非常具体的用途。</span><span class="sxs-lookup"><span data-stu-id="bec48-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="bec48-109">其他模块（如传送模块）介于这两种类别之间。</span><span class="sxs-lookup"><span data-stu-id="bec48-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="bec48-110">默认情况下，Dynamics 365 Commerce 站点中有一个入门套件模块库，用于实现大多数基本的电子商务方案。</span><span class="sxs-lookup"><span data-stu-id="bec48-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="bec48-111">仅使用这些模块应该就可以构造端到端的电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="bec48-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="bec48-112">但是，您也可能希望自定义这些模块或生成新的自定义模块来满足特定需要。</span><span class="sxs-lookup"><span data-stu-id="bec48-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="bec48-113">如果要生成自定义模块，提供了模块设计软件开发工具包 (SDK) 来帮助您创建自定义模块库。</span><span class="sxs-lookup"><span data-stu-id="bec48-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="bec48-114">容器模块和插槽</span><span class="sxs-lookup"><span data-stu-id="bec48-114">Container modules and slots</span></span>

<span data-ttu-id="bec48-115">前面介绍过，设计某些模块是为了容纳子模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="bec48-116">这些模块称为*容器*，并允许嵌套模块层次结构。</span><span class="sxs-lookup"><span data-stu-id="bec48-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="bec48-117">容器模块中包含*插槽*。</span><span class="sxs-lookup"><span data-stu-id="bec48-117">Container modules include *slots*.</span></span> <span data-ttu-id="bec48-118">插槽用于处理容器中子模块的布局和用途。</span><span class="sxs-lookup"><span data-stu-id="bec48-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="bec48-119">例如，用于定义多个重要插槽的基本页面容器模块（任何页面的顶级模块）。</span><span class="sxs-lookup"><span data-stu-id="bec48-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="bec48-120">页眉插槽</span><span class="sxs-lookup"><span data-stu-id="bec48-120">A header slot</span></span>
- <span data-ttu-id="bec48-121">主体插槽</span><span class="sxs-lookup"><span data-stu-id="bec48-121">A body slot</span></span>
- <span data-ttu-id="bec48-122">页脚插槽</span><span class="sxs-lookup"><span data-stu-id="bec48-122">A footer slot</span></span>

<span data-ttu-id="bec48-123">模块的开发人员定义这些插槽，并确定可以在其中直接放入哪些和多少子模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="bec48-124">例如，页眉插槽可能仅支持**页眉模块**类型的一个模块，而主体模块支持任何类型任意数量的模块（除了其他页面容器模块）。</span><span class="sxs-lookup"><span data-stu-id="bec48-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="bec48-125">在创作工具中，页面作者不必提前了解每个插槽中可以放入哪些模块，不可以放入哪些模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="bec48-126">当页面作者厇插槽，然后尝试选择要为其添加的模块时，将看到该插槽支持的模块类型筛选后的视图。</span><span class="sxs-lookup"><span data-stu-id="bec48-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="bec48-127">内容模块</span><span class="sxs-lookup"><span data-stu-id="bec48-127">Content modules</span></span>

<span data-ttu-id="bec48-128">内容模块中包含内容和媒体内容，如文本（如标题、段落和链接）或资产引用（如图像、视频和 PDF）。</span><span class="sxs-lookup"><span data-stu-id="bec48-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="bec48-129">例如，**主图**、**特色**和**横幅**就是典型的内容模块类型。</span><span class="sxs-lookup"><span data-stu-id="bec48-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="bec48-130">这三种类型的模块中可以包含文本或媒体，不需要任何子模块即可在页面中显示内容。</span><span class="sxs-lookup"><span data-stu-id="bec48-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="bec48-131">典型日常页面和内容创作活动大部分涉及内容模块，主要是因为这些模块定义其父容器模块中呈现的实际内容。</span><span class="sxs-lookup"><span data-stu-id="bec48-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="bec48-132">提供了许多内容模块，这些模块通常是向页面嵌套模块层次结构添加的最后内容。</span><span class="sxs-lookup"><span data-stu-id="bec48-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="bec48-133">下图显示父容器模块插槽内如何嵌套模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![嵌套模块](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="bec48-135">添加或删除模块</span><span class="sxs-lookup"><span data-stu-id="bec48-135">Add or remove modules</span></span>

<span data-ttu-id="bec48-136">以下过程介绍如何添加和删除模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="bec48-137">添加模块</span><span class="sxs-lookup"><span data-stu-id="bec48-137">Add a module</span></span>

<span data-ttu-id="bec48-138">若要向页面中的插槽或容器添加模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bec48-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="bec48-139">在左侧的大纲窗格中，选择可向其添加子模块的容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="bec48-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bec48-140">模块设计者定义可添加到特定模块插槽的模块类型的列表。</span><span class="sxs-lookup"><span data-stu-id="bec48-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="bec48-141">然后，模板作者可优化允许的模块选项，以便帮助确保基于特定模板生成的所有页面获得一致的搜索引擎优化 (SEO) 和创作效率。</span><span class="sxs-lookup"><span data-stu-id="bec48-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="bec48-142">选择模块的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="bec48-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="bec48-143">将显示**添加模块**对话框。</span><span class="sxs-lookup"><span data-stu-id="bec48-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="bec48-144">将自动筛选此对话框，使其仅显示所选容器或插槽中支持的模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="bec48-145">模块列表由页面的目标或容器模块定义决定。</span><span class="sxs-lookup"><span data-stu-id="bec48-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bec48-146">如果容器或插槽不支持新子模块，则**添加模块**选项不可用。</span><span class="sxs-lookup"><span data-stu-id="bec48-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="bec48-147">在对话框中，搜索并选择要添加到页面的模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="bec48-148">**特色**和**主图**模块类型非常适合初学者。</span><span class="sxs-lookup"><span data-stu-id="bec48-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="bec48-149">选择**确定**将所选模块添加到页面中的所选容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="bec48-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="bec48-150">删除模块</span><span class="sxs-lookup"><span data-stu-id="bec48-150">Remove a module</span></span>

<span data-ttu-id="bec48-151">若要从站点中的插槽或容器删除模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bec48-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="bec48-152">在左侧大纲窗格中，选择要删除的模块的名称旁边的省略号按钮，然后选择废纸篓按钮。</span><span class="sxs-lookup"><span data-stu-id="bec48-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="bec48-153">系统提示确认要删除模块时，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="bec48-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="bec48-154">配置模块</span><span class="sxs-lookup"><span data-stu-id="bec48-154">Configure modules</span></span>

<span data-ttu-id="bec48-155">以下过程介绍如何配置内容模块和容器模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="bec48-156">配置内容模块</span><span class="sxs-lookup"><span data-stu-id="bec48-156">Configure a content module</span></span>

<span data-ttu-id="bec48-157">若要在页面中配置内容模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bec48-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="bec48-158">在左侧的大纲窗格中，选择一个内容模块类型（例如，**特色**、**主图**或**横幅**）。</span><span class="sxs-lookup"><span data-stu-id="bec48-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="bec48-159">在右侧的属性窗格中，通过选择标题展开嵌套的控件，然后设置所有必需控件值。</span><span class="sxs-lookup"><span data-stu-id="bec48-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="bec48-160">如果属性窗格有**数据配置**部分，请选择该部分将其展开。</span><span class="sxs-lookup"><span data-stu-id="bec48-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="bec48-161">否则，转到步骤 5。</span><span class="sxs-lookup"><span data-stu-id="bec48-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="bec48-162">如果有**添加数据源**按钮，选择该按钮，然后选择要添加的内容项。</span><span class="sxs-lookup"><span data-stu-id="bec48-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="bec48-163">输入所有必需或所需模块控件的设置。</span><span class="sxs-lookup"><span data-stu-id="bec48-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="bec48-164">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bec48-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="bec48-165">配置容器模块</span><span class="sxs-lookup"><span data-stu-id="bec48-165">Configure a container module</span></span>

<span data-ttu-id="bec48-166">若要在页面中配置容器模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bec48-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="bec48-167">在页面中选择一个容器模块（例如，传送或流体容器模块）。</span><span class="sxs-lookup"><span data-stu-id="bec48-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="bec48-168">在右侧的属性窗格中，通过选择标题展开嵌套的控件，然后设置所有必需控件值。</span><span class="sxs-lookup"><span data-stu-id="bec48-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="bec48-169">在左侧大纲窗格中，选择容器或容器内的任何插槽的名称旁边的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="bec48-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="bec48-170">然后向所选容器添加子模块。</span><span class="sxs-lookup"><span data-stu-id="bec48-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="bec48-171">有关详细信息，请参阅本主题前文的[添加模块](#add-a-module)过程。</span><span class="sxs-lookup"><span data-stu-id="bec48-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="bec48-172">如果多个子模块以同级的形式存在于父容器中，可以更改其在父容器中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="bec48-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="bec48-173">选择一个容器的省略号按钮，然后使用向上箭头按钮或向下箭头按钮。</span><span class="sxs-lookup"><span data-stu-id="bec48-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bec48-174">其他资源</span><span class="sxs-lookup"><span data-stu-id="bec48-174">Additional resources</span></span>

[<span data-ttu-id="bec48-175">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="bec48-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="bec48-176">使用模板</span><span class="sxs-lookup"><span data-stu-id="bec48-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="bec48-177">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="bec48-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="bec48-178">使用片段</span><span class="sxs-lookup"><span data-stu-id="bec48-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="bec48-179">向页面添加容器模块</span><span class="sxs-lookup"><span data-stu-id="bec48-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="bec48-180">向页面添加内容放置模块</span><span class="sxs-lookup"><span data-stu-id="bec48-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="bec48-181">使用发布组</span><span class="sxs-lookup"><span data-stu-id="bec48-181">Work with publish groups</span></span>](publish-groups.md)

