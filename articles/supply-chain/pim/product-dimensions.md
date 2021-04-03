---
title: 产品维度
description: 产品有五个维度 - 颜色、配置、尺寸、样式和版本。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ca0a7233004522de2af7281416169f0393feeb11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260639"
---
# <a name="product-dimensions"></a><span data-ttu-id="c7ff5-105">产品维度</span><span class="sxs-lookup"><span data-stu-id="c7ff5-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ff5-106">产品有五个维度：颜色、配置、尺寸、样式和版本。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-106">There are five product dimensions: color, configuration, size, style, and version.</span></span> <span data-ttu-id="c7ff5-107">您在维度组中合并产品维度，并将维度组分配给基础产品。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="c7ff5-108">产品维度的组合确定如何定义产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="c7ff5-109">产品维度是用于标识产品变型的特性。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="c7ff5-110">您可以使用产品维度的组合来定义产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="c7ff5-111">必须至少为基础产品定义一个产品维度，以便创建产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="c7ff5-112">产品变型</span><span class="sxs-lookup"><span data-stu-id="c7ff5-112">Product variants</span></span>

<span data-ttu-id="c7ff5-113">产品变型也称作物料。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="c7ff5-114">物料是有形产品，与服务不同。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-114">An item is a tangible product, which isn't the same as a service.</span></span> <span data-ttu-id="c7ff5-115">也可以使用服务类型定义产品主数据。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-115">It's also possible to define a product master with the service type.</span></span> <span data-ttu-id="c7ff5-116">使用服务类型，您可以指定包含服务的产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-116">By using the service type, you can specify product variants that include services.</span></span> <span data-ttu-id="c7ff5-117">例如，您可以为咨询工作指定产品主数据，为高级顾问和初级顾问执行的工作指定产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-117">For example, you can specify a product master for consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="c7ff5-118">产品维度</span><span class="sxs-lookup"><span data-stu-id="c7ff5-118">Product dimensions</span></span>

<span data-ttu-id="c7ff5-119">产品变型可以基于产品维度值生成。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-119">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="c7ff5-120">可以在以下位置创建尺寸、颜色和样式维度的产品维度值：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-120">Product dimension values for the size, color, and style dimensions can be created in the following locations:</span></span>

- <span data-ttu-id="c7ff5-121">**尺寸** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 尺寸**）</span><span class="sxs-lookup"><span data-stu-id="c7ff5-121">**Size** page (**Product information management \> Setup \> Dimension and variant groups \> Sizes**)</span></span>
- <span data-ttu-id="c7ff5-122">**颜色** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 颜色**）</span><span class="sxs-lookup"><span data-stu-id="c7ff5-122">**Color** page (**Product information management \> Setup \> Dimension and variant groups \> Colors**)</span></span>
- <span data-ttu-id="c7ff5-123">**样式** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 样式**）</span><span class="sxs-lookup"><span data-stu-id="c7ff5-123">**Style** page (**Product information management \> Setup \> Dimension and variant groups \> Styles**)</span></span>

<span data-ttu-id="c7ff5-124">通常使用产品配置器或基于维度的配置器创建配置维度的产品维度值。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-124">Product dimension values for the configuration dimension are typically created by using either the Product configurator or the Dimension-based configurator.</span></span> 

<span data-ttu-id="c7ff5-125">产品版本通常是在产品在其生命周期内演进时针对特定版本创建的。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-125">Product versions are usually created for specific versions as the product evolves during its lifecycle.</span></span> <span data-ttu-id="c7ff5-126">本主题后面将详细介绍产品版本。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-126">Product versions are covered in detail later in this topic.</span></span>

<span data-ttu-id="c7ff5-127">产品维度还可以在 **产品维度** 页中创建和维护，可从以下位置访问该页：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-127">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>

