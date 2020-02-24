---
title: 容器模块
description: 此主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 93c16da0988cc955835231bdd1f7342f19063f85
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025497"
---
# <a name="container-module"></a><span data-ttu-id="35423-103">容器模块</span><span class="sxs-lookup"><span data-stu-id="35423-103">Container module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35423-104">此主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="35423-104">This topic covers container modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35423-105">概览</span><span class="sxs-lookup"><span data-stu-id="35423-105">Overview</span></span>

<span data-ttu-id="35423-106">容器是在其内部承载其他模块的模块。</span><span class="sxs-lookup"><span data-stu-id="35423-106">A container module is a module that hosts other modules inside it.</span></span> <span data-ttu-id="35423-107">容器模块的主要用途是通过为其设置的属性定义它所包含的模块的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-107">The primary purpose of a container module is to define, through the properties that are set for it, the layout of the modules that it contains.</span></span> <span data-ttu-id="35423-108">例如，这些模块可以按两列、三列、四列或六列布局并排显示。</span><span class="sxs-lookup"><span data-stu-id="35423-108">For example, those modules can appear side by side in a two-column, three-column, four-column, or six-column layout.</span></span> <span data-ttu-id="35423-109">其还可限制为容器宽度，也可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="35423-109">They can also be limited to the width of the container, or they can fill the screen.</span></span> <span data-ttu-id="35423-110">还可以向每个容器模块添加标题。</span><span class="sxs-lookup"><span data-stu-id="35423-110">A heading can also be added to every container module.</span></span>

<span data-ttu-id="35423-111">支持以下三个容器模块：容器、2 插槽容器和 3 插槽容器。</span><span class="sxs-lookup"><span data-stu-id="35423-111">Three container modules are supported: container, container with 2-slots, and container with 3-slots.</span></span> <span data-ttu-id="35423-112">任何类型的模块都可以放到这些容器中。</span><span class="sxs-lookup"><span data-stu-id="35423-112">Modules of any type can be put inside these containers.</span></span> 

> [!NOTE] 
> <span data-ttu-id="35423-113">建议始终将模块放在容器模块内，使其可限制为容器宽度。</span><span class="sxs-lookup"><span data-stu-id="35423-113">We recommend that you always put modules inside a container module, so that they can be limited to the width of the container.</span></span>

## <a name="examples-of-container-modules-in-e-commerce"></a><span data-ttu-id="35423-114">电子商务中的容器模块示例</span><span class="sxs-lookup"><span data-stu-id="35423-114">Examples of container modules in e-Commerce</span></span>

- <span data-ttu-id="35423-115">站点作者需要三列布局，其中三个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="35423-115">A site author wants a three-column layout, where three modules appear side by side.</span></span> <span data-ttu-id="35423-116">因此，站点作者使用 3 插槽容器类型的容器模块。</span><span class="sxs-lookup"><span data-stu-id="35423-116">Therefore, the site author uses a container module of the container with 3-slots type.</span></span>
- <span data-ttu-id="35423-117">站点作者需要六列布局，其中六个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="35423-117">A site author wants a six-column layout, where six modules appear side by side.</span></span> <span data-ttu-id="35423-118">因此，站点作者使用内部有六个列的容器类型的容器。</span><span class="sxs-lookup"><span data-stu-id="35423-118">Therefore, the site author uses a container of the contain type that has six columns inside it.</span></span>
- <span data-ttu-id="35423-119">站点作者要在页面中放置模块，但不希望其充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="35423-119">A site author wants to put a module on a page but doesn't want it to fill the screen.</span></span> <span data-ttu-id="35423-120">因此，站点作者将该模块添加到容器模块，并将容器的**宽度**属性设置为**适合容器**。</span><span class="sxs-lookup"><span data-stu-id="35423-120">Therefore, the site author adds the module to a container module and sets the container's **Width** property to **Fit container**.</span></span>

## <a name="container-module-properties"></a><span data-ttu-id="35423-121">容器模块属性</span><span class="sxs-lookup"><span data-stu-id="35423-121">Container module properties</span></span>

