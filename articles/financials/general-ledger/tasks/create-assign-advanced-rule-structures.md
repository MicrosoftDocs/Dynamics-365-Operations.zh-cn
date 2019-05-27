---
title: 创建和分配高级规则结构
description: 此任务指南介绍创建高级规则结构并分配至帐户结构的步骤。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558898"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="719dd-103">创建和分配高级规则结构</span><span class="sxs-lookup"><span data-stu-id="719dd-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="719dd-104">此任务指南介绍创建高级规则结构并分配至帐户结构的步骤。</span><span class="sxs-lookup"><span data-stu-id="719dd-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="719dd-105">此指南使用演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="719dd-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="719dd-106">创建高级规则结构</span><span class="sxs-lookup"><span data-stu-id="719dd-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="719dd-107">转到“总帐”>“会计科目表”>“结构”>“高级规则结构”。</span><span class="sxs-lookup"><span data-stu-id="719dd-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="719dd-108">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="719dd-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="719dd-109">在“高级规则结构”字段中，输入描述规则结构的名称。</span><span class="sxs-lookup"><span data-stu-id="719dd-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="719dd-110">在“描述”字段中，输入描述结构的值。</span><span class="sxs-lookup"><span data-stu-id="719dd-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="719dd-111">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="719dd-111">Click OK.</span></span>
6. <span data-ttu-id="719dd-112">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="719dd-112">Click Add segment.</span></span>
7. <span data-ttu-id="719dd-113">在“分部”列表中，选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="719dd-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="719dd-114">例如：商店。</span><span class="sxs-lookup"><span data-stu-id="719dd-114">For example, Store.</span></span>  
8. <span data-ttu-id="719dd-115">单击“添加分部”。</span><span class="sxs-lookup"><span data-stu-id="719dd-115">Click Add segment.</span></span>
9. <span data-ttu-id="719dd-116">在列表中，单击高级规则结构的链接以进行查看。</span><span class="sxs-lookup"><span data-stu-id="719dd-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="719dd-117">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="719dd-117">Click Activate.</span></span>
11. <span data-ttu-id="719dd-118">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="719dd-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="719dd-119">应用高级规则结构到科目结构中</span><span class="sxs-lookup"><span data-stu-id="719dd-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="719dd-120">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="719dd-120">Close the form.</span></span>
2. <span data-ttu-id="719dd-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="719dd-121">Close the page.</span></span>
3. <span data-ttu-id="719dd-122">转到“总帐”>“会计科目表”>“结构”>“配置科目结构”。</span><span class="sxs-lookup"><span data-stu-id="719dd-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="719dd-123">在列表中，找到并选择您想应用高级规则的科目结构。</span><span class="sxs-lookup"><span data-stu-id="719dd-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="719dd-124">单击科目结构的名称，以打开该科目结构。</span><span class="sxs-lookup"><span data-stu-id="719dd-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="719dd-125">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="719dd-125">Click Edit.</span></span>
    * <span data-ttu-id="719dd-126">您还可以点击“高级规则”，将会提示您将科目结构设置为草稿模式。</span><span class="sxs-lookup"><span data-stu-id="719dd-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="719dd-127">单击“高级规则”。</span><span class="sxs-lookup"><span data-stu-id="719dd-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="719dd-128">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="719dd-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="719dd-129">在“高级规则”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="719dd-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="719dd-130">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="719dd-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="719dd-131">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="719dd-131">Click Create.</span></span>
12. <span data-ttu-id="719dd-132">单击“添加新条件”。</span><span class="sxs-lookup"><span data-stu-id="719dd-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="719dd-133">在“目标位置”字段中，选择主科目或财务维度。</span><span class="sxs-lookup"><span data-stu-id="719dd-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="719dd-134">在“运算符”字段中，选择一个选项，例如“介于并包含”。</span><span class="sxs-lookup"><span data-stu-id="719dd-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="719dd-135">在“值”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="719dd-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="719dd-136">在“范围”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="719dd-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="719dd-137">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="719dd-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="719dd-138">在列表中，找到满足您输入的条件时使用的高级规则结构。</span><span class="sxs-lookup"><span data-stu-id="719dd-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="719dd-139">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="719dd-139">Click Add.</span></span>
20. <span data-ttu-id="719dd-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="719dd-140">Close the page.</span></span>
21. <span data-ttu-id="719dd-141">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="719dd-141">Click Activate.</span></span>
22. <span data-ttu-id="719dd-142">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="719dd-142">Click Activate.</span></span>

