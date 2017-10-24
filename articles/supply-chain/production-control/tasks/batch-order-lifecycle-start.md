--- 
title: "从创建到开始的批次订单生命周期"
description: "该过程向您介绍批次订单生命周期中的第一部分。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 94f706241545282fd2744c3be4edc253f2998aff
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="1a81c-103">从创建到开始的批次订单生命周期</span><span class="sxs-lookup"><span data-stu-id="1a81c-103">Batch order lifecycle from create to start</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a81c-104">该过程向您介绍批次订单生命周期中的第一部分。</span><span class="sxs-lookup"><span data-stu-id="1a81c-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="1a81c-105">从创建、成本预估和对生产作业计划到批次订单的实际开始。</span><span class="sxs-lookup"><span data-stu-id="1a81c-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="1a81c-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="1a81c-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="1a81c-107">使用其他数据集运行该过程的先决条件是具备有效配方和工艺路线的发布产品。</span><span class="sxs-lookup"><span data-stu-id="1a81c-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="1a81c-108">创建批次订单</span><span class="sxs-lookup"><span data-stu-id="1a81c-108">Create a batch order</span></span>
1. <span data-ttu-id="1a81c-109">转至“所有生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-109">Go to All production orders.</span></span>
2. <span data-ttu-id="1a81c-110">单击“新批次订单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-110">Click New batch order.</span></span>
3. <span data-ttu-id="1a81c-111">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1a81c-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="1a81c-112">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-112">Click Create.</span></span>
5. <span data-ttu-id="1a81c-113">使用“快速筛选器”在“生产”字段筛选值“b”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="1a81c-114">查看生产配方和预期联产品</span><span class="sxs-lookup"><span data-stu-id="1a81c-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="1a81c-115">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1a81c-116">单击“配方”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-116">Click Formula.</span></span>
3. <span data-ttu-id="1a81c-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-117">Close the page.</span></span>
4. <span data-ttu-id="1a81c-118">单击“联产品”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-118">Click Co-products.</span></span>
5. <span data-ttu-id="1a81c-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="1a81c-120">估计批次订单</span><span class="sxs-lookup"><span data-stu-id="1a81c-120">Estimate the batch order</span></span>
1. <span data-ttu-id="1a81c-121">单击“估计”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-121">Click Estimate.</span></span>
2. <span data-ttu-id="1a81c-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-122">Click OK.</span></span>
3. <span data-ttu-id="1a81c-123">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1a81c-124">单击“查看计算明细”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-124">Click View calculation details.</span></span>
5. <span data-ttu-id="1a81c-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="1a81c-126">发布批次订单</span><span class="sxs-lookup"><span data-stu-id="1a81c-126">Release the batch order</span></span>
1. <span data-ttu-id="1a81c-127">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1a81c-128">单击“下达”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-128">Click Release.</span></span>
3. <span data-ttu-id="1a81c-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="1a81c-130">计划生产作业</span><span class="sxs-lookup"><span data-stu-id="1a81c-130">Schedule production jobs</span></span>
1. <span data-ttu-id="1a81c-131">在“操作窗格”上，单击“计划” 。</span><span class="sxs-lookup"><span data-stu-id="1a81c-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="1a81c-132">单击“计划作业”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="1a81c-133">在“有限产能”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="1a81c-134">在“有限物料”字段中，选择“否”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="1a81c-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-135">Click OK.</span></span>
6. <span data-ttu-id="1a81c-136">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="1a81c-137">单击“所有作业”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-137">Click All jobs.</span></span>
8. <span data-ttu-id="1a81c-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="1a81c-139">开始批次订单</span><span class="sxs-lookup"><span data-stu-id="1a81c-139">Start the batch order</span></span>
1. <span data-ttu-id="1a81c-140">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-140">Click Start.</span></span>
2. <span data-ttu-id="1a81c-141">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="1a81c-141">Click the General tab.</span></span>
3. <span data-ttu-id="1a81c-142">在“立即将领料单过帐”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="1a81c-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-143">Click OK.</span></span>
5. <span data-ttu-id="1a81c-144">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="1a81c-145">单击“领料单”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-145">Click Picking list.</span></span>
7. <span data-ttu-id="1a81c-146">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1a81c-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1a81c-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-147">Close the page.</span></span>
9. <span data-ttu-id="1a81c-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-148">Close the page.</span></span>
10. <span data-ttu-id="1a81c-149">单击“工艺卡”。</span><span class="sxs-lookup"><span data-stu-id="1a81c-149">Click Route card.</span></span>
11. <span data-ttu-id="1a81c-150">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1a81c-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1a81c-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-151">Close the page.</span></span>
13. <span data-ttu-id="1a81c-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a81c-152">Close the page.</span></span>

