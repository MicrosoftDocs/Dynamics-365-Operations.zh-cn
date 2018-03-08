---
title: "产品变型编号和名称的命名法"
description: "此主题介绍如何设置产品编号命名法来替换固定的[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式] 格式。"
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 6a620f2a0105d578d419d3aac816c7d78fbf3e46
ms.contentlocale: zh-cn
ms.lasthandoff: 03/07/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="a9e76-103">产品变型编号和名称的命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-103">Nomenclature of product variant numbers and names</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a9e76-104">此主题介绍如何设置产品编号命名法来替换固定的[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式] 格式。</span><span class="sxs-lookup"><span data-stu-id="a9e76-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="a9e76-105">新的命名法具有目标格式，包括您选择的基础产品编号、有效产品维度和文本分隔符。</span><span class="sxs-lookup"><span data-stu-id="a9e76-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="a9e76-106">您还可以创建产品名称的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="a9e76-107">最后，您可以构建命名法以识别由基于约束的产品配置器创建的配置。</span><span class="sxs-lookup"><span data-stu-id="a9e76-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="a9e76-108">这些命名法可包含您选择的属性。</span><span class="sxs-lookup"><span data-stu-id="a9e76-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="a9e76-109">产品变型编号和产品变型名称的命名法让您可以在产品变型的标识符中包含细分信息。</span><span class="sxs-lookup"><span data-stu-id="a9e76-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="a9e76-110">这些细分信息可能包括基础产品编号和名称、产品维度 ID 和名称、编号规则、文本常量和属性。</span><span class="sxs-lookup"><span data-stu-id="a9e76-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="a9e76-111">在您创建销售订单或采购订单时，此功能可以快速查找特定产品变型。</span><span class="sxs-lookup"><span data-stu-id="a9e76-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="a9e76-112">通过使用**产品命名法**页，您创建产品变型编号和产品变型名称的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="a9e76-113">若要打开此页，单击**产品信息管理** &gt; **设置**。</span><span class="sxs-lookup"><span data-stu-id="a9e76-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="a9e76-114">预定义产品变型命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="a9e76-115">根据以下三种配置技术的其中一种生成基础产品的产品变型：</span><span class="sxs-lookup"><span data-stu-id="a9e76-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="a9e76-116">预定义的变型</span><span class="sxs-lookup"><span data-stu-id="a9e76-116">Predefined variants</span></span>
-   <span data-ttu-id="a9e76-117">基于约束</span><span class="sxs-lookup"><span data-stu-id="a9e76-117">Constraint-based</span></span>
-   <span data-ttu-id="a9e76-118">基于维度</span><span class="sxs-lookup"><span data-stu-id="a9e76-118">Dimension-based</span></span>

<span data-ttu-id="a9e76-119">每个产品变型都有一个编号和名称，且产品变型标识命名法允许您选择每个产品变型编号或名称中要使用的细分信息。</span><span class="sxs-lookup"><span data-stu-id="a9e76-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="a9e76-120">您可以选择以下**产品命名法**页面上的细分信息：</span><span class="sxs-lookup"><span data-stu-id="a9e76-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a9e76-121">基础产品编号</span><span class="sxs-lookup"><span data-stu-id="a9e76-121">Product master number</span></span>
-   <span data-ttu-id="a9e76-122">基础产品名称</span><span class="sxs-lookup"><span data-stu-id="a9e76-122">Product master name</span></span>
-   <span data-ttu-id="a9e76-123">编号规则值</span><span class="sxs-lookup"><span data-stu-id="a9e76-123">Number sequence value</span></span>
-   <span data-ttu-id="a9e76-124">文本常量</span><span class="sxs-lookup"><span data-stu-id="a9e76-124">Text constant</span></span>
-   <span data-ttu-id="a9e76-125">产品维度</span><span class="sxs-lookup"><span data-stu-id="a9e76-125">Product dimensions</span></span>
    -   <span data-ttu-id="a9e76-126">配置 ID 或名称</span><span class="sxs-lookup"><span data-stu-id="a9e76-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="a9e76-127">颜色 ID 或名称</span><span class="sxs-lookup"><span data-stu-id="a9e76-127">Color ID or name</span></span>
    -   <span data-ttu-id="a9e76-128">尺寸 ID 或名称</span><span class="sxs-lookup"><span data-stu-id="a9e76-128">Size ID or name</span></span>
    -   <span data-ttu-id="a9e76-129">样式 ID 或名称</span><span class="sxs-lookup"><span data-stu-id="a9e76-129">Style ID or name</span></span>

