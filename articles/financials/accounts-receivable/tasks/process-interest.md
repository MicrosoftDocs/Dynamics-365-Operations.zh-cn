--- 
title: "处理利息"
description: "此过程将向您展示如何创建、打印和过帐利息单。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 214e12132557c12d19575f04ce69101b7457f37a
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="process-interest"></a><span data-ttu-id="23479-103">处理利息</span><span class="sxs-lookup"><span data-stu-id="23479-103">Process interest</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23479-104">此过程将向您展示如何创建、打印和过帐利息单。</span><span class="sxs-lookup"><span data-stu-id="23479-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="23479-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="23479-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="23479-106">在过帐模板设置利息。</span><span class="sxs-lookup"><span data-stu-id="23479-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="23479-107">转到“信用征收”>“设置”>“客户过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="23479-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="23479-108">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="23479-108">Click Edit.</span></span>
    * <span data-ttu-id="23479-109">从下拉列表中选择利息代码。</span><span class="sxs-lookup"><span data-stu-id="23479-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="23479-110">如果您不希望使用此过帐模板计算交易利息，则将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="23479-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="23479-111">“表单限制”选项卡可允许您更改处理利息的方法。</span><span class="sxs-lookup"><span data-stu-id="23479-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="23479-112">如果此字段设置为“是”，则根据此过帐模板计算利息。</span><span class="sxs-lookup"><span data-stu-id="23479-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="23479-113">计算利息</span><span class="sxs-lookup"><span data-stu-id="23479-113">Calculate interest</span></span>
1. <span data-ttu-id="23479-114">转到“信用征收”>“利息”>“创建利息单”。</span><span class="sxs-lookup"><span data-stu-id="23479-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="23479-115">您必须为您将要计算的利息选择交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="23479-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="23479-116">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="23479-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="23479-117">如果您选择“利息”，您将在利息单中计算利息。</span><span class="sxs-lookup"><span data-stu-id="23479-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="23479-118">您也许想要在包括这些交易之前，管理利息单中计算利息的法律。</span><span class="sxs-lookup"><span data-stu-id="23479-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="23479-119">利息为此该日期开始计算到“结束日期”。</span><span class="sxs-lookup"><span data-stu-id="23479-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="23479-120">如果您并未设定“开始日期“，则所有未过帐的利息单将会被取消，利息将从交易记录日期开始重新计算。</span><span class="sxs-lookup"><span data-stu-id="23479-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="23479-121">输入利息单的日期。</span><span class="sxs-lookup"><span data-stu-id="23479-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="23479-122">具有三个过帐模板选项：帐户 – 使用分配给客户帐户每张利息单的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="23479-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="23479-123">选择 – 使用在“过帐模板”字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="23479-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="23479-124">交易记录 –使用来自为每张利息单计算出利息的交易记录的单独过帐模板。</span><span class="sxs-lookup"><span data-stu-id="23479-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="23479-125">未分配过帐模板的交易记录将使用“应收账款参数单”的“分类帐”和“销售税”所指定的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="23479-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="23479-126">如果您将“使用过帐模板”更改为“选择”，则在此选择一个过帐模板。</span><span class="sxs-lookup"><span data-stu-id="23479-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="23479-127">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="23479-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="23479-128">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="23479-128">Click Filter.</span></span>
5. <span data-ttu-id="23479-129">在“条件”字段中，输入“客户 ID”。</span><span class="sxs-lookup"><span data-stu-id="23479-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="23479-130">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="23479-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="23479-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="23479-131">Click OK.</span></span>
7. <span data-ttu-id="23479-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="23479-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="23479-133">打印利息单</span><span class="sxs-lookup"><span data-stu-id="23479-133">Print interest notes</span></span>
1. <span data-ttu-id="23479-134">转到“信用征收”>“利息”>“审查和处理利息单”。</span><span class="sxs-lookup"><span data-stu-id="23479-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="23479-135">在“状态”字段中，选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="23479-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="23479-136">在“打印”字段中，选择“不打印”。</span><span class="sxs-lookup"><span data-stu-id="23479-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="23479-137">单击“打印”。</span><span class="sxs-lookup"><span data-stu-id="23479-137">Click Print.</span></span>
5. <span data-ttu-id="23479-138">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="23479-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="23479-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="23479-139">Click OK.</span></span>
7. <span data-ttu-id="23479-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="23479-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="23479-141">过帐利息单</span><span class="sxs-lookup"><span data-stu-id="23479-141">Post the interest note</span></span>
1. <span data-ttu-id="23479-142">选择准备过帐的利息单（状态为“已创建”）。</span><span class="sxs-lookup"><span data-stu-id="23479-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="23479-143">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="23479-143">Click Post.</span></span>
3. <span data-ttu-id="23479-144">输入利息单的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="23479-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="23479-145">选择“是”可以为每张利息单创建一个总帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="23479-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="23479-146">如果未选择“是”，应付给客户的所有利息单上的利息将累加起来，作为一笔交易记录过帐到总帐中。</span><span class="sxs-lookup"><span data-stu-id="23479-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="23479-147">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="23479-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="23479-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="23479-148">Click OK.</span></span>
6. <span data-ttu-id="23479-149">在“状态”字段中，选择“已过帐”。</span><span class="sxs-lookup"><span data-stu-id="23479-149">In the Status field, select 'Posted'.</span></span>