- <span data-ttu-id="c7ff5-128">转到 **产品信息管理 \> 产品 \> 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-128">Go to **Product information management \> Products \> Product masters**.</span></span> <span data-ttu-id="c7ff5-129">在操作窗格上，选择 **产品维度**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-129">On the Action Pane, select **Product dimensions**.</span></span>
- <span data-ttu-id="c7ff5-130">转到 **产品信息管理 \> 产品 \> 所有产品和产品主数据**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-130">Go to **Product information management \> Products \> All products and product masters**.</span></span> <span data-ttu-id="c7ff5-131">选择基础产品。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-131">Select a product master.</span></span> <span data-ttu-id="c7ff5-132">在操作窗格上，选择 **产品维度**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-132">On the Action Pane, select **Product dimensions**.</span></span>
- <span data-ttu-id="c7ff5-133">转到 **产品信息管理 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-133">Go to **Product information management \> Released products**.</span></span> <span data-ttu-id="c7ff5-134">选择基础产品。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-134">Select a product master.</span></span> <span data-ttu-id="c7ff5-135">在操作窗格的 **产品** 选项卡上，在 **产品主数据** 组中，选择 **产品维度**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-135">On the Action Pane, on the **Product** tab, in the **Product master** group, select **Product dimensions**.</span></span>

<span data-ttu-id="c7ff5-136">为物料可创建的变型数受限于可能的产品维度组合数。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-136">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

> [!TIP]
> <span data-ttu-id="c7ff5-137">例如，当您在订单行上使用产品时，您选择产品维度来标识要使用的产品变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-137">When you use a product on an order line, for example, you select the product dimensions to identify the product variant that you want to work with.</span></span>

## <a name="example"></a><span data-ttu-id="c7ff5-138">示例</span><span class="sxs-lookup"><span data-stu-id="c7ff5-138">Example</span></span>

<span data-ttu-id="c7ff5-139">一家公司销售牛仔裤。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-139">A company sells denim jeans.</span></span> <span data-ttu-id="c7ff5-140">物料 *牛仔裤* 使用颜色和尺寸产品维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-140">The item, *Jeans*, uses the color and size product dimensions.</span></span> <span data-ttu-id="c7ff5-141">销售的牛仔裤有三种不同的颜色和六种不同的尺寸。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-141">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="c7ff5-142">颜色有蓝色、黑色和棕色。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-142">The colors are blue, black, and brown.</span></span> <span data-ttu-id="c7ff5-143">尺寸有 XS、S、M、L、XL 和 XXL。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-143">The sizes are XS, S, M, L, XL, and XXL.</span></span> <span data-ttu-id="c7ff5-144">并非所有尺寸都提供三种颜色。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-144">Not all sizes are available in all three colors.</span></span> <span data-ttu-id="c7ff5-145">如果所有组合都可用，那么将有 18 种不同类型的牛仔裤。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-145">If all combinations were available, there would be 18 different types of jeans.</span></span> <span data-ttu-id="c7ff5-146">但是，在此示例中，仅生成以下九个产品变型组合。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-146">However, in this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="c7ff5-147">颜色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-147">Color</span></span> | <span data-ttu-id="c7ff5-148">大小</span><span class="sxs-lookup"><span data-stu-id="c7ff5-148">Size</span></span> |
|-------|------|
| <span data-ttu-id="c7ff5-149">蓝色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-149">Blue</span></span>  | <span data-ttu-id="c7ff5-150">XS</span><span class="sxs-lookup"><span data-stu-id="c7ff5-150">XS</span></span>   |
| <span data-ttu-id="c7ff5-151">蓝色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-151">Blue</span></span>  | <span data-ttu-id="c7ff5-152">六</span><span class="sxs-lookup"><span data-stu-id="c7ff5-152">S</span></span>    |
| <span data-ttu-id="c7ff5-153">蓝色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-153">Blue</span></span>  | <span data-ttu-id="c7ff5-154">一</span><span class="sxs-lookup"><span data-stu-id="c7ff5-154">M</span></span>    |
| <span data-ttu-id="c7ff5-155">黑色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-155">Black</span></span> | <span data-ttu-id="c7ff5-156">一</span><span class="sxs-lookup"><span data-stu-id="c7ff5-156">M</span></span>    |
| <span data-ttu-id="c7ff5-157">黑色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-157">Black</span></span> | <span data-ttu-id="c7ff5-158">L</span><span class="sxs-lookup"><span data-stu-id="c7ff5-158">L</span></span>    |
| <span data-ttu-id="c7ff5-159">黑色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-159">Black</span></span> | <span data-ttu-id="c7ff5-160">XL</span><span class="sxs-lookup"><span data-stu-id="c7ff5-160">XL</span></span>   |
| <span data-ttu-id="c7ff5-161">褐色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-161">Brown</span></span> | <span data-ttu-id="c7ff5-162">L</span><span class="sxs-lookup"><span data-stu-id="c7ff5-162">L</span></span>    |
| <span data-ttu-id="c7ff5-163">褐色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-163">Brown</span></span> | <span data-ttu-id="c7ff5-164">XL</span><span class="sxs-lookup"><span data-stu-id="c7ff5-164">XL</span></span>   |
| <span data-ttu-id="c7ff5-165">褐色</span><span class="sxs-lookup"><span data-stu-id="c7ff5-165">Brown</span></span> | <span data-ttu-id="c7ff5-166">XXL</span><span class="sxs-lookup"><span data-stu-id="c7ff5-166">XXL</span></span>  |

