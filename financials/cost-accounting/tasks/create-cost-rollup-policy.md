--- 
title: "创建成本累积政策"
description: "此过程显示如何创建成本累积政策并为其创建规则。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="8bda8-103">创建成本累积政策</span><span class="sxs-lookup"><span data-stu-id="8bda8-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bda8-104">此过程显示如何创建成本累积政策并为其创建规则。</span><span class="sxs-lookup"><span data-stu-id="8bda8-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="8bda8-105">使用 USP2 演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="8bda8-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8bda8-106">创建政策</span><span class="sxs-lookup"><span data-stu-id="8bda8-106">Create a policy</span></span>
1. <span data-ttu-id="8bda8-107">转到“成本核算”>“政策”>“成本累积政策”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="8bda8-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-108">Click New.</span></span>
3. <span data-ttu-id="8bda8-109">在“政策名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8bda8-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8bda8-111">在“成本对象维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-112">选择“成本累积 CC”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="8bda8-113">在“成本元素维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-114">选择“成本累积 CC”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="8bda8-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="8bda8-116">为成本累积政策创建规则</span><span class="sxs-lookup"><span data-stu-id="8bda8-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="8bda8-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-117">Click New.</span></span>
2. <span data-ttu-id="8bda8-118">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8bda8-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8bda8-119">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-120">选择“007”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-120">Select 007.</span></span>  
4. <span data-ttu-id="8bda8-121">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-122">选择“成本累积 CE”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="8bda8-123">在“辅助成本元素维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-124">在此示例中，将辅助成本元素 CC-007 映射到成本中心。</span><span class="sxs-lookup"><span data-stu-id="8bda8-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="8bda8-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-125">Click New.</span></span>
7. <span data-ttu-id="8bda8-126">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8bda8-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8bda8-127">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-128">选择“008”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-128">Select 008.</span></span>  
9. <span data-ttu-id="8bda8-129">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-130">选择“成本累积 CE”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="8bda8-131">在“辅助成本元素维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-132">在此示例中，将辅助成本元素 CC-008 映射到成本中心。</span><span class="sxs-lookup"><span data-stu-id="8bda8-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="8bda8-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-133">Click New.</span></span>
12. <span data-ttu-id="8bda8-134">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8bda8-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8bda8-135">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-136">选择“009”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-136">Select 009.</span></span>  
14. <span data-ttu-id="8bda8-137">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-138">选择“成本累积 CE”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="8bda8-139">在“辅助成本元素维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8bda8-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8bda8-140">在此示例中，将辅助成本元素 CC-009 映射到成本中心。</span><span class="sxs-lookup"><span data-stu-id="8bda8-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="8bda8-141">继续操作，直到所有成本中心均已映射到其相应辅助成本元素。</span><span class="sxs-lookup"><span data-stu-id="8bda8-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="8bda8-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8bda8-142">Click Save.</span></span>

