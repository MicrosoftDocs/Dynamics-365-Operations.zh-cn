---
title: 容器模块
description: 本主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e1d2d600a00ab71348fbef2bc2f30cc53bc5314
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797783"
---
# <a name="container-module"></a><span data-ttu-id="505e3-103">容器模块</span><span class="sxs-lookup"><span data-stu-id="505e3-103">Container module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="505e3-104">本主题介绍容器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="505e3-104">This topic covers container modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="505e3-105">容器是在其内部承载其他模块的模块。</span><span class="sxs-lookup"><span data-stu-id="505e3-105">A container module is a module that hosts other modules inside it.</span></span> <span data-ttu-id="505e3-106">容器模块的主要用途是通过为其设置的属性定义它所包含的模块的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-106">The primary purpose of a container module is to define, through the properties that are set for it, the layout of the modules that it contains.</span></span> <span data-ttu-id="505e3-107">例如，这些模块可以按两列、三列、四列或六列布局并排显示。</span><span class="sxs-lookup"><span data-stu-id="505e3-107">For example, those modules can appear side by side in a two-column, three-column, four-column, or six-column layout.</span></span> <span data-ttu-id="505e3-108">其还可限制为容器宽度，也可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="505e3-108">They can also be limited to the width of the container, or they can fill the screen.</span></span> <span data-ttu-id="505e3-109">还可以向每个容器模块添加标题。</span><span class="sxs-lookup"><span data-stu-id="505e3-109">A heading can also be added to every container module.</span></span>

<span data-ttu-id="505e3-110">支持以下三个容器模块：容器、2 插槽容器和 3 插槽容器。</span><span class="sxs-lookup"><span data-stu-id="505e3-110">Three container modules are supported: container, container with 2-slots, and container with 3-slots.</span></span> <span data-ttu-id="505e3-111">任何类型的模块都可以放到这些容器中。</span><span class="sxs-lookup"><span data-stu-id="505e3-111">Modules of any type can be put inside these containers.</span></span> 

> [!NOTE] 
> <span data-ttu-id="505e3-112">建议始终将模块放在容器模块内，使其可限制为容器宽度。</span><span class="sxs-lookup"><span data-stu-id="505e3-112">We recommend that you always put modules inside a container module, so that they can be limited to the width of the container.</span></span>

## <a name="examples-of-container-modules-in-e-commerce"></a><span data-ttu-id="505e3-113">电子商务中的容器模块示例</span><span class="sxs-lookup"><span data-stu-id="505e3-113">Examples of container modules in e-Commerce</span></span>

- <span data-ttu-id="505e3-114">站点作者需要三列布局，其中三个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="505e3-114">A site author wants a three-column layout, where three modules appear side by side.</span></span> <span data-ttu-id="505e3-115">因此，站点作者使用 3 插槽容器类型的容器模块。</span><span class="sxs-lookup"><span data-stu-id="505e3-115">Therefore, the site author uses a container module of the container with 3-slots type.</span></span>
- <span data-ttu-id="505e3-116">站点作者需要六列布局，其中六个模块并排显示。</span><span class="sxs-lookup"><span data-stu-id="505e3-116">A site author wants a six-column layout, where six modules appear side by side.</span></span> <span data-ttu-id="505e3-117">因此，站点作者使用内部有六个列的容器类型的容器。</span><span class="sxs-lookup"><span data-stu-id="505e3-117">Therefore, the site author uses a container of the contain type that has six columns inside it.</span></span>
- <span data-ttu-id="505e3-118">站点作者要在页面中放置模块，但不希望其充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="505e3-118">A site author wants to put a module on a page but doesn't want it to fill the screen.</span></span> <span data-ttu-id="505e3-119">因此，站点作者将该模块添加到容器模块，并将容器的 **宽度** 属性设置为 **适合容器**。</span><span class="sxs-lookup"><span data-stu-id="505e3-119">Therefore, the site author adds the module to a container module and sets the container's **Width** property to **Fit container**.</span></span>

<span data-ttu-id="505e3-120">下图显示了 Commerce 站点构建器中包含传送模块的容器模块的示例。</span><span class="sxs-lookup"><span data-stu-id="505e3-120">The following image shows an example of a container module that contains a carousel module in Commerce site builder.</span></span> <span data-ttu-id="505e3-121">在此示例中，容器模块的 **宽度** 属性设置为 **填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="505e3-121">In this example, the **Width** property of the container module is set to **Fill Screen**.</span></span>