## <a name="the-version-product-dimension"></a><span data-ttu-id="c7ff5-167">版本产品维度</span><span class="sxs-lookup"><span data-stu-id="c7ff5-167">The version product dimension</span></span>

<span data-ttu-id="c7ff5-168">版本是用于帮助您维护和跟踪整个供应链中产品的多个版本的产品维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-168">Version is a product dimension that is intended to help you maintain and track multiple versions of a product throughout the supply chain.</span></span> <span data-ttu-id="c7ff5-169">对于在不断缩短的产品生命周期、质量和可靠性要求提高，以及对产品安全的关注增加的世界中经营业务的制造商，如果要取得成功，版本跟踪至关重要。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-169">Version tracking is essential to the success of manufacturers that operate in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and increased focus on product safety.</span></span>

<span data-ttu-id="c7ff5-170">作为标准产品维度，版本的行为类似于现有产品尺寸（尺寸、样式、颜色和配置）。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-170">As a standard product dimension, version will behave similarly to the existing product dimensions (size, style, color, and configuration).</span></span> <span data-ttu-id="c7ff5-171">因此，除了跟踪产品版本，您还可以将其用于其他目的。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-171">Therefore, you can use it for other purposes besides tracking product versions.</span></span>

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a><span data-ttu-id="c7ff5-172">打开版本维度</span><span class="sxs-lookup"><span data-stu-id="c7ff5-172">Turn on the version dimension</span></span>

#### <a name="before-you-turn-on-the-version-dimension"></a><span data-ttu-id="c7ff5-173">在打开版本维度之前</span><span class="sxs-lookup"><span data-stu-id="c7ff5-173">Before you turn on the version dimension</span></span>

<span data-ttu-id="c7ff5-174">当您打开版本维度时，如果您安装了向库存维度添加自定义的其他解决方案，某些功能可能会被破坏或无法按预期工作。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-174">When you turn on the version dimension, some functionality could become broken or stop working as expected if you've installed other solutions that add customizations to the inventory dimensions.</span></span> <span data-ttu-id="c7ff5-175">为了使版本维度正常工作，您可能必须更新这些解决方案，让它们在对库存维度的引用中包括版本维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-175">For the version dimension to be fully functional, you might have to update those solutions so that they include the version dimension in their references to the inventory dimensions.</span></span>

<span data-ttu-id="c7ff5-176">在测试解决方案与版本维度的兼容性时，请关注以下要素：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-176">When you're testing your solutions for compatibility with the version dimension, look for the following elements:</span></span>

1. <span data-ttu-id="c7ff5-177">**功能：** 最重要的是，必须评估涉及库存维度的所有自定义，以确保它们可以与版本维度一起使用。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-177">**Functionality:** Most importantly, any customizations that involve the inventory dimensions must be assessed to ensure that they can work in conjunction with the version dimension.</span></span>
1. <span data-ttu-id="c7ff5-178">**对库存维度的引用：** 注意对库存维度的引用（即明确引用尺寸的地方）。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-178">**References to the inventory dimensions:** Look out for references to the inventory dimensions (that is, places where the dimensions are explicitly referenced).</span></span> <span data-ttu-id="c7ff5-179">对 `InventDimId` 的引用应该是自动完成的，但是要注意对样式或颜色的引用。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-179">References to `InventDimId` should work out of the box, but look out for references to style or color.</span></span> <span data-ttu-id="c7ff5-180">例如，请确保检查以下要素：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-180">For example, be sure to check the following elements:</span></span>

    - <span data-ttu-id="c7ff5-181">扩展类中的 API 调用</span><span class="sxs-lookup"><span data-stu-id="c7ff5-181">API calls in extended classes</span></span>
    - <span data-ttu-id="c7ff5-182">扩展代码中对特定库存维度的所有引用（此代码必须将版本维度与样式、颜色和尺寸维度安排在一起。）</span><span class="sxs-lookup"><span data-stu-id="c7ff5-182">All references to specific inventory dimensions in extension code (This code must float the version dimension together with the style, color, and size dimensions.)</span></span>