| <span data-ttu-id="35423-122">属性名称</span><span class="sxs-lookup"><span data-stu-id="35423-122">Property name</span></span>     | <span data-ttu-id="35423-123">值</span><span class="sxs-lookup"><span data-stu-id="35423-123">Values</span></span> | <span data-ttu-id="35423-124">说明</span><span class="sxs-lookup"><span data-stu-id="35423-124">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="35423-125">标题</span><span class="sxs-lookup"><span data-stu-id="35423-125">Heading</span></span>           | <span data-ttu-id="35423-126">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="35423-126">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="35423-127">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="35423-127">An optional heading can be provided for the container.</span></span> <span data-ttu-id="35423-128">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="35423-128">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="35423-129">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="35423-129">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="35423-130">宽度</span><span class="sxs-lookup"><span data-stu-id="35423-130">Width</span></span>             | <span data-ttu-id="35423-131">**适合容器**或**充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="35423-131">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="35423-132">如果此值设置为**适合容器**（默认值），则容器内的模块限制为容器的宽度。</span><span class="sxs-lookup"><span data-stu-id="35423-132">If the value is set to **Fit container** (the default value), the modules inside the container are limited to the width of the container.</span></span> <span data-ttu-id="35423-133">如果此值设置为**充满屏幕**，则模块不限制为容器宽度，而是可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="35423-133">If the value is set to **Fill screen**, the modules aren't limited to the container width but can fill the screen.</span></span> |
| <span data-ttu-id="35423-134">列数</span><span class="sxs-lookup"><span data-stu-id="35423-134">Number of columns</span></span> | <span data-ttu-id="35423-135">**1**、**2**、**3**、**4**、**6** 或 **12**</span><span class="sxs-lookup"><span data-stu-id="35423-135">**1**, **2**, **3**, **4**, **6**, or **12**</span></span> | <span data-ttu-id="35423-136">此属性定义容器中的列数。</span><span class="sxs-lookup"><span data-stu-id="35423-136">This property defines the number of columns in the container.</span></span> <span data-ttu-id="35423-137">一个容器中最多可以有 12 列。</span><span class="sxs-lookup"><span data-stu-id="35423-137">A container can have up to 12 columns.</span></span> |

## <a name="container-with-2-slots"></a><span data-ttu-id="35423-138">具有 2 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="35423-138">Container with 2-slots</span></span>

<span data-ttu-id="35423-139">2 插槽类型的容器已针对两列布局优化。</span><span class="sxs-lookup"><span data-stu-id="35423-139">The container with 2-slots type is optimized for a two-column layout.</span></span> <span data-ttu-id="35423-140">这种容器有两个插槽，可用于并排查看其内的模块。</span><span class="sxs-lookup"><span data-stu-id="35423-140">This type of container has two slots to allow for a side-by-side view of the modules that are inside.</span></span>

<span data-ttu-id="35423-141">可使用其他属性优化不同查看端口（移动设备、平板电脑、计算机等）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-141">Additional properties can be used to optimize the layout for different view ports (mobile devices, tablets, computers, and so on).</span></span> <span data-ttu-id="35423-142">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="35423-142">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="35423-143">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="35423-143">The following column width settings are available:</span></span>

- <span data-ttu-id="35423-144">**75%/25%** – 第一个模块的列宽为 75%，第二个模块的列宽为 25%。</span><span class="sxs-lookup"><span data-stu-id="35423-144">**75%/25%** – The first module has a column width of 75 percent, and the second module has a column width of 25 percent.</span></span> <span data-ttu-id="35423-145">也提供 **25%/75%** 选项。</span><span class="sxs-lookup"><span data-stu-id="35423-145">A **25%/75%** option is also available.</span></span>
- <span data-ttu-id="35423-146">**50%/50%** – 两个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="35423-146">**50%/50%** – Both modules have equal column width.</span></span>
- <span data-ttu-id="35423-147">**67%/33%** – 第一个模块的列宽为 67%，第二个模块的列宽为 33%。</span><span class="sxs-lookup"><span data-stu-id="35423-147">**67%/33%** – The first module has a column width of 67 percent, and the second module has a column width of 33 percent.</span></span> <span data-ttu-id="35423-148">也提供 **33%/67%** 选项。</span><span class="sxs-lookup"><span data-stu-id="35423-148">A **33%/67%** option is also available.</span></span>
- <span data-ttu-id="35423-149">**100%** – 两个模块采用完全列宽。</span><span class="sxs-lookup"><span data-stu-id="35423-149">**100%** – Both modules have a full-column width.</span></span> <span data-ttu-id="35423-150">因此，模块在一个列中垂直堆叠。</span><span class="sxs-lookup"><span data-stu-id="35423-150">Therefore, the modules are vertically stacked in a single column.</span></span> <span data-ttu-id="35423-151">虽然此单列布局与 2 插槽类型容器的意图相悖，却可能非常适合某些查看端口（例如，移动设备之类超小查看端口）。</span><span class="sxs-lookup"><span data-stu-id="35423-151">Although this single-column layout goes against intent of the container with 2-slots type, it might be preferable for some view ports (for example, extra-small view ports such as mobile devices).</span></span>

