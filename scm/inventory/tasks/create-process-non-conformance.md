---
title: "创建和处理符合项"
description: "使用此过程可以执行不符合项管理，基于现有的质检订单。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="3aaab-103">创建和处理符合项</span><span class="sxs-lookup"><span data-stu-id="3aaab-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aaab-104">使用此过程可以执行不符合项管理，基于现有的质检订单。</span><span class="sxs-lookup"><span data-stu-id="3aaab-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="3aaab-105">您可以在 USMF 演示公司运行此录制并可以使用建议的值。</span><span class="sxs-lookup"><span data-stu-id="3aaab-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="3aaab-106">此过程通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="3aaab-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="3aaab-107">作为先决条件，运行“检查货物质量”任务录制。</span><span class="sxs-lookup"><span data-stu-id="3aaab-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="3aaab-108">若要处理不符合项的审核，运行任务录制的用户必须有在用户页分配的“名称”值。</span><span class="sxs-lookup"><span data-stu-id="3aaab-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="3aaab-109">若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="3aaab-110">选择质检订单。</span><span class="sxs-lookup"><span data-stu-id="3aaab-110">Select a quality order</span></span>
1. <span data-ttu-id="3aaab-111">转到“质检订单”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="3aaab-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3aaab-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3aaab-113">选择从“检查货物质量”任务记录创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="3aaab-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="3aaab-114">创建一个不符合项</span><span class="sxs-lookup"><span data-stu-id="3aaab-114">Create a nonconformance</span></span>
1. <span data-ttu-id="3aaab-115">单击“查询”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-115">Click Inquiries.</span></span>
2. <span data-ttu-id="3aaab-116">单击“不符合项”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-116">Click Non conformances.</span></span>
3. <span data-ttu-id="3aaab-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-117">Click New.</span></span>
4. <span data-ttu-id="3aaab-118">在“问题类型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3aaab-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3aaab-119">选择在检查过程中发现的问题。</span><span class="sxs-lookup"><span data-stu-id="3aaab-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="3aaab-120">在“问题类型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3aaab-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3aaab-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3aaab-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3aaab-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3aaab-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3aaab-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="3aaab-124">批准/拒绝不符合项</span><span class="sxs-lookup"><span data-stu-id="3aaab-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="3aaab-125">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-125">Click Functions.</span></span>
2. <span data-ttu-id="3aaab-126">单击“批准不符合项”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="3aaab-127">对于本示例，批准不符合项。</span><span class="sxs-lookup"><span data-stu-id="3aaab-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="3aaab-128">批准的不符合项可以与相关操作关联，以记录在不符合项处理期间完成的工作，以及在本工作记录中，处理更正处理。</span><span class="sxs-lookup"><span data-stu-id="3aaab-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="3aaab-129">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="3aaab-130">创建更正操作</span><span class="sxs-lookup"><span data-stu-id="3aaab-130">Create a correction action</span></span>
1. <span data-ttu-id="3aaab-131">单击“更正”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-131">Click Corrections.</span></span>
2. <span data-ttu-id="3aaab-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-132">Click New.</span></span>
3. <span data-ttu-id="3aaab-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3aaab-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3aaab-134">在“人员编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3aaab-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3aaab-135">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3aaab-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3aaab-136">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-136">Click Select.</span></span>
7. <span data-ttu-id="3aaab-137">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-137">Click Attach.</span></span>
    * <span data-ttu-id="3aaab-138">创建关于更正的附注。</span><span class="sxs-lookup"><span data-stu-id="3aaab-138">Create a note about the correction.</span></span> <span data-ttu-id="3aaab-139">对于本示例，操作是联系供应商，以讨论不符合项情况。</span><span class="sxs-lookup"><span data-stu-id="3aaab-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="3aaab-140">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-140">Click New.</span></span>
9. <span data-ttu-id="3aaab-141">单击“附注”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-141">Click Note.</span></span>
    * <span data-ttu-id="3aaab-142">请注意，可以打印与不符合项管理有关的报告上的不同文档类型，具体取决于报告设置。</span><span class="sxs-lookup"><span data-stu-id="3aaab-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="3aaab-143">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3aaab-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3aaab-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3aaab-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="3aaab-145">维护更正</span><span class="sxs-lookup"><span data-stu-id="3aaab-145">Maintain a correction</span></span>
1. <span data-ttu-id="3aaab-146">单击“完成标记”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-146">Click Mark complete.</span></span>
2. <span data-ttu-id="3aaab-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-147">Click OK.</span></span>
3. <span data-ttu-id="3aaab-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3aaab-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="3aaab-149">关闭不符合项</span><span class="sxs-lookup"><span data-stu-id="3aaab-149">Close a nonconformance</span></span>
1. <span data-ttu-id="3aaab-150">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-150">Click Functions.</span></span>
2. <span data-ttu-id="3aaab-151">单击“关闭此不符合项”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="3aaab-152">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="3aaab-152">Click Yes.</span></span>
4. <span data-ttu-id="3aaab-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3aaab-153">Close the page.</span></span>
5. <span data-ttu-id="3aaab-154">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3aaab-154">Close the page.</span></span>
