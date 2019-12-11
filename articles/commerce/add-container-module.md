---
title: 容器模块
description: 此主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697052"
---
# <a name="container-module"></a><span data-ttu-id="87446-103">容器模块</span><span class="sxs-lookup"><span data-stu-id="87446-103">Container module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="87446-104">此主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="87446-104">This topic covers container modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87446-105">概览</span><span class="sxs-lookup"><span data-stu-id="87446-105">Overview</span></span>

<span data-ttu-id="87446-106">容器是在其内部承载其他模块的模块。</span><span class="sxs-lookup"><span data-stu-id="87446-106">A container module is a module that hosts other modules inside it.</span></span> <span data-ttu-id="87446-107">这是 Dynamics 365 Commerce 中最常用的容器。</span><span class="sxs-lookup"><span data-stu-id="87446-107">It's the most generic container that is used in Dynamics 365 Commerce.</span></span> <span data-ttu-id="87446-108">容器模块的主要用途是通过为其设置的属性定义容器模块内部的模块布局。</span><span class="sxs-lookup"><span data-stu-id="87446-108">The primary purpose of a container module is to define, through the properties that are set for it, the layout of the modules that are inside.</span></span> <span data-ttu-id="87446-109">例如，这些模块可以按两列、三列、四列或六列布局并排显示。</span><span class="sxs-lookup"><span data-stu-id="87446-109">For example, those modules can appear side by side in a two-column, three-column, four-column, or six-column layout.</span></span> <span data-ttu-id="87446-110">其还可限制为容器宽度，也可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="87446-110">They can also be limited to width of the container, or they can fill the screen.</span></span> <span data-ttu-id="87446-111">还可以向每个容器模块添加标题。</span><span class="sxs-lookup"><span data-stu-id="87446-111">A heading can also be added to every container module.</span></span>

<span data-ttu-id="87446-112">有三种标准容器模块：容器、2 插槽容器和 3 插槽容器。</span><span class="sxs-lookup"><span data-stu-id="87446-112">There are three standard types of container modules: container, container with 2-slots, and container with 3-slots.</span></span> <span data-ttu-id="87446-113">任何类型的模块都可以放到这些容器中。</span><span class="sxs-lookup"><span data-stu-id="87446-113">Modules of any type of module can be put inside these containers.</span></span> <span data-ttu-id="87446-114">还有特殊类型的容器模块，如传送、内容丰富块、内容放置、购物车、结帐、购买框、页眉和页脚。</span><span class="sxs-lookup"><span data-stu-id="87446-114">There are also special types of container modules, such as carousel, content rich block, content placement, cart, checkout, buy box, header, and footer.</span></span> <span data-ttu-id="87446-115">这些容器有特定用途，并且只能在其内放置支持的特定类型模块。</span><span class="sxs-lookup"><span data-stu-id="87446-115">These containers have specific purposes, and only specific supported types of modules can be put inside them.</span></span>

<span data-ttu-id="87446-116">建议将模块放在容器内，使其可限制为容器宽度。</span><span class="sxs-lookup"><span data-stu-id="87446-116">We recommend that you put modules inside a container, so that they can be limited to the width of the container.</span></span>

## <a name="examples-of-container-modules-in-e-commerce"></a><span data-ttu-id="87446-117">电子商务中的容器模块示例</span><span class="sxs-lookup"><span data-stu-id="87446-117">Examples of container modules in e-Commerce</span></span>

- <span data-ttu-id="87446-118">站点作者需要三列布局，其中三个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="87446-118">A site author wants a three-column layout, where three modules appear side by side.</span></span> <span data-ttu-id="87446-119">因此，站点作者使用 3 插槽容器类型的容器模块。</span><span class="sxs-lookup"><span data-stu-id="87446-119">Therefore, the site author uses a container module of the container with 3-slots type.</span></span>
- <span data-ttu-id="87446-120">站点作者需要六列布局，其中六个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="87446-120">A site author wants a six-column layout, where six modules appear side by side.</span></span> <span data-ttu-id="87446-121">因此，站点作者使用内部有六个列的容器类型的容器。</span><span class="sxs-lookup"><span data-stu-id="87446-121">Therefore, the site author uses a container of the contain type that has six columns inside it.</span></span>
- <span data-ttu-id="87446-122">站点作者要在页面中放置模块，但不希望其充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="87446-122">A site author wants to put a module on a page but doesn't want it to fill the screen.</span></span> <span data-ttu-id="87446-123">因此，站点作者将该模块添加到容器模块，并将容器的**宽度**属性设置为**适合容器**。</span><span class="sxs-lookup"><span data-stu-id="87446-123">Therefore, the site author adds the module to a container module and sets the container's **Width** property to **Fit container**.</span></span>

