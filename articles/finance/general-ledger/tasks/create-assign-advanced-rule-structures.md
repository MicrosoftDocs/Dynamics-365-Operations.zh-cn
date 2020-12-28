---
title: 创建和分配高级规则结构
description: 本主题介绍如何创建高级规则结构并分配给科目结构。
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440636"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="f0204-103">创建和分配高级规则结构</span><span class="sxs-lookup"><span data-stu-id="f0204-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0204-104">本主题介绍如何创建高级规则结构并分配给科目结构。</span><span class="sxs-lookup"><span data-stu-id="f0204-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="f0204-105">此指南使用演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="f0204-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="f0204-106">创建高级规则结构</span><span class="sxs-lookup"><span data-stu-id="f0204-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="f0204-107">转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 高级规则结构**。</span><span class="sxs-lookup"><span data-stu-id="f0204-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="f0204-108">选择 **新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="f0204-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="f0204-109">在 **高级规则结构** 字段中，输入用于描述规则结构的名称。</span><span class="sxs-lookup"><span data-stu-id="f0204-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="f0204-110">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f0204-110">Select **OK**.</span></span>
5. <span data-ttu-id="f0204-111">选择 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="f0204-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="f0204-112">在“分部”列表中，选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="f0204-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="f0204-113">例如，**商店**。</span><span class="sxs-lookup"><span data-stu-id="f0204-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="f0204-114">选择 **添加段落**。</span><span class="sxs-lookup"><span data-stu-id="f0204-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="f0204-115">选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="f0204-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="f0204-116">应用高级规则结构到科目结构中</span><span class="sxs-lookup"><span data-stu-id="f0204-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="f0204-117">转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 配置科目结构**。</span><span class="sxs-lookup"><span data-stu-id="f0204-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="f0204-118">在列表中，找到并选择您想应用高级规则的科目结构。</span><span class="sxs-lookup"><span data-stu-id="f0204-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="f0204-119">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="f0204-119">Select **Edit**.</span></span> <span data-ttu-id="f0204-120">您还可以选择 **高级规则**，将会提示您将科目结构设置为 **草稿模式**。</span><span class="sxs-lookup"><span data-stu-id="f0204-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="f0204-121">选择 **高级规则**。</span><span class="sxs-lookup"><span data-stu-id="f0204-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="f0204-122">选择 **新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="f0204-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="f0204-123">在 **高级规则** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0204-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="f0204-124">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0204-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="f0204-125">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="f0204-125">Select **Create**.</span></span>
9. <span data-ttu-id="f0204-126">选择 **添加新条件**。</span><span class="sxs-lookup"><span data-stu-id="f0204-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="f0204-127">在 **目标位置** 字段中，选择主科目或财务维度。</span><span class="sxs-lookup"><span data-stu-id="f0204-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="f0204-128">在 **运算符** 字段中，选择一个选项，例如 **介于** 和 **包含**。</span><span class="sxs-lookup"><span data-stu-id="f0204-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="f0204-129">在 **值** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0204-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="f0204-130">在 **范围** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0204-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="f0204-131">选择 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="f0204-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="f0204-132">在列表中，找到满足您输入的条件时使用的高级规则结构。</span><span class="sxs-lookup"><span data-stu-id="f0204-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="f0204-133">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0204-133">Select **Add**.</span></span>
17. <span data-ttu-id="f0204-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f0204-134">Close the page.</span></span>
18. <span data-ttu-id="f0204-135">选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="f0204-135">Select **Activate**.</span></span>

