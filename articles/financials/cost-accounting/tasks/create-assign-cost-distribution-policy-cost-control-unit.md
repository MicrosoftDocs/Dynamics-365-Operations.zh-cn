--- 
title: "创建成本分配政策并将其分配到成本控制单元"
description: "成本分配规则用于分配集体成本中心中已财务盘点的成本。"
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbd44816fc2f2569dd477fc21f59418a575bb835
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="4dcb6-103">创建成本分配政策并将其分配到成本控制单元</span><span class="sxs-lookup"><span data-stu-id="4dcb6-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dcb6-104">成本分配规则用于分配集体成本中心中已财务盘点的成本。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="4dcb6-105">成本会计师确保根据所选分配基数将成本分配给成本中心。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="4dcb6-106">将为成本控制单元分配政策和相应规则。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="4dcb6-107">此任务指南使用示例显示如何创建成本分配政策和相应规则。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="4dcb6-108">创建政策</span><span class="sxs-lookup"><span data-stu-id="4dcb6-108">Create a policy</span></span>
1. <span data-ttu-id="4dcb6-109">转到“成本核算”>“政策”>“成本分配政策”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="4dcb6-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-110">Click New.</span></span>
3. <span data-ttu-id="4dcb6-111">在“政策名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4dcb6-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4dcb6-113">在“成本对象维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-114">选择“组织”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-114">Select Organization.</span></span>  
6. <span data-ttu-id="4dcb6-115">在“成本元素维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-116">选择“CDS P/L”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="4dcb6-117">在“统计维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-118">选择“统计元素”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="4dcb6-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="4dcb6-120">为政策创建规则</span><span class="sxs-lookup"><span data-stu-id="4dcb6-120">Create rules for the policy</span></span>
1. <span data-ttu-id="4dcb6-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-121">Click New.</span></span>
2. <span data-ttu-id="4dcb6-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4dcb6-123">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-124">展开层次结构以选择“094”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="4dcb6-125">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-126">选择“其他运营费用”，然后选择“605110 清洁”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="4dcb6-127">在“成本行为”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="4dcb6-128">选择“固定成本”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="4dcb6-129">在“分配基准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="4dcb6-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-130">Click New.</span></span>
8. <span data-ttu-id="4dcb6-131">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4dcb6-132">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-133">展开层次结构以选择“094”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="4dcb6-134">在“成本元素维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4dcb6-135">选择“其他运营费用”，然后选择“605150 租金”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="4dcb6-136">在“成本行为”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="4dcb6-137">选择“固定成本”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="4dcb6-138">在“分配基准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="4dcb6-139">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="4dcb6-140">为成本控制单元分配规则</span><span class="sxs-lookup"><span data-stu-id="4dcb6-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="4dcb6-141">单击“成本控制单元的政策分配”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="4dcb6-142">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-142">Click New.</span></span>
3. <span data-ttu-id="4dcb6-143">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4dcb6-144">在“核算生效日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="4dcb6-145">在“有效会计年度”中选择“9 月 1 日”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="4dcb6-146">在“成本控制单元”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="4dcb6-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4dcb6-147">Click Save.</span></span>

