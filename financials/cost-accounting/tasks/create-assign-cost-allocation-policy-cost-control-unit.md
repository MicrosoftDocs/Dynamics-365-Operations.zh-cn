--- 
title: "创建成本分摊策略并将其分配到成本控制单元"
description: "此过程用于创建和分配成本分配政策，以及为成本控制单元分配相应规则。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="b5537-103">创建成本分摊策略并将其分配到成本控制单元</span><span class="sxs-lookup"><span data-stu-id="b5537-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5537-104">此过程用于创建和分配成本分配政策，以及为成本控制单元分配相应规则。</span><span class="sxs-lookup"><span data-stu-id="b5537-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="b5537-105">此录制使用 USP2 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="b5537-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="b5537-106">创建政策</span><span class="sxs-lookup"><span data-stu-id="b5537-106">Create a policy</span></span>
1. <span data-ttu-id="b5537-107">转到“成本核算”>“政策”>“成本分配政策”。</span><span class="sxs-lookup"><span data-stu-id="b5537-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="b5537-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5537-108">Click New.</span></span>
3. <span data-ttu-id="b5537-109">在“政策名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="b5537-110">在“成本对象维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b5537-111">选择“组织”。</span><span class="sxs-lookup"><span data-stu-id="b5537-111">Select Organization.</span></span>  
5. <span data-ttu-id="b5537-112">在“统计维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="b5537-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5537-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="b5537-114">创建分配规则</span><span class="sxs-lookup"><span data-stu-id="b5537-114">Create allocation rules</span></span>
1. <span data-ttu-id="b5537-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5537-115">Click New.</span></span>
2. <span data-ttu-id="b5537-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5537-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b5537-117">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="b5537-118">在“成本行为”字段中选择“总计”。</span><span class="sxs-lookup"><span data-stu-id="b5537-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="b5537-119">在“分配基准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="b5537-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5537-120">Click New.</span></span>
7. <span data-ttu-id="b5537-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5537-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b5537-122">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="b5537-123">在“成本行为”字段中选择“总计”。</span><span class="sxs-lookup"><span data-stu-id="b5537-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="b5537-124">在“分配基准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="b5537-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5537-125">Click New.</span></span>
12. <span data-ttu-id="b5537-126">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5537-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b5537-127">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="b5537-128">在“成本行为”字段中选择“总计”。</span><span class="sxs-lookup"><span data-stu-id="b5537-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="b5537-129">在“分配基准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="b5537-130">继续操作，直到创建了所有规则。</span><span class="sxs-lookup"><span data-stu-id="b5537-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="b5537-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5537-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="b5537-132">为成本控制单元分配政策</span><span class="sxs-lookup"><span data-stu-id="b5537-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="b5537-133">单击“成本控制单元的政策分配”。</span><span class="sxs-lookup"><span data-stu-id="b5537-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="b5537-134">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b5537-134">Click New.</span></span>
3. <span data-ttu-id="b5537-135">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b5537-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b5537-136">在“核算生效日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="b5537-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="b5537-137">规则具有时效性。</span><span class="sxs-lookup"><span data-stu-id="b5537-137">The rules are date-effective.</span></span> <span data-ttu-id="b5537-138">创建了更新版本时，用户或系统可让规则到期。</span><span class="sxs-lookup"><span data-stu-id="b5537-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="b5537-139">在“成本控制单元”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b5537-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="b5537-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b5537-140">Click Save.</span></span>