![容器模块的示例](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a><span data-ttu-id="505e3-123">容器模块属性</span><span class="sxs-lookup"><span data-stu-id="505e3-123">Container module properties</span></span>

| <span data-ttu-id="505e3-124">属性名称</span><span class="sxs-lookup"><span data-stu-id="505e3-124">Property name</span></span>     | <span data-ttu-id="505e3-125">值</span><span class="sxs-lookup"><span data-stu-id="505e3-125">Values</span></span> | <span data-ttu-id="505e3-126">说明</span><span class="sxs-lookup"><span data-stu-id="505e3-126">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="505e3-127">标题</span><span class="sxs-lookup"><span data-stu-id="505e3-127">Heading</span></span>           | <span data-ttu-id="505e3-128">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="505e3-128">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="505e3-129">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="505e3-129">An optional heading can be provided for the container.</span></span> <span data-ttu-id="505e3-130">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="505e3-130">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="505e3-131">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="505e3-131">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="505e3-132">宽度</span><span class="sxs-lookup"><span data-stu-id="505e3-132">Width</span></span>             | <span data-ttu-id="505e3-133">**适合容器** 或 **充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="505e3-133">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="505e3-134">如果此值设置为 **适合容器**（默认值），则容器内的模块限制为容器的宽度。</span><span class="sxs-lookup"><span data-stu-id="505e3-134">If the value is set to **Fit container** (the default value), the modules inside the container are limited to the width of the container.</span></span> <span data-ttu-id="505e3-135">如果此值设置为 **充满屏幕**，则模块不限制为容器宽度，而是可以充满屏幕。</span><span class="sxs-lookup"><span data-stu-id="505e3-135">If the value is set to **Fill screen**, the modules aren't limited to the container width but can fill the screen.</span></span> |
| <span data-ttu-id="505e3-136">列数</span><span class="sxs-lookup"><span data-stu-id="505e3-136">Number of columns</span></span> | <span data-ttu-id="505e3-137">**1**、**2**、**3**、**4**、**6** 或 **12**</span><span class="sxs-lookup"><span data-stu-id="505e3-137">**1**, **2**, **3**, **4**, **6**, or **12**</span></span> | <span data-ttu-id="505e3-138">此属性定义容器中的列数。</span><span class="sxs-lookup"><span data-stu-id="505e3-138">This property defines the number of columns in the container.</span></span> <span data-ttu-id="505e3-139">一个容器中最多可以有 12 列。</span><span class="sxs-lookup"><span data-stu-id="505e3-139">A container can have up to 12 columns.</span></span> |

## <a name="container-with-2-slots"></a><span data-ttu-id="505e3-140">具有 2 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="505e3-140">Container with 2-slots</span></span>

<span data-ttu-id="505e3-141">2 插槽类型的容器已针对两列布局优化。</span><span class="sxs-lookup"><span data-stu-id="505e3-141">The container with 2-slots type is optimized for a two-column layout.</span></span> <span data-ttu-id="505e3-142">这种容器有两个插槽，可用于并排查看其内的模块。</span><span class="sxs-lookup"><span data-stu-id="505e3-142">This type of container has two slots to allow for a side-by-side view of the modules that are inside.</span></span>

<span data-ttu-id="505e3-143">可使用其他属性优化不同查看端口（移动设备、平板电脑、计算机等）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-143">Additional properties can be used to optimize the layout for different view ports (mobile devices, tablets, computers, and so on).</span></span> <span data-ttu-id="505e3-144">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="505e3-144">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="505e3-145">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="505e3-145">The following column width settings are available:</span></span>

- <span data-ttu-id="505e3-146">**75%/25%** – 第一个模块的列宽为 75%，第二个模块的列宽为 25%。</span><span class="sxs-lookup"><span data-stu-id="505e3-146">**75%/25%** – The first module has a column width of 75 percent, and the second module has a column width of 25 percent.</span></span> <span data-ttu-id="505e3-147">也提供 **25%/75%** 选项。</span><span class="sxs-lookup"><span data-stu-id="505e3-147">A **25%/75%** option is also available.</span></span>
- <span data-ttu-id="505e3-148">**50%/50%** – 两个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="505e3-148">**50%/50%** – Both modules have equal column width.</span></span>
- <span data-ttu-id="505e3-149">**67%/33%** – 第一个模块的列宽为 67%，第二个模块的列宽为 33%。</span><span class="sxs-lookup"><span data-stu-id="505e3-149">**67%/33%** – The first module has a column width of 67 percent, and the second module has a column width of 33 percent.</span></span> <span data-ttu-id="505e3-150">也提供 **33%/67%** 选项。</span><span class="sxs-lookup"><span data-stu-id="505e3-150">A **33%/67%** option is also available.</span></span>
- <span data-ttu-id="505e3-151">**100%** – 两个模块采用完全列宽。</span><span class="sxs-lookup"><span data-stu-id="505e3-151">**100%** – Both modules have a full-column width.</span></span> <span data-ttu-id="505e3-152">因此，模块在一个列中垂直堆叠。</span><span class="sxs-lookup"><span data-stu-id="505e3-152">Therefore, the modules are vertically stacked in a single column.</span></span> <span data-ttu-id="505e3-153">虽然此单列布局与 2 插槽类型容器的意图相悖，却可能非常适合某些查看端口（例如，移动设备之类超小查看端口）。</span><span class="sxs-lookup"><span data-stu-id="505e3-153">Although this single-column layout goes against intent of the container with 2-slots type, it might be preferable for some view ports (for example, extra-small view ports such as mobile devices).</span></span>

### <a name="container-with-2-slots-properties"></a><span data-ttu-id="505e3-154">2 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="505e3-154">Container with 2-slots properties</span></span>

| <span data-ttu-id="505e3-155">属性名称</span><span class="sxs-lookup"><span data-stu-id="505e3-155">Property name</span></span>                   | <span data-ttu-id="505e3-156">值</span><span class="sxs-lookup"><span data-stu-id="505e3-156">Values</span></span> | <span data-ttu-id="505e3-157">说明</span><span class="sxs-lookup"><span data-stu-id="505e3-157">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="505e3-158">标题</span><span class="sxs-lookup"><span data-stu-id="505e3-158">Heading</span></span>                         | <span data-ttu-id="505e3-159">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="505e3-159">Heading text and heading tag</span></span> | <span data-ttu-id="505e3-160">可以为容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="505e3-160">An optional can be provided for the container.</span></span> |
| <span data-ttu-id="505e3-161">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-161">X-Small view port configuration</span></span> | <span data-ttu-id="505e3-162">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="505e3-162">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="505e3-163">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-163">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="505e3-164">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-164">Small view port configuration</span></span>   | <span data-ttu-id="505e3-165">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="505e3-165">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="505e3-166">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-166">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="505e3-167">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-167">Medium view port configuration</span></span>  | <span data-ttu-id="505e3-168">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="505e3-168">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="505e3-169">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-169">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="505e3-170">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-170">Large view port configuration</span></span>   | <span data-ttu-id="505e3-171">**25%/75%**、**75%/25%**、**50%/50%**、**67%/33%**、**33%/67%** 或 **100%**</span><span class="sxs-lookup"><span data-stu-id="505e3-171">**25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, or **100%**</span></span> | <span data-ttu-id="505e3-172">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-172">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="container-with-3-slots"></a><span data-ttu-id="505e3-173">具有 3 个插槽的容器</span><span class="sxs-lookup"><span data-stu-id="505e3-173">Container with 3-slots</span></span>

<span data-ttu-id="505e3-174">3 插槽模块容器已针对三列布局优化。</span><span class="sxs-lookup"><span data-stu-id="505e3-174">The container with 3-slots modules type is optimized for a three-column layout.</span></span>

<span data-ttu-id="505e3-175">可使用其他属性优化不同查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-175">Additional properties can be used to optimize the layout for different view ports.</span></span> <span data-ttu-id="505e3-176">可为每个查看端口定义各列的宽度。</span><span class="sxs-lookup"><span data-stu-id="505e3-176">For every view port, the width of each column can be defined.</span></span> <span data-ttu-id="505e3-177">提供了以下列宽设置：</span><span class="sxs-lookup"><span data-stu-id="505e3-177">The following column width settings are available:</span></span>

- <span data-ttu-id="505e3-178">**33%/33%/33%** – 所有三个模块的列宽相等。</span><span class="sxs-lookup"><span data-stu-id="505e3-178">**33%/33%/33%** – All three modules have equal column width.</span></span>
- <span data-ttu-id="505e3-179">**50%/25%/25%** – 第一个模块的列宽为 50%，其余两个模块的列宽分别为 25%。</span><span class="sxs-lookup"><span data-stu-id="505e3-179">**50%/25%/25%** – The first module has a column width of 50 percent, and each of the remaining two modules has a column width of 25 percent.</span></span> <span data-ttu-id="505e3-180">也提供 **25%/50%/25%** 和 **25%/25%/50%** 选项。</span><span class="sxs-lookup"><span data-stu-id="505e3-180">**25%/50%/25%** and **25%/25%/50%** options are also available.</span></span>
- <span data-ttu-id="505e3-181">**16%/16%/67%** – 前两个模块每个的列宽为 16%，第三个模块的列宽为 67%。</span><span class="sxs-lookup"><span data-stu-id="505e3-181">**16%/16%/67%** – Each of the first two modules has a column width of 16 percent, and the third module has a column width of 67 percent.</span></span> <span data-ttu-id="505e3-182">也提供 **16%/67%/16%** 和 **67%/16%/16%** 选项。</span><span class="sxs-lookup"><span data-stu-id="505e3-182">**16%/67%/16%** and **67%/16%/16%** options are also available.</span></span>

### <a name="container-with-3-slots-properties"></a><span data-ttu-id="505e3-183">3 插槽容器属性</span><span class="sxs-lookup"><span data-stu-id="505e3-183">Container with 3-slots properties</span></span>

| <span data-ttu-id="505e3-184">属性名称</span><span class="sxs-lookup"><span data-stu-id="505e3-184">Property name</span></span>                   | <span data-ttu-id="505e3-185">值</span><span class="sxs-lookup"><span data-stu-id="505e3-185">Values</span></span> | <span data-ttu-id="505e3-186">说明</span><span class="sxs-lookup"><span data-stu-id="505e3-186">Description</span></span> |
|---------------------------------|--------|-------------|
| <span data-ttu-id="505e3-187">标题</span><span class="sxs-lookup"><span data-stu-id="505e3-187">Heading</span></span>                         | <span data-ttu-id="505e3-188">标题文本和标题标记</span><span class="sxs-lookup"><span data-stu-id="505e3-188">Heading text and heading tag</span></span> | <span data-ttu-id="505e3-189">可以向容器提供可选标题。</span><span class="sxs-lookup"><span data-stu-id="505e3-189">An optional heading can be added to the container.</span></span> |
| <span data-ttu-id="505e3-190">超小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-190">X-Small view port configuration</span></span> | <span data-ttu-id="505e3-191">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="505e3-191">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="505e3-192">此属性定义超小查看端口的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-192">This property defines the layout for extra-small view ports.</span></span> |
| <span data-ttu-id="505e3-193">小查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-193">Small view port configuration</span></span>   | <span data-ttu-id="505e3-194">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="505e3-194">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="505e3-195">此属性定义小查看端口（如移动设备）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-195">This property defines the layout for small view ports, such as mobile devices.</span></span> |
| <span data-ttu-id="505e3-196">中等查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-196">Medium view port configuration</span></span>  | <span data-ttu-id="505e3-197">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="505e3-197">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="505e3-198">此属性定义中等查看端口（如平板电脑）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-198">This property defines the layout for medium view ports, such as tablets.</span></span> |
| <span data-ttu-id="505e3-199">大型查看端口配置</span><span class="sxs-lookup"><span data-stu-id="505e3-199">Large view port configuration</span></span>   | <span data-ttu-id="505e3-200">**33%/33%/33%**、**50%/25%/25%**、**25%/50%/25%**、**25%/25%/50%**、**16%/16%/67%**、**16%/67%/16%** 或 **67%/16%/16%**</span><span class="sxs-lookup"><span data-stu-id="505e3-200">**33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, or **67%/16%/16%**</span></span> | <span data-ttu-id="505e3-201">此属性定义大型查看端口（如计算机）的布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-201">This property defines the layout for large view ports, such as computers.</span></span> |

## <a name="add-a-container-module-to-a-page"></a><span data-ttu-id="505e3-202">向页面添加容器模块</span><span class="sxs-lookup"><span data-stu-id="505e3-202">Add a container module to a page</span></span>

<span data-ttu-id="505e3-203">若要向新页面添加容器播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="505e3-203">To add a container player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="505e3-204">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="505e3-204">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="505e3-205">在 **新建模板** 对话框的 **模板名称** 下，输入 **容器模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="505e3-205">In the **New Template** dialog box, under **Template name**, enter **Container template**, and then select **OK**.</span></span>
1. <span data-ttu-id="505e3-206">在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="505e3-206">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="505e3-207">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="505e3-207">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="505e3-208">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="505e3-208">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="505e3-209">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="505e3-209">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="505e3-210">在 **选择模板** 对话框中，选择您创建的视频播放器模板。</span><span class="sxs-lookup"><span data-stu-id="505e3-210">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="505e3-211">在 **页面名称** 下，输入 **容器页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="505e3-211">Under **Page name**, enter **Container page**, and then select **OK**.</span></span>
1. <span data-ttu-id="505e3-212">在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="505e3-212">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="505e3-213">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="505e3-213">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="505e3-214">在容器模块的属性窗格中，将 **列数** 属性设置为 **1**，将 **宽度** 属性设置为 **填充容器**。</span><span class="sxs-lookup"><span data-stu-id="505e3-214">In the property pane for the container module, set the **Number of columns** property to **1** and the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="505e3-215">在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="505e3-215">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="505e3-216">在 **添加模块** 对话框中，选择 **内容块** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="505e3-216">In the **Add Module** dialog box, select the **Content block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="505e3-217">在内容块模块的属性窗格中，配置标题、图像和布局。</span><span class="sxs-lookup"><span data-stu-id="505e3-217">In the property pane for the content block module, configure the heading, image, and layout.</span></span>
1. <span data-ttu-id="505e3-218">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="505e3-218">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="505e3-219">应该可以看到在容器模块宽度内填充的一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="505e3-219">You should see one feature module that fits within the width of the container module.</span></span>
1. <span data-ttu-id="505e3-220">在容器模块的属性窗格中，将 **列数** 属性的值设置为 **3**。</span><span class="sxs-lookup"><span data-stu-id="505e3-220">In the property pane for the container module, change the value of the **Number of columns** property to **3**.</span></span>
1. <span data-ttu-id="505e3-221">将另外两个内容块模块添加到容器模块，然后进行配置。</span><span class="sxs-lookup"><span data-stu-id="505e3-221">Add two more content block modules to the container module, and configure them.</span></span>
1. <span data-ttu-id="505e3-222">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="505e3-222">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="505e3-223">现在可以看到三个并排显示的内容块模块。</span><span class="sxs-lookup"><span data-stu-id="505e3-223">You should now see three content block modules that appear side by side.</span></span>
1. <span data-ttu-id="505e3-224">实现所需的布局后，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="505e3-224">After you've achieved the layout that you want, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="505e3-225">其他资源</span><span class="sxs-lookup"><span data-stu-id="505e3-225">Additional resources</span></span>

[<span data-ttu-id="505e3-226">模块库概述</span><span class="sxs-lookup"><span data-stu-id="505e3-226">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="505e3-227">可折叠模块</span><span class="sxs-lookup"><span data-stu-id="505e3-227">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="505e3-228">标签模块</span><span class="sxs-lookup"><span data-stu-id="505e3-228">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="505e3-229">传送模块</span><span class="sxs-lookup"><span data-stu-id="505e3-229">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="505e3-230">文本块模块</span><span class="sxs-lookup"><span data-stu-id="505e3-230">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="505e3-231">购买框模块</span><span class="sxs-lookup"><span data-stu-id="505e3-231">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="505e3-232">购物车模块</span><span class="sxs-lookup"><span data-stu-id="505e3-232">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="505e3-233">结账模块</span><span class="sxs-lookup"><span data-stu-id="505e3-233">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="505e3-234">标题模块</span><span class="sxs-lookup"><span data-stu-id="505e3-234">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="505e3-235">页脚模块</span><span class="sxs-lookup"><span data-stu-id="505e3-235">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]