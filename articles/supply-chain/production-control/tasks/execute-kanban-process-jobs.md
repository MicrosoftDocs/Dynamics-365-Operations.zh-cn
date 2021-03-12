---
title: 执行看板处理作业
description: 此过程介绍看板流程作业的执行。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9da49ae17d6c25166f6b0e05e3c45fc991c9a54d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994146"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="4d24b-103">执行看板处理作业</span><span class="sxs-lookup"><span data-stu-id="4d24b-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d24b-104">此过程介绍看板流程作业的执行。</span><span class="sxs-lookup"><span data-stu-id="4d24b-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="4d24b-105">第一个作业按预期数量完成并没有错误。</span><span class="sxs-lookup"><span data-stu-id="4d24b-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="4d24b-106">第二个作业完成时包含错误。</span><span class="sxs-lookup"><span data-stu-id="4d24b-106">The second job is completed with errors.</span></span> <span data-ttu-id="4d24b-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="4d24b-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4d24b-108">此过程是专为机器操作员设计的。</span><span class="sxs-lookup"><span data-stu-id="4d24b-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="4d24b-109">选择看板作业</span><span class="sxs-lookup"><span data-stu-id="4d24b-109">Select a kanban job</span></span>
1. <span data-ttu-id="4d24b-110">转到“生产控制”>“看板”>“处理作业的看板面板”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="4d24b-111">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="4d24b-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4d24b-112">单击包含资源组 1250 的行。</span><span class="sxs-lookup"><span data-stu-id="4d24b-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="4d24b-113">这筛选作业列表，将只显示 1250 工作单元的作业。</span><span class="sxs-lookup"><span data-stu-id="4d24b-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="4d24b-114">标记状态为“计划作业”的行。</span><span class="sxs-lookup"><span data-stu-id="4d24b-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="4d24b-115">按预期数量完成作业</span><span class="sxs-lookup"><span data-stu-id="4d24b-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="4d24b-116">展开或折叠“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="4d24b-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="4d24b-117">此部分显示有关卡号、物料编号、已订购数量和活动名称的重要信息。</span><span class="sxs-lookup"><span data-stu-id="4d24b-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="4d24b-118">展开或折叠“生产说明”部分。</span><span class="sxs-lookup"><span data-stu-id="4d24b-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="4d24b-119">此部分显示活动的生产说明。</span><span class="sxs-lookup"><span data-stu-id="4d24b-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="4d24b-120">说明可以是文本、图片、绘图和其他文档。</span><span class="sxs-lookup"><span data-stu-id="4d24b-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="4d24b-121">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-121">Click Start.</span></span>
    * <span data-ttu-id="4d24b-122">选择尚未完成的作业。</span><span class="sxs-lookup"><span data-stu-id="4d24b-122">Select a job that is not completed.</span></span> <span data-ttu-id="4d24b-123">使用“作业状态”字段中的状态图标查看作业状态。</span><span class="sxs-lookup"><span data-stu-id="4d24b-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="4d24b-124">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-124">Click Complete.</span></span>
    * <span data-ttu-id="4d24b-125">作业以预期质量完成。</span><span class="sxs-lookup"><span data-stu-id="4d24b-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="4d24b-126">作业完成时有错误</span><span class="sxs-lookup"><span data-stu-id="4d24b-126">Complete a job with errors</span></span>
1. <span data-ttu-id="4d24b-127">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-127">Click Start.</span></span>
    * <span data-ttu-id="4d24b-128">在作业完成后，列表中的下一个作业将被自动选择。</span><span class="sxs-lookup"><span data-stu-id="4d24b-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="4d24b-129">这就是在单击“开始”之前您不需要选择作业的原因。</span><span class="sxs-lookup"><span data-stu-id="4d24b-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="4d24b-130">在“操作窗格”上单击“制造”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="4d24b-131">单击“完成(详细信息)”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-131">Click Complete (details).</span></span>
4. <span data-ttu-id="4d24b-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4d24b-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4d24b-133">在“错误数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4d24b-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="4d24b-134">在“完好数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4d24b-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="4d24b-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4d24b-135">Click OK.</span></span>