### <a name="container-with-2-slots-properties"></a><span data-ttu-id="35423-152">2 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="35423-152">Container with 2-slots properties</span></span>

| <span data-ttu-id="35423-153">属性名称</span><span class="sxs-lookup"><span data-stu-id="35423-153">Property name</span></span>                   | <span data-ttu-id="35423-154">值</span><span class="sxs-lookup"><span data-stu-id="35423-154">Values</span></span> | <span data-ttu-id="35423-155">说明</span><span class="sxs-lookup"><span data-stu-id="35423-155">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="35423-156">标题</span><span class="sxs-lookup"><span data-stu-id="35423-156">Heading</span></span>                         | <span data-ttu-id="35423-157">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="35423-157">Heading text and heading tag</span></span> | <span data-ttu-id="35423-158">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="35423-158">An optional can be provided for the container.</span></span> |
| <span data-ttu-id="35423-159">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-159">X-Small view port configuration</span></span> | <span data-ttu-id="35423-160">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="35423-160">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="35423-161">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-161">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="35423-162">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-162">Small view port configuration</span></span>   | <span data-ttu-id="35423-163">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="35423-163">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="35423-164">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-164">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="35423-165">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-165">Medium view port configuration</span></span>  | <span data-ttu-id="35423-166">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="35423-166">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="35423-167">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-167">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="35423-168">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-168">Large view port configuration</span></span>   | <span data-ttu-id="35423-169">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="35423-169">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="35423-170">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-170">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="container-with-3-slots"></a><span data-ttu-id="35423-171">具有 3 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="35423-171">Container with 3-slots</span></span>

<span data-ttu-id="35423-172">3 插槽模块容器已针对三列布局优化。</span><span class="sxs-lookup"><span data-stu-id="35423-172">The container with 3-slots modules type is optimized for a three-column layout.</span></span>

<span data-ttu-id="35423-173">可使用其他属性优化不同查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-173">Additional properties can be used to optimize the layout for different view ports.</span></span> <span data-ttu-id="35423-174">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="35423-174">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="35423-175">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="35423-175">The following column width settings are available:</span></span>

- <span data-ttu-id="35423-176">**33%/33%/33%** – 所有三个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="35423-176">**33%/33%/33%** – All three modules have equal column width.</span></span>
- <span data-ttu-id="35423-177">**50%/25%/25%** – 第一个模块的列宽为 50%，其余两个模块的列宽分别为 25%。</span><span class="sxs-lookup"><span data-stu-id="35423-177">**50%/25%/25%** – The first module has a column width of 50 percent, and each of the remaining two modules has a column width of 25 percent.</span></span> <span data-ttu-id="35423-178">也提供 **25%/50%/25%** 和 **25%/25%/50%** 选项。</span><span class="sxs-lookup"><span data-stu-id="35423-178">**25%/50%/25%** and **25%/25%/50%** options are also available.</span></span>
- <span data-ttu-id="35423-179">**16%/16%/67%** – 前两个模块每个的列宽为 16%，第三个模块的列宽为 67%。</span><span class="sxs-lookup"><span data-stu-id="35423-179">**16%/16%/67%** – Each of the first two modules has a column width of 16 percent, and the third module has a column width of 67 percent.</span></span> <span data-ttu-id="35423-180">也提供 **16%/67%/16%** 和 **67%/16%/16%** 选项。</span><span class="sxs-lookup"><span data-stu-id="35423-180">**16%/67%/16%** and **67%/16%/16%** options are also available.</span></span>

### <a name="container-with-3-slots-properties"></a><span data-ttu-id="35423-181">3 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="35423-181">Container with 3-slots properties</span></span>

