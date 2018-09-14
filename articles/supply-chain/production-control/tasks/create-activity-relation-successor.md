--- 
title: "创建活动关系 - 后续活动"
description: "精益生产流的活动流通过活动关系记录。"
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e5e5844939e1eb40e31530c434c096c5b3be7abe
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="866de-103">创建活动关系：后续活动</span><span class="sxs-lookup"><span data-stu-id="866de-103">Create activity relation: Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="866de-104">精益生产流的活动流通过活动关系记录。</span><span class="sxs-lookup"><span data-stu-id="866de-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="866de-105">此记录显示如何创建活动关系。</span><span class="sxs-lookup"><span data-stu-id="866de-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="866de-106">先决条件：</span><span class="sxs-lookup"><span data-stu-id="866de-106">Prerequisites:</span></span>

- <span data-ttu-id="866de-107">一个生产流程和草稿模式的版本。</span><span class="sxs-lookup"><span data-stu-id="866de-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="866de-108">创建了在生产流中彼此衔接的两个活动，但两者不相关。</span><span class="sxs-lookup"><span data-stu-id="866de-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="866de-109">找到生产流版本</span><span class="sxs-lookup"><span data-stu-id="866de-109">Find the production flow version</span></span> 
1. <span data-ttu-id="866de-110">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="866de-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="866de-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="866de-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="866de-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="866de-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="866de-113">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="866de-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="866de-114">在列表中，选择一个草稿版本。</span><span class="sxs-lookup"><span data-stu-id="866de-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="866de-115">可在生产流的草稿或有效版本中添加活动关系。</span><span class="sxs-lookup"><span data-stu-id="866de-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="866de-116">打开活动概览</span><span class="sxs-lookup"><span data-stu-id="866de-116">Open the activity overview</span></span>
1. <span data-ttu-id="866de-117">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="866de-117">Click Activities.</span></span>
    * <span data-ttu-id="866de-118">请注意，窗体显示生产流的所有活动分配到您正在操作的生产流版本中。</span><span class="sxs-lookup"><span data-stu-id="866de-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="866de-119">添加后续活动</span><span class="sxs-lookup"><span data-stu-id="866de-119">Add a Successor</span></span>
1. <span data-ttu-id="866de-120">单击“添加后续活动”。</span><span class="sxs-lookup"><span data-stu-id="866de-120">Click Add successor.</span></span>
2. <span data-ttu-id="866de-121">在“活动”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="866de-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="866de-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="866de-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="866de-123">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="866de-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="866de-124">选择“约束”复选框。</span><span class="sxs-lookup"><span data-stu-id="866de-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="866de-125">在“约束值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="866de-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="866de-126">约束时间是在前导活动的计划结束时间（到期日期和时间）和后续的计划开始时间之间安排的时间。</span><span class="sxs-lookup"><span data-stu-id="866de-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="866de-127">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="866de-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="866de-128">在“周期时间比率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="866de-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="866de-129">如果两个活动以相同的单位产品生产时间运行，周期时间比率应为 1。</span><span class="sxs-lookup"><span data-stu-id="866de-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="866de-130">如果前导活动以后续活动的两倍速度运行，比率应为 2。</span><span class="sxs-lookup"><span data-stu-id="866de-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="866de-131">周期时间比率用于计算生产流活动的单个周期时间。</span><span class="sxs-lookup"><span data-stu-id="866de-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="866de-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="866de-132">Click OK.</span></span>
10. <span data-ttu-id="866de-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="866de-133">Close the page.</span></span>
11. <span data-ttu-id="866de-134">单击“网格面板”选项卡。</span><span class="sxs-lookup"><span data-stu-id="866de-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="866de-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="866de-135">Close the page.</span></span>
13. <span data-ttu-id="866de-136">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="866de-136">Refresh the page.</span></span>