## <a name="container-module-properties"></a><span data-ttu-id="87446-124">容器模块属性</span><span class="sxs-lookup"><span data-stu-id="87446-124">Container module properties</span></span>

| <span data-ttu-id="87446-125">属性名称</span><span class="sxs-lookup"><span data-stu-id="87446-125">Property name</span></span>     | <span data-ttu-id="87446-126">值</span><span class="sxs-lookup"><span data-stu-id="87446-126">Values</span></span> | <span data-ttu-id="87446-127">说明</span><span class="sxs-lookup"><span data-stu-id="87446-127">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="87446-128">标题</span><span class="sxs-lookup"><span data-stu-id="87446-128">Heading</span></span>           | <span data-ttu-id="87446-129">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="87446-129">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="87446-130">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="87446-130">An optional heading can be provided for the container.</span></span> <span data-ttu-id="87446-131">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="87446-131">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="87446-132">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="87446-132">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="87446-133">宽度</span><span class="sxs-lookup"><span data-stu-id="87446-133">Width</span></span>             | <span data-ttu-id="87446-134">**适合容器**或**充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="87446-134">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="87446-135">如果此值设置为**适合容器**（默认值），则容器内的模块限制为容器的宽度。</span><span class="sxs-lookup"><span data-stu-id="87446-135">If the value is set to **Fit container** (the default value), the modules inside the container are limited to the width of the container.</span></span> <span data-ttu-id="87446-136">如果此值设置为**充满屏幕**，则模块不限制为容器宽度，而是可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="87446-136">If the value is set to **Fill screen**, the modules aren't limited to the container width but can fill the screen.</span></span> |
| <span data-ttu-id="87446-137">列数</span><span class="sxs-lookup"><span data-stu-id="87446-137">Number of columns</span></span> | <span data-ttu-id="87446-138">**1**、**2**、**3**、**4**、**6** 或 **12**</span><span class="sxs-lookup"><span data-stu-id="87446-138">**1**, **2**, **3**, **4**, **6**, or **12**</span></span> | <span data-ttu-id="87446-139">此属性定义容器中的列数。</span><span class="sxs-lookup"><span data-stu-id="87446-139">This property defines the number of columns in the container.</span></span> <span data-ttu-id="87446-140">一个容器中最多可以有 12 列。</span><span class="sxs-lookup"><span data-stu-id="87446-140">A container can have up to 12 columns.</span></span> |

## <a name="container-with-2-slots"></a><span data-ttu-id="87446-141">具有 2 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="87446-141">Container with 2-slots</span></span>

<span data-ttu-id="87446-142">2 插槽类型的容器已针对两列布局优化。</span><span class="sxs-lookup"><span data-stu-id="87446-142">The container with 2-slots type is optimized for a two-column layout.</span></span> <span data-ttu-id="87446-143">这种容器有两个插槽，可用于并排查看其内的模块。</span><span class="sxs-lookup"><span data-stu-id="87446-143">This type of container has two slots to allow for a side-by-side view of the modules that are inside.</span></span>

<span data-ttu-id="87446-144">可使用其他属性优化不同查看端口（移动设备、平板电脑、计算机等）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-144">Additional properties can be used to optimize the layout for different view ports (mobile devices, tablets, computers, and so on).</span></span> <span data-ttu-id="87446-145">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="87446-145">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="87446-146">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="87446-146">The following column width settings are available:</span></span>

- <span data-ttu-id="87446-147">**75%/25%** – 第一个模块的列宽为 75%，第二个模块的列宽为 25%。</span><span class="sxs-lookup"><span data-stu-id="87446-147">**75%/25%** – The first module has a column width of 75 percent, and the second module has a column width of 25 percent.</span></span> <span data-ttu-id="87446-148">也提供 **25%/75%** 选项。</span><span class="sxs-lookup"><span data-stu-id="87446-148">A **25%/75%** option is also available.</span></span>
- <span data-ttu-id="87446-149">**50%/50%** – 两个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="87446-149">**50%/50%** – Both modules have equal column width.</span></span>
- <span data-ttu-id="87446-150">**67%/33%** – 第一个模块的列宽为 67%，第二个模块的列宽为 33%。</span><span class="sxs-lookup"><span data-stu-id="87446-150">**67%/33%** – The first module has a column width of 67 percent, and the second module has a column width of 33 percent.</span></span> <span data-ttu-id="87446-151">也提供 **33%/67%** 选项。</span><span class="sxs-lookup"><span data-stu-id="87446-151">A **33%/67%** option is also available.</span></span>
- <span data-ttu-id="87446-152">**100%** – 两个模块采用完全列宽。</span><span class="sxs-lookup"><span data-stu-id="87446-152">**100%** – Both modules have a full-column width.</span></span> <span data-ttu-id="87446-153">因此，模块在一个列中垂直堆叠。</span><span class="sxs-lookup"><span data-stu-id="87446-153">Therefore, the modules are vertically stacked in a single column.</span></span> <span data-ttu-id="87446-154">虽然此单列布局与 2 插槽类型容器的意图相悖，却可能非常适合某些查看端口（例如，移动设备之类超小查看端口）。</span><span class="sxs-lookup"><span data-stu-id="87446-154">Although this single-column layout goes against intent of the container with 2-slots type, it might be preferable for some view ports (for example, extra-small view ports such as mobile devices).</span></span>