1. <span data-ttu-id="c7ff5-183">**对过时 API 调用的引用：** 在引入版本维度时，Microsoft 已经尝试尽可能让更少的 API 过时。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-183">**References to obsolete API calls:** In its introduction of the version dimension, Microsoft has tried to make as few APIs as possible obsolete.</span></span> <span data-ttu-id="c7ff5-184">当您打开 **产品维度 - 版本** 配置键时，极少数已过时的 API 会发出警告。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-184">The few APIs that have been made obsolete will issue a warning when you turn on the **Product dimension - version** configuration key.</span></span> <span data-ttu-id="c7ff5-185">在生产系统中打开版本维度之前，必须在扩展解决方案中修复对这些 API 的调用。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-185">Calls to those API must be fixed in your extended solutions before you turn on the version dimension in a production system.</span></span> <span data-ttu-id="c7ff5-186">以下是特定于版本的过时 API：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-186">Here are the version-specific obsolete APIs:</span></span>

    - <span data-ttu-id="c7ff5-187">RetailTransactionServiceInventory::getProductRecordId</span><span class="sxs-lookup"><span data-stu-id="c7ff5-187">RetailTransactionServiceInventory::getProductRecordId</span></span>
    - <span data-ttu-id="c7ff5-188">EcoResProductNumberIdentifiedProductVariantEntity::find</span><span class="sxs-lookup"><span data-stu-id="c7ff5-188">EcoResProductNumberIdentifiedProductVariantEntity::find</span></span>
    - <span data-ttu-id="c7ff5-189">EGAISAlcoholProduction_RU::findByItemDim</span><span class="sxs-lookup"><span data-stu-id="c7ff5-189">EGAISAlcoholProduction_RU::findByItemDim</span></span>
    - <span data-ttu-id="c7ff5-190">PCVariantConfiguration::findByProductMasterAndDimensions</span><span class="sxs-lookup"><span data-stu-id="c7ff5-190">PCVariantConfiguration::findByProductMasterAndDimensions</span></span>

1. <span data-ttu-id="c7ff5-191">**地图：** 如果有任何地图使用库存维度，则必须更新这些地图的相应的关系映射，以使其包含版本维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-191">**Maps:** If any maps use the inventory dimensions, the corresponding relation mapping to these maps must be updated so that they include the version dimension.</span></span> <span data-ttu-id="c7ff5-192">在扩展模型或表扩展中，查找字段包含库存维度的表。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-192">In the extended model or table extensions, look out for tables where the fields include inventory dimensions.</span></span>
1. <span data-ttu-id="c7ff5-193">**Microsoft Dynamics 365 Commerce 功能：** 打开后，版本维度将出现在 Dynamics 365 Supply Chain Management 中特定于 Commerce 的代码中。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-193">**Microsoft Dynamics 365 Commerce functionality:** After it's turned on, the version dimension will appear throughout the Commerce-specific code in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c7ff5-194">但是，Commerce 渠道数据库、销售点 (POS) 或电子商务应用程序尚不支持版本维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-194">However, the version dimension isn't yet supported by the Commerce channel database or in the Point of Sale (POS) or e-Commerce applications.</span></span> <span data-ttu-id="c7ff5-195">这些特定于 Commerce 的应用程序将不支持用户按版本维度销售/装运或退回/接收库存。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-195">These Commerce-specific applications won't support users selling/shipping or returning/receiving inventory by version dimension.</span></span> <span data-ttu-id="c7ff5-196">库存可用性查询功能不会在 Commerce 应用中按版本维度识别库存。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-196">Inventory availability lookup functions won't discern inventory by version dimension in Commerce apps.</span></span> <span data-ttu-id="c7ff5-197">此行为类似于当前整个 Commerce 中的配置维度的行为。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-197">This behavior resembles the current behavior of the config dimension throughout Commerce.</span></span>