| <span data-ttu-id="35423-182">属性名称</span><span class="sxs-lookup"><span data-stu-id="35423-182">Property name</span></span>                   | <span data-ttu-id="35423-183">值</span><span class="sxs-lookup"><span data-stu-id="35423-183">Values</span></span> | <span data-ttu-id="35423-184">说明</span><span class="sxs-lookup"><span data-stu-id="35423-184">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="35423-185">标题</span><span class="sxs-lookup"><span data-stu-id="35423-185">Heading</span></span>                         | <span data-ttu-id="35423-186">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="35423-186">Heading text and heading tag</span></span> | <span data-ttu-id="35423-187">可以向容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="35423-187">An optional heading can be added to the container.</span></span> |
| <span data-ttu-id="35423-188">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-188">X-Small view port configuration</span></span> | <span data-ttu-id="35423-189">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="35423-189">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="35423-190">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-190">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="35423-191">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-191">Small view port configuration</span></span>   | <span data-ttu-id="35423-192">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="35423-192">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="35423-193">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-193">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="35423-194">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-194">Medium view port configuration</span></span>  | <span data-ttu-id="35423-195">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="35423-195">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="35423-196">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-196">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="35423-197">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="35423-197">Large view port configuration</span></span>   | <span data-ttu-id="35423-198">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="35423-198">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="35423-199">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="35423-199">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="add-a-container-module-to-a-page"></a><span data-ttu-id="35423-200">向页面添加容器模块</span><span class="sxs-lookup"><span data-stu-id="35423-200">Add a container module to a page</span></span>

<span data-ttu-id="35423-201">若要向新页面添加容器播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="35423-201">To add a container player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="35423-202">创建一个名称为**容器模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="35423-202">Create a page template that is named **container template**.</span></span> 
1. <span data-ttu-id="35423-203">在**正文**插槽中，添加一个**默认页面**模块。</span><span class="sxs-lookup"><span data-stu-id="35423-203">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="35423-204">编辑完模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="35423-204">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="35423-205">使用您刚才创建的容器模板创建一个名称为**容器页**的页面。</span><span class="sxs-lookup"><span data-stu-id="35423-205">Use the container template that you just created to create a page that is named **container page**.</span></span>
1. <span data-ttu-id="35423-206">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="35423-206">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="35423-207">在容器模块的属性窗格中，将**列数**属性设置为 **1**，将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="35423-207">In the property pane for the container module, set the **Number of columns** property to **1** and the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="35423-208">在容器模块中，添加内容块模块。</span><span class="sxs-lookup"><span data-stu-id="35423-208">In the container module, add a content block module.</span></span>
1. <span data-ttu-id="35423-209">在内容块模块的属性窗格中，配置标题、图像和布局。</span><span class="sxs-lookup"><span data-stu-id="35423-209">In the property pane for the content block module, configure the heading, image, and layout.</span></span>
1. <span data-ttu-id="35423-210">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="35423-210">Save and preview the page.</span></span> <span data-ttu-id="35423-211">应该可以看到在容器模块宽度内填充的一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="35423-211">You should see one feature module that fits within the width of the container module.</span></span>
1. <span data-ttu-id="35423-212">在容器模块的属性窗格中，将**列数**属性的值设置为 **3**。</span><span class="sxs-lookup"><span data-stu-id="35423-212">In the property pane for the container module, change the value of the **Number of columns** property to **3**.</span></span>
1. <span data-ttu-id="35423-213">向容器模块再添加两个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="35423-213">Add two more content block modules to the container module.</span></span>
1. <span data-ttu-id="35423-214">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="35423-214">Save and preview the page.</span></span> <span data-ttu-id="35423-215">现在可以看到三个并排显示的内容块模块。</span><span class="sxs-lookup"><span data-stu-id="35423-215">You should now see three content block modules that appear side by side.</span></span>
1. <span data-ttu-id="35423-216">获得所需布局之后，编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="35423-216">After you've achieved the layout that you want, finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35423-217">其他资源</span><span class="sxs-lookup"><span data-stu-id="35423-217">Additional resources</span></span>

[<span data-ttu-id="35423-218">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="35423-218">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="35423-219">传送模块</span><span class="sxs-lookup"><span data-stu-id="35423-219">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="35423-220">文本块模块</span><span class="sxs-lookup"><span data-stu-id="35423-220">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="35423-221">购买框模块</span><span class="sxs-lookup"><span data-stu-id="35423-221">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="35423-222">购物车模块</span><span class="sxs-lookup"><span data-stu-id="35423-222">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="35423-223">结账模块</span><span class="sxs-lookup"><span data-stu-id="35423-223">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="35423-224">标题模块</span><span class="sxs-lookup"><span data-stu-id="35423-224">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="35423-225">页脚模块</span><span class="sxs-lookup"><span data-stu-id="35423-225">Footer module</span></span>](author-footer-module.md)
