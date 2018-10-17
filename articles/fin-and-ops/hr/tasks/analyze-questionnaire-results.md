--- 
title: "分析调查表结果"
description: "调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。"
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a70ea145d8c7134a32e8f0fc6980daca9a010bb0
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="ec9fc-103">分析调查表结果</span><span class="sxs-lookup"><span data-stu-id="ec9fc-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec9fc-104">调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="ec9fc-105">若要启动此过程，请转到“调查表”>“查看和分析结果”>“调查表统计”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="ec9fc-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="ec9fc-107">创建调查表统计记录</span><span class="sxs-lookup"><span data-stu-id="ec9fc-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="ec9fc-108">转到“调查表统计”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="ec9fc-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-109">Click New.</span></span>
3. <span data-ttu-id="ec9fc-110">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ec9fc-111">在“统计”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="ec9fc-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ec9fc-113">在“调查表”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ec9fc-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ec9fc-115">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-115">Click the General tab.</span></span>
    * <span data-ttu-id="ec9fc-116">如果您想添加匿名结果或工作人员、联系人和申请人的结果，请选择此项。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="ec9fc-117">选择或取消选择“工作人员”复选框。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="ec9fc-118">如果您将按资历或年龄查看结果，请指定您希望在结构分组时使用的间隔依据。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="ec9fc-119">在年龄段中输入 5，则将会根据 5 岁年龄段对结果进行分组。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="ec9fc-120">在“年龄”字段中，输入数字。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="ec9fc-121">如果您想要对整个调查表、每个结果组、每个问题或每个问题行运行计算，请选择此项。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="ec9fc-122">选择您希望的结果分组方式。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="ec9fc-123">例如，如果计算每个问题的平均数，您可能想要在查看问题时按结果分组。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="ec9fc-124">选择进行计算的数据。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="ec9fc-125">例如，如果您想要查看工作人员调查表的平均百分比和平均分。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="ec9fc-126">单击“范围”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-126">Click the Range tab.</span></span>
    * <span data-ttu-id="ec9fc-127">使用范围限制结果，设置为仅满足范围标准的结果。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="ec9fc-128">单击“分组依据”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="ec9fc-129">进行分组，以确定如何显示结果。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="ec9fc-130">例如，首先按性别将结果分组，然后按年龄分组。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="ec9fc-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ec9fc-132">将分组移动到所选的一侧，并以期望的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="ec9fc-133">执行统计计算。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="ec9fc-134">单击“执行”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-134">Click Execute.</span></span>
    * <span data-ttu-id="ec9fc-135">选择您想对结果执行的计算方式。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="ec9fc-136">例如，计算所选组在调查表中的平均百分比，或统计所选组的分数结果。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="ec9fc-137">选择或取消选择“删除先前搜索”复选框。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="ec9fc-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="ec9fc-139">查看调查表统计运行的结果。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="ec9fc-140">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-140">Click Result.</span></span>
2. <span data-ttu-id="ec9fc-141">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-141">Click Result.</span></span>
3. <span data-ttu-id="ec9fc-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ec9fc-142">Close the page.</span></span>