#### <a name="turn-on-the-version-dimension"></a><span data-ttu-id="c7ff5-198">打开版本维度</span><span class="sxs-lookup"><span data-stu-id="c7ff5-198">Turn on the version dimension</span></span>

<span data-ttu-id="c7ff5-199">版本维度只有在系统中打开之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-199">Before you can use the version dimension, it must be turned on in your system.</span></span> <span data-ttu-id="c7ff5-200">此任务需要管理员权限。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-200">This task requires admin permissions.</span></span>

1. <span data-ttu-id="c7ff5-201">转到 **系统管理 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-201">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="c7ff5-202">打开名为 *产品维度版本* 的功能。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-202">Turn on the feature that is named *Product dimension version*.</span></span> <span data-ttu-id="c7ff5-203">（有关详细信息，请参阅[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。）</span><span class="sxs-lookup"><span data-stu-id="c7ff5-203">(For more information, see [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)</span></span>
1. <span data-ttu-id="c7ff5-204">将您的系统设置为[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-204">Put your system into [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="c7ff5-205">转到 **系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-205">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="c7ff5-206">在 **配置键** 选项卡上，展开 **贸易**，选中 **产品维度 - 版本** 的复选框。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-206">On the **Configuration keys** tab, expand **Trade**, and select the check box for **Product dimension - version**.</span></span>
1. <span data-ttu-id="c7ff5-207">关闭[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-207">Turn off [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="areas-where-the-version-dimension-isnt-supported"></a><span data-ttu-id="c7ff5-208">版本维度不受支持的区域</span><span class="sxs-lookup"><span data-stu-id="c7ff5-208">Areas where the version dimension isn't supported</span></span>

<span data-ttu-id="c7ff5-209">以下区域不支持版本维度（您仍然可以使用这些区域，但无法向其中添加版本化产品(使用版本维度的产品)）。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-209">The following areas don't support the version dimension (you can still use these areas but you won't be able to add versioned products (products where the version dimension is used) to them).</span></span> <span data-ttu-id="c7ff5-210">例如，您不能将版本化物料添加到供应商目录。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-210">For example, you can't add a versioned item to a vendor catalog.</span></span> <span data-ttu-id="c7ff5-211">这是因为将使用版本维度的产品添加到这些区域会导致中断性变更。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-211">This is because adding products with the version dimension to these areas would cause breaking changes.</span></span>

- <span data-ttu-id="c7ff5-212">成本对象月报表</span><span class="sxs-lookup"><span data-stu-id="c7ff5-212">Cost object monthly statement</span></span>
- <span data-ttu-id="c7ff5-213">成本对象报表缓存</span><span class="sxs-lookup"><span data-stu-id="c7ff5-213">Cost object statement cache</span></span>
- <span data-ttu-id="c7ff5-214">按物料划分的 MCR 销售统计信息</span><span class="sxs-lookup"><span data-stu-id="c7ff5-214">MCR sales statistics per item</span></span>
- <span data-ttu-id="c7ff5-215">供应商目录</span><span class="sxs-lookup"><span data-stu-id="c7ff5-215">Vendor catalogs</span></span>
- <span data-ttu-id="c7ff5-216">EcoResProductDimensionGroupEntity</span><span class="sxs-lookup"><span data-stu-id="c7ff5-216">EcoResProductDimensionGroupEntity</span></span>

<span data-ttu-id="c7ff5-217">此外，Commerce 中的订单创建和订单处理功能（例如，POS、呼叫中心和电子商务订单）也不支持版本维度。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-217">In addition, the order creation and order processing features in Commerce (for example, for POS, call center, and e-commerce orders) don't support the version dimension.</span></span> <span data-ttu-id="c7ff5-218">对于何时增强 Commerce 订单以支持版本维度没有确定的时间线。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-218">There is no confirmed timeline as to when Commerce orders will be enhanced to support it.</span></span>

### <a name="functional-characteristics-of-the-version-dimension"></a><span data-ttu-id="c7ff5-219">版本维度的功能特征</span><span class="sxs-lookup"><span data-stu-id="c7ff5-219">Functional characteristics of the version dimension</span></span>

<span data-ttu-id="c7ff5-220">版本维度的工作方式与其他产品维度相同。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-220">The version dimension works like the other product dimensions.</span></span> <span data-ttu-id="c7ff5-221">但是，由于特定的性质，并且由于目的是维护和跟踪产品的多个版本，因此它的行为略有不同。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-221">However, because of its specific nature, and because it's intended to maintain and track multiple versions of a product, it behaves slightly differently.</span></span> <span data-ttu-id="c7ff5-222">以下是一些异同点：</span><span class="sxs-lookup"><span data-stu-id="c7ff5-222">Here are some of the differences and similarities:</span></span>

- <span data-ttu-id="c7ff5-223">**没有版本组。**</span><span class="sxs-lookup"><span data-stu-id="c7ff5-223">**There is no version group.**</span></span>

    <span data-ttu-id="c7ff5-224">虽然尺寸、颜色和样式（颜色组、尺寸组和样式组）存在组概念，但是不存在版本组概念。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-224">Although the concept of groups exists for size, color, and style (color group, size group, and style group), no version group concept exists.</span></span> <span data-ttu-id="c7ff5-225">通过组，您可以预定义适用的值，以比如在为产品分配颜色组时，产品可以使用该颜色组中的所有颜色。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-225">Groups let you predefine the applicable values so that when, for example, you assign a color group to a product, the product can use all the colors in that color group.</span></span> <span data-ttu-id="c7ff5-226">此概念不适用于版本维度，因为产品采用的版本不是在创建产品时预定义的。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-226">This concept doesn't apply to the version dimension, because the versions that a product takes aren't predefined when the product is created.</span></span> <span data-ttu-id="c7ff5-227">而是根据需要在产品的生命周期内创建的。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-227">Instead, versions are created during the lifecycle of the product, as they are required.</span></span> <span data-ttu-id="c7ff5-228">通常，如果产品的形式、适合度和功能保持不变，将创建新版本而不是新产品。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-228">Typically, if the form, fit, and function of the product remain the same, you create a new version instead of a new product.</span></span>

- <span data-ttu-id="c7ff5-229">**产品变型建议的工作方式与目前相同。**</span><span class="sxs-lookup"><span data-stu-id="c7ff5-229">**Product variant suggestions work as they currently do.**</span></span>

    <span data-ttu-id="c7ff5-230">产品变型建议将为所有版本维度值创建建议，就像为其他维度创建建议一样。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-230">Product variant suggestions will create suggestions for all version dimension values, just as they do for other dimensions.</span></span> <span data-ttu-id="c7ff5-231">创建和发布版本化产品的流程与使用其他维度的产品相同。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-231">The process of creating and releasing versioned products is the same as it is for products that use other dimensions.</span></span> <span data-ttu-id="c7ff5-232">当您创建版本化产品时，第一个版本 (V1) 将创建为产品维度，并会发布变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-232">When you create a versioned product, the first version (V1) will be created as a product dimension, and the variants will be released.</span></span> <span data-ttu-id="c7ff5-233">当产品更改，需要新版本时，将增加新版本值 (V2)，并发布所需的变型。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-233">As the product changes and a new version is needed, the new version value (V2) will be added, and the required variants will be released.</span></span> <span data-ttu-id="c7ff5-234">预期不会为产品预先创建所有版本（V1、V2 和 V3）。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-234">There is no expectation  that all the versions (V1, V2, and V3) will be created in advance for the product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7ff5-235">如果您打开并使用版本维度，某些引用库存维度的解决方案可能会如预期的停止工作。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-235">If you turn on and use the version dimension, some solutions that reference the inventory dimensions might stop working as expected.</span></span> <span data-ttu-id="c7ff5-236">要确认并解决这些问题，请与独立软件供应商 (ISV) 联系，告知受影响的解决方案。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-236">To confirm and fix these issues, contact the independent software vendor (ISV) for your affected solutions.</span></span> <span data-ttu-id="c7ff5-237">有关详细信息，请参阅[启用版本维度](#enable-version-dim)。</span><span class="sxs-lookup"><span data-stu-id="c7ff5-237">For more information, see [Enable the version dimension](#enable-version-dim).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]