---
title: 创建成本行为策略并将其分配到成本控制单元
description: 成本行为是将成本分类为固定或可变。
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757e5a5be94e7190f4dbb51d667dc8adec4b824a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826315"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="b5cfc-103">创建成本行为策略并将其分配到成本控制单元</span><span class="sxs-lookup"><span data-stu-id="b5cfc-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5cfc-104">成本行为是将成本分类为固定或可变。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="b5cfc-105">必须将政策和相应规则分配给成本控制单元，政策才能生效。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="b5cfc-106">此过程用于创建政策，然后将其分配给成本控制单元。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="b5cfc-107">创建成本行为层次结构</span><span class="sxs-lookup"><span data-stu-id="b5cfc-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="b5cfc-108">转到“成本核算”>“维度”>“维度层次结构”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="b5cfc-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-109">Click New.</span></span>
3. <span data-ttu-id="b5cfc-110">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-110">Click Create.</span></span>
4. <span data-ttu-id="b5cfc-111">在“维度层次结构名称”中，键入“成本行为层次结构”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="b5cfc-112">在“维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-113">选择“成本元素”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="b5cfc-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-114">Click Save.</span></span>
7. <span data-ttu-id="b5cfc-115">单击“查看层次结构”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="b5cfc-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-116">Click New.</span></span>
9. <span data-ttu-id="b5cfc-117">在“节点名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="b5cfc-118">输入固定成本</span><span class="sxs-lookup"><span data-stu-id="b5cfc-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="b5cfc-119">在树中，选择“成本行为层次结构”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="b5cfc-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-120">Click New.</span></span>
12. <span data-ttu-id="b5cfc-121">在“节点名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="b5cfc-122">输入可变成本。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="b5cfc-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-123">Click Save.</span></span>
14. <span data-ttu-id="b5cfc-124">在树中，选择“成本行为层次结构\固定成本”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="b5cfc-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-125">Click New.</span></span>
16. <span data-ttu-id="b5cfc-126">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="b5cfc-127">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-128">维度成员的范围中可包含差距，但是这些成员不能重叠。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="b5cfc-129">在“截止维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-130">维度成员的范围中可包含差距，但是这些成员不能重叠。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="b5cfc-131">在树中，选择“成本行为层次结构\可变成本”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="b5cfc-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-132">Click New.</span></span>
21. <span data-ttu-id="b5cfc-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="b5cfc-134">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-135">维度成员的范围中可包含差距，但是这些成员不能重叠。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="b5cfc-136">在“截止维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-137">维度成员的范围中可包含差距，但是这些成员不能重叠。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="b5cfc-138">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="b5cfc-139">创建策略和规则</span><span class="sxs-lookup"><span data-stu-id="b5cfc-139">Create the policy and rules</span></span>
1. <span data-ttu-id="b5cfc-140">转到“成本核算”>“政策”>“成本行为政策”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="b5cfc-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-141">Click New.</span></span>
3. <span data-ttu-id="b5cfc-142">在“政策名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="b5cfc-143">在“成本元素维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-144">选择刚才创建的政策层次结构。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="b5cfc-145">在“成本对象维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-146">选择“组织”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-146">Select Organization.</span></span>  
6. <span data-ttu-id="b5cfc-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-147">Click Save.</span></span>
7. <span data-ttu-id="b5cfc-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-148">Click New.</span></span>
8. <span data-ttu-id="b5cfc-149">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b5cfc-150">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-151">展开层次结构以选择“可变成本”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="b5cfc-152">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b5cfc-153">默认情况下，可变百分比为 100%。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="b5cfc-154">单击“成本控制单元的政策分配”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="b5cfc-155">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-155">Click New.</span></span>
13. <span data-ttu-id="b5cfc-156">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b5cfc-157">在“核算生效日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="b5cfc-158">规则具有时效性，创建了更新版本时，用户或系统可让规则到期。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="b5cfc-159">在“成本控制单元”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="b5cfc-160">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5cfc-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]