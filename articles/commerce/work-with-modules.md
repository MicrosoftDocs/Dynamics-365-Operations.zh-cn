---
title: 使用模块
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 89d95814e892e3afcb6514ab0d0219f7b08b9c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000451"
---
# <a name="work-with-modules"></a><span data-ttu-id="6423e-103">使用模块</span><span class="sxs-lookup"><span data-stu-id="6423e-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6423e-104">此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。</span><span class="sxs-lookup"><span data-stu-id="6423e-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6423e-105">概览</span><span class="sxs-lookup"><span data-stu-id="6423e-105">Overview</span></span>

<span data-ttu-id="6423e-106">模块是构成页面结构的逻辑构建基块，其具有多种用途和作用范围。</span><span class="sxs-lookup"><span data-stu-id="6423e-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="6423e-107">某些模块是高级别容器，唯一用途是容纳和组织其他模块（子模块）。</span><span class="sxs-lookup"><span data-stu-id="6423e-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="6423e-108">其他模块（如简单图像放置模块）具有非常具体的用途。</span><span class="sxs-lookup"><span data-stu-id="6423e-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="6423e-109">其他模块（如传送模块）介于这两种类别之间。</span><span class="sxs-lookup"><span data-stu-id="6423e-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="6423e-110">默认情况下，Dynamics 365 Commerce 站点中有一个模块库，用于实现大多数基本的电子商务方案。</span><span class="sxs-lookup"><span data-stu-id="6423e-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="6423e-111">仅使用这些模块应该就可以构造端到端的电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="6423e-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="6423e-112">但是，您也可能希望自定义这些模块或生成新的自定义模块来满足特定需要。</span><span class="sxs-lookup"><span data-stu-id="6423e-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="6423e-113">如果要生成自定义模块，提供了模块设计软件开发工具包 (SDK) 来帮助您创建自定义模块库。</span><span class="sxs-lookup"><span data-stu-id="6423e-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="6423e-114">容器模块和插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-114">Container modules and slots</span></span>

<span data-ttu-id="6423e-115">前面介绍过，设计某些模块是为了容纳子模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="6423e-116">这些模块称为 *容器*，并允许嵌套模块层次结构。</span><span class="sxs-lookup"><span data-stu-id="6423e-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="6423e-117">容器模块中包含 *插槽*。</span><span class="sxs-lookup"><span data-stu-id="6423e-117">Container modules include *slots*.</span></span> <span data-ttu-id="6423e-118">插槽用于处理容器中子模块的布局和用途。</span><span class="sxs-lookup"><span data-stu-id="6423e-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="6423e-119">例如，用于定义多个重要插槽的基本页面容器模块（任何页面的顶级模块）。</span><span class="sxs-lookup"><span data-stu-id="6423e-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="6423e-120">页眉插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-120">A header slot</span></span>
- <span data-ttu-id="6423e-121">子页眉插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-121">A sub-header slot</span></span>
- <span data-ttu-id="6423e-122">主插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-122">A main slot</span></span>
- <span data-ttu-id="6423e-123">页脚插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-123">A footer slot</span></span>
- <span data-ttu-id="6423e-124">子页脚插槽</span><span class="sxs-lookup"><span data-stu-id="6423e-124">A sub-footer slot</span></span>

<span data-ttu-id="6423e-125">模块的开发人员定义这些插槽，并确定可以在其中直接放入哪些和多少子模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="6423e-126">例如，页眉插槽可能仅支持 **页眉模块** 类型的一个模块，而主体模块支持任何类型任意数量的模块（除了其他页面容器模块）。</span><span class="sxs-lookup"><span data-stu-id="6423e-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="6423e-127">在创作工具中，页面作者不必提前了解每个插槽中可以放入哪些模块，不可以放入哪些模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="6423e-128">当页面作者厇插槽，然后尝试选择要为其添加的模块时，将看到该插槽支持的模块类型筛选后的视图。</span><span class="sxs-lookup"><span data-stu-id="6423e-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="6423e-129">内容模块</span><span class="sxs-lookup"><span data-stu-id="6423e-129">Content modules</span></span>

