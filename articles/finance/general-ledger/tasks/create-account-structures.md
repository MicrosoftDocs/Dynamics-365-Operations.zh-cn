---
title: 创建科目结构
description: 此任务指南介绍创建科目结构的步骤。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a8df7d7d9c4555bf46ac1cc3f71695837b1369b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968571"
---
# <a name="create-account-structures"></a><span data-ttu-id="de27f-103">创建科目结构</span><span class="sxs-lookup"><span data-stu-id="de27f-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de27f-104">此任务指南介绍创建科目结构的步骤。</span><span class="sxs-lookup"><span data-stu-id="de27f-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="de27f-105">步骤使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="de27f-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="de27f-106">转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 配置科目结构**。</span><span class="sxs-lookup"><span data-stu-id="de27f-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="de27f-107">在 **操作窗格** 中，单击 **新建** 打开对话框。</span><span class="sxs-lookup"><span data-stu-id="de27f-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="de27f-108">在 **科目结构** 字段中，输入描述科目结构的用途的名称。</span><span class="sxs-lookup"><span data-stu-id="de27f-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="de27f-109">在 **描述** 字段中，输入指出科目结构用途的描述。</span><span class="sxs-lookup"><span data-stu-id="de27f-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="de27f-110">单击 **创建**。</span><span class="sxs-lookup"><span data-stu-id="de27f-110">Click **Create**.</span></span>
6. <span data-ttu-id="de27f-111">在 **段落和允许的值**，单击 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="de27f-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="de27f-112">在维度列表中，选择要添加到科目结构的维度。</span><span class="sxs-lookup"><span data-stu-id="de27f-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="de27f-113">在列表末尾，单击 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="de27f-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="de27f-114">根据需要重复步骤 6 到 9。</span><span class="sxs-lookup"><span data-stu-id="de27f-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="de27f-115">在 **允许的值详细信息** 部分中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="de27f-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="de27f-116">例如，单击 **主科目** 字段。</span><span class="sxs-lookup"><span data-stu-id="de27f-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="de27f-117">在 **运算符** 字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="de27f-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="de27f-118">在 **值** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="de27f-119">例如：600000。</span><span class="sxs-lookup"><span data-stu-id="de27f-119">For example, 600000.</span></span>  
13. <span data-ttu-id="de27f-120">在 **范围** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-120">In the **through** field, type a value.</span></span> <span data-ttu-id="de27f-121">例如：699999。</span><span class="sxs-lookup"><span data-stu-id="de27f-121">For example, 699999.</span></span>  
14. <span data-ttu-id="de27f-122">在 **允许的值详细信息** 部分中，单击 **应用**。</span><span class="sxs-lookup"><span data-stu-id="de27f-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="de27f-123">根据需要重复步骤 10 到 15。</span><span class="sxs-lookup"><span data-stu-id="de27f-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="de27f-124">在 **允许的值详细信息** 部分中，单击 **添加新条件**。</span><span class="sxs-lookup"><span data-stu-id="de27f-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="de27f-125">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="de27f-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="de27f-126">在 **值** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="de27f-127">例如：033。</span><span class="sxs-lookup"><span data-stu-id="de27f-127">For example, 033.</span></span>  
19. <span data-ttu-id="de27f-128">在 **范围** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-128">In the **through** field, type a value.</span></span> <span data-ttu-id="de27f-129">例如：034。</span><span class="sxs-lookup"><span data-stu-id="de27f-129">For example, 034.</span></span>  
20. <span data-ttu-id="de27f-130">单击 **应用**。</span><span class="sxs-lookup"><span data-stu-id="de27f-130">Click **Apply**.</span></span>
21. <span data-ttu-id="de27f-131">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="de27f-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="de27f-132">例如：成本中心。</span><span class="sxs-lookup"><span data-stu-id="de27f-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="de27f-133">在 **成本中心** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="de27f-134">例如：007..021。</span><span class="sxs-lookup"><span data-stu-id="de27f-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="de27f-135">在 **段落和允许的值**，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="de27f-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="de27f-136">在 **主科目** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="de27f-137">例如：600000..699999</span><span class="sxs-lookup"><span data-stu-id="de27f-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="de27f-138">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="de27f-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="de27f-139">例如：部门。</span><span class="sxs-lookup"><span data-stu-id="de27f-139">For example, Department.</span></span>  
26. <span data-ttu-id="de27f-140">在“部门”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-140">In the Department field, type a value.</span></span> <span data-ttu-id="de27f-141">例如：032。</span><span class="sxs-lookup"><span data-stu-id="de27f-141">For example, 032.</span></span>  
27. <span data-ttu-id="de27f-142">在“成本中心”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="de27f-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="de27f-143">例如：086。</span><span class="sxs-lookup"><span data-stu-id="de27f-143">For example, 086.</span></span>  
28. <span data-ttu-id="de27f-144">在 **操作窗格** 上，单击 **验证**。</span><span class="sxs-lookup"><span data-stu-id="de27f-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="de27f-145">在 **操作窗格** 上，单击 **激活**。</span><span class="sxs-lookup"><span data-stu-id="de27f-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="de27f-146">单击 **启用**。</span><span class="sxs-lookup"><span data-stu-id="de27f-146">Click **Activate**.</span></span>

