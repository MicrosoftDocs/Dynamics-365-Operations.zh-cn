---
title: "产品维度"
description: "有四产品维度 - 颜色、配置、大小和样式。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e9b1400de76858ca458d6742fba63c967ac6ad74
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="product-dimensions"></a><span data-ttu-id="5ef3c-105">产品维度</span><span class="sxs-lookup"><span data-stu-id="5ef3c-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="5ef3c-106">有四产品维度 - 颜色、配置、大小和样式。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="5ef3c-107">您在维度组中合并产品维度，并将维度组分配给基础产品。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="5ef3c-108">产品维度的组合确定如何定义产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="5ef3c-109">产品维度是用于标识产品变型的特性。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="5ef3c-110">您可以使用产品维度的组合来定义产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="5ef3c-111">必须至少为基础产品定义一个产品维度，以便创建产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="5ef3c-112">产品变型</span><span class="sxs-lookup"><span data-stu-id="5ef3c-112">Product variants</span></span>
----------------

<span data-ttu-id="5ef3c-113">产品变型也称作物料。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="5ef3c-114">该物料是与服务不同的有形产品。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="5ef3c-115">还可以用服务类型定义基础产品。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="5ef3c-116">通过使用“服务”类型，可以指定包括服务的产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="5ef3c-117">例如，您可以为咨询工作指定基础产品，为高级顾问和初级顾问执行的工作指定产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="5ef3c-118">产品维度</span><span class="sxs-lookup"><span data-stu-id="5ef3c-118">Product dimensions</span></span>
<span data-ttu-id="5ef3c-119">以下产品维度可用：配置、颜色、尺寸和样式。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="5ef3c-120">产品变型可以基于产品维度值生成。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="5ef3c-121">产品维度值（例如尺寸、颜色和样式）可以在**尺寸**、**颜色**和**样式**页创建，可以从以下位置访问这些页：**产品信息管理** &gt; **设置** &gt; **维度和变型组** &gt; **尺寸/颜色/样式**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="5ef3c-122">配置维度的产品维度值通常使用产品配置器或基于维度的配置器创建。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="5ef3c-123">产品维度还可以在**产品维度**页中创建和维护，可从以下位置访问该页：</span><span class="sxs-lookup"><span data-stu-id="5ef3c-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="5ef3c-124">单击**产品信息管理** &gt; **产品** &gt; **基础产品**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="5ef3c-125">在**操作窗格**上单击**产品维度**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="5ef3c-126">单击**产品信息管理** &gt; **产品** &gt; **所有产品和基础产品**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="5ef3c-127">选择基础产品。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-127">Select a product master.</span></span> <span data-ttu-id="5ef3c-128">在**操作窗格**上单击**产品维度**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="5ef3c-129">单击**产品信息管理** &gt; **已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="5ef3c-130">选择基础产品。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-130">Select a product master.</span></span> <span data-ttu-id="5ef3c-131">在**操作窗格**上，单击**产品**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="5ef3c-132">在**基础产品**组，单击**产品维度**。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="5ef3c-133">为物料可创建的变型数受限于可能的产品维度组合数。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="5ef3c-134">**提示**</span><span class="sxs-lookup"><span data-stu-id="5ef3c-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef3c-135">例如，当您在订单行上使用一个产品时，选择产品维度以确定您要使用的产品变型。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="5ef3c-136">示例</span><span class="sxs-lookup"><span data-stu-id="5ef3c-136">Example</span></span>
<span data-ttu-id="5ef3c-137">一家公司销售牛仔裤。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-137">A company sells denim jeans.</span></span> <span data-ttu-id="5ef3c-138">物料（即牛仔裤）使用颜色和尺寸产品维度。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="5ef3c-139">销售的牛仔裤有三种不同的颜色和六种不同的尺寸。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="5ef3c-140">颜色：蓝色、黑色、棕色 尺寸：XS、S、M、L、XL、XXL 不是全部三种颜色都提供所有尺寸。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="5ef3c-141">如果所有组合均可用，将得到 18 种不同类型的牛仔裤。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="5ef3c-142">在此示例中，只生产了以下九个产品变型组合。</span><span class="sxs-lookup"><span data-stu-id="5ef3c-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="5ef3c-143">颜色</span><span class="sxs-lookup"><span data-stu-id="5ef3c-143">Color</span></span> | <span data-ttu-id="5ef3c-144">大小</span><span class="sxs-lookup"><span data-stu-id="5ef3c-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="5ef3c-145">蓝色</span><span class="sxs-lookup"><span data-stu-id="5ef3c-145">Blue</span></span>  | <span data-ttu-id="5ef3c-146">XS</span><span class="sxs-lookup"><span data-stu-id="5ef3c-146">XS</span></span>   |
| <span data-ttu-id="5ef3c-147">蓝色</span><span class="sxs-lookup"><span data-stu-id="5ef3c-147">Blue</span></span>  | <span data-ttu-id="5ef3c-148">六</span><span class="sxs-lookup"><span data-stu-id="5ef3c-148">S</span></span>    |
| <span data-ttu-id="5ef3c-149">蓝色</span><span class="sxs-lookup"><span data-stu-id="5ef3c-149">Blue</span></span>  | <span data-ttu-id="5ef3c-150">一</span><span class="sxs-lookup"><span data-stu-id="5ef3c-150">M</span></span>    |
| <span data-ttu-id="5ef3c-151">黑</span><span class="sxs-lookup"><span data-stu-id="5ef3c-151">Black</span></span> | <span data-ttu-id="5ef3c-152">一</span><span class="sxs-lookup"><span data-stu-id="5ef3c-152">M</span></span>    |
| <span data-ttu-id="5ef3c-153">黑</span><span class="sxs-lookup"><span data-stu-id="5ef3c-153">Black</span></span> | <span data-ttu-id="5ef3c-154">L</span><span class="sxs-lookup"><span data-stu-id="5ef3c-154">L</span></span>    |
| <span data-ttu-id="5ef3c-155">黑</span><span class="sxs-lookup"><span data-stu-id="5ef3c-155">Black</span></span> | <span data-ttu-id="5ef3c-156">XL</span><span class="sxs-lookup"><span data-stu-id="5ef3c-156">XL</span></span>   |
| <span data-ttu-id="5ef3c-157">棕</span><span class="sxs-lookup"><span data-stu-id="5ef3c-157">Brown</span></span> | <span data-ttu-id="5ef3c-158">L</span><span class="sxs-lookup"><span data-stu-id="5ef3c-158">L</span></span>    |
| <span data-ttu-id="5ef3c-159">棕</span><span class="sxs-lookup"><span data-stu-id="5ef3c-159">Brown</span></span> | <span data-ttu-id="5ef3c-160">XL</span><span class="sxs-lookup"><span data-stu-id="5ef3c-160">XL</span></span>   |
| <span data-ttu-id="5ef3c-161">棕</span><span class="sxs-lookup"><span data-stu-id="5ef3c-161">Brown</span></span> | <span data-ttu-id="5ef3c-162">XXL</span><span class="sxs-lookup"><span data-stu-id="5ef3c-162">XXL</span></span>  |