<span data-ttu-id="a9e76-130">定义产品变型标识编号命名法后，您可将其与产品维度组关联。</span><span class="sxs-lookup"><span data-stu-id="a9e76-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="a9e76-131">随后将根据命名法为引用此产品维度组的所有基础产品分配产品变型编号。</span><span class="sxs-lookup"><span data-stu-id="a9e76-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="a9e76-132">但是，产品变型名称命名法不能与产品维度组关联。</span><span class="sxs-lookup"><span data-stu-id="a9e76-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="a9e76-133">您还可以将产品变型标识命名法直接分配给基础产品。</span><span class="sxs-lookup"><span data-stu-id="a9e76-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="a9e76-134">在这种情况下，将根据命名法为属于该基础产品的产品变型分配产品变型编号和名称。</span><span class="sxs-lookup"><span data-stu-id="a9e76-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="a9e76-135">示例</span><span class="sxs-lookup"><span data-stu-id="a9e76-135">Example</span></span>

<span data-ttu-id="a9e76-136">T 恤衫 (TS1234) 生产为三个尺寸（S、M、L）、四种颜色（红色、绿色、蓝色、黄色）和两种款式（Polo、V）。</span><span class="sxs-lookup"><span data-stu-id="a9e76-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="a9e76-137">因此，可能有 24 个产品变型 (= 3 × 4 × 2)。</span><span class="sxs-lookup"><span data-stu-id="a9e76-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="a9e76-138">您创建具有以下细分信息的产品变型编号命名法：</span><span class="sxs-lookup"><span data-stu-id="a9e76-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a9e76-139">基础产品编号</span><span class="sxs-lookup"><span data-stu-id="a9e76-139">Product master number</span></span>
2.  <span data-ttu-id="a9e76-140">文本常量："-"</span><span class="sxs-lookup"><span data-stu-id="a9e76-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="a9e76-141">颜色</span><span class="sxs-lookup"><span data-stu-id="a9e76-141">Color</span></span>
4.  <span data-ttu-id="a9e76-142">文本常量："-"</span><span class="sxs-lookup"><span data-stu-id="a9e76-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="a9e76-143">尺寸</span><span class="sxs-lookup"><span data-stu-id="a9e76-143">Size</span></span>
6.  <span data-ttu-id="a9e76-144">文本常量："-"</span><span class="sxs-lookup"><span data-stu-id="a9e76-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="a9e76-145">样式</span><span class="sxs-lookup"><span data-stu-id="a9e76-145">Style</span></span>

<span data-ttu-id="a9e76-146">在这种情况下，红色小码 Polo T 恤衫的产品变型编号为 TS1234-Red-Small-Polo。</span><span class="sxs-lookup"><span data-stu-id="a9e76-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="a9e76-147">基于约束的配置命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="a9e76-148">对于基于约束的配置，您可以为配置产品维度构建专门的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="a9e76-149">您可以选择以下**产品命名法**页面上的细分信息：</span><span class="sxs-lookup"><span data-stu-id="a9e76-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a9e76-150">编号规则值</span><span class="sxs-lookup"><span data-stu-id="a9e76-150">Number sequence value</span></span>
-   <span data-ttu-id="a9e76-151">文本常量</span><span class="sxs-lookup"><span data-stu-id="a9e76-151">Text constant</span></span>
-   <span data-ttu-id="a9e76-152">属性值</span><span class="sxs-lookup"><span data-stu-id="a9e76-152">Attribute value</span></span>

