--- 
title: "创建预定义的产品变型"
description: "此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="447dd-103">创建预定义的产品变型</span><span class="sxs-lookup"><span data-stu-id="447dd-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="447dd-104">此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。</span><span class="sxs-lookup"><span data-stu-id="447dd-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="447dd-105">创建此过程使用的演示数据公司为 USMF。</span><span class="sxs-lookup"><span data-stu-id="447dd-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="447dd-106">创建基础产品</span><span class="sxs-lookup"><span data-stu-id="447dd-106">Create a product master</span></span>
1. <span data-ttu-id="447dd-107">转到“产品信息管理”>“产品”>“基础产品”。</span><span class="sxs-lookup"><span data-stu-id="447dd-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="447dd-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-108">Click New.</span></span>
3. <span data-ttu-id="447dd-109">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="447dd-110">如果尚未针对产品编号字段设置任何编号规则，则不需要手动输入产品编号。</span><span class="sxs-lookup"><span data-stu-id="447dd-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="447dd-111">换言之，如果已为该字段设置了编号规则，则跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="447dd-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="447dd-112">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="447dd-113">在“产品维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="447dd-114">选择产品维度组 SizeCol（尺寸和颜色）。</span><span class="sxs-lookup"><span data-stu-id="447dd-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="447dd-115">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="447dd-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="447dd-116">添加产品维度</span><span class="sxs-lookup"><span data-stu-id="447dd-116">Add product dimensions</span></span>
1. <span data-ttu-id="447dd-117">单击“产品维度”。</span><span class="sxs-lookup"><span data-stu-id="447dd-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="447dd-118">此示例显示如何手动输入产品维度。</span><span class="sxs-lookup"><span data-stu-id="447dd-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="447dd-119">您还可以选择选择包括您要使用的产品维度值的尺寸、颜色或样式组。</span><span class="sxs-lookup"><span data-stu-id="447dd-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="447dd-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-120">Click New.</span></span>
3. <span data-ttu-id="447dd-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="447dd-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="447dd-122">在“尺寸”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="447dd-123">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="447dd-124">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-124">Click New.</span></span>
7. <span data-ttu-id="447dd-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="447dd-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="447dd-126">在“尺寸”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="447dd-127">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="447dd-128">单击“颜色”选项卡。</span><span class="sxs-lookup"><span data-stu-id="447dd-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="447dd-129">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-129">Click New.</span></span>
12. <span data-ttu-id="447dd-130">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="447dd-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="447dd-131">在“颜色”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="447dd-132">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="447dd-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-133">Click New.</span></span>
16. <span data-ttu-id="447dd-134">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="447dd-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="447dd-135">在“颜色”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="447dd-136">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="447dd-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="447dd-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="447dd-137">Click Save.</span></span>
20. <span data-ttu-id="447dd-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="447dd-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="447dd-139">生成产品变型</span><span class="sxs-lookup"><span data-stu-id="447dd-139">Generate product variants</span></span>
1. <span data-ttu-id="447dd-140">单击“产品变型”。</span><span class="sxs-lookup"><span data-stu-id="447dd-140">Click Product variants.</span></span>
2. <span data-ttu-id="447dd-141">单击“变型建议”。</span><span class="sxs-lookup"><span data-stu-id="447dd-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="447dd-142">单击“选择全部”。</span><span class="sxs-lookup"><span data-stu-id="447dd-142">Click Select all.</span></span>
    * <span data-ttu-id="447dd-143">在此示例中，选择所有可能的变型。</span><span class="sxs-lookup"><span data-stu-id="447dd-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="447dd-144">如果仅可能的产品维度组合的子集将用于创建变型，则您可以选择单个条目。</span><span class="sxs-lookup"><span data-stu-id="447dd-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="447dd-145">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="447dd-145">Click Create.</span></span>
    * <span data-ttu-id="447dd-146">您可以基于产品维度值的组合生成所有变型的描述。</span><span class="sxs-lookup"><span data-stu-id="447dd-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="447dd-147">描述是可选的。</span><span class="sxs-lookup"><span data-stu-id="447dd-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="447dd-148">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="447dd-148">Click Save.</span></span>