### <a name="container-with-2-slots-properties"></a><span data-ttu-id="87446-155">2 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="87446-155">Container with 2-slots properties</span></span>

| <span data-ttu-id="87446-156">属性名称</span><span class="sxs-lookup"><span data-stu-id="87446-156">Property name</span></span>                   | <span data-ttu-id="87446-157">值</span><span class="sxs-lookup"><span data-stu-id="87446-157">Values</span></span> | <span data-ttu-id="87446-158">说明</span><span class="sxs-lookup"><span data-stu-id="87446-158">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="87446-159">标题</span><span class="sxs-lookup"><span data-stu-id="87446-159">Heading</span></span>                         | <span data-ttu-id="87446-160">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="87446-160">Heading text and heading tag</span></span> | <span data-ttu-id="87446-161">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="87446-161">An optional can be provided for the container.</span></span> |
| <span data-ttu-id="87446-162">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-162">X-Small view port configuration</span></span> | <span data-ttu-id="87446-163">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="87446-163">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="87446-164">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-164">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="87446-165">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-165">Small view port configuration</span></span>   | <span data-ttu-id="87446-166">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="87446-166">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="87446-167">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-167">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="87446-168">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-168">Medium view port configuration</span></span>  | <span data-ttu-id="87446-169">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="87446-169">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="87446-170">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-170">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="87446-171">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-171">Large view port configuration</span></span>   | <span data-ttu-id="87446-172">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="87446-172">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="87446-173">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-173">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="container-with-3-slots"></a><span data-ttu-id="87446-174">具有 3 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="87446-174">Container with 3-slots</span></span>

<span data-ttu-id="87446-175">3 插槽模块容器已针对三列布局优化。</span><span class="sxs-lookup"><span data-stu-id="87446-175">The container with 3-slots modules type is optimized for a three-column layout.</span></span>

<span data-ttu-id="87446-176">可使用其他属性优化不同查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-176">Additional properties can be used to optimize the layout for different view ports.</span></span> <span data-ttu-id="87446-177">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="87446-177">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="87446-178">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="87446-178">The following column width settings are available:</span></span>

- <span data-ttu-id="87446-179">**33%/33%/33%** – 所有三个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="87446-179">**33%/33%/33%** – All three modules have equal column width.</span></span>
- <span data-ttu-id="87446-180">**50%/25%/25%** – 第一个模块的列宽为 50%，其余两个模块的列宽分别为 25%。</span><span class="sxs-lookup"><span data-stu-id="87446-180">**50%/25%/25%** – The first module has a column width of 50 percent, and each of the remaining two modules has a column width of 25 percent.</span></span> <span data-ttu-id="87446-181">也提供 **25%/50%/25%** 和 **25%/25%/50%** 选项。</span><span class="sxs-lookup"><span data-stu-id="87446-181">**25%/50%/25%** and **25%/25%/50%** options are also available.</span></span>
- <span data-ttu-id="87446-182">**16%/16%/67%** – 前两个模块每个的列宽为 16%，第三个模块的列宽为 67%。</span><span class="sxs-lookup"><span data-stu-id="87446-182">**16%/16%/67%** – Each of the first two modules has a column width of 16 percent, and the third module has a column width of 67 percent.</span></span> <span data-ttu-id="87446-183">也提供 **16%/67%/16%** 和 **67%/16%/16%** 选项。</span><span class="sxs-lookup"><span data-stu-id="87446-183">**16%/67%/16%** and **67%/16%/16%** options are also available.</span></span>

### <a name="container-with-3-slots-properties"></a><span data-ttu-id="87446-184">3 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="87446-184">Container with 3-slots properties</span></span>