<span data-ttu-id="a9e76-153">产品模型配置中的每个组件都可以有自己的配置命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="a9e76-154">仅可使用属于此组件的属性。</span><span class="sxs-lookup"><span data-stu-id="a9e76-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="a9e76-155">子组件或用户要求的属性不能使用。</span><span class="sxs-lookup"><span data-stu-id="a9e76-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="a9e76-156">示例</span><span class="sxs-lookup"><span data-stu-id="a9e76-156">Example</span></span>

<span data-ttu-id="a9e76-157">产品配置模型有具有两个属性的根组件：</span><span class="sxs-lookup"><span data-stu-id="a9e76-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="a9e76-158">材料（塑料，木头，钢）</span><span class="sxs-lookup"><span data-stu-id="a9e76-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="a9e76-159">长度 (10…100)</span><span class="sxs-lookup"><span data-stu-id="a9e76-159">Length (10...100)</span></span>

<span data-ttu-id="a9e76-160">您创建具有以下细分信息的配置命名法：</span><span class="sxs-lookup"><span data-stu-id="a9e76-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a9e76-161">属性值：材料</span><span class="sxs-lookup"><span data-stu-id="a9e76-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="a9e76-162">文本常量："AAA"</span><span class="sxs-lookup"><span data-stu-id="a9e76-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="a9e76-163">属性值：长度</span><span class="sxs-lookup"><span data-stu-id="a9e76-163">Attribute value: Length</span></span>

<span data-ttu-id="a9e76-164">在这种情况下，长度为 78 的木质材料的配置 ID 将是 WoodAAA78。</span><span class="sxs-lookup"><span data-stu-id="a9e76-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="a9e76-165">基于维度的配置命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="a9e76-166">对于基于维度的配置，您可以为配置产品维度构建专门的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="a9e76-167">您可以选择以下**产品命名法**页面上的细分信息：</span><span class="sxs-lookup"><span data-stu-id="a9e76-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a9e76-168">编号规则值</span><span class="sxs-lookup"><span data-stu-id="a9e76-168">Number sequence value</span></span>
-   <span data-ttu-id="a9e76-169">文本常量</span><span class="sxs-lookup"><span data-stu-id="a9e76-169">Text constant</span></span>
-   <span data-ttu-id="a9e76-170">配置组项</span><span class="sxs-lookup"><span data-stu-id="a9e76-170">Configuration group item</span></span>

<span data-ttu-id="a9e76-171">您可以为物料清单 (BOM) 定义配置命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="a9e76-172">示例</span><span class="sxs-lookup"><span data-stu-id="a9e76-172">Example</span></span>

<span data-ttu-id="a9e76-173">物料清单具有可分为两个配置组的四个物料清单行：</span><span class="sxs-lookup"><span data-stu-id="a9e76-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="a9e76-174">物料清单行：M0007，标准机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="a9e76-175">配置组：机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="a9e76-176">物料清单行：M0008，高端机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="a9e76-177">配置组：机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="a9e76-178">物料清单行：M0021，前格栅布料</span><span class="sxs-lookup"><span data-stu-id="a9e76-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="a9e76-179">配置组：前格栅</span><span class="sxs-lookup"><span data-stu-id="a9e76-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="a9e76-180">物料清单行：M0022，前格栅金属</span><span class="sxs-lookup"><span data-stu-id="a9e76-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="a9e76-181">配置组：前格栅</span><span class="sxs-lookup"><span data-stu-id="a9e76-181">Configuration group: Front grill</span></span>

<span data-ttu-id="a9e76-182">您创建具有以下细分信息的配置命名法：</span><span class="sxs-lookup"><span data-stu-id="a9e76-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a9e76-183">配置组：机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="a9e76-184">文本常量："&"</span><span class="sxs-lookup"><span data-stu-id="a9e76-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="a9e76-185">配置组：前格栅</span><span class="sxs-lookup"><span data-stu-id="a9e76-185">Configuration group: Front grill</span></span>

