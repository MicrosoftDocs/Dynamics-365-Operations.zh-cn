--- 
title: "创建产品配置模型"
description: "该过程显示如何创建产品配置模型和输入基础信息，如属性和子组件。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4c5012ac05db7fc8769afa54115b203623809c9f
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="4b20f-103">创建产品配置模型</span><span class="sxs-lookup"><span data-stu-id="4b20f-103">Create a product configuration model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b20f-104">该过程显示如何创建产品配置模型和输入基础信息，如属性和子组件。</span><span class="sxs-lookup"><span data-stu-id="4b20f-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="4b20f-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="4b20f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="4b20f-106">创建产品模型</span><span class="sxs-lookup"><span data-stu-id="4b20f-106">Create a product model</span></span>
1. <span data-ttu-id="4b20f-107">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="4b20f-108">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="4b20f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-109">Click New.</span></span>
4. <span data-ttu-id="4b20f-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4b20f-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="4b20f-112">在“求解器策略”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4b20f-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="4b20f-113">求解器策略确定如何处理基于约束的产品配置模型中的约束。</span><span class="sxs-lookup"><span data-stu-id="4b20f-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="4b20f-114">此选择可对产品配置模型的性能造成影响。</span><span class="sxs-lookup"><span data-stu-id="4b20f-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="4b20f-115">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4b20f-116">根组件表示产品配置模型，但是还可用于其他产品模型中。</span><span class="sxs-lookup"><span data-stu-id="4b20f-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="4b20f-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-117">Click OK.</span></span>
9. <span data-ttu-id="4b20f-118">在“重复使用配置”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4b20f-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="4b20f-119">如果重复使用配置参数设置为“是”，且在每一配置会话和重复使用后发现有完全匹配，系统将检查相同的配置。</span><span class="sxs-lookup"><span data-stu-id="4b20f-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="4b20f-120">添加属性</span><span class="sxs-lookup"><span data-stu-id="4b20f-120">Add attributes</span></span>
1. <span data-ttu-id="4b20f-121">展开“属性”部分。</span><span class="sxs-lookup"><span data-stu-id="4b20f-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="4b20f-122">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-122">Click Add.</span></span>
3. <span data-ttu-id="4b20f-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4b20f-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4b20f-124">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4b20f-125">在“求解器名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="4b20f-126">求解器名称由产品配置器的约束求解器使用。</span><span class="sxs-lookup"><span data-stu-id="4b20f-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="4b20f-127">该名称不能包含空格或特殊字符（下划线 _ 除外）。</span><span class="sxs-lookup"><span data-stu-id="4b20f-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="4b20f-128">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4b20f-129">描述文本将显示给配置用户，因此可帮助选择正确的属性值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="4b20f-130">在“属性类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="4b20f-131">属性类型确定可供属性使用的值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="4b20f-132">在“加入重复使用”复选框。</span><span class="sxs-lookup"><span data-stu-id="4b20f-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="4b20f-133">该选项只有选择“重复使用配置”选项后才可用。</span><span class="sxs-lookup"><span data-stu-id="4b20f-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="4b20f-134">在“重复使用”复选框中加入属性表示，在系统寻找完全匹配时将考虑该属性。</span><span class="sxs-lookup"><span data-stu-id="4b20f-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="4b20f-135">添加子组件</span><span class="sxs-lookup"><span data-stu-id="4b20f-135">Add subcomponents</span></span>
1. <span data-ttu-id="4b20f-136">展开“子组件”部分。</span><span class="sxs-lookup"><span data-stu-id="4b20f-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="4b20f-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-137">Click Add.</span></span>
3. <span data-ttu-id="4b20f-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4b20f-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4b20f-139">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4b20f-140">在“求解器名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="4b20f-141">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="4b20f-142">在“组件”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="4b20f-143">每个子组件必须引用一个组件定义。</span><span class="sxs-lookup"><span data-stu-id="4b20f-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="4b20f-144">此设计支持可重复使用的组件，并确保一旦定义一个组件，其可用于许多产品模型中。</span><span class="sxs-lookup"><span data-stu-id="4b20f-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="4b20f-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-145">Click Save.</span></span>
9. <span data-ttu-id="4b20f-146">单击“物料清单行详细信息”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-146">Click BOM line details.</span></span>
    * <span data-ttu-id="4b20f-147">物料清单行详细信息窗体使得用户能够为子组件选择所需的属性。</span><span class="sxs-lookup"><span data-stu-id="4b20f-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="4b20f-148">每一性能可被给予固定值或映射到一个属性。</span><span class="sxs-lookup"><span data-stu-id="4b20f-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="4b20f-149">映射到一个属性将导致物料清单行性能有不同的值（取决于配置选择）。</span><span class="sxs-lookup"><span data-stu-id="4b20f-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="4b20f-150">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4b20f-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="4b20f-151">每一子组件表示含基于约束的配置技术的可配置基础产品。</span><span class="sxs-lookup"><span data-stu-id="4b20f-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="4b20f-152">此引用通过物料编号作出。</span><span class="sxs-lookup"><span data-stu-id="4b20f-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="4b20f-153">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="4b20f-153">Select the Set check box.</span></span>
12. <span data-ttu-id="4b20f-154">在“计算”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="4b20f-155">设置计算选项，确保在运行产品成本计算时将产品包含在内。</span><span class="sxs-lookup"><span data-stu-id="4b20f-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="4b20f-156">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4b20f-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="4b20f-157">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="4b20f-157">Select the Set check box.</span></span>
15. <span data-ttu-id="4b20f-158">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4b20f-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4b20f-159">“数量”字段确定在配置产品中消耗的产品数量。</span><span class="sxs-lookup"><span data-stu-id="4b20f-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="4b20f-160">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="4b20f-160">Select the Set check box.</span></span>
17. <span data-ttu-id="4b20f-161">在“每个系列”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4b20f-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="4b20f-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4b20f-162">Click OK.</span></span>


