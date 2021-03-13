---
title: 提交和审查项目预算
description: 此过程显示如何创建和提交项目的预算。
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b871a3fef3515d3a79fb4b55406a93fc16d02faa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018720"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="4a445-103">提交和审查项目预算</span><span class="sxs-lookup"><span data-stu-id="4a445-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a445-104">此过程显示如何创建和提交项目的预算。</span><span class="sxs-lookup"><span data-stu-id="4a445-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="4a445-105">创建项目预算时，您可以输入成本的已评估收入和成本，然后将其用于控制实际项目交易记录。</span><span class="sxs-lookup"><span data-stu-id="4a445-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="4a445-106">在项目预算中，必须将所有原始预算和修订发送到项目工作流以供审核。</span><span class="sxs-lookup"><span data-stu-id="4a445-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="4a445-107">工作流提供给您对流程的增强了的控制，并创建了一个更改历史记录。</span><span class="sxs-lookup"><span data-stu-id="4a445-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="4a445-108">此任务是使用 USSI 数据集创建的。</span><span class="sxs-lookup"><span data-stu-id="4a445-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="4a445-109">在 **导航窗格** 中，转到 **模块 > 项目管理与核算 > 项目 > 所有项目**。</span><span class="sxs-lookup"><span data-stu-id="4a445-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="4a445-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4a445-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4a445-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4a445-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4a445-112">在 **操作窗格** 中，单击 **计划**。</span><span class="sxs-lookup"><span data-stu-id="4a445-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="4a445-113">单击 **项目预算**。</span><span class="sxs-lookup"><span data-stu-id="4a445-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="4a445-114">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a445-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="4a445-115">展开 **成本** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="4a445-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="4a445-116">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4a445-116">Click **New**.</span></span>
9. <span data-ttu-id="4a445-117">在 **交易类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4a445-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="4a445-118">在 **类别** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4a445-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="4a445-119">在 **原始预算** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4a445-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="4a445-120">展开 **收入** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="4a445-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="4a445-121">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4a445-121">Click **New**.</span></span>
14. <span data-ttu-id="4a445-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4a445-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="4a445-123">在 **交易类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="4a445-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="4a445-124">在 **类别** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4a445-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="4a445-125">在 **原始预算** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4a445-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="4a445-126">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4a445-126">Click **Save**.</span></span>
19. <span data-ttu-id="4a445-127">单击 **工作流**。</span><span class="sxs-lookup"><span data-stu-id="4a445-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="4a445-128">单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="4a445-128">Click **Submit**.</span></span>
21. <span data-ttu-id="4a445-129">在 **注释** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a445-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="4a445-130">单击 **提交**。</span><span class="sxs-lookup"><span data-stu-id="4a445-130">Click **Submit**.</span></span>