<span data-ttu-id="a9e76-186">在这种情况下，具有布料前格栅的标准机柜的配置 ID 将为 M0007&M0021。</span><span class="sxs-lookup"><span data-stu-id="a9e76-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="a9e76-187">产品变型和配置组合的命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="a9e76-188">使用基于约束的配置技术或基于维度的配置技术配置基础产品的产品变型时，产品变型的产品变型编号可以包括来自配置维度的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="a9e76-189">请执行以下步骤配置变型。</span><span class="sxs-lookup"><span data-stu-id="a9e76-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="a9e76-190">在**产品命名法**页面上，定义包括配置维度的产品变型编号命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="a9e76-191">将此命名法分配给具有配置维度的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="a9e76-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="a9e76-192">定义要用于配置产品变型的组件或物料清单的配置命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="a9e76-193">您还可以创建产品变型名称的命名法。</span><span class="sxs-lookup"><span data-stu-id="a9e76-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="a9e76-194">产品变型名称可以配置为包括配置 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="a9e76-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="a9e76-195">基于约束的配置示例</span><span class="sxs-lookup"><span data-stu-id="a9e76-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="a9e76-196">对于此示例，您使用包括以下细分信息的产品变型编号命名法：</span><span class="sxs-lookup"><span data-stu-id="a9e76-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="a9e76-197">基础产品编号</span><span class="sxs-lookup"><span data-stu-id="a9e76-197">Product master number</span></span>
2.  <span data-ttu-id="a9e76-198">文本常量 "\_"</span><span class="sxs-lookup"><span data-stu-id="a9e76-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="a9e76-199">配置</span><span class="sxs-lookup"><span data-stu-id="a9e76-199">Configuration</span></span>

<span data-ttu-id="a9e76-200">配置命名法由以下细分信息组成：</span><span class="sxs-lookup"><span data-stu-id="a9e76-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="a9e76-201">属性值：材料</span><span class="sxs-lookup"><span data-stu-id="a9e76-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="a9e76-202">文本常量："AAA"</span><span class="sxs-lookup"><span data-stu-id="a9e76-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="a9e76-203">属性值：长度</span><span class="sxs-lookup"><span data-stu-id="a9e76-203">Attribute value: Length</span></span>

<span data-ttu-id="a9e76-204">您输入以下细分信息的值：</span><span class="sxs-lookup"><span data-stu-id="a9e76-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="a9e76-205">基础产品编号 = **M0099**</span><span class="sxs-lookup"><span data-stu-id="a9e76-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="a9e76-206">材料 = **塑料**</span><span class="sxs-lookup"><span data-stu-id="a9e76-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="a9e76-207">长度 = **12**</span><span class="sxs-lookup"><span data-stu-id="a9e76-207">Length = **12**</span></span>

<span data-ttu-id="a9e76-208">在这种情况下，产品变型编号将为 M0099\_PlasticAAA12。</span><span class="sxs-lookup"><span data-stu-id="a9e76-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="a9e76-209">基于维度的配置示例</span><span class="sxs-lookup"><span data-stu-id="a9e76-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="a9e76-210">对于此示例，您使用包括以下细分信息的产品变型编号命名法：</span><span class="sxs-lookup"><span data-stu-id="a9e76-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="a9e76-211">基础产品编号</span><span class="sxs-lookup"><span data-stu-id="a9e76-211">Product master number</span></span>
2.  <span data-ttu-id="a9e76-212">文本常量 "//"</span><span class="sxs-lookup"><span data-stu-id="a9e76-212">Text constant "//"</span></span>
3.  <span data-ttu-id="a9e76-213">配置</span><span class="sxs-lookup"><span data-stu-id="a9e76-213">Configuration</span></span>

<span data-ttu-id="a9e76-214">配置命名法由以下细分信息组成：</span><span class="sxs-lookup"><span data-stu-id="a9e76-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="a9e76-215">配置组：机柜</span><span class="sxs-lookup"><span data-stu-id="a9e76-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="a9e76-216">文本常量："&"</span><span class="sxs-lookup"><span data-stu-id="a9e76-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="a9e76-217">配置组：前格栅</span><span class="sxs-lookup"><span data-stu-id="a9e76-217">Configuration group: Front grill</span></span>

