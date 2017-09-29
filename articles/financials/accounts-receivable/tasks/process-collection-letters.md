--- 
title: "处理催款单"
description: "该过程说明如何创建、打印并过帐收款单。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="19139-103">处理催款单</span><span class="sxs-lookup"><span data-stu-id="19139-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19139-104">该过程说明如何创建、打印并过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="19139-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="19139-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="19139-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="19139-106">在该过帐上设置收款单的排序</span><span class="sxs-lookup"><span data-stu-id="19139-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="19139-107">转到“信用征收”>“设置”>“客户过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="19139-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="19139-108">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="19139-108">Click Edit.</span></span>
    * <span data-ttu-id="19139-109">从下拉列表中选择收款单排序。</span><span class="sxs-lookup"><span data-stu-id="19139-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="19139-110">如果不使用该过帐模板生成交易收款单，则该字段保留空白。</span><span class="sxs-lookup"><span data-stu-id="19139-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="19139-111">通过该表格的限制选项卡，可以更改处理收款单的方式。</span><span class="sxs-lookup"><span data-stu-id="19139-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="19139-112">如果此字段设置为“是”，则将在此过帐模板创建收款单。</span><span class="sxs-lookup"><span data-stu-id="19139-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="19139-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="19139-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="19139-114">创建催款单</span><span class="sxs-lookup"><span data-stu-id="19139-114">Create collection letters</span></span>
1. <span data-ttu-id="19139-115">转到“信用与收款”>“收款单”>“创建收款单”。</span><span class="sxs-lookup"><span data-stu-id="19139-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="19139-116">必须选择收款单的交易类型。</span><span class="sxs-lookup"><span data-stu-id="19139-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="19139-117">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="19139-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="19139-118">在“催款单”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="19139-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="19139-119">输入该收款单的日期。</span><span class="sxs-lookup"><span data-stu-id="19139-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="19139-120">具有两个过帐模板选项：帐户 – 使用分配给客户帐户每张利息单的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="19139-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="19139-121">选择 – 使用在“过帐模板”字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="19139-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="19139-122">如果将“使用过帐模板”更改为“选择”，则请选择一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="19139-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="19139-123">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="19139-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="19139-124">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="19139-124">Click Filter.</span></span>
6. <span data-ttu-id="19139-125">在“条件”字段中，在“条件”字段中，输入一个客户 ID。</span><span class="sxs-lookup"><span data-stu-id="19139-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="19139-126">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="19139-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="19139-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="19139-127">Click OK.</span></span>
8. <span data-ttu-id="19139-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="19139-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="19139-129">打印收款单</span><span class="sxs-lookup"><span data-stu-id="19139-129">Print collection letters</span></span>
1. <span data-ttu-id="19139-130">转到“信用和收款”>“收款单”>“查看并处理收款单”。</span><span class="sxs-lookup"><span data-stu-id="19139-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="19139-131">在“状态”字段中，选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="19139-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="19139-132">在“打印”字段中，选择“不打印”。</span><span class="sxs-lookup"><span data-stu-id="19139-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="19139-133">单击“打印”。</span><span class="sxs-lookup"><span data-stu-id="19139-133">Click Print.</span></span>
5. <span data-ttu-id="19139-134">单击“注解收款单”。</span><span class="sxs-lookup"><span data-stu-id="19139-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="19139-135">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="19139-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="19139-136">输入过帐的截止日期</span><span class="sxs-lookup"><span data-stu-id="19139-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="19139-137">单击“确认”以打印收款单。</span><span class="sxs-lookup"><span data-stu-id="19139-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="19139-138">过帐收款单</span><span class="sxs-lookup"><span data-stu-id="19139-138">Post the collection letter</span></span>
1. <span data-ttu-id="19139-139">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="19139-139">Click Post.</span></span>
2. <span data-ttu-id="19139-140">输入该收款单的过帐日期</span><span class="sxs-lookup"><span data-stu-id="19139-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="19139-141">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="19139-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="19139-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="19139-142">Click OK.</span></span>
5. <span data-ttu-id="19139-143">在“状态”字段中，选择“已过帐”。</span><span class="sxs-lookup"><span data-stu-id="19139-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="19139-144">在“打印”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="19139-144">In the Printed field, select an option.</span></span>


