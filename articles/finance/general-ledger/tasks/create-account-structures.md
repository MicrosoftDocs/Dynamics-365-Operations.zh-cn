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
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235781"
---
# <a name="create-account-structures"></a><span data-ttu-id="3cefd-103">创建科目结构</span><span class="sxs-lookup"><span data-stu-id="3cefd-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cefd-104">此任务指南介绍创建科目结构的步骤。</span><span class="sxs-lookup"><span data-stu-id="3cefd-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="3cefd-105">步骤使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="3cefd-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="3cefd-106">转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 配置科目结构**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="3cefd-107">在 **操作窗格** 中，单击 **新建** 打开对话框。</span><span class="sxs-lookup"><span data-stu-id="3cefd-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="3cefd-108">在 **科目结构** 字段中，输入描述科目结构的用途的名称。</span><span class="sxs-lookup"><span data-stu-id="3cefd-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="3cefd-109">在 **描述** 字段中，输入指出科目结构用途的描述。</span><span class="sxs-lookup"><span data-stu-id="3cefd-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="3cefd-110">单击 **创建**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-110">Click **Create**.</span></span>
6. <span data-ttu-id="3cefd-111">在 **段落和允许的值**，单击 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="3cefd-112">在维度列表中，选择要添加到科目结构的维度。</span><span class="sxs-lookup"><span data-stu-id="3cefd-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="3cefd-113">在列表末尾，单击 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="3cefd-114">根据需要重复步骤 6 到 9。</span><span class="sxs-lookup"><span data-stu-id="3cefd-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="3cefd-115">在 **允许的值详细信息** 部分中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="3cefd-116">例如，单击 **主科目** 字段。</span><span class="sxs-lookup"><span data-stu-id="3cefd-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="3cefd-117">在 **运算符** 字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="3cefd-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="3cefd-118">在 **值** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="3cefd-119">例如：600000。</span><span class="sxs-lookup"><span data-stu-id="3cefd-119">For example, 600000.</span></span>  
13. <span data-ttu-id="3cefd-120">在 **范围** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-120">In the **through** field, type a value.</span></span> <span data-ttu-id="3cefd-121">例如：699999。</span><span class="sxs-lookup"><span data-stu-id="3cefd-121">For example, 699999.</span></span>  
14. <span data-ttu-id="3cefd-122">在 **允许的值详细信息** 部分中，单击 **应用**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="3cefd-123">根据需要重复步骤 10 到 15。</span><span class="sxs-lookup"><span data-stu-id="3cefd-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="3cefd-124">在 **允许的值详细信息** 部分中，单击 **添加新条件**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="3cefd-125">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="3cefd-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="3cefd-126">在 **值** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="3cefd-127">例如：033。</span><span class="sxs-lookup"><span data-stu-id="3cefd-127">For example, 033.</span></span>  
19. <span data-ttu-id="3cefd-128">在 **范围** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-128">In the **through** field, type a value.</span></span> <span data-ttu-id="3cefd-129">例如：034。</span><span class="sxs-lookup"><span data-stu-id="3cefd-129">For example, 034.</span></span>  
20. <span data-ttu-id="3cefd-130">单击 **应用**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-130">Click **Apply**.</span></span>
21. <span data-ttu-id="3cefd-131">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="3cefd-132">例如：成本中心。</span><span class="sxs-lookup"><span data-stu-id="3cefd-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="3cefd-133">在 **成本中心** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="3cefd-134">例如：007..021。</span><span class="sxs-lookup"><span data-stu-id="3cefd-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="3cefd-135">在 **段落和允许的值**，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="3cefd-136">在 **主科目** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="3cefd-137">例如：600000..699999</span><span class="sxs-lookup"><span data-stu-id="3cefd-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="3cefd-138">在网格中，选择分部以编辑允许的值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="3cefd-139">例如：部门。</span><span class="sxs-lookup"><span data-stu-id="3cefd-139">For example, Department.</span></span>  
26. <span data-ttu-id="3cefd-140">在“部门”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-140">In the Department field, type a value.</span></span> <span data-ttu-id="3cefd-141">例如：032。</span><span class="sxs-lookup"><span data-stu-id="3cefd-141">For example, 032.</span></span>  
27. <span data-ttu-id="3cefd-142">在“成本中心”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3cefd-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="3cefd-143">例如：086。</span><span class="sxs-lookup"><span data-stu-id="3cefd-143">For example, 086.</span></span>  
28. <span data-ttu-id="3cefd-144">在 **操作窗格** 上，单击 **验证**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="3cefd-145">在 **操作窗格** 上，单击 **激活**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="3cefd-146">单击 **启用**。</span><span class="sxs-lookup"><span data-stu-id="3cefd-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]