<span data-ttu-id="a9e76-218">您输入以下细分信息的值：</span><span class="sxs-lookup"><span data-stu-id="a9e76-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="a9e76-219">基础产品编号 = **D0123**</span><span class="sxs-lookup"><span data-stu-id="a9e76-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="a9e76-220">机柜 = **M0008**</span><span class="sxs-lookup"><span data-stu-id="a9e76-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="a9e76-221">前格栅 = **M0022**</span><span class="sxs-lookup"><span data-stu-id="a9e76-221">Front grill = **M0022**</span></span>

<span data-ttu-id="a9e76-222">在这种情况下，产品变型编号将为 D0123//M0008&M0022。</span><span class="sxs-lookup"><span data-stu-id="a9e76-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="a9e76-223">编号冲突</span><span class="sxs-lookup"><span data-stu-id="a9e76-223">Numbering conflicts</span></span>
<span data-ttu-id="a9e76-224">在有些情况下，设置的产品变型编号命名法可能不会产生唯一的产品变型编号。</span><span class="sxs-lookup"><span data-stu-id="a9e76-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="a9e76-225">例如，如果一个有效的产品维度不包括在使用预定义的变型配置技术的基础产品的命名法中，产品变型编号则可能不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a9e76-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="a9e76-226">您处理冲突的方法因配置技术而异。</span><span class="sxs-lookup"><span data-stu-id="a9e76-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="a9e76-227">预定义的变型</span><span class="sxs-lookup"><span data-stu-id="a9e76-227">Predefined variants</span></span>

<span data-ttu-id="a9e76-228">如果您试图手动创建或自动生成产品变型，且多个产品变型末尾为相同的产品变型编号，则将发生错误。</span><span class="sxs-lookup"><span data-stu-id="a9e76-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="a9e76-229">若要避免此情况，应在产品维度组中使用所有活动产品维度。</span><span class="sxs-lookup"><span data-stu-id="a9e76-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="a9e76-230">或者，包括编号规则以帮助保证产品变型编号是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a9e76-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="a9e76-231">基于约束的配置</span><span class="sxs-lookup"><span data-stu-id="a9e76-231">Constraint-based configurations</span></span>

<span data-ttu-id="a9e76-232">根据命名法，系统可能尝试为配置分配一个非唯一的产品变型编号。</span><span class="sxs-lookup"><span data-stu-id="a9e76-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="a9e76-233">在这种情况下，系统将使用配置维度的编号规则作为产品变型编号，您将收到警告。</span><span class="sxs-lookup"><span data-stu-id="a9e76-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="a9e76-234">若要避免此情况，您应在命名法中包括足够的属性以帮助保证唯一的产品变型编号。</span><span class="sxs-lookup"><span data-stu-id="a9e76-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="a9e76-235">您还应确保为此组件启用**重复使用**选项。</span><span class="sxs-lookup"><span data-stu-id="a9e76-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="a9e76-236">基于维度的配置</span><span class="sxs-lookup"><span data-stu-id="a9e76-236">Dimension-based configurations</span></span>

<span data-ttu-id="a9e76-237">在配置流程的一个步骤中，系统将根据命名法建议一个配置值。</span><span class="sxs-lookup"><span data-stu-id="a9e76-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="a9e76-238">在此步骤中，您可以手动更改配置值。</span><span class="sxs-lookup"><span data-stu-id="a9e76-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="a9e76-239">当您保存配置时，系统将确认配置值是否唯一。</span><span class="sxs-lookup"><span data-stu-id="a9e76-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="a9e76-240">如果您输入的值不是唯一的，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="a9e76-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="a9e76-241">若要保存配置，您必须输入唯一配置值。</span><span class="sxs-lookup"><span data-stu-id="a9e76-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="a9e76-242">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9e76-242">See also</span></span>
--------

[<span data-ttu-id="a9e76-243">为预定义的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="a9e76-244">为配置的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="a9e76-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


