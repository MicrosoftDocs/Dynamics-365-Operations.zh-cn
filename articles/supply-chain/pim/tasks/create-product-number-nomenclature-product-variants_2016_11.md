---
title: 为配置的产品变型创建产品编号命名法
description: 此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6970b37594bc999f8f1ea112a6056f15faccc02c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213232"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="0d77f-103">为配置的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0d77f-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d77f-104">此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。</span><span class="sxs-lookup"><span data-stu-id="0d77f-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="0d77f-105">此过程还演示如何为产品配置模型组件构建配置命名法。</span><span class="sxs-lookup"><span data-stu-id="0d77f-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="0d77f-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0d77f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0d77f-107">为基础产品 D0004 分配了新的产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="0d77f-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="0d77f-108">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="0d77f-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="0d77f-109">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0d77f-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="0d77f-110">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="0d77f-111">单击“产品命名法”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="0d77f-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-112">Click New.</span></span>
4. <span data-ttu-id="0d77f-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0d77f-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0d77f-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-115">Click Add.</span></span>
7. <span data-ttu-id="0d77f-116">单击“基础产品编号”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-116">Click Product master number.</span></span>
8. <span data-ttu-id="0d77f-117">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-117">Click Add.</span></span>
9. <span data-ttu-id="0d77f-118">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-118">Click Text constant.</span></span>
10. <span data-ttu-id="0d77f-119">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0d77f-120">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="0d77f-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-121">Click Add.</span></span>
13. <span data-ttu-id="0d77f-122">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-122">Click Configuration.</span></span>
14. <span data-ttu-id="0d77f-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="0d77f-124">为基础产品分配产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0d77f-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="0d77f-125">单击“基础产品”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-125">Click Product masters.</span></span>
2. <span data-ttu-id="0d77f-126">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="0d77f-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0d77f-127">例如，使用值“D”在“产品编号”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="0d77f-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="0d77f-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0d77f-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0d77f-129">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-129">Click Edit.</span></span>
5. <span data-ttu-id="0d77f-130">在“使用命名法”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="0d77f-131">在“产品变型编号命名法”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="0d77f-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-132">Close the page.</span></span>
8. <span data-ttu-id="0d77f-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="0d77f-134">为产品配置模型组件创建命名法</span><span class="sxs-lookup"><span data-stu-id="0d77f-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="0d77f-135">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="0d77f-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0d77f-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0d77f-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0d77f-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0d77f-138">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-138">Click Edit.</span></span>
5. <span data-ttu-id="0d77f-139">在“使用配置命名法”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="0d77f-140">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-140">Click Add.</span></span>
7. <span data-ttu-id="0d77f-141">单击“属性值”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-141">Click Attribute value.</span></span>
8. <span data-ttu-id="0d77f-142">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0d77f-143">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="0d77f-144">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-144">Click Add.</span></span>
11. <span data-ttu-id="0d77f-145">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-145">Click Text constant.</span></span>
12. <span data-ttu-id="0d77f-146">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0d77f-147">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="0d77f-148">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-148">Click Add.</span></span>
15. <span data-ttu-id="0d77f-149">单击“属性值”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-149">Click Attribute value.</span></span>
16. <span data-ttu-id="0d77f-150">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="0d77f-151">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="0d77f-152">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-152">Click Add.</span></span>
19. <span data-ttu-id="0d77f-153">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-153">Click Text constant.</span></span>
20. <span data-ttu-id="0d77f-154">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="0d77f-155">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="0d77f-156">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-156">Click Add.</span></span>
23. <span data-ttu-id="0d77f-157">单击“属性值”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-157">Click Attribute value.</span></span>
24. <span data-ttu-id="0d77f-158">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="0d77f-159">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="0d77f-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-160">Click Add.</span></span>
27. <span data-ttu-id="0d77f-161">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-161">Click Text constant.</span></span>
28. <span data-ttu-id="0d77f-162">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="0d77f-163">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="0d77f-164">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-164">Click Add.</span></span>
31. <span data-ttu-id="0d77f-165">单击“属性值”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-165">Click Attribute value.</span></span>
32. <span data-ttu-id="0d77f-166">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="0d77f-167">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="0d77f-168">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-168">Click Add.</span></span>
35. <span data-ttu-id="0d77f-169">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-169">Click Text constant.</span></span>
36. <span data-ttu-id="0d77f-170">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="0d77f-171">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="0d77f-172">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-172">Click Add.</span></span>
39. <span data-ttu-id="0d77f-173">单击“编号规则值”。</span><span class="sxs-lookup"><span data-stu-id="0d77f-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="0d77f-174">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0d77f-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="0d77f-175">在“编号规则”字段中，输入或选一个值。</span><span class="sxs-lookup"><span data-stu-id="0d77f-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="0d77f-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-176">Close the page.</span></span>
43. <span data-ttu-id="0d77f-177">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-177">Close the page.</span></span>
44. <span data-ttu-id="0d77f-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0d77f-178">Close the page.</span></span>