<span data-ttu-id="6423e-130">内容模块中包含内容和媒体内容，如文本（如标题、段落和链接）或资产引用（如图像、视频和 PDF）。</span><span class="sxs-lookup"><span data-stu-id="6423e-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="6423e-131">典型的内容模块类型包括内容块、文本块和促销横幅模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="6423e-132">这三种类型的模块中可以包含文本或媒体，不需要任何子模块即可在页面中显示内容。</span><span class="sxs-lookup"><span data-stu-id="6423e-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="6423e-133">典型日常页面和内容创作活动大部分涉及内容模块，主要是因为这些模块定义其父容器模块中呈现的实际内容。</span><span class="sxs-lookup"><span data-stu-id="6423e-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="6423e-134">提供了许多内容模块，这些模块通常是向页面嵌套模块层次结构添加的最后内容。</span><span class="sxs-lookup"><span data-stu-id="6423e-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="6423e-135">下图显示父容器模块插槽内如何嵌套模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![嵌套模块](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="6423e-137">添加或删除模块</span><span class="sxs-lookup"><span data-stu-id="6423e-137">Add or remove modules</span></span>

<span data-ttu-id="6423e-138">以下过程介绍如何添加和删除模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="6423e-139">添加模块</span><span class="sxs-lookup"><span data-stu-id="6423e-139">Add a module</span></span>

<span data-ttu-id="6423e-140">若要向页面中的插槽或容器添加模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6423e-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="6423e-141">在左侧的大纲窗格中或直接在主画布中，选择可向其添加子模块的容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="6423e-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6423e-142">模块设计者定义可添加到特定模块插槽的模块类型的列表。</span><span class="sxs-lookup"><span data-stu-id="6423e-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="6423e-143">然后，模板作者可优化允许的模块选项，以便帮助确保基于特定模板生成的所有页面获得一致的搜索引擎优化 (SEO) 和创作效率。</span><span class="sxs-lookup"><span data-stu-id="6423e-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="6423e-144">将模块添加到插槽时，将自动筛选 **添加模块** 对话框，使其仅显示所选容器或插槽中支持的模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="6423e-145">此允许模块列表由页面的模板或容器模块定义决定。</span><span class="sxs-lookup"><span data-stu-id="6423e-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="6423e-146">如果使用大纲窗格，请选择模块名称旁边的省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="6423e-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="6423e-147">如果直接在画布中使用控件，请在一个空插槽中或与当前所选模块相邻的插槽中选择加号 (**+**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="6423e-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6423e-148">如果容器或插槽不支持新子模块，则 **添加模块** 选项不可用。</span><span class="sxs-lookup"><span data-stu-id="6423e-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="6423e-149">在 **添加模块** 对话框中，选择要添加到页面的模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="6423e-150">**内容块** 是一个很好的适合初学者使用的模块类型。</span><span class="sxs-lookup"><span data-stu-id="6423e-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="6423e-151">选择 **确定** 将所选模块添加到页面中的所选容器或插槽。</span><span class="sxs-lookup"><span data-stu-id="6423e-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="6423e-152">删除模块</span><span class="sxs-lookup"><span data-stu-id="6423e-152">Remove a module</span></span>

<span data-ttu-id="6423e-153">若要从站点中的插槽或容器删除模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6423e-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="6423e-154">在左侧大纲窗格中，选择要删除的模块的名称旁边的省略号 (**...**)，然后选择垃圾桶符号。</span><span class="sxs-lookup"><span data-stu-id="6423e-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="6423e-155">或者，您可以在主画布中选择所选模块工具栏上的垃圾桶符号。</span><span class="sxs-lookup"><span data-stu-id="6423e-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="6423e-156">系统提示确认要删除模块时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6423e-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="6423e-157">将模块移到新位置</span><span class="sxs-lookup"><span data-stu-id="6423e-157">Move a module to a new position</span></span>

<span data-ttu-id="6423e-158">要将模块移到页面中的新位置，请使用以下任何一种方法。</span><span class="sxs-lookup"><span data-stu-id="6423e-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="6423e-159">使用大纲窗格移动模块</span><span class="sxs-lookup"><span data-stu-id="6423e-159">Move a module using the outline pane</span></span>

<span data-ttu-id="6423e-160">要使用大纲窗格移动模块，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6423e-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="6423e-161">在大纲窗格中选中并点住要移动的模块，然后将其拖到大纲中的新位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="6423e-162">大纲和画布上的蓝线表示可以放置模块的位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="6423e-163">释放模块，将其放到新位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="6423e-164">直接在画布内移动模块</span><span class="sxs-lookup"><span data-stu-id="6423e-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="6423e-165">要直接在画布内移动模块，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6423e-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="6423e-166">选择要在画布中移动的模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="6423e-167">选择模块工具栏中的向上或向下指示箭头符号，然后将箭头拖到页面的新位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="6423e-168">画布和大纲中的蓝线表示可以放置模块的位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="6423e-169">如果无法向上或向下移动模块，该箭头符号将灰显。</span><span class="sxs-lookup"><span data-stu-id="6423e-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="6423e-170">释放模块，将其放到新位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="6423e-171">使用省略号菜单移动模块</span><span class="sxs-lookup"><span data-stu-id="6423e-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="6423e-172">要使用省略号菜单移动模块，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6423e-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="6423e-173">在大纲或画布中选择一个模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="6423e-174">在大纲窗格中，或在画布的模块工具栏中，选择模块名称旁边的省略号 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="6423e-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="6423e-175">如果可以在容器或插槽中上下移动模块，您会看到 **上移** 或 **下移** 选项。</span><span class="sxs-lookup"><span data-stu-id="6423e-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="6423e-176">选择所需的移动选项，相对同级模块向上或向下移动模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="6423e-177">配置模块</span><span class="sxs-lookup"><span data-stu-id="6423e-177">Configure modules</span></span>

<span data-ttu-id="6423e-178">以下过程介绍如何配置内容模块和容器模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="6423e-179">配置内容模块</span><span class="sxs-lookup"><span data-stu-id="6423e-179">Configure a content module</span></span>

<span data-ttu-id="6423e-180">若要在页面中配置内容模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6423e-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="6423e-181">在左侧的大纲窗格中，展开树并选择任何内容模块（例如，**内容块**）。</span><span class="sxs-lookup"><span data-stu-id="6423e-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="6423e-182">或者，您可以在主画布中选择模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="6423e-183">在右侧的模块属性窗格中，输入任何所需模块控件的属性。</span><span class="sxs-lookup"><span data-stu-id="6423e-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="6423e-184">在命令栏上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6423e-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="6423e-185">这还将刷新预览画布。</span><span class="sxs-lookup"><span data-stu-id="6423e-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="6423e-186">编辑模块文本属性</span><span class="sxs-lookup"><span data-stu-id="6423e-186">Edit module text properties</span></span>

<span data-ttu-id="6423e-187">非只读的模块文本属性可以直接在画布中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="6423e-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="6423e-188">若要编辑模块文本属性，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6423e-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="6423e-189">在画布中选择文本控件，然后将光标置于要编辑文本的位置。</span><span class="sxs-lookup"><span data-stu-id="6423e-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="6423e-190">输入文本内容。</span><span class="sxs-lookup"><span data-stu-id="6423e-190">Enter your text content.</span></span>
1. <span data-ttu-id="6423e-191">选择文本内容以外的任何位置以继续编辑其他内容。</span><span class="sxs-lookup"><span data-stu-id="6423e-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="6423e-192">内联图像选择</span><span class="sxs-lookup"><span data-stu-id="6423e-192">Inline image selection</span></span>

<span data-ttu-id="6423e-193">非只读的模块图像可以直接从画布中更改。</span><span class="sxs-lookup"><span data-stu-id="6423e-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="6423e-194">要为内容模块选择新图像，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6423e-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="6423e-195">在画布中，双击图像。</span><span class="sxs-lookup"><span data-stu-id="6423e-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="6423e-196">这将打开媒体选择器窗口。</span><span class="sxs-lookup"><span data-stu-id="6423e-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="6423e-197">查找并选择要使用的新图像，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6423e-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="6423e-198">现在，新图像已呈现在画布中。</span><span class="sxs-lookup"><span data-stu-id="6423e-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="6423e-199">配置容器模块</span><span class="sxs-lookup"><span data-stu-id="6423e-199">Configure a container module</span></span>

<span data-ttu-id="6423e-200">若要在页面中配置容器模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6423e-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="6423e-201">在页面中选择一个容器模块（例如，传送或流体容器模块）。</span><span class="sxs-lookup"><span data-stu-id="6423e-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="6423e-202">在右侧的属性窗格中，通过选择标题展开嵌套的控件，然后设置所有必需控件值。</span><span class="sxs-lookup"><span data-stu-id="6423e-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="6423e-203">在左侧大纲窗格中，选择容器或容器内的任何插槽的名称旁边的省略号按钮，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="6423e-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="6423e-204">然后向所选容器添加子模块。</span><span class="sxs-lookup"><span data-stu-id="6423e-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="6423e-205">有关详细信息，请参阅本主题前文的[使用模块](#add-a-module)部分。</span><span class="sxs-lookup"><span data-stu-id="6423e-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="6423e-206">如果多个子模块以同级的形式存在于父容器中，可以更改其在父容器中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="6423e-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="6423e-207">选择一个容器的省略号按钮，然后使用向上箭头按钮或向下箭头按钮。</span><span class="sxs-lookup"><span data-stu-id="6423e-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6423e-208">其他资源</span><span class="sxs-lookup"><span data-stu-id="6423e-208">Additional resources</span></span>

[<span data-ttu-id="6423e-209">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="6423e-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6423e-210">使用模板</span><span class="sxs-lookup"><span data-stu-id="6423e-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="6423e-211">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="6423e-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="6423e-212">使用片段</span><span class="sxs-lookup"><span data-stu-id="6423e-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="6423e-213">向页面添加容器模块</span><span class="sxs-lookup"><span data-stu-id="6423e-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="6423e-214">使用发布组</span><span class="sxs-lookup"><span data-stu-id="6423e-214">Work with publish groups</span></span>](publish-groups.md)

