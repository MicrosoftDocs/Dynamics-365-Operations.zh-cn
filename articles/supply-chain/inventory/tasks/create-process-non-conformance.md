---
title: 创建和处理符合项
description: 此主题介绍如何执行不符合项管理，基于现有的质检订单。
author: perlynne
manager: AnnBe
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e9cf42f80ef7a4c9c5f68a308386db5835c8f2e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916637"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="11595-103">创建和处理符合项</span><span class="sxs-lookup"><span data-stu-id="11595-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11595-104">此主题介绍如何执行不符合项管理，基于现有的质检订单。</span><span class="sxs-lookup"><span data-stu-id="11595-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="11595-105">您可以在 USMF 演示公司运行此录制并可以使用建议的值。</span><span class="sxs-lookup"><span data-stu-id="11595-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="11595-106">此过程通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="11595-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="11595-107">作为先决条件，按照[检查货物质量](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)中的说明完成操作。</span><span class="sxs-lookup"><span data-stu-id="11595-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="11595-108">若要处理不符合项的审核，运行任务录制的用户必须有在用户页分配的“名称”值。</span><span class="sxs-lookup"><span data-stu-id="11595-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="11595-109">若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。</span><span class="sxs-lookup"><span data-stu-id="11595-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="11595-110">选择质检订单。</span><span class="sxs-lookup"><span data-stu-id="11595-110">Select a quality order</span></span>
1. <span data-ttu-id="11595-111">在导航窗格中，转到**模块 > 库存管理 > 定期任务 > 质量管理 > 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="11595-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="11595-112">在列表中，选择在[检查货物质量](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)中创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="11595-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="11595-113">创建一个不符合项</span><span class="sxs-lookup"><span data-stu-id="11595-113">Create a nonconformance</span></span>
1. <span data-ttu-id="11595-114">在操作窗格中，选择**查询**。</span><span class="sxs-lookup"><span data-stu-id="11595-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="11595-115">选择**不符合项**。</span><span class="sxs-lookup"><span data-stu-id="11595-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="11595-116">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="11595-116">Select **New**.</span></span>
4. <span data-ttu-id="11595-117">在**问题类型**字段的下拉菜单中，选择质检过程中找到的问题。</span><span class="sxs-lookup"><span data-stu-id="11595-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="11595-118">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="11595-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="11595-119">批准/拒绝不符合项</span><span class="sxs-lookup"><span data-stu-id="11595-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="11595-120">选择**功能**。</span><span class="sxs-lookup"><span data-stu-id="11595-120">Select **Functions**.</span></span>
2. <span data-ttu-id="11595-121">选择**审核不符合项**。</span><span class="sxs-lookup"><span data-stu-id="11595-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="11595-122">对于本示例，批准不符合项。</span><span class="sxs-lookup"><span data-stu-id="11595-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="11595-123">批准的不符合项可以与相关操作关联，以记录在不符合项处理期间完成的工作，如本主题中所示，处理更正处理。</span><span class="sxs-lookup"><span data-stu-id="11595-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="11595-124">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="11595-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="11595-125">创建更正操作</span><span class="sxs-lookup"><span data-stu-id="11595-125">Create a correction action</span></span>
1. <span data-ttu-id="11595-126">选择**更正**。</span><span class="sxs-lookup"><span data-stu-id="11595-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="11595-127">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="11595-127">Select **New**.</span></span>
3. <span data-ttu-id="11595-128">在新行的**人员编号**字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="11595-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="11595-129">单击**选择**。</span><span class="sxs-lookup"><span data-stu-id="11595-129">Click **Select**.</span></span>
5. <span data-ttu-id="11595-130">选择**附加**。</span><span class="sxs-lookup"><span data-stu-id="11595-130">Select **Attach**.</span></span> <span data-ttu-id="11595-131">创建关于更正的附注。</span><span class="sxs-lookup"><span data-stu-id="11595-131">Create a note about the correction.</span></span> <span data-ttu-id="11595-132">对于本示例，操作是联系供应商，以讨论不符合项情况。</span><span class="sxs-lookup"><span data-stu-id="11595-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="11595-133">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="11595-133">Select **New**.</span></span>
7. <span data-ttu-id="11595-134">选择**单据**。</span><span class="sxs-lookup"><span data-stu-id="11595-134">Select **Note**.</span></span> <span data-ttu-id="11595-135">可以打印与不符合项管理有关的报告上的不同文档类型，具体取决于报告设置。</span><span class="sxs-lookup"><span data-stu-id="11595-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="11595-136">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="11595-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="11595-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="11595-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="11595-138">维护更正</span><span class="sxs-lookup"><span data-stu-id="11595-138">Maintain a correction</span></span>
1. <span data-ttu-id="11595-139">选择**标记完成**。</span><span class="sxs-lookup"><span data-stu-id="11595-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="11595-140">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="11595-140">Select **OK**.</span></span>
3. <span data-ttu-id="11595-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="11595-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="11595-142">关闭不符合项</span><span class="sxs-lookup"><span data-stu-id="11595-142">Close a nonconformance</span></span>
1. <span data-ttu-id="11595-143">选择**功能**。</span><span class="sxs-lookup"><span data-stu-id="11595-143">Select **Functions**.</span></span>
2. <span data-ttu-id="11595-144">选择**关闭不符合项**。</span><span class="sxs-lookup"><span data-stu-id="11595-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="11595-145">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="11595-145">Select **Yes**.</span></span>
4. <span data-ttu-id="11595-146">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="11595-146">Close the pages.</span></span>
