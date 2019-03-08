---
title: 创建科目结构
description: 此任务指南介绍创建科目结构的步骤。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "356384"
---
# <a name="create-account-structures"></a><span data-ttu-id="9ff78-103">创建科目结构</span><span class="sxs-lookup"><span data-stu-id="9ff78-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ff78-104">此任务指南介绍创建科目结构的步骤。</span><span class="sxs-lookup"><span data-stu-id="9ff78-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="9ff78-105">步骤使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="9ff78-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="9ff78-106">转到“总帐”>“会计科目表”>“结构”>“配置科目结构”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="9ff78-107">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9ff78-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="9ff78-108">在“科目结构”字段中，输入描述科目结构的用途的名称。</span><span class="sxs-lookup"><span data-stu-id="9ff78-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="9ff78-109">在“描述”字段中，输入指出科目结构用途的描述。</span><span class="sxs-lookup"><span data-stu-id="9ff78-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="9ff78-110">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-110">Click Create.</span></span>
6. <span data-ttu-id="9ff78-111">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-111">Click Add segment.</span></span>
7. <span data-ttu-id="9ff78-112">在“维度”列表中，选择要添加到科目结构的维度。</span><span class="sxs-lookup"><span data-stu-id="9ff78-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="9ff78-113">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-113">Click Add segment.</span></span>
9. <span data-ttu-id="9ff78-114">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-114">Click Add segment.</span></span>
10. <span data-ttu-id="9ff78-115">在“维度”列表中，选择要添加到科目结构的维度。</span><span class="sxs-lookup"><span data-stu-id="9ff78-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="9ff78-116">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-116">Click Add segment.</span></span>
12. <span data-ttu-id="9ff78-117">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-117">Click Add segment.</span></span>
13. <span data-ttu-id="9ff78-118">在“维度”列表中，选择要添加到科目结构的维度。</span><span class="sxs-lookup"><span data-stu-id="9ff78-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="9ff78-119">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-119">Click Add segment.</span></span>
15. <span data-ttu-id="9ff78-120">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="9ff78-121">例如，单击“主科目”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="9ff78-122">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="9ff78-123">在“值”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="9ff78-124">例如：600000。</span><span class="sxs-lookup"><span data-stu-id="9ff78-124">For example, 600000.</span></span>  
18. <span data-ttu-id="9ff78-125">在“范围”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="9ff78-126">例如：699999。</span><span class="sxs-lookup"><span data-stu-id="9ff78-126">For example, 699999.</span></span>  
19. <span data-ttu-id="9ff78-127">单击“应用”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-127">Click Apply.</span></span>
20. <span data-ttu-id="9ff78-128">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="9ff78-129">例如：部门。</span><span class="sxs-lookup"><span data-stu-id="9ff78-129">For example, Department.</span></span>  
21. <span data-ttu-id="9ff78-130">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="9ff78-131">在“值”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="9ff78-132">例如：022。</span><span class="sxs-lookup"><span data-stu-id="9ff78-132">For example, 022.</span></span>  
23. <span data-ttu-id="9ff78-133">在“范围”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="9ff78-134">例如：031。</span><span class="sxs-lookup"><span data-stu-id="9ff78-134">For example, 031.</span></span>  
24. <span data-ttu-id="9ff78-135">单击“添加新条件”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="9ff78-136">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="9ff78-137">在“值”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="9ff78-138">例如：033。</span><span class="sxs-lookup"><span data-stu-id="9ff78-138">For example, 033.</span></span>  
27. <span data-ttu-id="9ff78-139">在“范围”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="9ff78-140">例如：034。</span><span class="sxs-lookup"><span data-stu-id="9ff78-140">For example, 034.</span></span>  
28. <span data-ttu-id="9ff78-141">单击“应用”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-141">Click Apply.</span></span>
29. <span data-ttu-id="9ff78-142">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="9ff78-143">例如：成本中心。</span><span class="sxs-lookup"><span data-stu-id="9ff78-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="9ff78-144">在“成本中心”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="9ff78-145">例如：007..021。</span><span class="sxs-lookup"><span data-stu-id="9ff78-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="9ff78-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-146">Click Add.</span></span>
32. <span data-ttu-id="9ff78-147">在“主科目”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="9ff78-148">例如：600000..699999</span><span class="sxs-lookup"><span data-stu-id="9ff78-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="9ff78-149">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="9ff78-150">例如：部门。</span><span class="sxs-lookup"><span data-stu-id="9ff78-150">For example, Department.</span></span>  
34. <span data-ttu-id="9ff78-151">在“部门”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="9ff78-152">例如：032。</span><span class="sxs-lookup"><span data-stu-id="9ff78-152">For example, 032.</span></span>  
35. <span data-ttu-id="9ff78-153">在“成本中心”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ff78-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="9ff78-154">例如：086。</span><span class="sxs-lookup"><span data-stu-id="9ff78-154">For example, 086.</span></span>  
36. <span data-ttu-id="9ff78-155">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-155">Click Validate.</span></span>
37. <span data-ttu-id="9ff78-156">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-156">Click Activate.</span></span>
38. <span data-ttu-id="9ff78-157">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="9ff78-157">Click Activate.</span></span>

