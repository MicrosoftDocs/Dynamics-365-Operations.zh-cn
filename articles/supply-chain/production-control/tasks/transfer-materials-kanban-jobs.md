---
title: 转移物料与看板作业
description: 此过程重点是撤销看板作业，以转移物料。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210356"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="807db-103">转移物料与看板作业</span><span class="sxs-lookup"><span data-stu-id="807db-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="807db-104">此过程重点是撤销看板作业，以转移物料。</span><span class="sxs-lookup"><span data-stu-id="807db-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="807db-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="807db-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="807db-106">此过程是专为仓库工作人员设计的。</span><span class="sxs-lookup"><span data-stu-id="807db-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="807db-107">显示转移作业。</span><span class="sxs-lookup"><span data-stu-id="807db-107">Display transfer jobs</span></span>
1. <span data-ttu-id="807db-108">转到“生产控制”>“看板”>“转移作业的看板面板”。</span><span class="sxs-lookup"><span data-stu-id="807db-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="807db-109">展开或折叠“筛选器”部分。</span><span class="sxs-lookup"><span data-stu-id="807db-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="807db-110">在筛选器部分，您可以通过筛选生产流、活动名称、源仓库和位置以及目标仓库和位置指定想看见的作业。</span><span class="sxs-lookup"><span data-stu-id="807db-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="807db-111">在“源仓库”字段中，键入“11”。</span><span class="sxs-lookup"><span data-stu-id="807db-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="807db-112">在“目标位置”字段中，键入“12”。</span><span class="sxs-lookup"><span data-stu-id="807db-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="807db-113">开始转移作业</span><span class="sxs-lookup"><span data-stu-id="807db-113">Start a transfer job</span></span>
1. <span data-ttu-id="807db-114">在列表中，取消选中的行（若有）。</span><span class="sxs-lookup"><span data-stu-id="807db-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="807db-115">在列表中，选择第 4 行 。</span><span class="sxs-lookup"><span data-stu-id="807db-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="807db-116">选择状态为“未计划”的第一个作业。</span><span class="sxs-lookup"><span data-stu-id="807db-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="807db-117">确保只选中这一作业。</span><span class="sxs-lookup"><span data-stu-id="807db-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="807db-118">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="807db-118">Click Start.</span></span>
    * <span data-ttu-id="807db-119">请注意，图标指示作业开始。</span><span class="sxs-lookup"><span data-stu-id="807db-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="807db-120">选择第二个转移作业并更改数量</span><span class="sxs-lookup"><span data-stu-id="807db-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="807db-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="807db-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="807db-122">您可以选中多个作业，但现在只选中行 5。</span><span class="sxs-lookup"><span data-stu-id="807db-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="807db-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="807db-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="807db-124">确保上一步中的作业是唯一选中的作业。</span><span class="sxs-lookup"><span data-stu-id="807db-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="807db-125">取消选择所有其他作业。</span><span class="sxs-lookup"><span data-stu-id="807db-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="807db-126">请注意，“作业数量”字段中的值供稍后参考。</span><span class="sxs-lookup"><span data-stu-id="807db-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="807db-127">将作业数量设置为“30”。</span><span class="sxs-lookup"><span data-stu-id="807db-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="807db-128">请注意该警告！</span><span class="sxs-lookup"><span data-stu-id="807db-128">Notice the warning!</span></span> <span data-ttu-id="807db-129">不允许进行 30 项转移。</span><span class="sxs-lookup"><span data-stu-id="807db-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="807db-130">根据看板规则的设置，您只能转移原始数量。</span><span class="sxs-lookup"><span data-stu-id="807db-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="807db-131">使用以前在“作业数量”字段中记下的值</span><span class="sxs-lookup"><span data-stu-id="807db-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="807db-132">将作业数量设置为前一个值。</span><span class="sxs-lookup"><span data-stu-id="807db-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="807db-133">开始第二个转移作业</span><span class="sxs-lookup"><span data-stu-id="807db-133">Start the second transfer job</span></span>
1. <span data-ttu-id="807db-134">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="807db-134">Click Start.</span></span>
    * <span data-ttu-id="807db-135">这将开始行 5 中作业的转移。</span><span class="sxs-lookup"><span data-stu-id="807db-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="807db-136">完成两个转移作业</span><span class="sxs-lookup"><span data-stu-id="807db-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="807db-137">在列表中，选择第 4 行 。</span><span class="sxs-lookup"><span data-stu-id="807db-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="807db-138">现在选中了行 4 和行 5 两个转移作业。</span><span class="sxs-lookup"><span data-stu-id="807db-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="807db-139">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="807db-139">Click Complete.</span></span>
    * <span data-ttu-id="807db-140">这将完成两个作业的转移。</span><span class="sxs-lookup"><span data-stu-id="807db-140">This will complete the transfer of both jobs.</span></span>  

