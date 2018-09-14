--- 
title: "处理催款单"
description: "该过程说明如何创建、打印并过帐收款单。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a1bdf9528b52daa7bb719ea5a751a01e56a8c963
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="7b51e-103">处理催款单</span><span class="sxs-lookup"><span data-stu-id="7b51e-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b51e-104">该过程说明如何创建、打印并过帐收款单。</span><span class="sxs-lookup"><span data-stu-id="7b51e-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="7b51e-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="7b51e-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="7b51e-106">在该过帐上设置收款单的排序</span><span class="sxs-lookup"><span data-stu-id="7b51e-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="7b51e-107">转到“信用征收”>“设置”>“客户过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="7b51e-108">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-108">Click Edit.</span></span>
    * <span data-ttu-id="7b51e-109">从下拉列表中选择收款单排序。</span><span class="sxs-lookup"><span data-stu-id="7b51e-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="7b51e-110">如果不使用该过帐模板生成交易收款单，则该字段保留空白。</span><span class="sxs-lookup"><span data-stu-id="7b51e-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="7b51e-111">通过该表格的限制选项卡，可以更改处理收款单的方式。</span><span class="sxs-lookup"><span data-stu-id="7b51e-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="7b51e-112">如果此字段设置为“是”，则将在此过帐模板创建收款单。</span><span class="sxs-lookup"><span data-stu-id="7b51e-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="7b51e-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7b51e-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="7b51e-114">创建催款单</span><span class="sxs-lookup"><span data-stu-id="7b51e-114">Create collection letters</span></span>
1. <span data-ttu-id="7b51e-115">转到“信用与收款”>“收款单”>“创建收款单”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="7b51e-116">必须选择收款单的交易类型。</span><span class="sxs-lookup"><span data-stu-id="7b51e-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="7b51e-117">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="7b51e-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="7b51e-118">在“催款单”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7b51e-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="7b51e-119">输入该收款单的日期。</span><span class="sxs-lookup"><span data-stu-id="7b51e-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="7b51e-120">具有两个过帐模板选项：帐户 – 使用分配给客户帐户每张利息单的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="7b51e-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="7b51e-121">选择 – 使用在“过帐模板”字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="7b51e-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="7b51e-122">如果将“使用过帐模板”更改为“选择”，则请选择一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="7b51e-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="7b51e-123">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="7b51e-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="7b51e-124">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-124">Click Filter.</span></span>
6. <span data-ttu-id="7b51e-125">在“条件”字段中，在“条件”字段中，输入一个客户 ID。</span><span class="sxs-lookup"><span data-stu-id="7b51e-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="7b51e-126">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="7b51e-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="7b51e-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-127">Click OK.</span></span>
8. <span data-ttu-id="7b51e-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="7b51e-129">打印收款单</span><span class="sxs-lookup"><span data-stu-id="7b51e-129">Print collection letters</span></span>
1. <span data-ttu-id="7b51e-130">转到“信用和收款”>“收款单”>“查看并处理收款单”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="7b51e-131">在“状态”字段中，选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="7b51e-132">在“打印”字段中，选择“不打印”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="7b51e-133">单击“打印”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-133">Click Print.</span></span>
5. <span data-ttu-id="7b51e-134">单击“注解收款单”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="7b51e-135">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="7b51e-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7b51e-136">输入过帐的截止日期</span><span class="sxs-lookup"><span data-stu-id="7b51e-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="7b51e-137">单击“确认”以打印收款单。</span><span class="sxs-lookup"><span data-stu-id="7b51e-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="7b51e-138">过帐收款单</span><span class="sxs-lookup"><span data-stu-id="7b51e-138">Post the collection letter</span></span>
1. <span data-ttu-id="7b51e-139">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-139">Click Post.</span></span>
2. <span data-ttu-id="7b51e-140">输入该收款单的过帐日期</span><span class="sxs-lookup"><span data-stu-id="7b51e-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="7b51e-141">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="7b51e-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="7b51e-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-142">Click OK.</span></span>
5. <span data-ttu-id="7b51e-143">在“状态”字段中，选择“已过帐”。</span><span class="sxs-lookup"><span data-stu-id="7b51e-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="7b51e-144">在“打印”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7b51e-144">In the Printed field, select an option.</span></span>