| <span data-ttu-id="87446-185">属性名称</span><span class="sxs-lookup"><span data-stu-id="87446-185">Property name</span></span>                   | <span data-ttu-id="87446-186">值</span><span class="sxs-lookup"><span data-stu-id="87446-186">Values</span></span> | <span data-ttu-id="87446-187">说明</span><span class="sxs-lookup"><span data-stu-id="87446-187">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="87446-188">标题</span><span class="sxs-lookup"><span data-stu-id="87446-188">Heading</span></span>                         | <span data-ttu-id="87446-189">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="87446-189">Heading text and heading tag</span></span> | <span data-ttu-id="87446-190">可以向容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="87446-190">An optional heading can be added to the container.</span></span> |
| <span data-ttu-id="87446-191">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-191">X-Small view port configuration</span></span> | <span data-ttu-id="87446-192">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="87446-192">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="87446-193">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-193">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="87446-194">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-194">Small view port configuration</span></span>   | <span data-ttu-id="87446-195">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="87446-195">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="87446-196">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-196">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="87446-197">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-197">Medium view port configuration</span></span>  | <span data-ttu-id="87446-198">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="87446-198">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="87446-199">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-199">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="87446-200">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="87446-200">Large view port configuration</span></span>   | <span data-ttu-id="87446-201">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="87446-201">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="87446-202">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="87446-202">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="add-a-container-module-to-a-page"></a><span data-ttu-id="87446-203">向页面添加容器模块</span><span class="sxs-lookup"><span data-stu-id="87446-203">Add a container module to a page</span></span>

<span data-ttu-id="87446-204">若要向新页面添加容器播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="87446-204">To add a container player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="87446-205">创建一个名称为**容器模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="87446-205">Create a page template that is named **container template**.</span></span>
1. <span data-ttu-id="87446-206">在默认页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="87446-206">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="87446-207">在容器模块中添加一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="87446-207">In the container module, add a feature module.</span></span>
1. <span data-ttu-id="87446-208">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="87446-208">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="87446-209">使用您刚才创建的容器模板创建一个名称为**容器页**的页面。</span><span class="sxs-lookup"><span data-stu-id="87446-209">Use the container template that you just created to create a page that is named **container page**.</span></span>
1. <span data-ttu-id="87446-210">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="87446-210">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="87446-211">在容器模块的属性窗格中，将**列数**属性设置为 **1**，将**宽度**属性设置为**适合容器**。</span><span class="sxs-lookup"><span data-stu-id="87446-211">In the property pane for the container module, set the **Number of columns** property to **1** and the **Width** property to **Fit container**.</span></span>
1. <span data-ttu-id="87446-212">在容器模块中添加一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="87446-212">In the container module, add a feature module.</span></span>
1. <span data-ttu-id="87446-213">在特色模块的属性窗格中，配置标题。</span><span class="sxs-lookup"><span data-stu-id="87446-213">In the property pane for the feature module, configure a heading.</span></span>
1. <span data-ttu-id="87446-214">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="87446-214">Save and preview the page.</span></span> <span data-ttu-id="87446-215">应该可以看到在容器模块宽度内填充的一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="87446-215">You should see one feature module that fits within the width of the container module.</span></span>
1. <span data-ttu-id="87446-216">在容器模块的属性窗格中，将**列数**属性的值设置为 **3**。</span><span class="sxs-lookup"><span data-stu-id="87446-216">In the property pane for the container module, change the the value of the **Number of columns** property to **3**.</span></span>
1. <span data-ttu-id="87446-217">向容器模块再添加两个特色模块。</span><span class="sxs-lookup"><span data-stu-id="87446-217">Add two more feature modules to the container module.</span></span>
1. <span data-ttu-id="87446-218">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="87446-218">Save and preview the page.</span></span> <span data-ttu-id="87446-219">现在可以看到三个并排显示的特色模块。</span><span class="sxs-lookup"><span data-stu-id="87446-219">You should now see three feature modules that appear side by side.</span></span>
1. <span data-ttu-id="87446-220">获得所需布局之后，签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="87446-220">After you've achieved the layout that you want, check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87446-221">其他资源</span><span class="sxs-lookup"><span data-stu-id="87446-221">Additional resources</span></span>

[<span data-ttu-id="87446-222">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="87446-222">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="87446-223">传送模块</span><span class="sxs-lookup"><span data-stu-id="87446-223">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="87446-224">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="87446-224">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="87446-225">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="87446-225">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="87446-226">购买框模块</span><span class="sxs-lookup"><span data-stu-id="87446-226">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="87446-227">购物车模块</span><span class="sxs-lookup"><span data-stu-id="87446-227">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="87446-228">结帐模块</span><span class="sxs-lookup"><span data-stu-id="87446-228">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="87446-229">页眉模块</span><span class="sxs-lookup"><span data-stu-id="87446-229">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="87446-230">页脚模块</span><span class="sxs-lookup"><span data-stu-id="87446-230">Footer module</span></span>](author-footer-module.md)
